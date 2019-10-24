Sec3-Lec44 ==> Passing Method References Between Components => use of bind
==========================================================================
We may also need to pass a value to our function.
So we will pass value newName to switchNameHandler :

switchNameHandler = (newName) => {
  console.log('Button Clicked !!! ');
  this.setState({
    persons:[
      {name: newName, age:28},
      {name:'Manu' , age:29},
      {name:'Stephanie' , age:27}
    ]
  })
}

 <button onClick={this.switchNameHandler.bind(this,'Maximilian')}>
 Switch Names</button>

<PersonProp 
name={this.state.persons[1].name} 
age={this.state.persons[1].age} 
click={this.switchNameHandler.bind(this,'Max !!')} > My Hobby : Racing
</PersonProp>

Note : "this" inside bind refers to the the "this" inside function switchNameHandler so its complete object