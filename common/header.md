<navbar placement="top" type="inverse">
  <a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand">{{ module_pair }} <small>{{ period }}</small></a>
  <li><a href="{{baseUrl}}/index.html" class="nav-link"><md>**Schedule**</md></a></li>
  <li><a href="{{baseUrl}}/se-book-adapted/index.html" class="nav-link"><md>**Textbook**</md></a></li>
  <li><a href="{{baseUrl}}/admin/index-tic2002.html" class="nav-link"><md>**Admin Info**</md></a></li>
  <dropdown text="Links" class="nav-link">
    <li><a href="{{bugs_link}}" target="_blank" class="dropdown-item"> {{ fas_bug }} Report Bugs</a></li>
    <li><a href="{{forum_link}}" target="_blank" class="dropdown-item">{{ fas_comment }} Forum</a></li>
    <li><a href="{{ivle_announcements}}" target="_blank" class="dropdown-item">{{ glyphicon_bullhorn }} Announcements</a></li>
    <li><a href="{{ivle_files}}" target="_blank" class="dropdown-item">{{ fas_file_upload }} File Submissions</a></li>
    <li><a href="{{java_coding_standard}}" target="_blank" class="dropdown-item">{{ fas_code }} Java Coding Standard</a></li>
    <li><a href="{{module_org}}/samplerepo-things" target="_blank" class="dropdown-item">{{ icon_repo }} samplerepo-things</a></li>
    <li><a href="{{module_org}}/addressbook-level1" target="_blank" class="dropdown-item">{{ icon_repo }} Addressbook-level1</a></li>
    <li><a href="{{module_org}}/addressbook-level2" target="_blank" class="dropdown-item">{{ icon_repo }} Addressbook-level2</a></li>
  </dropdown>
  <li slot="right" class="nav-link">
    <form class="navbar-form">
      <searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback" menu-align-right ></searchbar>
    </form>
  </li>
</navbar>
