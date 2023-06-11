const student = {
  ID: 1,
  FirstName: "Jane",
  LastName: "Smith",
  age: 22,
  Gender: "Female",
  Email: "janesmith@example.com",
  PhoneNumber: "987-654-3210",
  Address: "456 Elm Street",
  Major: "Psychology",
  YearOfStudy: "4",
  Status: "Pending",
  isDelete: false,
};

const student2 = {
  ID: 2,
  FirstName: "John",
  LastName: "Doe",
  age: 20,
  Gender: "Male",
  Email: "johndoe@example.com",
  PhoneNumber: "123-456-7890",
  Address: "123 Main Street",
  Major: "Computer Science",
  YearOfStudy: "2",
  Status: "Active",
  isDelete: false,
};

const studentsArr = [student,student2];

const checkFields =()=>
{
if(!document.getElementById('id') || !document.getElementById('firstName')
 || !document.getElementById('lastName') || ! document.getElementById('age')
 || !document.getElementById('gender') || !document.getElementById('email')
 || !document.getElementById('phoneNumber') || !document.getElementById('address')
 || !document.getElementById('major') || !document.getElementById('yearOfStudy')
 || !document.getElementById('status')
 )
 {
  alert("There is one or more field is Empty");
  return;
 }
}



// const filterByAge = studentsArr.filter( stdObj =>
//   {
//     if (document.getElementById(filter-age) == stdObj.age)
//     {
//       document.getElementById(filter-age).innerHTML =  stdObj.FirstName +" - ";
      
//     }

//   });

  //const filterByMajor = studentsArr.filter(stdObj => document.getElementById(filter-major) === document.getElementById(filter-major).innerHTML . stdObj.FirstName +" - " , 0 );






const addStudent = ()=>
{
  const stdObj = {
    ID: document.getElementById('id') ,
    FirstName: document.getElementById('firstName'),
    LastName: document.getElementById('lastName'),
    age: document.getElementById('age'),
    Gender: document.getElementById('gender'),
    Email: document.getElementById('email'),
    PhoneNumber: document.getElementById('phoneNumber'),
    Address: document.getElementById('address'),
    Major: document.getElementById('major'),
    YearOfStudy: document.getElementById('yearOfStudy'),
    Status:document.getElementById('status'),
    isDelete: false,
    }
  studentsArr.push(stdObj);  
  console.log('stdObj :>> ', stdObj);
  showStudent(stdObj.ID);
};

console.log('studentsArr :>> ', studentsArr);




const printStd = ()=>
{
  const std = 
  ` 
   <tr>
  <td>1</td>
  <td>${ stdObj.FirstName}</td>
  <td>
      <button onclick="${activeFun()}">Activate</button>
      <button onclick="${showStudent(stdObj.ID)}">Show Data</button>
      <button onclick="${stdObj.ID}">Delete</button>
  </td>
  </tr> 
  `
return std;  

}

const activeFun = ()=>
{ 
  stdObj.foreach((id) =>{
    if (stdObj.ID == stdId)
{
  if (stdObj.Status !== "active")
  {
    stdObj.Status = "active";
  }
  else
  {
    stdObj.Status = "pending";
  }
}
  })

}

const deleteStudent = (id)=>
{
stdObj.map((id)=>{if(stdObj.ID == id)
  {
    stdObj.isDelete = true;
  }
  else
  {
    stdObj.isDelete = false;
  }})



}




const showStudent = (stdId) => {
  console.log("stdId", stdId);
  const studentData = document.getElementById("std-data");
  if (stdId === 1) {
    studentData.classList.remove("display-block");
    studentData.classList.add("display-none");
    alert("The Student is Pending");
  } else {
    studentData.classList.remove("display-none");
    studentData.classList.add("display-block");
  }
};


