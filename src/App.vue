<template>
    <div class="container">
        <form>
            <div class="row">
                <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                    <!-- Exercise 1 -->
                    <!-- Create a Signup Form where you retrieve the following Information -->
                    <!-- Full Name (First Name + Last Name) -->
                    <!-- Mail -->
                    <!-- Password -->
                    <!-- Store Data? Yes/No -->
                    <form action="https://echo.htmlacademy.ru" method="POST" @submit.prevent="submitted">
                      <label for="firstName">First Name</label><br>
                      <input type="text" name="firstName" id="firstName" placeholder="Jon" v-model="firstName">
                      <br><br>
                      <label for="lastName">Last Name</label><br>
                      <input type="text" name="lastName" id="lastName" placeholder="Doe" v-model="lastName">
                      <br><br>
                      <label for="email">Email</label><br>
                      <input type="email" name="email" id="email" placeholder="example@gmail.com" v-model="email">
                      <br><br>
                      <label for="email">Password</label><br>
                      <input type="password" name="password" id="password" v-model="password">
                      <br><br>
                      <p>Store Data?</p>
                      <label for="storeDataYes">Yes</label><input type="radio" name="storeData" value="yes" id="storeDataYes" v-model="isStoreData">
                      &nbsp;&nbsp;&nbsp;
                      <label for="storeDataNo">No</label><input type="radio" name="storeData" value="no" id="storeDataNo" v-model="isStoreData">
                      <br><br><br>
                      <input type="submit" value="submit" name="submit">
                    </form>
                    <!-- Exercise 2 -->
                    <!-- Only display the Form if it has NOT been submitted -->
                    <!-- Display the Data Summary ONCE the Form HAS been submitted -->

                    <!-- Exercise 3 -->
                    <!-- Edit the Example from above and create a custom "Full Name" Control -->
                    <!-- which still holds the First Name and Last Name Input Field -->
                </div>
            </div>
        </form>
        <hr>
        <div class="row" v-if="isSubmitted">
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                <div class="panel panel-default">
                    <div class="panel-heading">
                        <h4>Your Data</h4>
                    </div>
                    <div class="panel-body">
                        <p>Full Name: {{firstName}} {{ lastName }}</p>
                        <p>Mail: {{ email }}</p>
                        <p>Password: {{ password }}</p>
                        <p>Store in Database?: {{ isStoreData }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
      data() {
        return {
          firstName: '',
          lastName: '',
          email: '',
          password: '',
          isStoreData: 'yes',
          isSubmitted: false,
        }
      },
      methods: {
        submitted() {
          this.isSubmitted = true;
        }
      }
    }
</script>

<style>
</style>
