<!--
<VFSHome name="Title" />
Copyright (c) 2023. Kibble Game Studios Inc. All Rights Reserved.
-->
<script>

    import Controller from '@/plugins/controller'

    class MyPageController extends Controller {

        constructor( name, subComponentList = []) {
            super( name, subComponentList );
            this.vm = {
                formData: {
                    name:"",
                    studentNumber:0,
                }
            }
        }
    }

    export default new MyPageController('MyPage');

</script>
<template>

    <section class="flexbox columns myPage">
        <h1 class="flexitem left title">Student Information</h1>
        <h3>Enter new student below</h3>

        <div class="flexitem dialog">

            <form class="student-info">
                
                <label for="name">Student Name:
                    <input name="name" v-model="formData.name">
                </label><br/>

                <label for="sNumber">Student Number:
                    <input name="sNumber" type="number" v-model="formData.studentNumber">
                </label><br/>


                
            </form>
            <button value="Submit" id="submit" @click="infoStore.increment()">Submit</button>

            <label name="studentName">Student Name:</label>
            <label name="studentName">{{ formData.name }}</label> <br />

            <label name="studentName">Student Id:</label>
            <label name="studentName">{{ formData.studentNumber }}</label>
        </div>
    </section>

</template>
<style scoped>
    /* Local styles for this template */
    .myPage {
        margin:2vw;
        border: 1px solid black;
        background-color: lightgray;
        color: black;
        height: 78vh;
        width: 80vw;
    }

    .student-info {
        display: flex;
        justify-content: center;
        border: 2px solid #333;
        margin: 1em;
        padding: 2em;
    }


    select, input, button {
        font-size: 1.2em;
        font-weight: 700;
        height: 1.4em;

    }

    button {
        padding: .5em;
        margin: .25em;
        padding-bottom: 1.5em;
    }
</style>

