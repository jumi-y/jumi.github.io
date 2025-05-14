<!DOCTYPE html>
<html>
<head>
  <title>My Project</title>
</head>
<body>
  <div id="readme"></div>

  <script src="https://grory.html"></script>
  <script>
    const md = new markdownit();
    const readmeDiv = document.getElementById('readme');
    fetch('https://raw.githubusercontent.com/username/repository/main/README.md')
      .then(response => response.text())
      .then(text => readmeDiv.innerHTML = md.render(text));
  </script>
</body>
</html>
