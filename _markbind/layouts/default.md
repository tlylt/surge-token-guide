<head-bottom>
  <link rel="stylesheet" href="{{baseUrl}}/stylesheets/main.css">
</head-bottom>

<header fixed>
  <navbar type="dark">
    <a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand">Surge Token Guide</a>
    <li>
      <a href="https://github.com/tlylt/surge-token-guide" target="_blank" class="nav-link"><md>:fab-github:</md></a>
    </li>
    <li slot="right">
      <form class="navbar-form">
        <searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback" menu-align-right></searchbar>
      </form>
    </li>
  </navbar>
</header>

<div id="flex-body">
  <nav id="site-nav" class="fixed-header-padding">
    <div class="nav-component slim-scroll">
      <site-nav>
* [Home :house:]({{ baseUrl }}/index.html)
      </site-nav>
    </div>
  </nav>
  <div id="content-wrapper" class="fixed-header-padding">
    {{ content }}
  </div>
  <nav id="page-nav" class="fixed-header-padding">
    <div class="nav-component slim-scroll">
      <page-nav />
    </div>
  </nav>
</div>

<footer>
  <!-- Support MarkBind by including a link to us on your landing page! -->
  <div class="text-center">
    <small>[Generated by {{MarkBind}}]</small>
  </div>
</footer>