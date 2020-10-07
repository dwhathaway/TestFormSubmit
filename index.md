## Create a new GitHub App from an App Template Manifest

<script src="https://cdnjs.cloudflare.com/ajax/libs/js-yaml/3.14.0/js-yaml.min.js" integrity="sha512-ia9gcZkLHA+lkNST5XlseHz/No5++YBneMsDp1IZRJSbi1YqQvBeskJuG1kR+PH1w7E0bFgEZegcj0EwpXQnww==" crossorigin="anonymous"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/js-yaml/3.14.0/js-yaml.min.js" integrity="sha512-ia9gcZkLHA+lkNST5XlseHz/No5++YBneMsDp1IZRJSbi1YqQvBeskJuG1kR+PH1w7E0bFgEZegcj0EwpXQnww==" crossorigin="anonymous"></script>

<form action="https://github.com/settings/apps/new?state=abc123" method="post">
 Create a GitHub App Manifest: <textarea name="manifest" id="manifest"></textarea><br>
 <input type="submit" value="Submit">
</form>

<script>
 	input = document.getElementById("manifest");
	 
	 var appYamlUrl = 'https://raw.githubusercontent.com/dwhathaway/TestFormSubmit/main/App.yml';
	 
	 fetch(appYamlUrl)
	   .then(response => response.text())
	   .then(data => {
	   	var yamlObject = jsyaml.load(data)
	   	var jsonData = JSON.stringify(yamlObject);
	    // Do something with your data
	    input.value = jsonData;
	   });

</script>
