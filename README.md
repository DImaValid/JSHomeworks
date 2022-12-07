<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport"
        content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
</head>
<body>
<script>
  // - Створити функцію конструктор для об'єктів User з полями id, name, surname , email, phone
  //створити пустий масив, наповнити його 10 об'єктами new User(....)
  function User(id, name, surname, email, phone) {
    this.id = id
    this.name = name
    this.surname = surname
    this.email = email
    this.phone = phone
  }

  let userArray = []
  let user0 = new User(1)
  let user1 = new User(2)
  let user2 = new User(3)
  let user3 = new User(4)
  let user4 = new User(5)
  let user5 = new User(6)
  let user6 = new User(7)
  let user7 = new User(8)
  let user9 = new User(9)
  let user00 = new User(12)
  userArray.push(user0, user1, user00, user9, user7, user6, user5, user4, user3, user2)

  //- Взяти масив з  User[] з попереднього завдання, та відфільтрувати , залишивши тільки об'єкти з парними id (filter)
  let filter = userArray.filter(value => value.id % 2 === 0)
  console.log(filter)
  // - Взяти масив з  User[] з попереднього завдання, та відсортувати його по id. по зростанню (sort)
  let sort = userArray.sort((a, b) => a.id - b.id)
  console.log(sort)
  //- створити класс для об'єктів Client з полями id, name, surname , email, phone, order (поле є масивом зі списком товарів)
  //створити пустий масив, наповнити його 10 об'єктами Client
  // - Взяти масив (Client [] з попереднього завдання).Відсортувати його по кількості товарів в полі order по зростанню. (sort)
  class Client {


    constructor(id, name, surname, email, phone, order) {
      this.id = id;
      this.name = name;
      this.surname = surname;
      this.email = email;
      this.phone = phone;
      this.order = order;
    }
  }

  let clientArray = []
  let client0 = new Client(1, 2, 3, 4, 5, [6])
  let client1 = new Client(1, 2, 3, 4, 5, [2])
  let client2 = new Client(1, 2, 3, 4, 5, [3, 4])
  let client3 = new Client(1, 2, 3, 4, 5, [4, 5, 4])
  let client4 = new Client(1, 2, 3, 4, 5, [2, 3])
  let client5 = new Client(1, 2, 3, 4, 5, [4, 3, 4, 5])
  let client6 = new Client(1, 2, 3, 4, 5, [2, 3])
  let client7 = new Client(1, 2, 3, 4, 5, [4, 5, 3, 4])
  let client8 = new Client(1, 2, 3, 4, 5, [2, 3, 2])
  let client9 = new Client(1, 2, 3, 4, 5, [3, 4])
  clientArray.push(client0, client1, client2, client3, client4, client5, client6, client7, client8, client9)
  let sortofClients = clientArray.sort((a, b) => b.order.length - a.order.length)
  console.log(sortofClients)
  //- Створити функцію конструктор яка дозволяє створювати об'єкти car, з властивостями модель, виробник, рік випуску, максимальна швидкість, об'єм двигуна. додати в об'єкт функції:
  //-- drive () - яка виводить в консоль `їдемо зі швидкістю ${максимальна швидкість} на годину`
  //-- info () - яка виводить всю інформацію про автомобіль в форматі `назва поля - значення поля`
  //-- increaseMaxSpeed (newSpeed) - яка підвищує значення максимальної швидкості на значення newSpeed
  //-- changeYear (newValue) - змінює рік випуску на значення newValue
  //-- addDriver (driver) - приймає об'єкт який "водій" з довільним набором полів, і додає його в поточний об'єкт car
  function Car(model, year, engine, make, maxSpeed) {

    this.model = model
    this.year = year
    this.engine = engine
    this.make = make
    this.maxSpeed = maxSpeed
    this.drive = function (){

      console.log(`Швидкість ${this.maxSpeed}`)
    }
    this.info = function (){
      for (const Key in this) {
        if (typeof this[Key] !== `function`){
          (`${Key} -- ${this[Key]}`)}

      }
    }
    this.increaseMaxSpeed = function (newSpeed){
      this.maxSpeed += newSpeed
    }
    this.changeYear = function (newValue){
      this.year = newValue
    }
  this.addDriver = function (Crewman){
      this.Crewman = Crewman
  }
  }
let newCar=new Car('TT',1999,2.4,'Audi',270)
  newCar.info();
  //- (Те саме, тільки через клас)
  //Створити клас який дозволяє створювати об'єкти car, з властивостями модель, виробник, рік випуску, максимальна швидкість, об'єм двигуна. додати в об'єкт функції:
  // -- drive () - яка виводить в консоль `їдемо зі швидкістю ${максимальна швидкість} на годину`
  //  -- info () - яка виводить всю інформацію про автомобіль в форматі `назва поля - значення поля`
  //  -- increaseMaxSpeed (newSpeed) - яка підвищує значення максимальної швидкості на значення newSpeed
  //  -- changeYear (newValue) - змінює рік випуску на значення newValue
  //  -- addDriver (driver) - приймає об'єкт який "водій" з довільним набором полів, і додає його в поточний об'єкт car


  // -створити класс/функцію конструктор попелюшка з полями ім'я, вік, розмір ноги. Створити масив з 10 попелюшок.
  // Сторити об'єкт класу "принц" за допомоги класу який має поля ім'я, вік, туфелька яку він знайшов.
  //   За допомоги циклу знайти яка попелюшка повинна бути з принцом.
  //  Додатково, знайти необхідну попелюшку за допомоги функції масиву find та відповідного колбеку
class Sinderbella{
  constructor(name, age, footSize) {
    this.name = name;
    this.age = age;
    this.footSize = footSize;
  }
}
  let Bella0=new Sinderbella(1,2,33)
  let Bella9=new Sinderbella(1,2,311)
  let Bella8=new Sinderbella(1,2,40)
  let Bella7=new Sinderbella(1,2,39)
  let Bella6=new Sinderbella(1,2,30)
  let Bella5=new Sinderbella(1,2,31)
  let Bella4=new Sinderbella(12222,2,33)
  let Bella3=new Sinderbella(1,2,32)
  let Bella2=new Sinderbella(1,2,34)
  let Bella1=new Sinderbella(1,2,32)
  let arrofBellas=[]
  arrofBellas.push(Bella0,Bella9,Bella8,Bella7,Bella6,Bella5,Bella4,Bella3,Bella2,Bella1)
  class Prince{

    constructor(name, age, Size) {
      this.name = name;
      this.age = age;
      this.Size = Size;
    }
  }

  let search = function (arr,boy){
    for (const arrElement of arr) {
      if (arr.footSize === boy.Size){

        console.log(`Bella is ${arrElement.name}`)
      } else {
        console.log("Eror")}
    }
  }
  let prince1 = new Prince(1,2,33)
  search(arrofBellas,prince1)
</script>

</body>
</html>
