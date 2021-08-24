const app ={
  el:'#app',
data(){
    return{
      beggin:'Введите список дел',
      title:'To Do List',
      inpvalue:'',
      notes:[],
    allert:'Нажмите на Задание чтобы его удалить или на кнопку',

    }
},
methods:{
  InputChangeHandler(event){
this.inpvalue = event.target.value
  },
  addnewnote(){
    if (this.inpvalue !== ''){
       this.notes.push(this.inpvalue)
    this.inpvalue = ''

    }
   
  },
  
  removenote(idx){
this.notes.splice(idx,1)
  },
  
}
}

Vue.createApp(app).mount('#app')
