# buccwheat.github.io

<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>My GitHub Page</title>
  <style>
    .tab-content {
      display: none;
    }
  </style>
</head>
<body>
  <ul class="tab-nav">
    <li><button onclick="openTab(event, 'cv')">CV</button></li>
    <li><button onclick="openTab(event, 'blog')">Blog</button></li>
    <li><button onclick="openTab(event, 'projects')">Projects</button></li>
  </ul>

  <div id="cv" class="tab-content">
    <!-- Add your CV information here -->
    <h2>CV Information</h2>
    <p>Insert your CV content here...</p>
  </div>

  <div id="blog" class="tab-content">
    <!-- Add your blog-like entries here -->
    <h2>Blog Entries</h2>
    <p>Insert your blog content here...</p>
  </div>

  <div id="projects" class="tab-content">
    <!-- Add your projects here -->
    <h2>Projects</h2>
    <p>Insert your projects content here...</p>
  </div>

  <script>
    function openTab(evt, tabName) {
      var i, tabContent, tabLinks;

      tabContent = document.getElementsByClassName("tab-content");
      for (i = 0; i < tabContent.length; i++) {
        tabContent[i].style.display = "none";
      }

      tabLinks = document.getElementsByClassName("tab-nav")[0].getElementsByTagName("button");
      for (i = 0; i < tabLinks.length; i++) {
        tabLinks[i].className = tabLinks[i].className.replace(" active", "");
      }

      document.getElementById(tabName).style.display = "block";
      evt.currentTarget.className += " active";
    }
  </script>
</body>
</html>
