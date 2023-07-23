<template>
  <div>
    <form action="">
      <label for="">Email</label>
      <input type="email" required v-model="email" />

      <label for="">Password</label>
      <input type="password" required v-model="password" />

      <select v-model="roles">
        <option value="web developer" >Web Developer</option>
        <option value="web designer">Web Designer</option>
      </select>
      <input type="checkbox" v-model="checkbox">
      <label for="">Accept terms and condition</label> <br>

      <label for="">Skills</label>
      <input type="text" @keyup="addSkill" v-model="skill">
      

    </form>
    <p>Email is : {{ email }}</p>
    <p>Password is : {{ password }}</p>
    <p>Roles is : {{ roles }}</p>
    <p>Skill are : {{ skills }}</p>

  </div>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      password:"",
      roles:"web developer",
      checkbox:false,
      skills:[],
      skill:""
    };
  },
  methods:{
    addSkill(e){
       if(e.key === ",") {
            this.skills.push(this.skill);
            this.skill=""
       }
    }
  }
};
</script>

<style>
form {
  max-width: 420px;
  margin: 30px auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
}
label {
  color: #aaa;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.6em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}
input,
select {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #ddd;
  color: #555;
}
input[type="checkbox"] {
  display: inline-block;
  width: 16px;
  margin: 0 10px 0 0;
  position: relative;
  top: 2px;
}
.cross {
  cursor: pointer;
  color: red;
}

.create {
  background-color: royalblue;
  padding: 8px;
  color: white;
  border-radius: 10px;
}
.align {
  text-align: center;
}
.error {
  color: crimson;
}
</style>
