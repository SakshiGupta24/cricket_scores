# cricket_scores
Get live cricket updates using this web application.
<!DOCTYPE html>
<html>
   <head>
      <meta charset="utf-8">
	   <link href="https://fonts.googleapis.com/css?family=ZCOOL+XiaoWei" rel="stylesheet">
      <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
      <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
      <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js">
      <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
      <title>CricFuzz</title>
      <style>
      body{
          background: #9fdf9f;
  background: radial-gradient(to right, rgb(51, 153, 102), rgb(204, 255, 220));
  font-family: 'ZCOOL XiaoWei', serif;
  
}
  h1 { 
  display: block;
  font-size: 5em;
  font-weight: bold;
}
      </style>
      <script>
         var scoresSettings = {
           "async": true,
           "crossDomain": true,
           "url": " https://cricapi.com/api/cricketScore?apikey=5dcOx3NouRgLk1tAw2e6RVhIeIJ3&unique_id=1175368",
           "method": "GET"
         }	
		 $.ajax(scoresSettings).done(function (response) {
           console.log(response);
           var details = response;
           $("#para").append(details.score);
         });
 
      </script>
   </head>
   <body>
   <center>
       <div class="container">
      <h1 class="text-primary">CricFuzz</h1>
	  <h2 class="text-secondary">Get Live Cricket Updates</h2>
      <br><br>
      <p class="btn btn-primary "id="para">Status: </p>
<button type="submit" class="btn btn-default" onclick="window.location.reload()"><span class="glyphicon glyphicon-repeat"></span> Get Updated Scores</button>
</div>
</center>
   </body>
</html>
