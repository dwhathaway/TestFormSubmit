# TestFormSubmit

<form action="https://github.com/organizations/dwhathaway/settings/apps/new?state=abc123" method="post">
 Create a GitHub App Manifest: <input type="text" name="manifest" id="manifest"><br>
 <input type="submit" value="Submit">
</form>
<script>
 input = document.getElementById("manifest")
 input.value = JSON.stringify({
   "name": "Octoapp",
   "url": "https://www.example.com",
   "hook_attributes": {
     "url": "https://example.com/github/events",
   },
   "redirect_url": "https://example.com/callback",
   "public": true,
   "default_permissions": {
     "issues": "write",
     "checks": "write"
   },
   "default_events": [
     "issues",
     "issue_comment",
     "check_suite",
     "check_run"
   ]
 })
</script>
<img src="https://www.google.com/url?sa=i&url=https%3A%2F%2Fgithub.com%2Flogos&psig=AOvVaw1_mOpcBISknVcXHQJMYRIz&ust=1602732331283000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCMD7qqyRs-wCFQAAAAAdAAAAABAD"
onclick="alert('hello');" />
