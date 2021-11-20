<template>
<form @submit.prevent="handleSubmit">
    <h3>SIGN UP</h3>


  <div class ="form-group">
  <label for="email"> FULLNAME:</label>
  <input type="text"  class="form-group"  v-model="fullname" placeholder="fullname">
    </div>

  <div class ="form-group">
  <label for="email">EMAIL:</label>
  <input type="email"  class="form-group"  v-model="email" placeholder="email">
    </div>

    
  <div class ="form-group">
  <label for="email">PASSWORD:</label>
  <input type="password"  class="form-group"  v-model="password" placeholder="password">
    </div>

  <div class ="form-group">
  <label for="email">CONFIRM PASSWORD:</label>
  <input type="password"  class="form-group" v-model="confirm_password" placeholder="confrim password">
    </div>
    <button class="btn btn-primary btn-block">sign up</button>

</form>
</template>

<script>
import axios from 'axios'
 export default{
     name : 'Register',
     data(){
       return{
       fullname: '',
       email: '',
       password: '',
       confirm_password: '',
     }
     },
     methods:{
       async  handleSubmit(){
         
         const response = await axios.post('register', {
           fullname: this.fullname,
           email: this.email,
           password: this.password,
           confirm_password: this.confirm_password,
         
         });
         console.log(response);
            
       }
     }
 }
</script>


