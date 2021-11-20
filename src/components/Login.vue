<template>

<form>
    <h3>LOGIN</h3>
    <div class ="form-group">
  <label for="email">EMAIL:</label>
  <input type="email"  class="form-group" placeholder="email">
    </div>

    
 <div class ="form-group">
  <label for="lname">PASSWORD:</label>
  <input type="password"  class="form-group" placeholder="password">
    </div>
    <button class="btn btn-primary btn-block">Login</button>
</form>
</template>

<script>

export default{

    name: 'Login'

}
</script>
