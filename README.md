<!DOCTYPE HTML>
<!--
/*
 * JavaScript Templates Demo
 * https://github.com/blueimp/JavaScript-Templates
 *
 * Copyright 2011, Sebastian Tschan
 * https://blueimp.net
 *
 * Licensed under the MIT license:
 * https://opensource.org/licenses/MIT
 */
-->
<html lang="en">
<head>
<!--[if IE]>
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
<![endif]-->
<meta charset="utf-8">
<title>JavaScript Templates Demo</title>
<meta name="description" content="1KB lightweight, fast &amp; powerful JavaScript templating engine with zero dependencies. Compatible with server-side environments like Node.js, module loaders like RequireJS, Browserify or webpack and all web browsers.">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel="stylesheet" href="css/demo.css">
</head>
<body>
<h1>JavaScript Templates Demo</h1>
<p><strong>1KB</strong> lightweight, fast &amp; powerful <a href="https://developer.mozilla.org/en/JavaScript/">JavaScript</a> templating engine with zero dependencies.<br>
Compatible with server-side environments like <a href="http://nodejs.org/">Node.js</a>, module loaders like <a href="http://requirejs.org/">RequireJS</a>, <a href="http://browserify.org/">Browserify</a> or <a href="https://webpack.github.io/">webpack</a> and all web browsers.</p>
<ul class="navigation">
    <li><a href="https://github.com/blueimp/JavaScript-Templates/tags">Download</a></li>
    <li><a href="https://github.com/blueimp/JavaScript-Templates">Source Code</a></li>
    <li><a href="https://github.com/blueimp/JavaScript-Templates/blob/master/README.md">Documentation</a></li>
    <li><a href="test/">Test</a></li>
    <li><a href="https://blueimp.net">&copy; Sebastian Tschan</a></li>
</ul>
<form>
    <h2>Template</h2>
    <textarea rows="12" id="template"></textarea>
    <br>
    <h2>Data (JSON)</h2>
    <textarea rows="14" id="data"></textarea>
    <br>
    <button type="submit" id="render">Render</button>
    <button type="reset" id="reset">Reset</button>
    <h2>Result</h2>
    <div id="result" class="result"></div>
    <br>
</form>
<script type="text/x-tmpl" id="tmpl-demo">
<h3>{%=o.title%}</h3>
<p>Released under the
<a href="{%=o.license.url%}">{%=o.license.name%}</a>.</p>
<h4>Features</h4>
<ul>
{% for (var i=0; i<o.features.length; i++) { %}
    <li>{%=o.features[i]%}</li>
{% } %}
</ul>
</script>
<script type="text/x-tmpl" id="tmpl-data">
{
    "title": "JavaScript Templates",
    "license": {
        "name": "MIT license",
        "url": "https://opensource.org/licenses/MIT"
    },
    "features": [
        "lightweight & fast",
        "powerful",
        "zero dependencies"
    ]
}
</script>
<script type="text/x-tmpl" id="tmpl-error">
<h3 class="error">{%=o.title%}</h3>
<code>{%=o.error%}</code>
</script>
<script src="js/tmpl.js"></script>
<script src="js/demo/demo.js"></script>
</body>
</html>