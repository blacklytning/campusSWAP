<template>
<div class = register-block>
    <h1>CampusSWAP</h1>
    <div class = form-fields>
        <h2>Create an Account</h2>
        <input type = "email" id="email" placeholder="Institute Email Address">
        <input type="text" v-for = "field in textFields" :id = "field" :placeholder = "field">
        <input type = "password" v-for = "pass in passwordFields" :id = "pass" :placeholder="pass">
        <button class = submit>Submit</button>
        <submitButton class = submit />
    </div>
</div>
</template>
<script>
    export default{
        data(){
            return{
                textFields: ["MoodleID", "First Name", "Last Name"],
                passwordFields: ["Password", "Confirm Password"]
            } 
        }
    }
</script>

<style scoped>
    .register-block{
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: space-around;
        align-items: center;
        flex-wrap: wrap;
    }
    h1{
        color: white;
        font-size: 78px;
    }

    h2{
        color: white;
        font-size: 40px;
    }
    .form-fields{
        border-radius: 10px;
        padding: 0 30px;
        height: 100%;
        background-color: gainsboro;
        
        color: white;
        backdrop-filter: blur(10px);
        display: flex;
        flex-direction: column;       
        justify-content: center;
        align-items: center;
        gap: 2rem;
    }

    input{
        display: block;
        height: 30px;
        width: 80%;
        border-radius: 5px;
        opacity: 0.4;
        border: none;
        outline: none;
    }

    input:active{
        outline: 1px solid white;
    }

    button{
        color: #021B79;
        width: 80%;
        height: 30px;
        border: none;

    }
</style>
