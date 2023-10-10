<template>
<div class="wrapper">
    <h1 class="title">User Page</h1>
   <!-- <nuxt-img 
          class="post-img"
    /> -->

    
  <form action="/upload" method="post" enctype="multipart/form-data">
      
      <div class="userinformation">
        <!-- Text input -->

        <label for="companyinfo">Company Info:</label>
        <input type="text" id="companyinfo" name="companyinfo" placeholder="Introduction...">

        <label for="currentprogram">Ongoing Programs:</label>
        <input type="text" id="currentprogram" name="currentprogram" placeholder="Now we have...">

        <label for="opennings">Looking for:</label>
        <input type="text" id="opennings" name="opennings" placeholder="We are looking for...">
      </div>
        <!-- File upload input -->
      <div>
        <label for="fileToUpload">Upload an image:</label>
        <input type="file" name="fileToUpload" id="fileToUpload"><br>
      </div>

        <!-- Submit button for the entire form -->
        
  </form>
  <div class="contentButtons">
    <Button :link="localePath('/user-page') + '/'" >Upload Content</Button><br>
    <Button :link="localePath('/user-page') + '/'" > Upload Pictures </Button> <!-- Translation needed-->
  </div>
</div>


</template>

<script>




</script>


<style>
.contentButtons {
    display: flex;
    flex-direction:column;
    align-items:center;
}
.post-img {
  max-width: 100%;
  border-radius: 1rem;
  margin-bottom: 2rem;
}
form{
  display: flex;
  flex-direction:column;
  align-items: center;
}

label{
  display:block;
  margin-bottom:5px;
}
input{
  width:600px;
  height:250px;
  margin-bottom:10px;
}
</style>