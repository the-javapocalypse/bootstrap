---
layout: home
---

<main class="bd-masthead" id="content" role="main">
  <div class="container">
    <div class="row align-items-center">
      <div class="col-6 mx-auto col-md-6 order-md-2">
        {{- partial "icons/bootstrap-stack.svg" (dict "class" "img-fluid mb-3 mb-md-0" "width" "512" "height" "430") -}}
      </div>
      <div class="col-md-6 order-md-1 text-center text-md-left pr-md-5">
        <h1 class="mb-3 bd-text-purple-bright">Bootstrap</h1>
        <p class="lead">
          Build responsive, mobile-first projects on the web with the world’s most popular front-end component library.
        </p>
        <p class="lead mb-4">
          Bootstrap is an open source toolkit for developing with HTML, CSS, and JS. Quickly prototype your ideas or build your entire app with our Sass variables and mixins, responsive grid system, extensive prebuilt components, and powerful plugins built on jQuery.
        </p>
        <div class="row mx-n2">
          <div class="col-md px-2">
            <a href="{{< ref "/getting-started/introduction.md" >}}" class="btn btn-lg btn-bd-primary w-100 mb-3" onclick="ga('send', 'event', 'Jumbotron actions', 'Get started', 'Get started');">Get started</a>
          </div>
          <div class="col-md px-2">
            <a href="{{% ref "/getting-started/download.md" %}}" class="btn btn-lg btn-outline-secondary w-100 mb-3" onclick="ga('send', 'event', 'Jumbotron actions', 'Download', 'Download {{< param current_version >}}');">Download</a>
          </div>
        </div>
        <p class="text-muted mb-0">
          Currently v{{< param current_version >}}
        </p>
      </div>
    </div>
    {{< partial "ads.html" >}}
  </div>
</main>

<div class="masthead-followup row m-0 border border-white">
  <div class="col-12 col-md-4 p-3 p-md-5 bg-light border border-white">
    <!-- Icon by Bytesize https://github.com/danklammer/bytesize-icons -->
    {{- partial "icons/import.svg" (dict "class" "text-primary mb-2" "width" "32" "height" "32") -}}
    <h3>Installation</h3>
    <p>Include Bootstrap’s source Sass and JavaScript files via npm, Composer or Meteor. Package managed installs don’t include documentation, but do include our build system and readme.</p>

{{< highlight sh >}}
npm install bootstrap
{{< /highlight >}}

{{< highlight sh >}}
gem install bootstrap -v {{< param current_ruby_version >}}
{{< /highlight >}}

    <hr class="half-rule">
    <a class="btn btn-outline-primary" href="{{ .Site.BaseURL }}/docs/{{< param docs_version >}}/getting-started/download/">Read installation docs</a>
  </div>

  <div class="col-12 col-md-4 p-3 p-md-5 bg-light border border-white">
    <!-- Icon by Bytesize https://github.com/danklammer/bytesize-icons -->
    {{- partial "icons/download.svg" (dict "class" "text-primary mb-2" "width" "32" "height" "32") -}}
    <h3>BootstrapCDN</h3>
    <p>When you only need to include Bootstrap’s compiled CSS or JS, you can use <a href="https://www.bootstrapcdn.com/">BootstrapCDN</a>.</p>

<h5>CSS only</h5>
{{< highlight html >}}
<link rel="stylesheet" href="{{< param "cdn.css" >}}" integrity="{{< param "cdn.css_hash" >}}" crossorigin="anonymous">
{{< /highlight >}}

<h5>JS, Popper.js, and jQuery</h5>
{{< highlight html >}}
<script src="{{< param "cdn.jquery" >}}" integrity="{{< param "cdn.jquery_hash" >}}" crossorigin="anonymous"></script>
<script src="{{< param "cdn.popper" >}}" integrity="{{< param "cdn.popper_hash" >}}" crossorigin="anonymous"></script>
<script src="{{< param "cdn.js" >}}" integrity="{{< param "cdn.js_hash" >}}" crossorigin="anonymous"></script>
{{< /highlight >}}
    <hr class="half-rule">
    <a class="btn btn-outline-primary" href="{{ .Site.BaseURL }}/docs/{{< param docs_version >}}/layout/overview/">Explore the docs</a>
  </div>

  <div class="col-12 col-md-4 p-3 p-md-5 bg-light border border-white">
    <!-- Icon by Bytesize https://github.com/danklammer/bytesize-icons -->
    {{- partial "icons/lightning.svg" (dict "class" "text-primary mb-2" "width" "32" "height" "32") -}}
    <h3>Official Themes</h3>
    <p>
      Take Bootstrap 4 to the next level with official premium themes—toolkits built on Bootstrap with new components and plugins, docs, and build tools.
    </p>
    <img class="img-fluid mt-3 mx-auto" srcset="{{ .Site.BaseURL }}/docs/{{< param docs_version >}}/assets/img/bootstrap-themes.png,
                                                {{ .Site.BaseURL }}/docs/{{< param docs_version >}}/assets/img/bootstrap-themes@2x.png 2x"
                                        src="{{ .Site.BaseURL }}/docs/{{< param docs_version >}}/assets/img/bootstrap-themes.png" alt="Bootstrap Themes" width="500" height="200">
    <hr class="half-rule">
    <a href="{{< param themes >}}/" class="btn btn-outline-primary">Browse themes</a>
  </div>
</div>
