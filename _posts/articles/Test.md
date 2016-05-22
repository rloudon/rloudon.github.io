---
layout: post
title: "Welcome One and All"
date: 2016-05-22
categories: articles
tags: [data science, R, data.table, R package, data wrangling]
comments: true
share: true
---



# Portable R with Shiny

1. Preparing

2. Packaging

3. Publish

Bonus: TopoJSON mapping versus Shapefiles





## Test

<iframe srcdoc=' &lt;!doctype HTML&gt;
&lt;meta charset = &#039;utf-8&#039;&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;link rel=&#039;stylesheet&#039; href=&#039;http://nvd3.org/assets/css/nv.d3.css&#039;&gt;
    
    &lt;script src=&#039;http://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    &lt;script src=&#039;http://d3js.org/d3.v3.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    &lt;script src=&#039;http://timelyportfolio.github.io/rCharts_nvd3_tests/libraries/widgets/nvd3/js/nv.d3.min-new.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    &lt;script src=&#039;http://nvd3.org/assets/lib/fisheye.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    &lt;style&gt;
    .rChart {
      display: block;
      margin-left: auto; 
      margin-right: auto;
      width: 800px;
      height: 400px;
    }  
    &lt;/style&gt;
    
  &lt;/head&gt;
  &lt;body &gt;
    
    &lt;div id = &#039;chartfb0773e4c&#039; class = &#039;rChart nvd3&#039;&gt;&lt;/div&gt;    
    &lt;script type=&#039;text/javascript&#039;&gt;
 $(document).ready(function(){
      drawchartfb0773e4c()
    });
    function drawchartfb0773e4c(){  
      var opts = {
 &quot;dom&quot;: &quot;chartfb0773e4c&quot;,
&quot;width&quot;:    800,
&quot;height&quot;:    400,
&quot;x&quot;: &quot;Hair&quot;,
&quot;y&quot;: &quot;Freq&quot;,
&quot;group&quot;: &quot;Eye&quot;,
&quot;type&quot;: &quot;multiBarChart&quot;,
&quot;id&quot;: &quot;chartfb0773e4c&quot; 
},
        data = [
 {
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             32 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             53 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             10 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              3 
},
{
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             11 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             50 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             10 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             30 
},
{
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             10 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             25 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              7 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              5 
},
{
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              3 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             15 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              7 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              8 
} 
]
  
      if(!(opts.type===&quot;pieChart&quot; || opts.type===&quot;sparklinePlus&quot; || opts.type===&quot;bulletChart&quot;)) {
        var data = d3.nest()
          .key(function(d){
            //return opts.group === undefined ? &#039;main&#039; : d[opts.group]
            //instead of main would think a better default is opts.x
            return opts.group === undefined ? opts.y : d[opts.group];
          })
          .entries(data);
      }
      
      if (opts.disabled != undefined){
        data.map(function(d, i){
          d.disabled = opts.disabled[i]
        })
      }
      
      nv.addGraph(function() {
        var chart = nv.models[opts.type]()
          .width(opts.width)
          .height(opts.height)
          
        if (opts.type != &quot;bulletChart&quot;){
          chart
            .x(function(d) { return d[opts.x] })
            .y(function(d) { return d[opts.y] })
        }
          
         
        
          
        

        
        
        
      
       d3.select(&quot;#&quot; + opts.id)
        .append(&#039;svg&#039;)
        .datum(data)
        .transition().duration(500)
        .call(chart);

       nv.utils.windowResize(chart.update);
       return chart;
      });
    };
&lt;/script&gt;
    
    &lt;script&gt;&lt;/script&gt;    
  &lt;/body&gt;
&lt;/html&gt; ' scrolling='no' frameBorder='0' seamless class='rChart  nvd3  ' id='iframe-chartfb0773e4c'> </iframe>
 <style>iframe.rChart{ width: 100%; height: 400px;}</style>
<div id = 'fig1' class = 'rChart nvd3'></div>
<script type='text/javascript'>
 $(document).ready(function(){
      drawfig1()
    });
    function drawfig1(){  
      var opts = {
 "dom": "fig1",
"width":    800,
"height":    400,
"x": "Hair",
"y": "Freq",
"group": "Eye",
"type": "multiBarChart",
"id": "fig1" 
},
        data = [
 {
 "Hair": "Black",
"Eye": "Brown",
"Sex": "Male",
"Freq":             32 
},
{
 "Hair": "Brown",
"Eye": "Brown",
"Sex": "Male",
"Freq":             53 
},
{
 "Hair": "Red",
"Eye": "Brown",
"Sex": "Male",
"Freq":             10 
},
{
 "Hair": "Blond",
"Eye": "Brown",
"Sex": "Male",
"Freq":              3 
},
{
 "Hair": "Black",
"Eye": "Blue",
"Sex": "Male",
"Freq":             11 
},
{
 "Hair": "Brown",
"Eye": "Blue",
"Sex": "Male",
"Freq":             50 
},
{
 "Hair": "Red",
"Eye": "Blue",
"Sex": "Male",
"Freq":             10 
},
{
 "Hair": "Blond",
"Eye": "Blue",
"Sex": "Male",
"Freq":             30 
},
{
 "Hair": "Black",
"Eye": "Hazel",
"Sex": "Male",
"Freq":             10 
},
{
 "Hair": "Brown",
"Eye": "Hazel",
"Sex": "Male",
"Freq":             25 
},
{
 "Hair": "Red",
"Eye": "Hazel",
"Sex": "Male",
"Freq":              7 
},
{
 "Hair": "Blond",
"Eye": "Hazel",
"Sex": "Male",
"Freq":              5 
},
{
 "Hair": "Black",
"Eye": "Green",
"Sex": "Male",
"Freq":              3 
},
{
 "Hair": "Brown",
"Eye": "Green",
"Sex": "Male",
"Freq":             15 
},
{
 "Hair": "Red",
"Eye": "Green",
"Sex": "Male",
"Freq":              7 
},
{
 "Hair": "Blond",
"Eye": "Green",
"Sex": "Male",
"Freq":              8 
} 
]
  
      if(!(opts.type==="pieChart" || opts.type==="sparklinePlus" || opts.type==="bulletChart")) {
        var data = d3.nest()
          .key(function(d){
            //return opts.group === undefined ? 'main' : d[opts.group]
            //instead of main would think a better default is opts.x
            return opts.group === undefined ? opts.y : d[opts.group];
          })
          .entries(data);
      }
      
      if (opts.disabled != undefined){
        data.map(function(d, i){
          d.disabled = opts.disabled[i]
        })
      }
      
      nv.addGraph(function() {
        var chart = nv.models[opts.type]()
          .width(opts.width)
          .height(opts.height)
          
        if (opts.type != "bulletChart"){
          chart
            .x(function(d) { return d[opts.x] })
            .y(function(d) { return d[opts.y] })
        }
          
         
        
          
        

        
        
        
      
       d3.select("#" + opts.id)
        .append('svg')
        .datum(data)
        .transition().duration(500)
        .call(chart);

       nv.utils.windowResize(chart.update);
       return chart;
      });
    };
</script>
<iframe srcdoc=' &lt;!doctype HTML&gt;
&lt;meta charset = &#039;utf-8&#039;&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;link rel=&#039;stylesheet&#039; href=&#039;C:/Program Files/R/R-3.2.3/library/rCharts/libraries/nvd3/css/nv.d3.css&#039;&gt;
    &lt;link rel=&#039;stylesheet&#039; href=&#039;C:/Program Files/R/R-3.2.3/library/rCharts/libraries/nvd3/css/rNVD3.css&#039;&gt;
    
    &lt;script src=&#039;C:/Program Files/R/R-3.2.3/library/rCharts/libraries/nvd3/js/jquery-1.8.2.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    &lt;script src=&#039;C:/Program Files/R/R-3.2.3/library/rCharts/libraries/nvd3/js/d3.v3.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    &lt;script src=&#039;C:/Program Files/R/R-3.2.3/library/rCharts/libraries/nvd3/js/nv.d3.min-new.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    &lt;script src=&#039;C:/Program Files/R/R-3.2.3/library/rCharts/libraries/nvd3/js/fisheye.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    &lt;style&gt;
    .rChart {
      display: block;
      margin-left: auto; 
      margin-right: auto;
      width: 800px;
      height: 400px;
    }  
    &lt;/style&gt;
    
  &lt;/head&gt;
  &lt;body &gt;
    
    &lt;div id = &#039;fig1&#039; class = &#039;rChart nvd3&#039;&gt;&lt;/div&gt;    
    &lt;script type=&#039;text/javascript&#039;&gt;
 $(document).ready(function(){
      drawfig1()
    });
    function drawfig1(){  
      var opts = {
 &quot;dom&quot;: &quot;fig1&quot;,
&quot;width&quot;:    800,
&quot;height&quot;:    400,
&quot;x&quot;: &quot;Hair&quot;,
&quot;y&quot;: &quot;Freq&quot;,
&quot;group&quot;: &quot;Eye&quot;,
&quot;type&quot;: &quot;multiBarChart&quot;,
&quot;id&quot;: &quot;fig1&quot; 
},
        data = [
 {
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             32 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             53 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             10 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              3 
},
{
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             11 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             50 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             10 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             30 
},
{
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             10 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             25 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              7 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              5 
},
{
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              3 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             15 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              7 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              8 
} 
]
  
      if(!(opts.type===&quot;pieChart&quot; || opts.type===&quot;sparklinePlus&quot; || opts.type===&quot;bulletChart&quot;)) {
        var data = d3.nest()
          .key(function(d){
            //return opts.group === undefined ? &#039;main&#039; : d[opts.group]
            //instead of main would think a better default is opts.x
            return opts.group === undefined ? opts.y : d[opts.group];
          })
          .entries(data);
      }
      
      if (opts.disabled != undefined){
        data.map(function(d, i){
          d.disabled = opts.disabled[i]
        })
      }
      
      nv.addGraph(function() {
        var chart = nv.models[opts.type]()
          .width(opts.width)
          .height(opts.height)
          
        if (opts.type != &quot;bulletChart&quot;){
          chart
            .x(function(d) { return d[opts.x] })
            .y(function(d) { return d[opts.y] })
        }
          
         
        
          
        

        
        
        
      
       d3.select(&quot;#&quot; + opts.id)
        .append(&#039;svg&#039;)
        .datum(data)
        .transition().duration(500)
        .call(chart);

       nv.utils.windowResize(chart.update);
       return chart;
      });
    };
&lt;/script&gt;
    
    &lt;script&gt;&lt;/script&gt;    
  &lt;/body&gt;
&lt;/html&gt; ' scrolling='no' frameBorder='0' seamless class='rChart  nvd3  ' id='iframe-fig1'> </iframe>
 <style>iframe.rChart{ width: 100%; height: 400px;}</style>


{% highlight text %}
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
   2.00   26.00   36.00   42.98   56.00  120.00 
{% endhighlight %}



## R Markdown

This is an R Markdown presentation. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown.



# Slide with R Code and Output


{% highlight text %}
     speed           dist       
 Min.   : 4.0   Min.   :  2.00  
 1st Qu.:12.0   1st Qu.: 26.00  
 Median :15.0   Median : 36.00  
 Mean   :15.4   Mean   : 42.98  
 3rd Qu.:19.0   3rd Qu.: 56.00  
 Max.   :25.0   Max.   :120.00  
{% endhighlight %}

# Leaflet HTMLWidget

<!--html_preserve--><div id="htmlwidget-6635" style="width:612px;height:378px;" class="leaflet"></div>
<script type="application/json" data-for="htmlwidget-6635">{"x":{"calls":[{"method":"addTiles","args":["http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"maxNativeZoom":null,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"continuousWorld":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":null,"unloadInvisibleTiles":null,"updateWhenIdle":null,"detectRetina":false,"reuseTiles":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap</a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA</a>"}]},{"method":"addMarkers","args":[-36.852,174.768,null,null,null,{"clickable":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},"The birthplace of R",null,null]}],"limits":{"lat":[-36.852,-36.852],"lng":[174.768,174.768]}},"evals":[]}</script><!--/html_preserve-->

# Parallel Coordinates

<iframe srcdoc=' &lt;!doctype HTML&gt;
&lt;meta charset = &#039;utf-8&#039;&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;link rel=&#039;stylesheet&#039; href=&#039;http://cdn.oesmith.co.uk/morris-0.4.2.min.css&#039;&gt;
    
    &lt;script src=&#039;http://ajax.googleapis.com/ajax/libs/jquery/1.9.0/jquery.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    &lt;script src=&#039;http://cdnjs.cloudflare.com/ajax/libs/raphael/2.1.0/raphael-min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    &lt;script src=&#039;http://cdn.oesmith.co.uk/morris-0.4.2.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    &lt;style&gt;
    .rChart {
      display: block;
      margin-left: auto; 
      margin-right: auto;
      width: 800px;
      height: 400px;
    }  
    &lt;/style&gt;
    
  &lt;/head&gt;
  &lt;body &gt;
    
    &lt;div id = &#039;chartfb02ecf686a&#039; class = &#039;rChart morris&#039;&gt;&lt;/div&gt;    
    &lt;script type=&#039;text/javascript&#039;&gt;
    var chartParams = {
 &quot;element&quot;: &quot;chartfb02ecf686a&quot;,
&quot;width&quot;:            800,
&quot;height&quot;:            400,
&quot;xkey&quot;: &quot;date&quot;,
&quot;ykeys&quot;: [
 &quot;psavert&quot;,
&quot;uempmed&quot; 
],
&quot;data&quot;: [
 {
 &quot;date&quot;: &quot;1967-07-01&quot;,
&quot;pce&quot;:          507.4,
&quot;pop&quot;: 198712,
&quot;psavert&quot;:           12.5,
&quot;uempmed&quot;:            4.5,
&quot;unemploy&quot;: 2944 
},
{
 &quot;date&quot;: &quot;1967-08-01&quot;,
&quot;pce&quot;:          510.5,
&quot;pop&quot;: 198911,
&quot;psavert&quot;:           12.5,
&quot;uempmed&quot;:            4.7,
&quot;unemploy&quot;: 2945 
},
{
 &quot;date&quot;: &quot;1967-09-01&quot;,
&quot;pce&quot;:          516.3,
&quot;pop&quot;: 199113,
&quot;psavert&quot;:           11.7,
&quot;uempmed&quot;:            4.6,
&quot;unemploy&quot;: 2958 
},
{
 &quot;date&quot;: &quot;1967-10-01&quot;,
&quot;pce&quot;:          512.9,
&quot;pop&quot;: 199311,
&quot;psavert&quot;:           12.5,
&quot;uempmed&quot;:            4.9,
&quot;unemploy&quot;: 3143 
},
{
 &quot;date&quot;: &quot;1967-11-01&quot;,
&quot;pce&quot;:          518.1,
&quot;pop&quot;: 199498,
&quot;psavert&quot;:           12.5,
&quot;uempmed&quot;:            4.7,
&quot;unemploy&quot;: 3066 
},
{
 &quot;date&quot;: &quot;1967-12-01&quot;,
&quot;pce&quot;:          525.8,
&quot;pop&quot;: 199657,
&quot;psavert&quot;:           12.1,
&quot;uempmed&quot;:            4.8,
&quot;unemploy&quot;: 3018 
},
{
 &quot;date&quot;: &quot;1968-01-01&quot;,
&quot;pce&quot;:          531.5,
&quot;pop&quot;: 199808,
&quot;psavert&quot;:           11.7,
&quot;uempmed&quot;:            5.1,
&quot;unemploy&quot;: 2878 
},
{
 &quot;date&quot;: &quot;1968-02-01&quot;,
&quot;pce&quot;:          534.2,
&quot;pop&quot;: 199920,
&quot;psavert&quot;:           12.2,
&quot;uempmed&quot;:            4.5,
&quot;unemploy&quot;: 3001 
},
{
 &quot;date&quot;: &quot;1968-03-01&quot;,
&quot;pce&quot;:          544.9,
&quot;pop&quot;: 200056,
&quot;psavert&quot;:           11.6,
&quot;uempmed&quot;:            4.1,
&quot;unemploy&quot;: 2877 
},
{
 &quot;date&quot;: &quot;1968-04-01&quot;,
&quot;pce&quot;:          544.6,
&quot;pop&quot;: 200208,
&quot;psavert&quot;:           12.2,
&quot;uempmed&quot;:            4.6,
&quot;unemploy&quot;: 2709 
},
{
 &quot;date&quot;: &quot;1968-05-01&quot;,
&quot;pce&quot;:          550.4,
&quot;pop&quot;: 200361,
&quot;psavert&quot;:             12,
&quot;uempmed&quot;:            4.4,
&quot;unemploy&quot;: 2740 
},
{
 &quot;date&quot;: &quot;1968-06-01&quot;,
&quot;pce&quot;:          556.8,
&quot;pop&quot;: 200536,
&quot;psavert&quot;:           11.6,
&quot;uempmed&quot;:            4.4,
&quot;unemploy&quot;: 2938 
},
{
 &quot;date&quot;: &quot;1968-07-01&quot;,
&quot;pce&quot;:          563.8,
&quot;pop&quot;: 200706,
&quot;psavert&quot;:           10.6,
&quot;uempmed&quot;:            4.5,
&quot;unemploy&quot;: 2883 
},
{
 &quot;date&quot;: &quot;1968-08-01&quot;,
&quot;pce&quot;:          567.6,
&quot;pop&quot;: 200898,
&quot;psavert&quot;:           10.4,
&quot;uempmed&quot;:            4.2,
&quot;unemploy&quot;: 2768 
},
{
 &quot;date&quot;: &quot;1968-09-01&quot;,
&quot;pce&quot;:          568.8,
&quot;pop&quot;: 201095,
&quot;psavert&quot;:           10.4,
&quot;uempmed&quot;:            4.6,
&quot;unemploy&quot;: 2686 
},
{
 &quot;date&quot;: &quot;1968-10-01&quot;,
&quot;pce&quot;:          572.3,
&quot;pop&quot;: 201290,
&quot;psavert&quot;:           10.6,
&quot;uempmed&quot;:            4.8,
&quot;unemploy&quot;: 2689 
},
{
 &quot;date&quot;: &quot;1968-11-01&quot;,
&quot;pce&quot;:          577.4,
&quot;pop&quot;: 201466,
&quot;psavert&quot;:           10.4,
&quot;uempmed&quot;:            4.4,
&quot;unemploy&quot;: 2715 
},
{
 &quot;date&quot;: &quot;1968-12-01&quot;,
&quot;pce&quot;:          577.2,
&quot;pop&quot;: 201621,
&quot;psavert&quot;:           10.9,
&quot;uempmed&quot;:            4.4,
&quot;unemploy&quot;: 2685 
},
{
 &quot;date&quot;: &quot;1969-01-01&quot;,
&quot;pce&quot;:          584.2,
&quot;pop&quot;: 201760,
&quot;psavert&quot;:             10,
&quot;uempmed&quot;:            4.4,
&quot;unemploy&quot;: 2718 
},
{
 &quot;date&quot;: &quot;1969-02-01&quot;,
&quot;pce&quot;:          589.5,
&quot;pop&quot;: 201881,
&quot;psavert&quot;:            9.4,
&quot;uempmed&quot;:            4.9,
&quot;unemploy&quot;: 2692 
},
{
 &quot;date&quot;: &quot;1969-03-01&quot;,
&quot;pce&quot;:          589.7,
&quot;pop&quot;: 202023,
&quot;psavert&quot;:            9.9,
&quot;uempmed&quot;:              4,
&quot;unemploy&quot;: 2712 
},
{
 &quot;date&quot;: &quot;1969-04-01&quot;,
&quot;pce&quot;:          594.7,
&quot;pop&quot;: 202161,
&quot;psavert&quot;:            9.5,
&quot;uempmed&quot;:              4,
&quot;unemploy&quot;: 2758 
},
{
 &quot;date&quot;: &quot;1969-05-01&quot;,
&quot;pce&quot;:          601.1,
&quot;pop&quot;: 202331,
&quot;psavert&quot;:             10,
&quot;uempmed&quot;:            4.2,
&quot;unemploy&quot;: 2713 
},
{
 &quot;date&quot;: &quot;1969-06-01&quot;,
&quot;pce&quot;:          601.7,
&quot;pop&quot;: 202507,
&quot;psavert&quot;:           10.9,
&quot;uempmed&quot;:            4.4,
&quot;unemploy&quot;: 2816 
},
{
 &quot;date&quot;: &quot;1969-07-01&quot;,
&quot;pce&quot;:          603.5,
&quot;pop&quot;: 202677,
&quot;psavert&quot;:           11.7,
&quot;uempmed&quot;:            4.4,
&quot;unemploy&quot;: 2868 
},
{
 &quot;date&quot;: &quot;1969-08-01&quot;,
&quot;pce&quot;:          610.8,
&quot;pop&quot;: 202877,
&quot;psavert&quot;:           11.5,
&quot;uempmed&quot;:            4.4,
&quot;unemploy&quot;: 2856 
},
{
 &quot;date&quot;: &quot;1969-09-01&quot;,
&quot;pce&quot;:          614.1,
&quot;pop&quot;: 203090,
&quot;psavert&quot;:           11.5,
&quot;uempmed&quot;:            4.7,
&quot;unemploy&quot;: 3040 
},
{
 &quot;date&quot;: &quot;1969-10-01&quot;,
&quot;pce&quot;:          619.4,
&quot;pop&quot;: 203302,
&quot;psavert&quot;:           11.3,
&quot;uempmed&quot;:            4.5,
&quot;unemploy&quot;: 3049 
},
{
 &quot;date&quot;: &quot;1969-11-01&quot;,
&quot;pce&quot;:          621.4,
&quot;pop&quot;: 203500,
&quot;psavert&quot;:           11.5,
&quot;uempmed&quot;:            4.8,
&quot;unemploy&quot;: 2856 
},
{
 &quot;date&quot;: &quot;1969-12-01&quot;,
&quot;pce&quot;:          623.7,
&quot;pop&quot;: 203675,
&quot;psavert&quot;:           11.7,
&quot;uempmed&quot;:            4.6,
&quot;unemploy&quot;: 2884 
},
{
 &quot;date&quot;: &quot;1970-01-01&quot;,
&quot;pce&quot;:          629.6,
&quot;pop&quot;: 203849,
&quot;psavert&quot;:           11.7,
&quot;uempmed&quot;:            4.6,
&quot;unemploy&quot;: 3201 
},
{
 &quot;date&quot;: &quot;1970-02-01&quot;,
&quot;pce&quot;:          634.9,
&quot;pop&quot;: 204008,
&quot;psavert&quot;:           11.6,
&quot;uempmed&quot;:            4.5,
&quot;unemploy&quot;: 3453 
},
{
 &quot;date&quot;: &quot;1970-03-01&quot;,
&quot;pce&quot;:          633.2,
&quot;pop&quot;: 204156,
&quot;psavert&quot;:           12.3,
&quot;uempmed&quot;:            4.6,
&quot;unemploy&quot;: 3635 
},
{
 &quot;date&quot;: &quot;1970-04-01&quot;,
&quot;pce&quot;:            637,
&quot;pop&quot;: 204401,
&quot;psavert&quot;:           13.3,
&quot;uempmed&quot;:            4.1,
&quot;unemploy&quot;: 3797 
},
{
 &quot;date&quot;: &quot;1970-05-01&quot;,
&quot;pce&quot;:          643.4,
&quot;pop&quot;: 204607,
&quot;psavert&quot;:           12.3,
&quot;uempmed&quot;:            4.7,
&quot;unemploy&quot;: 3919 
},
{
 &quot;date&quot;: &quot;1970-06-01&quot;,
&quot;pce&quot;:          647.2,
&quot;pop&quot;: 204830,
&quot;psavert&quot;:           11.7,
&quot;uempmed&quot;:            4.9,
&quot;unemploy&quot;: 4071 
},
{
 &quot;date&quot;: &quot;1970-07-01&quot;,
&quot;pce&quot;:          649.5,
&quot;pop&quot;: 205052,
&quot;psavert&quot;:           13.2,
&quot;uempmed&quot;:            5.1,
&quot;unemploy&quot;: 4175 
},
{
 &quot;date&quot;: &quot;1970-08-01&quot;,
&quot;pce&quot;:          653.9,
&quot;pop&quot;: 205295,
&quot;psavert&quot;:           13.1,
&quot;uempmed&quot;:            5.4,
&quot;unemploy&quot;: 4256 
},
{
 &quot;date&quot;: &quot;1970-09-01&quot;,
&quot;pce&quot;:          660.1,
&quot;pop&quot;: 205540,
&quot;psavert&quot;:           12.9,
&quot;uempmed&quot;:            5.2,
&quot;unemploy&quot;: 4456 
},
{
 &quot;date&quot;: &quot;1970-10-01&quot;,
&quot;pce&quot;:          659.3,
&quot;pop&quot;: 205788,
&quot;psavert&quot;:             13,
&quot;uempmed&quot;:            5.2,
&quot;unemploy&quot;: 4591 
},
{
 &quot;date&quot;: &quot;1970-11-01&quot;,
&quot;pce&quot;:          657.6,
&quot;pop&quot;: 206024,
&quot;psavert&quot;:           13.3,
&quot;uempmed&quot;:            5.6,
&quot;unemploy&quot;: 4898 
},
{
 &quot;date&quot;: &quot;1970-12-01&quot;,
&quot;pce&quot;:          666.6,
&quot;pop&quot;: 206238,
&quot;psavert&quot;:           12.9,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 5076 
},
{
 &quot;date&quot;: &quot;1971-01-01&quot;,
&quot;pce&quot;:          677.2,
&quot;pop&quot;: 206466,
&quot;psavert&quot;:           13.1,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 4986 
},
{
 &quot;date&quot;: &quot;1971-02-01&quot;,
&quot;pce&quot;:          680.4,
&quot;pop&quot;: 206668,
&quot;psavert&quot;:           13.1,
&quot;uempmed&quot;:            6.3,
&quot;unemploy&quot;: 4903 
},
{
 &quot;date&quot;: &quot;1971-03-01&quot;,
&quot;pce&quot;:            683,
&quot;pop&quot;: 206855,
&quot;psavert&quot;:           13.3,
&quot;uempmed&quot;:            6.4,
&quot;unemploy&quot;: 4987 
},
{
 &quot;date&quot;: &quot;1971-04-01&quot;,
&quot;pce&quot;:          689.8,
&quot;pop&quot;: 207065,
&quot;psavert&quot;:             13,
&quot;uempmed&quot;:            6.5,
&quot;unemploy&quot;: 4959 
},
{
 &quot;date&quot;: &quot;1971-05-01&quot;,
&quot;pce&quot;:          692.2,
&quot;pop&quot;: 207260,
&quot;psavert&quot;:           13.4,
&quot;uempmed&quot;:            6.7,
&quot;unemploy&quot;: 4996 
},
{
 &quot;date&quot;: &quot;1971-06-01&quot;,
&quot;pce&quot;:          700.8,
&quot;pop&quot;: 207462,
&quot;psavert&quot;:           14.4,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 4949 
},
{
 &quot;date&quot;: &quot;1971-07-01&quot;,
&quot;pce&quot;:          699.9,
&quot;pop&quot;: 207661,
&quot;psavert&quot;:           13.6,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 5035 
},
{
 &quot;date&quot;: &quot;1971-08-01&quot;,
&quot;pce&quot;:            706,
&quot;pop&quot;: 207881,
&quot;psavert&quot;:           13.6,
&quot;uempmed&quot;:            6.4,
&quot;unemploy&quot;: 5134 
},
{
 &quot;date&quot;: &quot;1971-09-01&quot;,
&quot;pce&quot;:          714.1,
&quot;pop&quot;: 208114,
&quot;psavert&quot;:           12.9,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 5042 
},
{
 &quot;date&quot;: &quot;1971-10-01&quot;,
&quot;pce&quot;:          716.9,
&quot;pop&quot;: 208345,
&quot;psavert&quot;:             13,
&quot;uempmed&quot;:            6.5,
&quot;unemploy&quot;: 4954 
},
{
 &quot;date&quot;: &quot;1971-11-01&quot;,
&quot;pce&quot;:          722.1,
&quot;pop&quot;: 208555,
&quot;psavert&quot;:           12.8,
&quot;uempmed&quot;:            6.4,
&quot;unemploy&quot;: 5161 
},
{
 &quot;date&quot;: &quot;1971-12-01&quot;,
&quot;pce&quot;:          729.6,
&quot;pop&quot;: 208740,
&quot;psavert&quot;:           12.9,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 5154 
},
{
 &quot;date&quot;: &quot;1972-01-01&quot;,
&quot;pce&quot;:          732.6,
&quot;pop&quot;: 208917,
&quot;psavert&quot;:           12.4,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 5019 
},
{
 &quot;date&quot;: &quot;1972-02-01&quot;,
&quot;pce&quot;:          737.3,
&quot;pop&quot;: 209061,
&quot;psavert&quot;:           12.6,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 4928 
},
{
 &quot;date&quot;: &quot;1972-03-01&quot;,
&quot;pce&quot;:          750.4,
&quot;pop&quot;: 209212,
&quot;psavert&quot;:           11.5,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 5038 
},
{
 &quot;date&quot;: &quot;1972-04-01&quot;,
&quot;pce&quot;:          753.8,
&quot;pop&quot;: 209386,
&quot;psavert&quot;:           11.3,
&quot;uempmed&quot;:            6.7,
&quot;unemploy&quot;: 4959 
},
{
 &quot;date&quot;: &quot;1972-05-01&quot;,
&quot;pce&quot;:          759.2,
&quot;pop&quot;: 209545,
&quot;psavert&quot;:           11.5,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 4922 
},
{
 &quot;date&quot;: &quot;1972-06-01&quot;,
&quot;pce&quot;:          762.9,
&quot;pop&quot;: 209725,
&quot;psavert&quot;:           11.4,
&quot;uempmed&quot;:            5.4,
&quot;unemploy&quot;: 4923 
},
{
 &quot;date&quot;: &quot;1972-07-01&quot;,
&quot;pce&quot;:          771.2,
&quot;pop&quot;: 209896,
&quot;psavert&quot;:           11.4,
&quot;uempmed&quot;:            6.1,
&quot;unemploy&quot;: 4913 
},
{
 &quot;date&quot;: &quot;1972-08-01&quot;,
&quot;pce&quot;:          777.7,
&quot;pop&quot;: 210075,
&quot;psavert&quot;:           11.8,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 4939 
},
{
 &quot;date&quot;: &quot;1972-09-01&quot;,
&quot;pce&quot;:          782.5,
&quot;pop&quot;: 210278,
&quot;psavert&quot;:             12,
&quot;uempmed&quot;:            5.6,
&quot;unemploy&quot;: 4849 
},
{
 &quot;date&quot;: &quot;1972-10-01&quot;,
&quot;pce&quot;:          796.3,
&quot;pop&quot;: 210479,
&quot;psavert&quot;:           12.7,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 4875 
},
{
 &quot;date&quot;: &quot;1972-11-01&quot;,
&quot;pce&quot;:          801.8,
&quot;pop&quot;: 210656,
&quot;psavert&quot;:           13.4,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 4602 
},
{
 &quot;date&quot;: &quot;1972-12-01&quot;,
&quot;pce&quot;:          807.5,
&quot;pop&quot;: 210821,
&quot;psavert&quot;:           13.4,
&quot;uempmed&quot;:            6.1,
&quot;unemploy&quot;: 4543 
},
{
 &quot;date&quot;: &quot;1973-01-01&quot;,
&quot;pce&quot;:          817.9,
&quot;pop&quot;: 210985,
&quot;psavert&quot;:           12.1,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 4326 
},
{
 &quot;date&quot;: &quot;1973-02-01&quot;,
&quot;pce&quot;:          827.2,
&quot;pop&quot;: 211120,
&quot;psavert&quot;:           12.2,
&quot;uempmed&quot;:            5.2,
&quot;unemploy&quot;: 4452 
},
{
 &quot;date&quot;: &quot;1973-03-01&quot;,
&quot;pce&quot;:          834.2,
&quot;pop&quot;: 211254,
&quot;psavert&quot;:           12.4,
&quot;uempmed&quot;:            5.5,
&quot;unemploy&quot;: 4394 
},
{
 &quot;date&quot;: &quot;1973-04-01&quot;,
&quot;pce&quot;:          837.2,
&quot;pop&quot;: 211420,
&quot;psavert&quot;:           12.8,
&quot;uempmed&quot;:              5,
&quot;unemploy&quot;: 4459 
},
{
 &quot;date&quot;: &quot;1973-05-01&quot;,
&quot;pce&quot;:          843.1,
&quot;pop&quot;: 211577,
&quot;psavert&quot;:           12.8,
&quot;uempmed&quot;:            4.9,
&quot;unemploy&quot;: 4329 
},
{
 &quot;date&quot;: &quot;1973-06-01&quot;,
&quot;pce&quot;:          845.8,
&quot;pop&quot;: 211746,
&quot;psavert&quot;:           13.2,
&quot;uempmed&quot;:              5,
&quot;unemploy&quot;: 4363 
},
{
 &quot;date&quot;: &quot;1973-07-01&quot;,
&quot;pce&quot;:          855.7,
&quot;pop&quot;: 211909,
&quot;psavert&quot;:           12.8,
&quot;uempmed&quot;:            5.2,
&quot;unemploy&quot;: 4305 
},
{
 &quot;date&quot;: &quot;1973-08-01&quot;,
&quot;pce&quot;:          854.9,
&quot;pop&quot;: 212092,
&quot;psavert&quot;:           13.6,
&quot;uempmed&quot;:            4.9,
&quot;unemploy&quot;: 4305 
},
{
 &quot;date&quot;: &quot;1973-09-01&quot;,
&quot;pce&quot;:          870.9,
&quot;pop&quot;: 212289,
&quot;psavert&quot;:           12.8,
&quot;uempmed&quot;:            5.4,
&quot;unemploy&quot;: 4350 
},
{
 &quot;date&quot;: &quot;1973-10-01&quot;,
&quot;pce&quot;:          869.8,
&quot;pop&quot;: 212475,
&quot;psavert&quot;:             14,
&quot;uempmed&quot;:            5.5,
&quot;unemploy&quot;: 4144 
},
{
 &quot;date&quot;: &quot;1973-11-01&quot;,
&quot;pce&quot;:          878.6,
&quot;pop&quot;: 212634,
&quot;psavert&quot;:             14,
&quot;uempmed&quot;:            5.1,
&quot;unemploy&quot;: 4396 
},
{
 &quot;date&quot;: &quot;1973-12-01&quot;,
&quot;pce&quot;:          878.4,
&quot;pop&quot;: 212785,
&quot;psavert&quot;:           14.4,
&quot;uempmed&quot;:            4.7,
&quot;unemploy&quot;: 4489 
},
{
 &quot;date&quot;: &quot;1974-01-01&quot;,
&quot;pce&quot;:          886.4,
&quot;pop&quot;: 212932,
&quot;psavert&quot;:             14,
&quot;uempmed&quot;:              5,
&quot;unemploy&quot;: 4644 
},
{
 &quot;date&quot;: &quot;1974-02-01&quot;,
&quot;pce&quot;:          891.6,
&quot;pop&quot;: 213074,
&quot;psavert&quot;:           13.8,
&quot;uempmed&quot;:            5.1,
&quot;unemploy&quot;: 4731 
},
{
 &quot;date&quot;: &quot;1974-03-01&quot;,
&quot;pce&quot;:          903.3,
&quot;pop&quot;: 213211,
&quot;psavert&quot;:             13,
&quot;uempmed&quot;:            4.8,
&quot;unemploy&quot;: 4634 
},
{
 &quot;date&quot;: &quot;1974-04-01&quot;,
&quot;pce&quot;:          912.7,
&quot;pop&quot;: 213361,
&quot;psavert&quot;:           12.7,
&quot;uempmed&quot;:              5,
&quot;unemploy&quot;: 4618 
},
{
 &quot;date&quot;: &quot;1974-05-01&quot;,
&quot;pce&quot;:          924.3,
&quot;pop&quot;: 213513,
&quot;psavert&quot;:           12.3,
&quot;uempmed&quot;:            4.6,
&quot;unemploy&quot;: 4705 
},
{
 &quot;date&quot;: &quot;1974-06-01&quot;,
&quot;pce&quot;:          929.9,
&quot;pop&quot;: 213686,
&quot;psavert&quot;:           12.5,
&quot;uempmed&quot;:            5.3,
&quot;unemploy&quot;: 4927 
},
{
 &quot;date&quot;: &quot;1974-07-01&quot;,
&quot;pce&quot;:          939.8,
&quot;pop&quot;: 213854,
&quot;psavert&quot;:           12.7,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 5063 
},
{
 &quot;date&quot;: &quot;1974-08-01&quot;,
&quot;pce&quot;:          956.6,
&quot;pop&quot;: 214042,
&quot;psavert&quot;:           11.6,
&quot;uempmed&quot;:              5,
&quot;unemploy&quot;: 5022 
},
{
 &quot;date&quot;: &quot;1974-09-01&quot;,
&quot;pce&quot;:          956.8,
&quot;pop&quot;: 214246,
&quot;psavert&quot;:           12.3,
&quot;uempmed&quot;:            5.3,
&quot;unemploy&quot;: 5437 
},
{
 &quot;date&quot;: &quot;1974-10-01&quot;,
&quot;pce&quot;:            961,
&quot;pop&quot;: 214451,
&quot;psavert&quot;:             13,
&quot;uempmed&quot;:            5.5,
&quot;unemploy&quot;: 5523 
},
{
 &quot;date&quot;: &quot;1974-11-01&quot;,
&quot;pce&quot;:            958,
&quot;pop&quot;: 214625,
&quot;psavert&quot;:           13.4,
&quot;uempmed&quot;:            5.2,
&quot;unemploy&quot;: 6140 
},
{
 &quot;date&quot;: &quot;1974-12-01&quot;,
&quot;pce&quot;:          963.6,
&quot;pop&quot;: 214782,
&quot;psavert&quot;:           13.6,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 6636 
},
{
 &quot;date&quot;: &quot;1975-01-01&quot;,
&quot;pce&quot;:          977.4,
&quot;pop&quot;: 214931,
&quot;psavert&quot;:           12.8,
&quot;uempmed&quot;:            6.3,
&quot;unemploy&quot;: 7501 
},
{
 &quot;date&quot;: &quot;1975-02-01&quot;,
&quot;pce&quot;:          991.3,
&quot;pop&quot;: 215065,
&quot;psavert&quot;:           12.1,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 7520 
},
{
 &quot;date&quot;: &quot;1975-03-01&quot;,
&quot;pce&quot;:          992.6,
&quot;pop&quot;: 215198,
&quot;psavert&quot;:           12.3,
&quot;uempmed&quot;:            7.2,
&quot;unemploy&quot;: 7978 
},
{
 &quot;date&quot;: &quot;1975-04-01&quot;,
&quot;pce&quot;:          997.2,
&quot;pop&quot;: 215353,
&quot;psavert&quot;:           13.9,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 8210 
},
{
 &quot;date&quot;: &quot;1975-05-01&quot;,
&quot;pce&quot;:         1021.2,
&quot;pop&quot;: 215523,
&quot;psavert&quot;:             17,
&quot;uempmed&quot;:            9.4,
&quot;unemploy&quot;: 8433 
},
{
 &quot;date&quot;: &quot;1975-06-01&quot;,
&quot;pce&quot;:         1029.1,
&quot;pop&quot;: 215768,
&quot;psavert&quot;:           13.9,
&quot;uempmed&quot;:            8.8,
&quot;unemploy&quot;: 8220 
},
{
 &quot;date&quot;: &quot;1975-07-01&quot;,
&quot;pce&quot;:         1042.2,
&quot;pop&quot;: 215973,
&quot;psavert&quot;:           12.3,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 8127 
},
{
 &quot;date&quot;: &quot;1975-08-01&quot;,
&quot;pce&quot;:         1049.4,
&quot;pop&quot;: 216195,
&quot;psavert&quot;:           12.6,
&quot;uempmed&quot;:            9.2,
&quot;unemploy&quot;: 7928 
},
{
 &quot;date&quot;: &quot;1975-09-01&quot;,
&quot;pce&quot;:         1057.2,
&quot;pop&quot;: 216393,
&quot;psavert&quot;:           12.6,
&quot;uempmed&quot;:            9.2,
&quot;unemploy&quot;: 7923 
},
{
 &quot;date&quot;: &quot;1975-10-01&quot;,
&quot;pce&quot;:         1063.2,
&quot;pop&quot;: 216587,
&quot;psavert&quot;:             13,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 7897 
},
{
 &quot;date&quot;: &quot;1975-11-01&quot;,
&quot;pce&quot;:           1078,
&quot;pop&quot;: 216771,
&quot;psavert&quot;:           12.3,
&quot;uempmed&quot;:            9.5,
&quot;unemploy&quot;: 7794 
},
{
 &quot;date&quot;: &quot;1975-12-01&quot;,
&quot;pce&quot;:         1094.4,
&quot;pop&quot;: 216931,
&quot;psavert&quot;:           11.5,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 7744 
},
{
 &quot;date&quot;: &quot;1976-01-01&quot;,
&quot;pce&quot;:         1109.5,
&quot;pop&quot;: 217095,
&quot;psavert&quot;:           11.3,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 7534 
},
{
 &quot;date&quot;: &quot;1976-02-01&quot;,
&quot;pce&quot;:         1110.1,
&quot;pop&quot;: 217249,
&quot;psavert&quot;:           11.9,
&quot;uempmed&quot;:            8.2,
&quot;unemploy&quot;: 7326 
},
{
 &quot;date&quot;: &quot;1976-03-01&quot;,
&quot;pce&quot;:         1117.3,
&quot;pop&quot;: 217381,
&quot;psavert&quot;:           11.8,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 7230 
},
{
 &quot;date&quot;: &quot;1976-04-01&quot;,
&quot;pce&quot;:         1127.8,
&quot;pop&quot;: 217528,
&quot;psavert&quot;:           11.2,
&quot;uempmed&quot;:            8.2,
&quot;unemploy&quot;: 7330 
},
{
 &quot;date&quot;: &quot;1976-05-01&quot;,
&quot;pce&quot;:         1125.1,
&quot;pop&quot;: 217685,
&quot;psavert&quot;:           11.8,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7053 
},
{
 &quot;date&quot;: &quot;1976-06-01&quot;,
&quot;pce&quot;:         1142.9,
&quot;pop&quot;: 217861,
&quot;psavert&quot;:           10.9,
&quot;uempmed&quot;:            7.8,
&quot;unemploy&quot;: 7322 
},
{
 &quot;date&quot;: &quot;1976-07-01&quot;,
&quot;pce&quot;:         1152.1,
&quot;pop&quot;: 218035,
&quot;psavert&quot;:           11.2,
&quot;uempmed&quot;:            7.7,
&quot;unemploy&quot;: 7490 
},
{
 &quot;date&quot;: &quot;1976-08-01&quot;,
&quot;pce&quot;:         1160.5,
&quot;pop&quot;: 218233,
&quot;psavert&quot;:           11.2,
&quot;uempmed&quot;:            7.9,
&quot;unemploy&quot;: 7518 
},
{
 &quot;date&quot;: &quot;1976-09-01&quot;,
&quot;pce&quot;:         1171.4,
&quot;pop&quot;: 218440,
&quot;psavert&quot;:           10.8,
&quot;uempmed&quot;:            7.8,
&quot;unemploy&quot;: 7380 
},
{
 &quot;date&quot;: &quot;1976-10-01&quot;,
&quot;pce&quot;:         1179.5,
&quot;pop&quot;: 218644,
&quot;psavert&quot;:           10.6,
&quot;uempmed&quot;:            7.7,
&quot;unemploy&quot;: 7430 
},
{
 &quot;date&quot;: &quot;1976-11-01&quot;,
&quot;pce&quot;:         1191.7,
&quot;pop&quot;: 218834,
&quot;psavert&quot;:           10.9,
&quot;uempmed&quot;:            8.4,
&quot;unemploy&quot;: 7620 
},
{
 &quot;date&quot;: &quot;1976-12-01&quot;,
&quot;pce&quot;:         1214.1,
&quot;pop&quot;: 219006,
&quot;psavert&quot;:            9.9,
&quot;uempmed&quot;:              8,
&quot;unemploy&quot;: 7545 
},
{
 &quot;date&quot;: &quot;1977-01-01&quot;,
&quot;pce&quot;:         1217.4,
&quot;pop&quot;: 219179,
&quot;psavert&quot;:            9.8,
&quot;uempmed&quot;:            7.5,
&quot;unemploy&quot;: 7280 
},
{
 &quot;date&quot;: &quot;1977-02-01&quot;,
&quot;pce&quot;:         1233.7,
&quot;pop&quot;: 219344,
&quot;psavert&quot;:            8.5,
&quot;uempmed&quot;:            7.2,
&quot;unemploy&quot;: 7443 
},
{
 &quot;date&quot;: &quot;1977-03-01&quot;,
&quot;pce&quot;:         1240.7,
&quot;pop&quot;: 219504,
&quot;psavert&quot;:            9.8,
&quot;uempmed&quot;:            7.2,
&quot;unemploy&quot;: 7307 
},
{
 &quot;date&quot;: &quot;1977-04-01&quot;,
&quot;pce&quot;:         1249.7,
&quot;pop&quot;: 219684,
&quot;psavert&quot;:            9.9,
&quot;uempmed&quot;:            7.3,
&quot;unemploy&quot;: 7059 
},
{
 &quot;date&quot;: &quot;1977-05-01&quot;,
&quot;pce&quot;:         1259.6,
&quot;pop&quot;: 219859,
&quot;psavert&quot;:            9.8,
&quot;uempmed&quot;:            7.9,
&quot;unemploy&quot;: 6911 
},
{
 &quot;date&quot;: &quot;1977-06-01&quot;,
&quot;pce&quot;:         1266.3,
&quot;pop&quot;: 220046,
&quot;psavert&quot;:           10.2,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 7134 
},
{
 &quot;date&quot;: &quot;1977-07-01&quot;,
&quot;pce&quot;:         1283.2,
&quot;pop&quot;: 220239,
&quot;psavert&quot;:           10.1,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 6829 
},
{
 &quot;date&quot;: &quot;1977-08-01&quot;,
&quot;pce&quot;:         1288.5,
&quot;pop&quot;: 220458,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:              7,
&quot;unemploy&quot;: 6925 
},
{
 &quot;date&quot;: &quot;1977-09-01&quot;,
&quot;pce&quot;:         1297.4,
&quot;pop&quot;: 220688,
&quot;psavert&quot;:           10.7,
&quot;uempmed&quot;:            6.7,
&quot;unemploy&quot;: 6751 
},
{
 &quot;date&quot;: &quot;1977-10-01&quot;,
&quot;pce&quot;:         1314.3,
&quot;pop&quot;: 220904,
&quot;psavert&quot;:           10.7,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 6763 
},
{
 &quot;date&quot;: &quot;1977-11-01&quot;,
&quot;pce&quot;:           1330,
&quot;pop&quot;: 221109,
&quot;psavert&quot;:           10.8,
&quot;uempmed&quot;:              7,
&quot;unemploy&quot;: 6815 
},
{
 &quot;date&quot;: &quot;1977-12-01&quot;,
&quot;pce&quot;:         1339.3,
&quot;pop&quot;: 221303,
&quot;psavert&quot;:             11,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 6386 
},
{
 &quot;date&quot;: &quot;1978-01-01&quot;,
&quot;pce&quot;:           1333,
&quot;pop&quot;: 221477,
&quot;psavert&quot;:           11.4,
&quot;uempmed&quot;:            6.5,
&quot;unemploy&quot;: 6489 
},
{
 &quot;date&quot;: &quot;1978-02-01&quot;,
&quot;pce&quot;:         1358.9,
&quot;pop&quot;: 221629,
&quot;psavert&quot;:           10.7,
&quot;uempmed&quot;:            6.7,
&quot;unemploy&quot;: 6318 
},
{
 &quot;date&quot;: &quot;1978-03-01&quot;,
&quot;pce&quot;:         1381.4,
&quot;pop&quot;: 221792,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 6337 
},
{
 &quot;date&quot;: &quot;1978-04-01&quot;,
&quot;pce&quot;:         1400.2,
&quot;pop&quot;: 221991,
&quot;psavert&quot;:           10.3,
&quot;uempmed&quot;:            6.1,
&quot;unemploy&quot;: 6180 
},
{
 &quot;date&quot;: &quot;1978-05-01&quot;,
&quot;pce&quot;:         1415.9,
&quot;pop&quot;: 222176,
&quot;psavert&quot;:            9.8,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 6127 
},
{
 &quot;date&quot;: &quot;1978-06-01&quot;,
&quot;pce&quot;:         1429.8,
&quot;pop&quot;: 222379,
&quot;psavert&quot;:            9.5,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 6028 
},
{
 &quot;date&quot;: &quot;1978-07-01&quot;,
&quot;pce&quot;:         1430.8,
&quot;pop&quot;: 222585,
&quot;psavert&quot;:           10.3,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 6309 
},
{
 &quot;date&quot;: &quot;1978-08-01&quot;,
&quot;pce&quot;:           1451,
&quot;pop&quot;: 222805,
&quot;psavert&quot;:            9.9,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 6080 
},
{
 &quot;date&quot;: &quot;1978-09-01&quot;,
&quot;pce&quot;:         1456.9,
&quot;pop&quot;: 223053,
&quot;psavert&quot;:             10,
&quot;uempmed&quot;:            5.6,
&quot;unemploy&quot;: 6125 
},
{
 &quot;date&quot;: &quot;1978-10-01&quot;,
&quot;pce&quot;:           1471,
&quot;pop&quot;: 223271,
&quot;psavert&quot;:           10.2,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 5947 
},
{
 &quot;date&quot;: &quot;1978-11-01&quot;,
&quot;pce&quot;:         1484.7,
&quot;pop&quot;: 223477,
&quot;psavert&quot;:             10,
&quot;uempmed&quot;:            5.5,
&quot;unemploy&quot;: 6077 
},
{
 &quot;date&quot;: &quot;1978-12-01&quot;,
&quot;pce&quot;:         1500.5,
&quot;pop&quot;: 223670,
&quot;psavert&quot;:             10,
&quot;uempmed&quot;:            5.6,
&quot;unemploy&quot;: 6228 
},
{
 &quot;date&quot;: &quot;1979-01-01&quot;,
&quot;pce&quot;:         1506.3,
&quot;pop&quot;: 223865,
&quot;psavert&quot;:           10.6,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 6109 
},
{
 &quot;date&quot;: &quot;1979-02-01&quot;,
&quot;pce&quot;:         1521.6,
&quot;pop&quot;: 224053,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 6173 
},
{
 &quot;date&quot;: &quot;1979-03-01&quot;,
&quot;pce&quot;:           1535,
&quot;pop&quot;: 224235,
&quot;psavert&quot;:           10.7,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 6109 
},
{
 &quot;date&quot;: &quot;1979-04-01&quot;,
&quot;pce&quot;:         1542.3,
&quot;pop&quot;: 224438,
&quot;psavert&quot;:           10.4,
&quot;uempmed&quot;:            5.4,
&quot;unemploy&quot;: 6069 
},
{
 &quot;date&quot;: &quot;1979-05-01&quot;,
&quot;pce&quot;:         1562.7,
&quot;pop&quot;: 224632,
&quot;psavert&quot;:            9.8,
&quot;uempmed&quot;:            5.6,
&quot;unemploy&quot;: 5840 
},
{
 &quot;date&quot;: &quot;1979-06-01&quot;,
&quot;pce&quot;:         1579.6,
&quot;pop&quot;: 224843,
&quot;psavert&quot;:            9.3,
&quot;uempmed&quot;:            5.6,
&quot;unemploy&quot;: 5959 
},
{
 &quot;date&quot;: &quot;1979-07-01&quot;,
&quot;pce&quot;:         1590.1,
&quot;pop&quot;: 225055,
&quot;psavert&quot;:             10,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 5996 
},
{
 &quot;date&quot;: &quot;1979-08-01&quot;,
&quot;pce&quot;:         1619.7,
&quot;pop&quot;: 225295,
&quot;psavert&quot;:            9.2,
&quot;uempmed&quot;:            4.8,
&quot;unemploy&quot;: 6320 
},
{
 &quot;date&quot;: &quot;1979-09-01&quot;,
&quot;pce&quot;:         1638.1,
&quot;pop&quot;: 225547,
&quot;psavert&quot;:            8.9,
&quot;uempmed&quot;:            5.5,
&quot;unemploy&quot;: 6190 
},
{
 &quot;date&quot;: &quot;1979-10-01&quot;,
&quot;pce&quot;:           1646,
&quot;pop&quot;: 225801,
&quot;psavert&quot;:            9.3,
&quot;uempmed&quot;:            5.5,
&quot;unemploy&quot;: 6296 
},
{
 &quot;date&quot;: &quot;1979-11-01&quot;,
&quot;pce&quot;:         1661.7,
&quot;pop&quot;: 226027,
&quot;psavert&quot;:            9.4,
&quot;uempmed&quot;:            5.3,
&quot;unemploy&quot;: 6238 
},
{
 &quot;date&quot;: &quot;1979-12-01&quot;,
&quot;pce&quot;:         1670.7,
&quot;pop&quot;: 226243,
&quot;psavert&quot;:            9.8,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 6325 
},
{
 &quot;date&quot;: &quot;1980-01-01&quot;,
&quot;pce&quot;:         1701.6,
&quot;pop&quot;: 226451,
&quot;psavert&quot;:            9.6,
&quot;uempmed&quot;:            5.3,
&quot;unemploy&quot;: 6683 
},
{
 &quot;date&quot;: &quot;1980-02-01&quot;,
&quot;pce&quot;:         1705.6,
&quot;pop&quot;: 226656,
&quot;psavert&quot;:            9.8,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 6702 
},
{
 &quot;date&quot;: &quot;1980-03-01&quot;,
&quot;pce&quot;:         1712.4,
&quot;pop&quot;: 226849,
&quot;psavert&quot;:            9.8,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 6729 
},
{
 &quot;date&quot;: &quot;1980-04-01&quot;,
&quot;pce&quot;:         1699.5,
&quot;pop&quot;: 227061,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 7358 
},
{
 &quot;date&quot;: &quot;1980-05-01&quot;,
&quot;pce&quot;:         1704.3,
&quot;pop&quot;: 227251,
&quot;psavert&quot;:           10.6,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 7984 
},
{
 &quot;date&quot;: &quot;1980-06-01&quot;,
&quot;pce&quot;:           1723,
&quot;pop&quot;: 227522,
&quot;psavert&quot;:           10.4,
&quot;uempmed&quot;:            6.4,
&quot;unemploy&quot;: 8098 
},
{
 &quot;date&quot;: &quot;1980-07-01&quot;,
&quot;pce&quot;:         1751.2,
&quot;pop&quot;: 227726,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:              7,
&quot;unemploy&quot;: 8363 
},
{
 &quot;date&quot;: &quot;1980-08-01&quot;,
&quot;pce&quot;:         1767.7,
&quot;pop&quot;: 227953,
&quot;psavert&quot;:           10.6,
&quot;uempmed&quot;:            7.5,
&quot;unemploy&quot;: 8281 
},
{
 &quot;date&quot;: &quot;1980-09-01&quot;,
&quot;pce&quot;:         1784.1,
&quot;pop&quot;: 228186,
&quot;psavert&quot;:           11.1,
&quot;uempmed&quot;:            7.7,
&quot;unemploy&quot;: 8021 
},
{
 &quot;date&quot;: &quot;1980-10-01&quot;,
&quot;pce&quot;:         1820.4,
&quot;pop&quot;: 228417,
&quot;psavert&quot;:             11,
&quot;uempmed&quot;:            7.5,
&quot;unemploy&quot;: 8088 
},
{
 &quot;date&quot;: &quot;1980-11-01&quot;,
&quot;pce&quot;:         1830.2,
&quot;pop&quot;: 228612,
&quot;psavert&quot;:           11.5,
&quot;uempmed&quot;:            7.7,
&quot;unemploy&quot;: 8023 
},
{
 &quot;date&quot;: &quot;1980-12-01&quot;,
&quot;pce&quot;:         1855.5,
&quot;pop&quot;: 228779,
&quot;psavert&quot;:           11.2,
&quot;uempmed&quot;:            7.5,
&quot;unemploy&quot;: 7718 
},
{
 &quot;date&quot;: &quot;1981-01-01&quot;,
&quot;pce&quot;:         1874.7,
&quot;pop&quot;: 228937,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:            7.4,
&quot;unemploy&quot;: 8071 
},
{
 &quot;date&quot;: &quot;1981-02-01&quot;,
&quot;pce&quot;:         1889.4,
&quot;pop&quot;: 229071,
&quot;psavert&quot;:           10.4,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 8051 
},
{
 &quot;date&quot;: &quot;1981-03-01&quot;,
&quot;pce&quot;:         1908.1,
&quot;pop&quot;: 229224,
&quot;psavert&quot;:           10.3,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 7982 
},
{
 &quot;date&quot;: &quot;1981-04-01&quot;,
&quot;pce&quot;:         1909.1,
&quot;pop&quot;: 229403,
&quot;psavert&quot;:           10.3,
&quot;uempmed&quot;:            7.4,
&quot;unemploy&quot;: 7869 
},
{
 &quot;date&quot;: &quot;1981-05-01&quot;,
&quot;pce&quot;:         1918.2,
&quot;pop&quot;: 229575,
&quot;psavert&quot;:           10.4,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 8174 
},
{
 &quot;date&quot;: &quot;1981-06-01&quot;,
&quot;pce&quot;:         1938.5,
&quot;pop&quot;: 229761,
&quot;psavert&quot;:           10.2,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 8098 
},
{
 &quot;date&quot;: &quot;1981-07-01&quot;,
&quot;pce&quot;:         1945.7,
&quot;pop&quot;: 229966,
&quot;psavert&quot;:           11.7,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 7863 
},
{
 &quot;date&quot;: &quot;1981-08-01&quot;,
&quot;pce&quot;:         1969.8,
&quot;pop&quot;: 230187,
&quot;psavert&quot;:           11.4,
&quot;uempmed&quot;:            7.2,
&quot;unemploy&quot;: 8036 
},
{
 &quot;date&quot;: &quot;1981-09-01&quot;,
&quot;pce&quot;:         1968.2,
&quot;pop&quot;: 230412,
&quot;psavert&quot;:           11.9,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 8230 
},
{
 &quot;date&quot;: &quot;1981-10-01&quot;,
&quot;pce&quot;:         1966.2,
&quot;pop&quot;: 230641,
&quot;psavert&quot;:           12.5,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 8646 
},
{
 &quot;date&quot;: &quot;1981-11-01&quot;,
&quot;pce&quot;:         1972.4,
&quot;pop&quot;: 230822,
&quot;psavert&quot;:           12.7,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 9029 
},
{
 &quot;date&quot;: &quot;1981-12-01&quot;,
&quot;pce&quot;:         1989.9,
&quot;pop&quot;: 230989,
&quot;psavert&quot;:             12,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 9267 
},
{
 &quot;date&quot;: &quot;1982-01-01&quot;,
&quot;pce&quot;:         1997.4,
&quot;pop&quot;: 231157,
&quot;psavert&quot;:           12.2,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 9397 
},
{
 &quot;date&quot;: &quot;1982-02-01&quot;,
&quot;pce&quot;:         2021.4,
&quot;pop&quot;: 231313,
&quot;psavert&quot;:           11.6,
&quot;uempmed&quot;:            7.5,
&quot;unemploy&quot;: 9705 
},
{
 &quot;date&quot;: &quot;1982-03-01&quot;,
&quot;pce&quot;:         2024.4,
&quot;pop&quot;: 231470,
&quot;psavert&quot;:           11.7,
&quot;uempmed&quot;:            7.7,
&quot;unemploy&quot;: 9895 
},
{
 &quot;date&quot;: &quot;1982-04-01&quot;,
&quot;pce&quot;:         2027.2,
&quot;pop&quot;: 231645,
&quot;psavert&quot;:           12.4,
&quot;uempmed&quot;:            8.1,
&quot;unemploy&quot;: 10244 
},
{
 &quot;date&quot;: &quot;1982-05-01&quot;,
&quot;pce&quot;:         2045.9,
&quot;pop&quot;: 231809,
&quot;psavert&quot;:           11.7,
&quot;uempmed&quot;:            8.5,
&quot;unemploy&quot;: 10335 
},
{
 &quot;date&quot;: &quot;1982-06-01&quot;,
&quot;pce&quot;:         2050.2,
&quot;pop&quot;: 231992,
&quot;psavert&quot;:           11.6,
&quot;uempmed&quot;:            9.5,
&quot;unemploy&quot;: 10538 
},
{
 &quot;date&quot;: &quot;1982-07-01&quot;,
&quot;pce&quot;:         2075.1,
&quot;pop&quot;: 232188,
&quot;psavert&quot;:             12,
&quot;uempmed&quot;:            8.5,
&quot;unemploy&quot;: 10849 
},
{
 &quot;date&quot;: &quot;1982-08-01&quot;,
&quot;pce&quot;:         2083.7,
&quot;pop&quot;: 232392,
&quot;psavert&quot;:           11.9,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 10881 
},
{
 &quot;date&quot;: &quot;1982-09-01&quot;,
&quot;pce&quot;:         2108.9,
&quot;pop&quot;: 232599,
&quot;psavert&quot;:           11.1,
&quot;uempmed&quot;:            9.5,
&quot;unemploy&quot;: 11217 
},
{
 &quot;date&quot;: &quot;1982-10-01&quot;,
&quot;pce&quot;:         2130.7,
&quot;pop&quot;: 232816,
&quot;psavert&quot;:           10.7,
&quot;uempmed&quot;:            9.7,
&quot;unemploy&quot;: 11529 
},
{
 &quot;date&quot;: &quot;1982-11-01&quot;,
&quot;pce&quot;:         2154.7,
&quot;pop&quot;: 232993,
&quot;psavert&quot;:           10.3,
&quot;uempmed&quot;:             10,
&quot;unemploy&quot;: 11938 
},
{
 &quot;date&quot;: &quot;1982-12-01&quot;,
&quot;pce&quot;:         2167.4,
&quot;pop&quot;: 233160,
&quot;psavert&quot;:           10.3,
&quot;uempmed&quot;:           10.2,
&quot;unemploy&quot;: 12051 
},
{
 &quot;date&quot;: &quot;1983-01-01&quot;,
&quot;pce&quot;:         2180.1,
&quot;pop&quot;: 233322,
&quot;psavert&quot;:           10.4,
&quot;uempmed&quot;:           11.1,
&quot;unemploy&quot;: 11534 
},
{
 &quot;date&quot;: &quot;1983-02-01&quot;,
&quot;pce&quot;:         2183.1,
&quot;pop&quot;: 233473,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:            9.8,
&quot;unemploy&quot;: 11545 
},
{
 &quot;date&quot;: &quot;1983-03-01&quot;,
&quot;pce&quot;:         2208.6,
&quot;pop&quot;: 233613,
&quot;psavert&quot;:             10,
&quot;uempmed&quot;:           10.4,
&quot;unemploy&quot;: 11408 
},
{
 &quot;date&quot;: &quot;1983-04-01&quot;,
&quot;pce&quot;:         2231.8,
&quot;pop&quot;: 233781,
&quot;psavert&quot;:            9.6,
&quot;uempmed&quot;:           10.9,
&quot;unemploy&quot;: 11268 
},
{
 &quot;date&quot;: &quot;1983-05-01&quot;,
&quot;pce&quot;:           2251,
&quot;pop&quot;: 233922,
&quot;psavert&quot;:            9.4,
&quot;uempmed&quot;:           12.3,
&quot;unemploy&quot;: 11154 
},
{
 &quot;date&quot;: &quot;1983-06-01&quot;,
&quot;pce&quot;:         2280.8,
&quot;pop&quot;: 234118,
&quot;psavert&quot;:            8.5,
&quot;uempmed&quot;:           11.3,
&quot;unemploy&quot;: 11246 
},
{
 &quot;date&quot;: &quot;1983-07-01&quot;,
&quot;pce&quot;:           2309,
&quot;pop&quot;: 234307,
&quot;psavert&quot;:              9,
&quot;uempmed&quot;:           10.1,
&quot;unemploy&quot;: 10548 
},
{
 &quot;date&quot;: &quot;1983-08-01&quot;,
&quot;pce&quot;:         2324.8,
&quot;pop&quot;: 234501,
&quot;psavert&quot;:            8.7,
&quot;uempmed&quot;:            9.3,
&quot;unemploy&quot;: 10623 
},
{
 &quot;date&quot;: &quot;1983-09-01&quot;,
&quot;pce&quot;:         2339.1,
&quot;pop&quot;: 234701,
&quot;psavert&quot;:              9,
&quot;uempmed&quot;:            9.3,
&quot;unemploy&quot;: 10282 
},
{
 &quot;date&quot;: &quot;1983-10-01&quot;,
&quot;pce&quot;:         2361.8,
&quot;pop&quot;: 234907,
&quot;psavert&quot;:            9.1,
&quot;uempmed&quot;:            9.4,
&quot;unemploy&quot;: 9887 
},
{
 &quot;date&quot;: &quot;1983-11-01&quot;,
&quot;pce&quot;:         2370.4,
&quot;pop&quot;: 235078,
&quot;psavert&quot;:            9.7,
&quot;uempmed&quot;:            9.3,
&quot;unemploy&quot;: 9499 
},
{
 &quot;date&quot;: &quot;1983-12-01&quot;,
&quot;pce&quot;:         2397.9,
&quot;pop&quot;: 235235,
&quot;psavert&quot;:            9.5,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 9331 
},
{
 &quot;date&quot;: &quot;1984-01-01&quot;,
&quot;pce&quot;:         2423.8,
&quot;pop&quot;: 235385,
&quot;psavert&quot;:            9.4,
&quot;uempmed&quot;:            9.1,
&quot;unemploy&quot;: 9008 
},
{
 &quot;date&quot;: &quot;1984-02-01&quot;,
&quot;pce&quot;:         2408.1,
&quot;pop&quot;: 235527,
&quot;psavert&quot;:           11.1,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 8791 
},
{
 &quot;date&quot;: &quot;1984-03-01&quot;,
&quot;pce&quot;:         2436.4,
&quot;pop&quot;: 235675,
&quot;psavert&quot;:           10.9,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 8746 
},
{
 &quot;date&quot;: &quot;1984-04-01&quot;,
&quot;pce&quot;:         2462.6,
&quot;pop&quot;: 235839,
&quot;psavert&quot;:           10.9,
&quot;uempmed&quot;:            8.2,
&quot;unemploy&quot;: 8762 
},
{
 &quot;date&quot;: &quot;1984-05-01&quot;,
&quot;pce&quot;:         2479.8,
&quot;pop&quot;: 235993,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:            9.1,
&quot;unemploy&quot;: 8456 
},
{
 &quot;date&quot;: &quot;1984-06-01&quot;,
&quot;pce&quot;:         2501.2,
&quot;pop&quot;: 236160,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:            7.5,
&quot;unemploy&quot;: 8226 
},
{
 &quot;date&quot;: &quot;1984-07-01&quot;,
&quot;pce&quot;:         2500.5,
&quot;pop&quot;: 236348,
&quot;psavert&quot;:             11,
&quot;uempmed&quot;:            7.5,
&quot;unemploy&quot;: 8537 
},
{
 &quot;date&quot;: &quot;1984-08-01&quot;,
&quot;pce&quot;:         2518.4,
&quot;pop&quot;: 236549,
&quot;psavert&quot;:           11.2,
&quot;uempmed&quot;:            7.3,
&quot;unemploy&quot;: 8519 
},
{
 &quot;date&quot;: &quot;1984-09-01&quot;,
&quot;pce&quot;:         2540.3,
&quot;pop&quot;: 236760,
&quot;psavert&quot;:           11.2,
&quot;uempmed&quot;:            7.6,
&quot;unemploy&quot;: 8367 
},
{
 &quot;date&quot;: &quot;1984-10-01&quot;,
&quot;pce&quot;:         2538.2,
&quot;pop&quot;: 236976,
&quot;psavert&quot;:           11.2,
&quot;uempmed&quot;:            7.2,
&quot;unemploy&quot;: 8381 
},
{
 &quot;date&quot;: &quot;1984-11-01&quot;,
&quot;pce&quot;:         2578.6,
&quot;pop&quot;: 237159,
&quot;psavert&quot;:           10.3,
&quot;uempmed&quot;:            7.2,
&quot;unemploy&quot;: 8198 
},
{
 &quot;date&quot;: &quot;1984-12-01&quot;,
&quot;pce&quot;:           2590,
&quot;pop&quot;: 237316,
&quot;psavert&quot;:           10.6,
&quot;uempmed&quot;:            7.3,
&quot;unemploy&quot;: 8358 
},
{
 &quot;date&quot;: &quot;1985-01-01&quot;,
&quot;pce&quot;:         2626.3,
&quot;pop&quot;: 237468,
&quot;psavert&quot;:            9.7,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 8423 
},
{
 &quot;date&quot;: &quot;1985-02-01&quot;,
&quot;pce&quot;:         2648.6,
&quot;pop&quot;: 237602,
&quot;psavert&quot;:            8.5,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 8321 
},
{
 &quot;date&quot;: &quot;1985-03-01&quot;,
&quot;pce&quot;:         2656.8,
&quot;pop&quot;: 237732,
&quot;psavert&quot;:            8.1,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 8339 
},
{
 &quot;date&quot;: &quot;1985-04-01&quot;,
&quot;pce&quot;:         2668.4,
&quot;pop&quot;: 237900,
&quot;psavert&quot;:            9.4,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 8395 
},
{
 &quot;date&quot;: &quot;1985-05-01&quot;,
&quot;pce&quot;:         2705.9,
&quot;pop&quot;: 238074,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 8302 
},
{
 &quot;date&quot;: &quot;1985-06-01&quot;,
&quot;pce&quot;:         2699.3,
&quot;pop&quot;: 238270,
&quot;psavert&quot;:              9,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 8460 
},
{
 &quot;date&quot;: &quot;1985-07-01&quot;,
&quot;pce&quot;:         2725.9,
&quot;pop&quot;: 238466,
&quot;psavert&quot;:            8.5,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 8513 
},
{
 &quot;date&quot;: &quot;1985-08-01&quot;,
&quot;pce&quot;:         2762.7,
&quot;pop&quot;: 238679,
&quot;psavert&quot;:            7.5,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 8196 
},
{
 &quot;date&quot;: &quot;1985-09-01&quot;,
&quot;pce&quot;:         2805.6,
&quot;pop&quot;: 238898,
&quot;psavert&quot;:            6.7,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 8248 
},
{
 &quot;date&quot;: &quot;1985-10-01&quot;,
&quot;pce&quot;:         2767.1,
&quot;pop&quot;: 239113,
&quot;psavert&quot;:            8.5,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 8298 
},
{
 &quot;date&quot;: &quot;1985-11-01&quot;,
&quot;pce&quot;:         2782.7,
&quot;pop&quot;: 239307,
&quot;psavert&quot;:            8.4,
&quot;uempmed&quot;:              7,
&quot;unemploy&quot;: 8128 
},
{
 &quot;date&quot;: &quot;1985-12-01&quot;,
&quot;pce&quot;:         2822.8,
&quot;pop&quot;: 239477,
&quot;psavert&quot;:              8,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 8138 
},
{
 &quot;date&quot;: &quot;1986-01-01&quot;,
&quot;pce&quot;:         2838.3,
&quot;pop&quot;: 239638,
&quot;psavert&quot;:              8,
&quot;uempmed&quot;:            6.7,
&quot;unemploy&quot;: 7795 
},
{
 &quot;date&quot;: &quot;1986-02-01&quot;,
&quot;pce&quot;:         2831.2,
&quot;pop&quot;: 239788,
&quot;psavert&quot;:            8.7,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 8402 
},
{
 &quot;date&quot;: &quot;1986-03-01&quot;,
&quot;pce&quot;:         2834.7,
&quot;pop&quot;: 239928,
&quot;psavert&quot;:            9.3,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 8383 
},
{
 &quot;date&quot;: &quot;1986-04-01&quot;,
&quot;pce&quot;:         2846.5,
&quot;pop&quot;: 240094,
&quot;psavert&quot;:            9.1,
&quot;uempmed&quot;:            6.7,
&quot;unemploy&quot;: 8364 
},
{
 &quot;date&quot;: &quot;1986-05-01&quot;,
&quot;pce&quot;:           2869,
&quot;pop&quot;: 240271,
&quot;psavert&quot;:            8.6,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 8439 
},
{
 &quot;date&quot;: &quot;1986-06-01&quot;,
&quot;pce&quot;:         2873.5,
&quot;pop&quot;: 240459,
&quot;psavert&quot;:            8.8,
&quot;uempmed&quot;:              7,
&quot;unemploy&quot;: 8508 
},
{
 &quot;date&quot;: &quot;1986-07-01&quot;,
&quot;pce&quot;:         2893.4,
&quot;pop&quot;: 240651,
&quot;psavert&quot;:            8.7,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 8319 
},
{
 &quot;date&quot;: &quot;1986-08-01&quot;,
&quot;pce&quot;:         2911.1,
&quot;pop&quot;: 240854,
&quot;psavert&quot;:            8.4,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 8135 
},
{
 &quot;date&quot;: &quot;1986-09-01&quot;,
&quot;pce&quot;:         2984.6,
&quot;pop&quot;: 241068,
&quot;psavert&quot;:            6.6,
&quot;uempmed&quot;:            7.4,
&quot;unemploy&quot;: 8310 
},
{
 &quot;date&quot;: &quot;1986-10-01&quot;,
&quot;pce&quot;:         2945.9,
&quot;pop&quot;: 241274,
&quot;psavert&quot;:            7.8,
&quot;uempmed&quot;:              7,
&quot;unemploy&quot;: 8243 
},
{
 &quot;date&quot;: &quot;1986-11-01&quot;,
&quot;pce&quot;:         2941.7,
&quot;pop&quot;: 241467,
&quot;psavert&quot;:            8.2,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 8159 
},
{
 &quot;date&quot;: &quot;1986-12-01&quot;,
&quot;pce&quot;:         3010.8,
&quot;pop&quot;: 241620,
&quot;psavert&quot;:            6.4,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 7883 
},
{
 &quot;date&quot;: &quot;1987-01-01&quot;,
&quot;pce&quot;:         2949.9,
&quot;pop&quot;: 241784,
&quot;psavert&quot;:            9.1,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 7892 
},
{
 &quot;date&quot;: &quot;1987-02-01&quot;,
&quot;pce&quot;:         3016.5,
&quot;pop&quot;: 241930,
&quot;psavert&quot;:            7.9,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 7865 
},
{
 &quot;date&quot;: &quot;1987-03-01&quot;,
&quot;pce&quot;:         3028.4,
&quot;pop&quot;: 242079,
&quot;psavert&quot;:            7.9,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 7862 
},
{
 &quot;date&quot;: &quot;1987-04-01&quot;,
&quot;pce&quot;:         3054.1,
&quot;pop&quot;: 242252,
&quot;psavert&quot;:            3.8,
&quot;uempmed&quot;:            7.1,
&quot;unemploy&quot;: 7542 
},
{
 &quot;date&quot;: &quot;1987-05-01&quot;,
&quot;pce&quot;:         3063.9,
&quot;pop&quot;: 242423,
&quot;psavert&quot;:            7.5,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 7574 
},
{
 &quot;date&quot;: &quot;1987-06-01&quot;,
&quot;pce&quot;:         3088.4,
&quot;pop&quot;: 242608,
&quot;psavert&quot;:              7,
&quot;uempmed&quot;:            6.5,
&quot;unemploy&quot;: 7398 
},
{
 &quot;date&quot;: &quot;1987-07-01&quot;,
&quot;pce&quot;:         3110.7,
&quot;pop&quot;: 242804,
&quot;psavert&quot;:            6.8,
&quot;uempmed&quot;:            6.5,
&quot;unemploy&quot;: 7268 
},
{
 &quot;date&quot;: &quot;1987-08-01&quot;,
&quot;pce&quot;:           3147,
&quot;pop&quot;: 243012,
&quot;psavert&quot;:            6.5,
&quot;uempmed&quot;:            6.4,
&quot;unemploy&quot;: 7261 
},
{
 &quot;date&quot;: &quot;1987-09-01&quot;,
&quot;pce&quot;:         3142.9,
&quot;pop&quot;: 243223,
&quot;psavert&quot;:              7,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 7102 
},
{
 &quot;date&quot;: &quot;1987-10-01&quot;,
&quot;pce&quot;:         3151.1,
&quot;pop&quot;: 243446,
&quot;psavert&quot;:            7.6,
&quot;uempmed&quot;:            6.3,
&quot;unemploy&quot;: 7227 
},
{
 &quot;date&quot;: &quot;1987-11-01&quot;,
&quot;pce&quot;:         3160.9,
&quot;pop&quot;: 243639,
&quot;psavert&quot;:            7.9,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 7035 
},
{
 &quot;date&quot;: &quot;1987-12-01&quot;,
&quot;pce&quot;:         3190.9,
&quot;pop&quot;: 243809,
&quot;psavert&quot;:              8,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 6936 
},
{
 &quot;date&quot;: &quot;1988-01-01&quot;,
&quot;pce&quot;:         3230.7,
&quot;pop&quot;: 243981,
&quot;psavert&quot;:            7.5,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 6953 
},
{
 &quot;date&quot;: &quot;1988-02-01&quot;,
&quot;pce&quot;:         3238.5,
&quot;pop&quot;: 244131,
&quot;psavert&quot;:            7.9,
&quot;uempmed&quot;:            6.3,
&quot;unemploy&quot;: 6929 
},
{
 &quot;date&quot;: &quot;1988-03-01&quot;,
&quot;pce&quot;:         3277.8,
&quot;pop&quot;: 244279,
&quot;psavert&quot;:            7.5,
&quot;uempmed&quot;:            6.4,
&quot;unemploy&quot;: 6876 
},
{
 &quot;date&quot;: &quot;1988-04-01&quot;,
&quot;pce&quot;:         3280.4,
&quot;pop&quot;: 244445,
&quot;psavert&quot;:            8.1,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 6601 
},
{
 &quot;date&quot;: &quot;1988-05-01&quot;,
&quot;pce&quot;:           3311,
&quot;pop&quot;: 244610,
&quot;psavert&quot;:            7.7,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 6779 
},
{
 &quot;date&quot;: &quot;1988-06-01&quot;,
&quot;pce&quot;:         3335.6,
&quot;pop&quot;: 244806,
&quot;psavert&quot;:            7.8,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 6546 
},
{
 &quot;date&quot;: &quot;1988-07-01&quot;,
&quot;pce&quot;:         3359.3,
&quot;pop&quot;: 245021,
&quot;psavert&quot;:            7.9,
&quot;uempmed&quot;:            6.1,
&quot;unemploy&quot;: 6605 
},
{
 &quot;date&quot;: &quot;1988-08-01&quot;,
&quot;pce&quot;:         3384.3,
&quot;pop&quot;: 245240,
&quot;psavert&quot;:            7.8,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 6843 
},
{
 &quot;date&quot;: &quot;1988-09-01&quot;,
&quot;pce&quot;:         3391.4,
&quot;pop&quot;: 245464,
&quot;psavert&quot;:            8.2,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 6604 
},
{
 &quot;date&quot;: &quot;1988-10-01&quot;,
&quot;pce&quot;:         3430.4,
&quot;pop&quot;: 245693,
&quot;psavert&quot;:              8,
&quot;uempmed&quot;:            5.6,
&quot;unemploy&quot;: 6568 
},
{
 &quot;date&quot;: &quot;1988-11-01&quot;,
&quot;pce&quot;:           3447,
&quot;pop&quot;: 245884,
&quot;psavert&quot;:            7.7,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 6537 
},
{
 &quot;date&quot;: &quot;1988-12-01&quot;,
&quot;pce&quot;:         3476.3,
&quot;pop&quot;: 246056,
&quot;psavert&quot;:            7.7,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 6518 
},
{
 &quot;date&quot;: &quot;1989-01-01&quot;,
&quot;pce&quot;:         3499.9,
&quot;pop&quot;: 246224,
&quot;psavert&quot;:              8,
&quot;uempmed&quot;:            5.6,
&quot;unemploy&quot;: 6682 
},
{
 &quot;date&quot;: &quot;1989-02-01&quot;,
&quot;pce&quot;:         3503.9,
&quot;pop&quot;: 246378,
&quot;psavert&quot;:            8.4,
&quot;uempmed&quot;:            5.4,
&quot;unemploy&quot;: 6359 
},
{
 &quot;date&quot;: &quot;1989-03-01&quot;,
&quot;pce&quot;:         3514.5,
&quot;pop&quot;: 246530,
&quot;psavert&quot;:            8.9,
&quot;uempmed&quot;:            5.4,
&quot;unemploy&quot;: 6205 
},
{
 &quot;date&quot;: &quot;1989-04-01&quot;,
&quot;pce&quot;:         3558.6,
&quot;pop&quot;: 246721,
&quot;psavert&quot;:            7.9,
&quot;uempmed&quot;:            5.4,
&quot;unemploy&quot;: 6468 
},
{
 &quot;date&quot;: &quot;1989-05-01&quot;,
&quot;pce&quot;:         3567.5,
&quot;pop&quot;: 246906,
&quot;psavert&quot;:            7.6,
&quot;uempmed&quot;:            5.3,
&quot;unemploy&quot;: 6375 
},
{
 &quot;date&quot;: &quot;1989-06-01&quot;,
&quot;pce&quot;:         3582.4,
&quot;pop&quot;: 247114,
&quot;psavert&quot;:            7.6,
&quot;uempmed&quot;:            5.4,
&quot;unemploy&quot;: 6577 
},
{
 &quot;date&quot;: &quot;1989-07-01&quot;,
&quot;pce&quot;:         3601.7,
&quot;pop&quot;: 247342,
&quot;psavert&quot;:            7.7,
&quot;uempmed&quot;:            5.6,
&quot;unemploy&quot;: 6495 
},
{
 &quot;date&quot;: &quot;1989-08-01&quot;,
&quot;pce&quot;:         3636.8,
&quot;pop&quot;: 247573,
&quot;psavert&quot;:            7.1,
&quot;uempmed&quot;:              5,
&quot;unemploy&quot;: 6511 
},
{
 &quot;date&quot;: &quot;1989-09-01&quot;,
&quot;pce&quot;:         3638.1,
&quot;pop&quot;: 247816,
&quot;psavert&quot;:            7.5,
&quot;uempmed&quot;:            4.9,
&quot;unemploy&quot;: 6590 
},
{
 &quot;date&quot;: &quot;1989-10-01&quot;,
&quot;pce&quot;:           3650,
&quot;pop&quot;: 248067,
&quot;psavert&quot;:            7.9,
&quot;uempmed&quot;:            4.9,
&quot;unemploy&quot;: 6630 
},
{
 &quot;date&quot;: &quot;1989-11-01&quot;,
&quot;pce&quot;:         3659.7,
&quot;pop&quot;: 248281,
&quot;psavert&quot;:              8,
&quot;uempmed&quot;:            4.8,
&quot;unemploy&quot;: 6725 
},
{
 &quot;date&quot;: &quot;1989-12-01&quot;,
&quot;pce&quot;:         3700.7,
&quot;pop&quot;: 248479,
&quot;psavert&quot;:            7.2,
&quot;uempmed&quot;:            4.9,
&quot;unemploy&quot;: 6667 
},
{
 &quot;date&quot;: &quot;1990-01-01&quot;,
&quot;pce&quot;:         3747.2,
&quot;pop&quot;: 248659,
&quot;psavert&quot;:            7.4,
&quot;uempmed&quot;:            5.1,
&quot;unemploy&quot;: 6752 
},
{
 &quot;date&quot;: &quot;1990-02-01&quot;,
&quot;pce&quot;:         3744.8,
&quot;pop&quot;: 248827,
&quot;psavert&quot;:            8.1,
&quot;uempmed&quot;:            5.3,
&quot;unemploy&quot;: 6651 
},
{
 &quot;date&quot;: &quot;1990-03-01&quot;,
&quot;pce&quot;:         3771.5,
&quot;pop&quot;: 249012,
&quot;psavert&quot;:            7.8,
&quot;uempmed&quot;:            5.1,
&quot;unemploy&quot;: 6598 
},
{
 &quot;date&quot;: &quot;1990-04-01&quot;,
&quot;pce&quot;:         3786.7,
&quot;pop&quot;: 249306,
&quot;psavert&quot;:            8.2,
&quot;uempmed&quot;:            4.8,
&quot;unemploy&quot;: 6797 
},
{
 &quot;date&quot;: &quot;1990-05-01&quot;,
&quot;pce&quot;:         3792.5,
&quot;pop&quot;: 249565,
&quot;psavert&quot;:              8,
&quot;uempmed&quot;:            5.2,
&quot;unemploy&quot;: 6742 
},
{
 &quot;date&quot;: &quot;1990-06-01&quot;,
&quot;pce&quot;:         3821.3,
&quot;pop&quot;: 249849,
&quot;psavert&quot;:            7.9,
&quot;uempmed&quot;:            5.2,
&quot;unemploy&quot;: 6590 
},
{
 &quot;date&quot;: &quot;1990-07-01&quot;,
&quot;pce&quot;:         3838.5,
&quot;pop&quot;: 250132,
&quot;psavert&quot;:              8,
&quot;uempmed&quot;:            5.4,
&quot;unemploy&quot;: 6922 
},
{
 &quot;date&quot;: &quot;1990-08-01&quot;,
&quot;pce&quot;:           3865,
&quot;pop&quot;: 250439,
&quot;psavert&quot;:            7.5,
&quot;uempmed&quot;:            5.4,
&quot;unemploy&quot;: 7188 
},
{
 &quot;date&quot;: &quot;1990-09-01&quot;,
&quot;pce&quot;:         3886.7,
&quot;pop&quot;: 250751,
&quot;psavert&quot;:            7.5,
&quot;uempmed&quot;:            5.6,
&quot;unemploy&quot;: 7368 
},
{
 &quot;date&quot;: &quot;1990-10-01&quot;,
&quot;pce&quot;:         3887.1,
&quot;pop&quot;: 251057,
&quot;psavert&quot;:            7.3,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 7459 
},
{
 &quot;date&quot;: &quot;1990-11-01&quot;,
&quot;pce&quot;:         3888.4,
&quot;pop&quot;: 251346,
&quot;psavert&quot;:            7.4,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 7764 
},
{
 &quot;date&quot;: &quot;1990-12-01&quot;,
&quot;pce&quot;:         3877.8,
&quot;pop&quot;: 251626,
&quot;psavert&quot;:            8.2,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 7901 
},
{
 &quot;date&quot;: &quot;1991-01-01&quot;,
&quot;pce&quot;:         3857.6,
&quot;pop&quot;: 251889,
&quot;psavert&quot;:            8.7,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 8015 
},
{
 &quot;date&quot;: &quot;1991-02-01&quot;,
&quot;pce&quot;:         3883.3,
&quot;pop&quot;: 252135,
&quot;psavert&quot;:            8.3,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 8265 
},
{
 &quot;date&quot;: &quot;1991-03-01&quot;,
&quot;pce&quot;:         3929.7,
&quot;pop&quot;: 252372,
&quot;psavert&quot;:            7.4,
&quot;uempmed&quot;:            6.7,
&quot;unemploy&quot;: 8586 
},
{
 &quot;date&quot;: &quot;1991-04-01&quot;,
&quot;pce&quot;:         3923.9,
&quot;pop&quot;: 252643,
&quot;psavert&quot;:              8,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 8439 
},
{
 &quot;date&quot;: &quot;1991-05-01&quot;,
&quot;pce&quot;:           3950,
&quot;pop&quot;: 252913,
&quot;psavert&quot;:            7.7,
&quot;uempmed&quot;:            6.4,
&quot;unemploy&quot;: 8736 
},
{
 &quot;date&quot;: &quot;1991-06-01&quot;,
&quot;pce&quot;:         3957.1,
&quot;pop&quot;: 253207,
&quot;psavert&quot;:            8.2,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 8692 
},
{
 &quot;date&quot;: &quot;1991-07-01&quot;,
&quot;pce&quot;:         3982.4,
&quot;pop&quot;: 253493,
&quot;psavert&quot;:            7.6,
&quot;uempmed&quot;:              7,
&quot;unemploy&quot;: 8586 
},
{
 &quot;date&quot;: &quot;1991-08-01&quot;,
&quot;pce&quot;:         3985.4,
&quot;pop&quot;: 253807,
&quot;psavert&quot;:            7.9,
&quot;uempmed&quot;:            7.3,
&quot;unemploy&quot;: 8666 
},
{
 &quot;date&quot;: &quot;1991-09-01&quot;,
&quot;pce&quot;:         4001.2,
&quot;pop&quot;: 254126,
&quot;psavert&quot;:            8.1,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 8722 
},
{
 &quot;date&quot;: &quot;1991-10-01&quot;,
&quot;pce&quot;:         3992.9,
&quot;pop&quot;: 254435,
&quot;psavert&quot;:            8.6,
&quot;uempmed&quot;:            7.2,
&quot;unemploy&quot;: 8842 
},
{
 &quot;date&quot;: &quot;1991-11-01&quot;,
&quot;pce&quot;:         4020.6,
&quot;pop&quot;: 254718,
&quot;psavert&quot;:            8.4,
&quot;uempmed&quot;:            7.5,
&quot;unemploy&quot;: 8931 
},
{
 &quot;date&quot;: &quot;1991-12-01&quot;,
&quot;pce&quot;:         4037.7,
&quot;pop&quot;: 254964,
&quot;psavert&quot;:            9.1,
&quot;uempmed&quot;:            7.8,
&quot;unemploy&quot;: 9198 
},
{
 &quot;date&quot;: &quot;1992-01-01&quot;,
&quot;pce&quot;:         4101.9,
&quot;pop&quot;: 255214,
&quot;psavert&quot;:            8.8,
&quot;uempmed&quot;:            8.1,
&quot;unemploy&quot;: 9283 
},
{
 &quot;date&quot;: &quot;1992-02-01&quot;,
&quot;pce&quot;:         4116.8,
&quot;pop&quot;: 255448,
&quot;psavert&quot;:            9.2,
&quot;uempmed&quot;:            8.2,
&quot;unemploy&quot;: 9454 
},
{
 &quot;date&quot;: &quot;1992-03-01&quot;,
&quot;pce&quot;:         4134.3,
&quot;pop&quot;: 255703,
&quot;psavert&quot;:            9.2,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 9460 
},
{
 &quot;date&quot;: &quot;1992-04-01&quot;,
&quot;pce&quot;:           4149,
&quot;pop&quot;: 255992,
&quot;psavert&quot;:            9.4,
&quot;uempmed&quot;:            8.5,
&quot;unemploy&quot;: 9415 
},
{
 &quot;date&quot;: &quot;1992-05-01&quot;,
&quot;pce&quot;:         4176.1,
&quot;pop&quot;: 256285,
&quot;psavert&quot;:            9.4,
&quot;uempmed&quot;:            8.8,
&quot;unemploy&quot;: 9744 
},
{
 &quot;date&quot;: &quot;1992-06-01&quot;,
&quot;pce&quot;:           4195,
&quot;pop&quot;: 256589,
&quot;psavert&quot;:            9.5,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 10040 
},
{
 &quot;date&quot;: &quot;1992-07-01&quot;,
&quot;pce&quot;:           4223,
&quot;pop&quot;: 256894,
&quot;psavert&quot;:            9.1,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 9850 
},
{
 &quot;date&quot;: &quot;1992-08-01&quot;,
&quot;pce&quot;:         4239.3,
&quot;pop&quot;: 257232,
&quot;psavert&quot;:            9.2,
&quot;uempmed&quot;:            8.8,
&quot;unemploy&quot;: 9787 
},
{
 &quot;date&quot;: &quot;1992-09-01&quot;,
&quot;pce&quot;:         4273.9,
&quot;pop&quot;: 257548,
&quot;psavert&quot;:            8.2,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 9781 
},
{
 &quot;date&quot;: &quot;1992-10-01&quot;,
&quot;pce&quot;:         4303.5,
&quot;pop&quot;: 257861,
&quot;psavert&quot;:            7.4,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 9398 
},
{
 &quot;date&quot;: &quot;1992-11-01&quot;,
&quot;pce&quot;:         4319.5,
&quot;pop&quot;: 258147,
&quot;psavert&quot;:            7.3,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 9565 
},
{
 &quot;date&quot;: &quot;1992-12-01&quot;,
&quot;pce&quot;:         4355.6,
&quot;pop&quot;: 258413,
&quot;psavert&quot;:            9.9,
&quot;uempmed&quot;:            9.3,
&quot;unemploy&quot;: 9557 
},
{
 &quot;date&quot;: &quot;1993-01-01&quot;,
&quot;pce&quot;:         4359.7,
&quot;pop&quot;: 258679,
&quot;psavert&quot;:            8.3,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 9325 
},
{
 &quot;date&quot;: &quot;1993-02-01&quot;,
&quot;pce&quot;:         4374.3,
&quot;pop&quot;: 258919,
&quot;psavert&quot;:            8.4,
&quot;uempmed&quot;:            8.5,
&quot;unemploy&quot;: 9183 
},
{
 &quot;date&quot;: &quot;1993-03-01&quot;,
&quot;pce&quot;:         4371.4,
&quot;pop&quot;: 259152,
&quot;psavert&quot;:            8.3,
&quot;uempmed&quot;:            8.5,
&quot;unemploy&quot;: 9056 
},
{
 &quot;date&quot;: &quot;1993-04-01&quot;,
&quot;pce&quot;:         4412.4,
&quot;pop&quot;: 259414,
&quot;psavert&quot;:            8.2,
&quot;uempmed&quot;:            8.4,
&quot;unemploy&quot;: 9110 
},
{
 &quot;date&quot;: &quot;1993-05-01&quot;,
&quot;pce&quot;:         4441.3,
&quot;pop&quot;: 259680,
&quot;psavert&quot;:            7.7,
&quot;uempmed&quot;:            8.1,
&quot;unemploy&quot;: 9149 
},
{
 &quot;date&quot;: &quot;1993-06-01&quot;,
&quot;pce&quot;:         4458.8,
&quot;pop&quot;: 259963,
&quot;psavert&quot;:            7.2,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 9121 
},
{
 &quot;date&quot;: &quot;1993-07-01&quot;,
&quot;pce&quot;:         4487.7,
&quot;pop&quot;: 260255,
&quot;psavert&quot;:              7,
&quot;uempmed&quot;:            8.2,
&quot;unemploy&quot;: 8930 
},
{
 &quot;date&quot;: &quot;1993-08-01&quot;,
&quot;pce&quot;:         4499.9,
&quot;pop&quot;: 260566,
&quot;psavert&quot;:            7.1,
&quot;uempmed&quot;:            8.2,
&quot;unemploy&quot;: 8763 
},
{
 &quot;date&quot;: &quot;1993-09-01&quot;,
&quot;pce&quot;:         4530.5,
&quot;pop&quot;: 260867,
&quot;psavert&quot;:            6.3,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 8714 
},
{
 &quot;date&quot;: &quot;1993-10-01&quot;,
&quot;pce&quot;:           4552,
&quot;pop&quot;: 261163,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:              8,
&quot;unemploy&quot;: 8750 
},
{
 &quot;date&quot;: &quot;1993-11-01&quot;,
&quot;pce&quot;:         4573.4,
&quot;pop&quot;: 261425,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 8542 
},
{
 &quot;date&quot;: &quot;1993-12-01&quot;,
&quot;pce&quot;:         4590.7,
&quot;pop&quot;: 261674,
&quot;psavert&quot;:            8.4,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 8477 
},
{
 &quot;date&quot;: &quot;1994-01-01&quot;,
&quot;pce&quot;:         4604.8,
&quot;pop&quot;: 261919,
&quot;psavert&quot;:            6.4,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 8630 
},
{
 &quot;date&quot;: &quot;1994-02-01&quot;,
&quot;pce&quot;:         4652.3,
&quot;pop&quot;: 262123,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:            9.2,
&quot;unemploy&quot;: 8583 
},
{
 &quot;date&quot;: &quot;1994-03-01&quot;,
&quot;pce&quot;:         4665.4,
&quot;pop&quot;: 262352,
&quot;psavert&quot;:            6.2,
&quot;uempmed&quot;:            9.3,
&quot;unemploy&quot;: 8470 
},
{
 &quot;date&quot;: &quot;1994-04-01&quot;,
&quot;pce&quot;:         4690.7,
&quot;pop&quot;: 262631,
&quot;psavert&quot;:            5.8,
&quot;uempmed&quot;:            9.1,
&quot;unemploy&quot;: 8331 
},
{
 &quot;date&quot;: &quot;1994-05-01&quot;,
&quot;pce&quot;:         4689.2,
&quot;pop&quot;: 262877,
&quot;psavert&quot;:            7.1,
&quot;uempmed&quot;:            9.2,
&quot;unemploy&quot;: 7915 
},
{
 &quot;date&quot;: &quot;1994-06-01&quot;,
&quot;pce&quot;:         4728.8,
&quot;pop&quot;: 263152,
&quot;psavert&quot;:            6.3,
&quot;uempmed&quot;:            9.3,
&quot;unemploy&quot;: 7927 
},
{
 &quot;date&quot;: &quot;1994-07-01&quot;,
&quot;pce&quot;:         4740.8,
&quot;pop&quot;: 263436,
&quot;psavert&quot;:            6.4,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 7946 
},
{
 &quot;date&quot;: &quot;1994-08-01&quot;,
&quot;pce&quot;:           4783,
&quot;pop&quot;: 263724,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:            8.9,
&quot;unemploy&quot;: 7933 
},
{
 &quot;date&quot;: &quot;1994-09-01&quot;,
&quot;pce&quot;:         4795.5,
&quot;pop&quot;: 264017,
&quot;psavert&quot;:            6.2,
&quot;uempmed&quot;:            9.2,
&quot;unemploy&quot;: 7734 
},
{
 &quot;date&quot;: &quot;1994-10-01&quot;,
&quot;pce&quot;:         4833.3,
&quot;pop&quot;: 264301,
&quot;psavert&quot;:            6.5,
&quot;uempmed&quot;:             10,
&quot;unemploy&quot;: 7632 
},
{
 &quot;date&quot;: &quot;1994-11-01&quot;,
&quot;pce&quot;:           4846,
&quot;pop&quot;: 264559,
&quot;psavert&quot;:            6.4,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 7375 
},
{
 &quot;date&quot;: &quot;1994-12-01&quot;,
&quot;pce&quot;:         4862.3,
&quot;pop&quot;: 264804,
&quot;psavert&quot;:            6.5,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 7230 
},
{
 &quot;date&quot;: &quot;1995-01-01&quot;,
&quot;pce&quot;:         4871.9,
&quot;pop&quot;: 265044,
&quot;psavert&quot;:            6.9,
&quot;uempmed&quot;:              8,
&quot;unemploy&quot;: 7375 
},
{
 &quot;date&quot;: &quot;1995-02-01&quot;,
&quot;pce&quot;:         4871.7,
&quot;pop&quot;: 265270,
&quot;psavert&quot;:            7.3,
&quot;uempmed&quot;:            8.1,
&quot;unemploy&quot;: 7187 
},
{
 &quot;date&quot;: &quot;1995-03-01&quot;,
&quot;pce&quot;:         4906.5,
&quot;pop&quot;: 265495,
&quot;psavert&quot;:              7,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7153 
},
{
 &quot;date&quot;: &quot;1995-04-01&quot;,
&quot;pce&quot;:         4911.5,
&quot;pop&quot;: 265755,
&quot;psavert&quot;:            6.3,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7645 
},
{
 &quot;date&quot;: &quot;1995-05-01&quot;,
&quot;pce&quot;:         4954.4,
&quot;pop&quot;: 265998,
&quot;psavert&quot;:            6.5,
&quot;uempmed&quot;:            9.1,
&quot;unemploy&quot;: 7430 
},
{
 &quot;date&quot;: &quot;1995-06-01&quot;,
&quot;pce&quot;:           4999,
&quot;pop&quot;: 266270,
&quot;psavert&quot;:            6.1,
&quot;uempmed&quot;:            7.9,
&quot;unemploy&quot;: 7427 
},
{
 &quot;date&quot;: &quot;1995-07-01&quot;,
&quot;pce&quot;:         4991.8,
&quot;pop&quot;: 266557,
&quot;psavert&quot;:            6.4,
&quot;uempmed&quot;:            8.5,
&quot;unemploy&quot;: 7527 
},
{
 &quot;date&quot;: &quot;1995-08-01&quot;,
&quot;pce&quot;:         5027.1,
&quot;pop&quot;: 266843,
&quot;psavert&quot;:            6.1,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7484 
},
{
 &quot;date&quot;: &quot;1995-09-01&quot;,
&quot;pce&quot;:         5042.5,
&quot;pop&quot;: 267152,
&quot;psavert&quot;:            6.1,
&quot;uempmed&quot;:            7.9,
&quot;unemploy&quot;: 7478 
},
{
 &quot;date&quot;: &quot;1995-10-01&quot;,
&quot;pce&quot;:         5035.9,
&quot;pop&quot;: 267456,
&quot;psavert&quot;:            6.5,
&quot;uempmed&quot;:            8.2,
&quot;unemploy&quot;: 7328 
},
{
 &quot;date&quot;: &quot;1995-11-01&quot;,
&quot;pce&quot;:         5077.8,
&quot;pop&quot;: 267715,
&quot;psavert&quot;:              6,
&quot;uempmed&quot;:              8,
&quot;unemploy&quot;: 7426 
},
{
 &quot;date&quot;: &quot;1995-12-01&quot;,
&quot;pce&quot;:         5120.1,
&quot;pop&quot;: 267943,
&quot;psavert&quot;:            5.5,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7423 
},
{
 &quot;date&quot;: &quot;1996-01-01&quot;,
&quot;pce&quot;:         5108.9,
&quot;pop&quot;: 268151,
&quot;psavert&quot;:            6.1,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7491 
},
{
 &quot;date&quot;: &quot;1996-02-01&quot;,
&quot;pce&quot;:         5156.1,
&quot;pop&quot;: 268364,
&quot;psavert&quot;:            6.1,
&quot;uempmed&quot;:            7.8,
&quot;unemploy&quot;: 7313 
},
{
 &quot;date&quot;: &quot;1996-03-01&quot;,
&quot;pce&quot;:         5196.4,
&quot;pop&quot;: 268595,
&quot;psavert&quot;:              6,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7318 
},
{
 &quot;date&quot;: &quot;1996-04-01&quot;,
&quot;pce&quot;:         5231.6,
&quot;pop&quot;: 268853,
&quot;psavert&quot;:              5,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 7415 
},
{
 &quot;date&quot;: &quot;1996-05-01&quot;,
&quot;pce&quot;:         5247.2,
&quot;pop&quot;: 269108,
&quot;psavert&quot;:            6.1,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 7423 
},
{
 &quot;date&quot;: &quot;1996-06-01&quot;,
&quot;pce&quot;:         5253.7,
&quot;pop&quot;: 269386,
&quot;psavert&quot;:            6.5,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7095 
},
{
 &quot;date&quot;: &quot;1996-07-01&quot;,
&quot;pce&quot;:         5275.8,
&quot;pop&quot;: 269667,
&quot;psavert&quot;:            6.1,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7337 
},
{
 &quot;date&quot;: &quot;1996-08-01&quot;,
&quot;pce&quot;:           5299,
&quot;pop&quot;: 269976,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:            8.4,
&quot;unemploy&quot;: 6882 
},
{
 &quot;date&quot;: &quot;1996-09-01&quot;,
&quot;pce&quot;:           5320,
&quot;pop&quot;: 270284,
&quot;psavert&quot;:              6,
&quot;uempmed&quot;:            8.5,
&quot;unemploy&quot;: 6979 
},
{
 &quot;date&quot;: &quot;1996-10-01&quot;,
&quot;pce&quot;:         5351.5,
&quot;pop&quot;: 270581,
&quot;psavert&quot;:            5.8,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7031 
},
{
 &quot;date&quot;: &quot;1996-11-01&quot;,
&quot;pce&quot;:           5375,
&quot;pop&quot;: 270878,
&quot;psavert&quot;:            5.8,
&quot;uempmed&quot;:            7.7,
&quot;unemploy&quot;: 7236 
},
{
 &quot;date&quot;: &quot;1996-12-01&quot;,
&quot;pce&quot;:         5401.7,
&quot;pop&quot;: 271125,
&quot;psavert&quot;:            5.7,
&quot;uempmed&quot;:            7.8,
&quot;unemploy&quot;: 7253 
},
{
 &quot;date&quot;: &quot;1997-01-01&quot;,
&quot;pce&quot;:         5434.9,
&quot;pop&quot;: 271360,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:            7.8,
&quot;unemploy&quot;: 7158 
},
{
 &quot;date&quot;: &quot;1997-02-01&quot;,
&quot;pce&quot;:         5457.7,
&quot;pop&quot;: 271585,
&quot;psavert&quot;:            5.7,
&quot;uempmed&quot;:            8.1,
&quot;unemploy&quot;: 7102 
},
{
 &quot;date&quot;: &quot;1997-03-01&quot;,
&quot;pce&quot;:         5477.6,
&quot;pop&quot;: 271821,
&quot;psavert&quot;:            5.8,
&quot;uempmed&quot;:            7.9,
&quot;unemploy&quot;: 7000 
},
{
 &quot;date&quot;: &quot;1997-04-01&quot;,
&quot;pce&quot;:         5482.8,
&quot;pop&quot;: 272083,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 6873 
},
{
 &quot;date&quot;: &quot;1997-05-01&quot;,
&quot;pce&quot;:         5484.3,
&quot;pop&quot;: 272342,
&quot;psavert&quot;:            6.2,
&quot;uempmed&quot;:              8,
&quot;unemploy&quot;: 6655 
},
{
 &quot;date&quot;: &quot;1997-06-01&quot;,
&quot;pce&quot;:         5518.2,
&quot;pop&quot;: 272622,
&quot;psavert&quot;:              6,
&quot;uempmed&quot;:              8,
&quot;unemploy&quot;: 6799 
},
{
 &quot;date&quot;: &quot;1997-07-01&quot;,
&quot;pce&quot;:           5573,
&quot;pop&quot;: 272912,
&quot;psavert&quot;:            5.5,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 6655 
},
{
 &quot;date&quot;: &quot;1997-08-01&quot;,
&quot;pce&quot;:         5611.8,
&quot;pop&quot;: 273237,
&quot;psavert&quot;:            5.4,
&quot;uempmed&quot;:            7.8,
&quot;unemploy&quot;: 6608 
},
{
 &quot;date&quot;: &quot;1997-09-01&quot;,
&quot;pce&quot;:         5625.6,
&quot;pop&quot;: 273553,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:            8.2,
&quot;unemploy&quot;: 6656 
},
{
 &quot;date&quot;: &quot;1997-10-01&quot;,
&quot;pce&quot;:         5661.2,
&quot;pop&quot;: 273852,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:            7.7,
&quot;unemploy&quot;: 6454 
},
{
 &quot;date&quot;: &quot;1997-11-01&quot;,
&quot;pce&quot;:         5685.2,
&quot;pop&quot;: 274126,
&quot;psavert&quot;:            5.8,
&quot;uempmed&quot;:            7.6,
&quot;unemploy&quot;: 6308 
},
{
 &quot;date&quot;: &quot;1997-12-01&quot;,
&quot;pce&quot;:         5716.4,
&quot;pop&quot;: 274372,
&quot;psavert&quot;:            5.8,
&quot;uempmed&quot;:            7.5,
&quot;unemploy&quot;: 6476 
},
{
 &quot;date&quot;: &quot;1998-01-01&quot;,
&quot;pce&quot;:         5714.4,
&quot;pop&quot;: 274626,
&quot;psavert&quot;:            6.7,
&quot;uempmed&quot;:            7.4,
&quot;unemploy&quot;: 6368 
},
{
 &quot;date&quot;: &quot;1998-02-01&quot;,
&quot;pce&quot;:         5748.4,
&quot;pop&quot;: 274838,
&quot;psavert&quot;:            6.8,
&quot;uempmed&quot;:              7,
&quot;unemploy&quot;: 6306 
},
{
 &quot;date&quot;: &quot;1998-03-01&quot;,
&quot;pce&quot;:           5775,
&quot;pop&quot;: 275047,
&quot;psavert&quot;:            6.9,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 6422 
},
{
 &quot;date&quot;: &quot;1998-04-01&quot;,
&quot;pce&quot;:         5812.9,
&quot;pop&quot;: 275304,
&quot;psavert&quot;:            6.6,
&quot;uempmed&quot;:            6.7,
&quot;unemploy&quot;: 5941 
},
{
 &quot;date&quot;: &quot;1998-05-01&quot;,
&quot;pce&quot;:         5863.3,
&quot;pop&quot;: 275564,
&quot;psavert&quot;:            6.3,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 6047 
},
{
 &quot;date&quot;: &quot;1998-06-01&quot;,
&quot;pce&quot;:         5897.2,
&quot;pop&quot;: 275836,
&quot;psavert&quot;:            6.2,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 6212 
},
{
 &quot;date&quot;: &quot;1998-07-01&quot;,
&quot;pce&quot;:         5915.6,
&quot;pop&quot;: 276115,
&quot;psavert&quot;:            6.3,
&quot;uempmed&quot;:            6.7,
&quot;unemploy&quot;: 6259 
},
{
 &quot;date&quot;: &quot;1998-08-01&quot;,
&quot;pce&quot;:           5951,
&quot;pop&quot;: 276418,
&quot;psavert&quot;:            6.2,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 6179 
},
{
 &quot;date&quot;: &quot;1998-09-01&quot;,
&quot;pce&quot;:         5991.8,
&quot;pop&quot;: 276714,
&quot;psavert&quot;:            5.8,
&quot;uempmed&quot;:            6.7,
&quot;unemploy&quot;: 6300 
},
{
 &quot;date&quot;: &quot;1998-10-01&quot;,
&quot;pce&quot;:         6025.8,
&quot;pop&quot;: 277003,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 6280 
},
{
 &quot;date&quot;: &quot;1998-11-01&quot;,
&quot;pce&quot;:         6042.7,
&quot;pop&quot;: 277277,
&quot;psavert&quot;:            5.7,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 6100 
},
{
 &quot;date&quot;: &quot;1998-12-01&quot;,
&quot;pce&quot;:         6098.2,
&quot;pop&quot;: 277526,
&quot;psavert&quot;:            5.2,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 6032 
},
{
 &quot;date&quot;: &quot;1999-01-01&quot;,
&quot;pce&quot;:         6099.1,
&quot;pop&quot;: 277790,
&quot;psavert&quot;:            5.7,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 5976 
},
{
 &quot;date&quot;: &quot;1999-02-01&quot;,
&quot;pce&quot;:         6128.2,
&quot;pop&quot;: 277992,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 6111 
},
{
 &quot;date&quot;: &quot;1999-03-01&quot;,
&quot;pce&quot;:         6159.7,
&quot;pop&quot;: 278198,
&quot;psavert&quot;:            5.3,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 5783 
},
{
 &quot;date&quot;: &quot;1999-04-01&quot;,
&quot;pce&quot;:         6223.6,
&quot;pop&quot;: 278451,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 6004 
},
{
 &quot;date&quot;: &quot;1999-05-01&quot;,
&quot;pce&quot;:         6253.4,
&quot;pop&quot;: 278717,
&quot;psavert&quot;:            4.3,
&quot;uempmed&quot;:            6.5,
&quot;unemploy&quot;: 5796 
},
{
 &quot;date&quot;: &quot;1999-06-01&quot;,
&quot;pce&quot;:         6281.9,
&quot;pop&quot;: 279001,
&quot;psavert&quot;:            4.2,
&quot;uempmed&quot;:            6.3,
&quot;unemploy&quot;: 5951 
},
{
 &quot;date&quot;: &quot;1999-07-01&quot;,
&quot;pce&quot;:         6309.5,
&quot;pop&quot;: 279295,
&quot;psavert&quot;:            4.1,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 6025 
},
{
 &quot;date&quot;: &quot;1999-08-01&quot;,
&quot;pce&quot;:         6354.8,
&quot;pop&quot;: 279602,
&quot;psavert&quot;:              4,
&quot;uempmed&quot;:            6.5,
&quot;unemploy&quot;: 5838 
},
{
 &quot;date&quot;: &quot;1999-09-01&quot;,
&quot;pce&quot;:         6407.4,
&quot;pop&quot;: 279903,
&quot;psavert&quot;:            3.5,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 5915 
},
{
 &quot;date&quot;: &quot;1999-10-01&quot;,
&quot;pce&quot;:         6431.2,
&quot;pop&quot;: 280203,
&quot;psavert&quot;:            3.9,
&quot;uempmed&quot;:            6.1,
&quot;unemploy&quot;: 5778 
},
{
 &quot;date&quot;: &quot;1999-11-01&quot;,
&quot;pce&quot;:         6467.2,
&quot;pop&quot;: 280471,
&quot;psavert&quot;:            4.1,
&quot;uempmed&quot;:            6.2,
&quot;unemploy&quot;: 5716 
},
{
 &quot;date&quot;: &quot;1999-12-01&quot;,
&quot;pce&quot;:         6568.2,
&quot;pop&quot;: 280716,
&quot;psavert&quot;:            3.7,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 5653 
},
{
 &quot;date&quot;: &quot;2000-01-01&quot;,
&quot;pce&quot;:         6564.7,
&quot;pop&quot;: 280976,
&quot;psavert&quot;:            4.7,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 5708 
},
{
 &quot;date&quot;: &quot;2000-02-01&quot;,
&quot;pce&quot;:         6648.7,
&quot;pop&quot;: 281190,
&quot;psavert&quot;:            4.2,
&quot;uempmed&quot;:            6.1,
&quot;unemploy&quot;: 5858 
},
{
 &quot;date&quot;: &quot;2000-03-01&quot;,
&quot;pce&quot;:         6714.8,
&quot;pop&quot;: 281409,
&quot;psavert&quot;:            3.9,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 5733 
},
{
 &quot;date&quot;: &quot;2000-04-01&quot;,
&quot;pce&quot;:           6701,
&quot;pop&quot;: 281653,
&quot;psavert&quot;:            4.4,
&quot;uempmed&quot;:            6.1,
&quot;unemploy&quot;: 5481 
},
{
 &quot;date&quot;: &quot;2000-05-01&quot;,
&quot;pce&quot;:         6737.2,
&quot;pop&quot;: 281877,
&quot;psavert&quot;:            4.2,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 5758 
},
{
 &quot;date&quot;: &quot;2000-06-01&quot;,
&quot;pce&quot;:         6773.6,
&quot;pop&quot;: 282126,
&quot;psavert&quot;:            4.2,
&quot;uempmed&quot;:            5.7,
&quot;unemploy&quot;: 5651 
},
{
 &quot;date&quot;: &quot;2000-07-01&quot;,
&quot;pce&quot;:         6793.7,
&quot;pop&quot;: 282385,
&quot;psavert&quot;:            4.6,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 5747 
},
{
 &quot;date&quot;: &quot;2000-08-01&quot;,
&quot;pce&quot;:         6828.7,
&quot;pop&quot;: 282653,
&quot;psavert&quot;:            4.6,
&quot;uempmed&quot;:            6.3,
&quot;unemploy&quot;: 5853 
},
{
 &quot;date&quot;: &quot;2000-09-01&quot;,
&quot;pce&quot;:         6913.1,
&quot;pop&quot;: 282932,
&quot;psavert&quot;:            3.8,
&quot;uempmed&quot;:            5.2,
&quot;unemploy&quot;: 5625 
},
{
 &quot;date&quot;: &quot;2000-10-01&quot;,
&quot;pce&quot;:         6919.6,
&quot;pop&quot;: 283201,
&quot;psavert&quot;:              4,
&quot;uempmed&quot;:            6.1,
&quot;unemploy&quot;: 5534 
},
{
 &quot;date&quot;: &quot;2000-11-01&quot;,
&quot;pce&quot;:         6934.5,
&quot;pop&quot;: 283453,
&quot;psavert&quot;:            3.8,
&quot;uempmed&quot;:            6.1,
&quot;unemploy&quot;: 5639 
},
{
 &quot;date&quot;: &quot;2000-12-01&quot;,
&quot;pce&quot;:         6979.1,
&quot;pop&quot;: 283696,
&quot;psavert&quot;:            3.5,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 5634 
},
{
 &quot;date&quot;: &quot;2001-01-01&quot;,
&quot;pce&quot;:         7009.8,
&quot;pop&quot;: 283920,
&quot;psavert&quot;:              4,
&quot;uempmed&quot;:            5.8,
&quot;unemploy&quot;: 6023 
},
{
 &quot;date&quot;: &quot;2001-02-01&quot;,
&quot;pce&quot;:         7029.3,
&quot;pop&quot;: 284137,
&quot;psavert&quot;:            4.1,
&quot;uempmed&quot;:            6.1,
&quot;unemploy&quot;: 6089 
},
{
 &quot;date&quot;: &quot;2001-03-01&quot;,
&quot;pce&quot;:         7022.1,
&quot;pop&quot;: 284350,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:            6.6,
&quot;unemploy&quot;: 6141 
},
{
 &quot;date&quot;: &quot;2001-04-01&quot;,
&quot;pce&quot;:         7036.2,
&quot;pop&quot;: 284581,
&quot;psavert&quot;:            4.3,
&quot;uempmed&quot;:            5.9,
&quot;unemploy&quot;: 6271 
},
{
 &quot;date&quot;: &quot;2001-05-01&quot;,
&quot;pce&quot;:         7083.1,
&quot;pop&quot;: 284810,
&quot;psavert&quot;:            3.7,
&quot;uempmed&quot;:            6.3,
&quot;unemploy&quot;: 6226 
},
{
 &quot;date&quot;: &quot;2001-06-01&quot;,
&quot;pce&quot;:         7097.1,
&quot;pop&quot;: 285062,
&quot;psavert&quot;:            3.7,
&quot;uempmed&quot;:              6,
&quot;unemploy&quot;: 6484 
},
{
 &quot;date&quot;: &quot;2001-07-01&quot;,
&quot;pce&quot;:         7109.2,
&quot;pop&quot;: 285309,
&quot;psavert&quot;:              5,
&quot;uempmed&quot;:            6.8,
&quot;unemploy&quot;: 6583 
},
{
 &quot;date&quot;: &quot;2001-08-01&quot;,
&quot;pce&quot;:         7146.1,
&quot;pop&quot;: 285570,
&quot;psavert&quot;:            6.1,
&quot;uempmed&quot;:            6.9,
&quot;unemploy&quot;: 7042 
},
{
 &quot;date&quot;: &quot;2001-09-01&quot;,
&quot;pce&quot;:         7054.8,
&quot;pop&quot;: 285843,
&quot;psavert&quot;:            6.3,
&quot;uempmed&quot;:            7.2,
&quot;unemploy&quot;: 7142 
},
{
 &quot;date&quot;: &quot;2001-10-01&quot;,
&quot;pce&quot;:         7250.2,
&quot;pop&quot;: 286098,
&quot;psavert&quot;:            2.7,
&quot;uempmed&quot;:            7.3,
&quot;unemploy&quot;: 7694 
},
{
 &quot;date&quot;: &quot;2001-11-01&quot;,
&quot;pce&quot;:         7209.6,
&quot;pop&quot;: 286341,
&quot;psavert&quot;:            3.4,
&quot;uempmed&quot;:            7.7,
&quot;unemploy&quot;: 8003 
},
{
 &quot;date&quot;: &quot;2001-12-01&quot;,
&quot;pce&quot;:           7190,
&quot;pop&quot;: 286570,
&quot;psavert&quot;:            3.8,
&quot;uempmed&quot;:            8.2,
&quot;unemploy&quot;: 8258 
},
{
 &quot;date&quot;: &quot;2002-01-01&quot;,
&quot;pce&quot;:         7217.7,
&quot;pop&quot;: 286788,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:            8.4,
&quot;unemploy&quot;: 8182 
},
{
 &quot;date&quot;: &quot;2002-02-01&quot;,
&quot;pce&quot;:         7259.7,
&quot;pop&quot;: 286994,
&quot;psavert&quot;:            5.3,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 8215 
},
{
 &quot;date&quot;: &quot;2002-03-01&quot;,
&quot;pce&quot;:         7276.7,
&quot;pop&quot;: 287190,
&quot;psavert&quot;:            5.3,
&quot;uempmed&quot;:            8.4,
&quot;unemploy&quot;: 8304 
},
{
 &quot;date&quot;: &quot;2002-04-01&quot;,
&quot;pce&quot;:         7345.6,
&quot;pop&quot;: 287397,
&quot;psavert&quot;:            5.1,
&quot;uempmed&quot;:            8.9,
&quot;unemploy&quot;: 8599 
},
{
 &quot;date&quot;: &quot;2002-05-01&quot;,
&quot;pce&quot;:         7321.8,
&quot;pop&quot;: 287623,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:            9.5,
&quot;unemploy&quot;: 8399 
},
{
 &quot;date&quot;: &quot;2002-06-01&quot;,
&quot;pce&quot;:         7366.1,
&quot;pop&quot;: 287864,
&quot;psavert&quot;:            5.4,
&quot;uempmed&quot;:             11,
&quot;unemploy&quot;: 8393 
},
{
 &quot;date&quot;: &quot;2002-07-01&quot;,
&quot;pce&quot;:         7424.2,
&quot;pop&quot;: 288105,
&quot;psavert&quot;:            4.6,
&quot;uempmed&quot;:            8.9,
&quot;unemploy&quot;: 8390 
},
{
 &quot;date&quot;: &quot;2002-08-01&quot;,
&quot;pce&quot;:           7449,
&quot;pop&quot;: 288360,
&quot;psavert&quot;:            4.4,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 8304 
},
{
 &quot;date&quot;: &quot;2002-09-01&quot;,
&quot;pce&quot;:         7426.1,
&quot;pop&quot;: 288618,
&quot;psavert&quot;:            4.9,
&quot;uempmed&quot;:            9.5,
&quot;unemploy&quot;: 8251 
},
{
 &quot;date&quot;: &quot;2002-10-01&quot;,
&quot;pce&quot;:         7469.3,
&quot;pop&quot;: 288870,
&quot;psavert&quot;:            4.7,
&quot;uempmed&quot;:            9.6,
&quot;unemploy&quot;: 8307 
},
{
 &quot;date&quot;: &quot;2002-11-01&quot;,
&quot;pce&quot;:         7499.8,
&quot;pop&quot;: 289106,
&quot;psavert&quot;:            4.7,
&quot;uempmed&quot;:            9.3,
&quot;unemploy&quot;: 8520 
},
{
 &quot;date&quot;: &quot;2002-12-01&quot;,
&quot;pce&quot;:         7552.6,
&quot;pop&quot;: 289313,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:            9.6,
&quot;unemploy&quot;: 8640 
},
{
 &quot;date&quot;: &quot;2003-01-01&quot;,
&quot;pce&quot;:         7579.5,
&quot;pop&quot;: 289518,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:            9.6,
&quot;unemploy&quot;: 8520 
},
{
 &quot;date&quot;: &quot;2003-02-01&quot;,
&quot;pce&quot;:         7573.6,
&quot;pop&quot;: 289714,
&quot;psavert&quot;:            4.7,
&quot;uempmed&quot;:            9.5,
&quot;unemploy&quot;: 8618 
},
{
 &quot;date&quot;: &quot;2003-03-01&quot;,
&quot;pce&quot;:         7627.5,
&quot;pop&quot;: 289911,
&quot;psavert&quot;:            4.6,
&quot;uempmed&quot;:            9.7,
&quot;unemploy&quot;: 8588 
},
{
 &quot;date&quot;: &quot;2003-04-01&quot;,
&quot;pce&quot;:         7661.7,
&quot;pop&quot;: 290125,
&quot;psavert&quot;:            4.6,
&quot;uempmed&quot;:           10.2,
&quot;unemploy&quot;: 8842 
},
{
 &quot;date&quot;: &quot;2003-05-01&quot;,
&quot;pce&quot;:         7669.2,
&quot;pop&quot;: 290346,
&quot;psavert&quot;:            5.1,
&quot;uempmed&quot;:            9.9,
&quot;unemploy&quot;: 8957 
},
{
 &quot;date&quot;: &quot;2003-06-01&quot;,
&quot;pce&quot;:         7722.9,
&quot;pop&quot;: 290584,
&quot;psavert&quot;:            4.9,
&quot;uempmed&quot;:           11.5,
&quot;unemploy&quot;: 9266 
},
{
 &quot;date&quot;: &quot;2003-07-01&quot;,
&quot;pce&quot;:         7783.8,
&quot;pop&quot;: 290820,
&quot;psavert&quot;:            5.5,
&quot;uempmed&quot;:           10.3,
&quot;unemploy&quot;: 9011 
},
{
 &quot;date&quot;: &quot;2003-08-01&quot;,
&quot;pce&quot;:         7878.9,
&quot;pop&quot;: 291072,
&quot;psavert&quot;:            5.3,
&quot;uempmed&quot;:           10.1,
&quot;unemploy&quot;: 8896 
},
{
 &quot;date&quot;: &quot;2003-09-01&quot;,
&quot;pce&quot;:           7874,
&quot;pop&quot;: 291321,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:           10.2,
&quot;unemploy&quot;: 8921 
},
{
 &quot;date&quot;: &quot;2003-10-01&quot;,
&quot;pce&quot;:         7890.6,
&quot;pop&quot;: 291574,
&quot;psavert&quot;:            4.6,
&quot;uempmed&quot;:           10.4,
&quot;unemploy&quot;: 8732 
},
{
 &quot;date&quot;: &quot;2003-11-01&quot;,
&quot;pce&quot;:         7950.4,
&quot;pop&quot;: 291807,
&quot;psavert&quot;:            4.7,
&quot;uempmed&quot;:           10.3,
&quot;unemploy&quot;: 8576 
},
{
 &quot;date&quot;: &quot;2003-12-01&quot;,
&quot;pce&quot;:         7974.3,
&quot;pop&quot;: 292008,
&quot;psavert&quot;:            4.8,
&quot;uempmed&quot;:           10.4,
&quot;unemploy&quot;: 8317 
},
{
 &quot;date&quot;: &quot;2004-01-01&quot;,
&quot;pce&quot;:         8037.3,
&quot;pop&quot;: 292192,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:           10.6,
&quot;unemploy&quot;: 8370 
},
{
 &quot;date&quot;: &quot;2004-02-01&quot;,
&quot;pce&quot;:         8072.1,
&quot;pop&quot;: 292368,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:           10.2,
&quot;unemploy&quot;: 8167 
},
{
 &quot;date&quot;: &quot;2004-03-01&quot;,
&quot;pce&quot;:           8121,
&quot;pop&quot;: 292561,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:           10.2,
&quot;unemploy&quot;: 8491 
},
{
 &quot;date&quot;: &quot;2004-04-01&quot;,
&quot;pce&quot;:         8141.6,
&quot;pop&quot;: 292779,
&quot;psavert&quot;:            4.7,
&quot;uempmed&quot;:            9.5,
&quot;unemploy&quot;: 8170 
},
{
 &quot;date&quot;: &quot;2004-05-01&quot;,
&quot;pce&quot;:         8212.9,
&quot;pop&quot;: 292997,
&quot;psavert&quot;:            4.7,
&quot;uempmed&quot;:            9.9,
&quot;unemploy&quot;: 8212 
},
{
 &quot;date&quot;: &quot;2004-06-01&quot;,
&quot;pce&quot;:         8204.6,
&quot;pop&quot;: 293223,
&quot;psavert&quot;:              5,
&quot;uempmed&quot;:             11,
&quot;unemploy&quot;: 8286 
},
{
 &quot;date&quot;: &quot;2004-07-01&quot;,
&quot;pce&quot;:         8270.7,
&quot;pop&quot;: 293463,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:            8.9,
&quot;unemploy&quot;: 8136 
},
{
 &quot;date&quot;: &quot;2004-08-01&quot;,
&quot;pce&quot;:         8294.4,
&quot;pop&quot;: 293719,
&quot;psavert&quot;:            4.6,
&quot;uempmed&quot;:            9.2,
&quot;unemploy&quot;: 7990 
},
{
 &quot;date&quot;: &quot;2004-09-01&quot;,
&quot;pce&quot;:           8373,
&quot;pop&quot;: 293971,
&quot;psavert&quot;:            3.9,
&quot;uempmed&quot;:            9.6,
&quot;unemploy&quot;: 7927 
},
{
 &quot;date&quot;: &quot;2004-10-01&quot;,
&quot;pce&quot;:         8417.9,
&quot;pop&quot;: 294230,
&quot;psavert&quot;:            3.8,
&quot;uempmed&quot;:            9.5,
&quot;unemploy&quot;: 8061 
},
{
 &quot;date&quot;: &quot;2004-11-01&quot;,
&quot;pce&quot;:         8458.4,
&quot;pop&quot;: 294466,
&quot;psavert&quot;:            3.4,
&quot;uempmed&quot;:            9.7,
&quot;unemploy&quot;: 7932 
},
{
 &quot;date&quot;: &quot;2004-12-01&quot;,
&quot;pce&quot;:         8516.5,
&quot;pop&quot;: 294694,
&quot;psavert&quot;:            6.3,
&quot;uempmed&quot;:            9.5,
&quot;unemploy&quot;: 7934 
},
{
 &quot;date&quot;: &quot;2005-01-01&quot;,
&quot;pce&quot;:         8521.2,
&quot;pop&quot;: 294914,
&quot;psavert&quot;:            2.9,
&quot;uempmed&quot;:            9.4,
&quot;unemploy&quot;: 7784 
},
{
 &quot;date&quot;: &quot;2005-02-01&quot;,
&quot;pce&quot;:         8575.7,
&quot;pop&quot;: 295105,
&quot;psavert&quot;:            2.7,
&quot;uempmed&quot;:            9.2,
&quot;unemploy&quot;: 7980 
},
{
 &quot;date&quot;: &quot;2005-03-01&quot;,
&quot;pce&quot;:         8622.5,
&quot;pop&quot;: 295287,
&quot;psavert&quot;:            2.7,
&quot;uempmed&quot;:            9.3,
&quot;unemploy&quot;: 7737 
},
{
 &quot;date&quot;: &quot;2005-04-01&quot;,
&quot;pce&quot;:         8715.9,
&quot;pop&quot;: 295490,
&quot;psavert&quot;:            2.1,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 7672 
},
{
 &quot;date&quot;: &quot;2005-05-01&quot;,
&quot;pce&quot;:         8680.6,
&quot;pop&quot;: 295704,
&quot;psavert&quot;:              3,
&quot;uempmed&quot;:            9.1,
&quot;unemploy&quot;: 7651 
},
{
 &quot;date&quot;: &quot;2005-06-01&quot;,
&quot;pce&quot;:         8775.3,
&quot;pop&quot;: 295936,
&quot;psavert&quot;:            2.2,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 7524 
},
{
 &quot;date&quot;: &quot;2005-07-01&quot;,
&quot;pce&quot;:         8867.9,
&quot;pop&quot;: 296186,
&quot;psavert&quot;:            1.9,
&quot;uempmed&quot;:            8.8,
&quot;unemploy&quot;: 7406 
},
{
 &quot;date&quot;: &quot;2005-08-01&quot;,
&quot;pce&quot;:         8872.6,
&quot;pop&quot;: 296440,
&quot;psavert&quot;:            2.4,
&quot;uempmed&quot;:            9.2,
&quot;unemploy&quot;: 7345 
},
{
 &quot;date&quot;: &quot;2005-09-01&quot;,
&quot;pce&quot;:         8923.6,
&quot;pop&quot;: 296707,
&quot;psavert&quot;:            2.3,
&quot;uempmed&quot;:            8.4,
&quot;unemploy&quot;: 7553 
},
{
 &quot;date&quot;: &quot;2005-10-01&quot;,
&quot;pce&quot;:         8959.6,
&quot;pop&quot;: 296972,
&quot;psavert&quot;:            2.6,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 7453 
},
{
 &quot;date&quot;: &quot;2005-11-01&quot;,
&quot;pce&quot;:         8987.7,
&quot;pop&quot;: 297207,
&quot;psavert&quot;:            2.7,
&quot;uempmed&quot;:            8.5,
&quot;unemploy&quot;: 7566 
},
{
 &quot;date&quot;: &quot;2005-12-01&quot;,
&quot;pce&quot;:         9026.8,
&quot;pop&quot;: 297431,
&quot;psavert&quot;:            2.8,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 7279 
},
{
 &quot;date&quot;: &quot;2006-01-01&quot;,
&quot;pce&quot;:         9100.1,
&quot;pop&quot;: 297647,
&quot;psavert&quot;:            3.7,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 7064 
},
{
 &quot;date&quot;: &quot;2006-02-01&quot;,
&quot;pce&quot;:         9134.7,
&quot;pop&quot;: 297854,
&quot;psavert&quot;:            3.8,
&quot;uempmed&quot;:            9.1,
&quot;unemploy&quot;: 7184 
},
{
 &quot;date&quot;: &quot;2006-03-01&quot;,
&quot;pce&quot;:         9168.1,
&quot;pop&quot;: 298060,
&quot;psavert&quot;:            3.7,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 7072 
},
{
 &quot;date&quot;: &quot;2006-04-01&quot;,
&quot;pce&quot;:         9223.3,
&quot;pop&quot;: 298281,
&quot;psavert&quot;:            3.4,
&quot;uempmed&quot;:            8.4,
&quot;unemploy&quot;: 7120 
},
{
 &quot;date&quot;: &quot;2006-05-01&quot;,
&quot;pce&quot;:         9254.1,
&quot;pop&quot;: 298496,
&quot;psavert&quot;:            3.2,
&quot;uempmed&quot;:            8.5,
&quot;unemploy&quot;: 6980 
},
{
 &quot;date&quot;: &quot;2006-06-01&quot;,
&quot;pce&quot;:         9283.8,
&quot;pop&quot;: 298739,
&quot;psavert&quot;:            3.4,
&quot;uempmed&quot;:            7.3,
&quot;unemploy&quot;: 7001 
},
{
 &quot;date&quot;: &quot;2006-07-01&quot;,
&quot;pce&quot;:         9360.4,
&quot;pop&quot;: 298996,
&quot;psavert&quot;:            2.9,
&quot;uempmed&quot;:              8,
&quot;unemploy&quot;: 7175 
},
{
 &quot;date&quot;: &quot;2006-08-01&quot;,
&quot;pce&quot;:         9368.6,
&quot;pop&quot;: 299263,
&quot;psavert&quot;:              3,
&quot;uempmed&quot;:            8.4,
&quot;unemploy&quot;: 7091 
},
{
 &quot;date&quot;: &quot;2006-09-01&quot;,
&quot;pce&quot;:         9393.9,
&quot;pop&quot;: 299554,
&quot;psavert&quot;:              3,
&quot;uempmed&quot;:              8,
&quot;unemploy&quot;: 6847 
},
{
 &quot;date&quot;: &quot;2006-10-01&quot;,
&quot;pce&quot;:         9413.3,
&quot;pop&quot;: 299835,
&quot;psavert&quot;:            3.1,
&quot;uempmed&quot;:            7.9,
&quot;unemploy&quot;: 6727 
},
{
 &quot;date&quot;: &quot;2006-11-01&quot;,
&quot;pce&quot;:         9431.2,
&quot;pop&quot;: 300094,
&quot;psavert&quot;:            3.2,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 6872 
},
{
 &quot;date&quot;: &quot;2006-12-01&quot;,
&quot;pce&quot;:         9516.5,
&quot;pop&quot;: 300340,
&quot;psavert&quot;:              3,
&quot;uempmed&quot;:            7.5,
&quot;unemploy&quot;: 6762 
},
{
 &quot;date&quot;: &quot;2007-01-01&quot;,
&quot;pce&quot;:         9553.1,
&quot;pop&quot;: 300574,
&quot;psavert&quot;:              3,
&quot;uempmed&quot;:            8.3,
&quot;unemploy&quot;: 7116 
},
{
 &quot;date&quot;: &quot;2007-02-01&quot;,
&quot;pce&quot;:         9590.8,
&quot;pop&quot;: 300802,
&quot;psavert&quot;:            3.3,
&quot;uempmed&quot;:            8.5,
&quot;unemploy&quot;: 6927 
},
{
 &quot;date&quot;: &quot;2007-03-01&quot;,
&quot;pce&quot;:         9631.6,
&quot;pop&quot;: 301021,
&quot;psavert&quot;:            3.6,
&quot;uempmed&quot;:            9.1,
&quot;unemploy&quot;: 6731 
},
{
 &quot;date&quot;: &quot;2007-04-01&quot;,
&quot;pce&quot;:         9670.6,
&quot;pop&quot;: 301254,
&quot;psavert&quot;:            3.2,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 6850 
},
{
 &quot;date&quot;: &quot;2007-05-01&quot;,
&quot;pce&quot;:         9708.9,
&quot;pop&quot;: 301483,
&quot;psavert&quot;:              3,
&quot;uempmed&quot;:            8.2,
&quot;unemploy&quot;: 6766 
},
{
 &quot;date&quot;: &quot;2007-06-01&quot;,
&quot;pce&quot;:         9723.3,
&quot;pop&quot;: 301739,
&quot;psavert&quot;:            2.8,
&quot;uempmed&quot;:            7.7,
&quot;unemploy&quot;: 6979 
},
{
 &quot;date&quot;: &quot;2007-07-01&quot;,
&quot;pce&quot;:         9759.6,
&quot;pop&quot;: 302004,
&quot;psavert&quot;:            2.8,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 7149 
},
{
 &quot;date&quot;: &quot;2007-08-01&quot;,
&quot;pce&quot;:         9800.6,
&quot;pop&quot;: 302267,
&quot;psavert&quot;:            2.6,
&quot;uempmed&quot;:            8.8,
&quot;unemploy&quot;: 7067 
},
{
 &quot;date&quot;: &quot;2007-09-01&quot;,
&quot;pce&quot;:         9837.5,
&quot;pop&quot;: 302546,
&quot;psavert&quot;:            2.8,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 7170 
},
{
 &quot;date&quot;: &quot;2007-10-01&quot;,
&quot;pce&quot;:         9853.9,
&quot;pop&quot;: 302807,
&quot;psavert&quot;:            2.8,
&quot;uempmed&quot;:            8.4,
&quot;unemploy&quot;: 7237 
},
{
 &quot;date&quot;: &quot;2007-11-01&quot;,
&quot;pce&quot;:         9928.6,
&quot;pop&quot;: 303054,
&quot;psavert&quot;:            2.5,
&quot;uempmed&quot;:            8.6,
&quot;unemploy&quot;: 7240 
},
{
 &quot;date&quot;: &quot;2007-12-01&quot;,
&quot;pce&quot;:         9947.6,
&quot;pop&quot;: 303287,
&quot;psavert&quot;:              3,
&quot;uempmed&quot;:            8.4,
&quot;unemploy&quot;: 7645 
},
{
 &quot;date&quot;: &quot;2008-01-01&quot;,
&quot;pce&quot;:         9963.2,
&quot;pop&quot;: 303506,
&quot;psavert&quot;:            3.4,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 7685 
},
{
 &quot;date&quot;: &quot;2008-02-01&quot;,
&quot;pce&quot;:         9955.7,
&quot;pop&quot;: 303711,
&quot;psavert&quot;:            3.9,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 7497 
},
{
 &quot;date&quot;: &quot;2008-03-01&quot;,
&quot;pce&quot;:        10004.2,
&quot;pop&quot;: 303907,
&quot;psavert&quot;:              4,
&quot;uempmed&quot;:            8.7,
&quot;unemploy&quot;: 7822 
},
{
 &quot;date&quot;: &quot;2008-04-01&quot;,
&quot;pce&quot;:        10044.6,
&quot;pop&quot;: 304117,
&quot;psavert&quot;:            3.5,
&quot;uempmed&quot;:            9.4,
&quot;unemploy&quot;: 7637 
},
{
 &quot;date&quot;: &quot;2008-05-01&quot;,
&quot;pce&quot;:        10093.3,
&quot;pop&quot;: 304323,
&quot;psavert&quot;:            7.9,
&quot;uempmed&quot;:            7.9,
&quot;unemploy&quot;: 8395 
},
{
 &quot;date&quot;: &quot;2008-06-01&quot;,
&quot;pce&quot;:        10149.4,
&quot;pop&quot;: 304556,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:              9,
&quot;unemploy&quot;: 8575 
},
{
 &quot;date&quot;: &quot;2008-07-01&quot;,
&quot;pce&quot;:        10151.1,
&quot;pop&quot;: 304798,
&quot;psavert&quot;:            4.4,
&quot;uempmed&quot;:            9.7,
&quot;unemploy&quot;: 8937 
},
{
 &quot;date&quot;: &quot;2008-08-01&quot;,
&quot;pce&quot;:        10140.3,
&quot;pop&quot;: 305045,
&quot;psavert&quot;:            3.7,
&quot;uempmed&quot;:            9.7,
&quot;unemploy&quot;: 9438 
},
{
 &quot;date&quot;: &quot;2008-09-01&quot;,
&quot;pce&quot;:        10083.2,
&quot;pop&quot;: 305309,
&quot;psavert&quot;:            4.4,
&quot;uempmed&quot;:           10.2,
&quot;unemploy&quot;: 9494 
},
{
 &quot;date&quot;: &quot;2008-10-01&quot;,
&quot;pce&quot;:         9983.3,
&quot;pop&quot;: 305554,
&quot;psavert&quot;:            5.4,
&quot;uempmed&quot;:           10.4,
&quot;unemploy&quot;: 10074 
},
{
 &quot;date&quot;: &quot;2008-11-01&quot;,
&quot;pce&quot;:         9851.2,
&quot;pop&quot;: 305786,
&quot;psavert&quot;:            6.3,
&quot;uempmed&quot;:            9.8,
&quot;unemploy&quot;: 10538 
},
{
 &quot;date&quot;: &quot;2008-12-01&quot;,
&quot;pce&quot;:         9744.2,
&quot;pop&quot;: 306004,
&quot;psavert&quot;:            6.5,
&quot;uempmed&quot;:           10.5,
&quot;unemploy&quot;: 11286 
},
{
 &quot;date&quot;: &quot;2009-01-01&quot;,
&quot;pce&quot;:         9792.1,
&quot;pop&quot;: 306208,
&quot;psavert&quot;:            6.5,
&quot;uempmed&quot;:           10.7,
&quot;unemploy&quot;: 12058 
},
{
 &quot;date&quot;: &quot;2009-02-01&quot;,
&quot;pce&quot;:         9775.7,
&quot;pop&quot;: 306402,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:           11.7,
&quot;unemploy&quot;: 12898 
},
{
 &quot;date&quot;: &quot;2009-03-01&quot;,
&quot;pce&quot;:         9742.9,
&quot;pop&quot;: 306588,
&quot;psavert&quot;:            6.1,
&quot;uempmed&quot;:           12.3,
&quot;unemploy&quot;: 13426 
},
{
 &quot;date&quot;: &quot;2009-04-01&quot;,
&quot;pce&quot;:         9741.9,
&quot;pop&quot;: 306787,
&quot;psavert&quot;:            6.7,
&quot;uempmed&quot;:           13.1,
&quot;unemploy&quot;: 13853 
},
{
 &quot;date&quot;: &quot;2009-05-01&quot;,
&quot;pce&quot;:         9759.7,
&quot;pop&quot;: 306984,
&quot;psavert&quot;:            8.1,
&quot;uempmed&quot;:           14.2,
&quot;unemploy&quot;: 14499 
},
{
 &quot;date&quot;: &quot;2009-06-01&quot;,
&quot;pce&quot;:         9807.6,
&quot;pop&quot;: 307206,
&quot;psavert&quot;:            6.7,
&quot;uempmed&quot;:           17.2,
&quot;unemploy&quot;: 14707 
},
{
 &quot;date&quot;: &quot;2009-07-01&quot;,
&quot;pce&quot;:         9835.2,
&quot;pop&quot;: 307439,
&quot;psavert&quot;:              6,
&quot;uempmed&quot;:             16,
&quot;unemploy&quot;: 14601 
},
{
 &quot;date&quot;: &quot;2009-08-01&quot;,
&quot;pce&quot;:         9961.9,
&quot;pop&quot;: 307685,
&quot;psavert&quot;:            4.9,
&quot;uempmed&quot;:           16.3,
&quot;unemploy&quot;: 14814 
},
{
 &quot;date&quot;: &quot;2009-09-01&quot;,
&quot;pce&quot;:         9875.4,
&quot;pop&quot;: 307946,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:           17.8,
&quot;unemploy&quot;: 15009 
},
{
 &quot;date&quot;: &quot;2009-10-01&quot;,
&quot;pce&quot;:         9924.6,
&quot;pop&quot;: 308189,
&quot;psavert&quot;:            5.4,
&quot;uempmed&quot;:           18.9,
&quot;unemploy&quot;: 15352 
},
{
 &quot;date&quot;: &quot;2009-11-01&quot;,
&quot;pce&quot;:         9946.1,
&quot;pop&quot;: 308418,
&quot;psavert&quot;:            5.7,
&quot;uempmed&quot;:           19.8,
&quot;unemploy&quot;: 15219 
},
{
 &quot;date&quot;: &quot;2009-12-01&quot;,
&quot;pce&quot;:        10000.6,
&quot;pop&quot;: 308633,
&quot;psavert&quot;:            5.7,
&quot;uempmed&quot;:           20.1,
&quot;unemploy&quot;: 15098 
},
{
 &quot;date&quot;: &quot;2010-01-01&quot;,
&quot;pce&quot;:        10003.4,
&quot;pop&quot;: 308833,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:             20,
&quot;unemploy&quot;: 15046 
},
{
 &quot;date&quot;: &quot;2010-02-01&quot;,
&quot;pce&quot;:        10034.7,
&quot;pop&quot;: 309027,
&quot;psavert&quot;:            5.2,
&quot;uempmed&quot;:           19.9,
&quot;unemploy&quot;: 15113 
},
{
 &quot;date&quot;: &quot;2010-03-01&quot;,
&quot;pce&quot;:        10095.5,
&quot;pop&quot;: 309212,
&quot;psavert&quot;:              5,
&quot;uempmed&quot;:           20.4,
&quot;unemploy&quot;: 15202 
},
{
 &quot;date&quot;: &quot;2010-04-01&quot;,
&quot;pce&quot;:        10106.9,
&quot;pop&quot;: 309191,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:           22.1,
&quot;unemploy&quot;: 15325 
},
{
 &quot;date&quot;: &quot;2010-05-01&quot;,
&quot;pce&quot;:        10140.2,
&quot;pop&quot;: 309376,
&quot;psavert&quot;:              6,
&quot;uempmed&quot;:           22.3,
&quot;unemploy&quot;: 14849 
},
{
 &quot;date&quot;: &quot;2010-06-01&quot;,
&quot;pce&quot;:        10165.9,
&quot;pop&quot;: 309562,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:           25.2,
&quot;unemploy&quot;: 14474 
},
{
 &quot;date&quot;: &quot;2010-07-01&quot;,
&quot;pce&quot;:        10184.3,
&quot;pop&quot;: 309767,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:           22.3,
&quot;unemploy&quot;: 14512 
},
{
 &quot;date&quot;: &quot;2010-08-01&quot;,
&quot;pce&quot;:        10247.1,
&quot;pop&quot;: 309989,
&quot;psavert&quot;:            5.8,
&quot;uempmed&quot;:             21,
&quot;unemploy&quot;: 14648 
},
{
 &quot;date&quot;: &quot;2010-09-01&quot;,
&quot;pce&quot;:        10268.9,
&quot;pop&quot;: 310218,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:           20.3,
&quot;unemploy&quot;: 14579 
},
{
 &quot;date&quot;: &quot;2010-10-01&quot;,
&quot;pce&quot;:        10343.7,
&quot;pop&quot;: 310451,
&quot;psavert&quot;:            5.4,
&quot;uempmed&quot;:           21.2,
&quot;unemploy&quot;: 14516 
},
{
 &quot;date&quot;: &quot;2010-11-01&quot;,
&quot;pce&quot;:        10399.8,
&quot;pop&quot;: 310657,
&quot;psavert&quot;:            5.3,
&quot;uempmed&quot;:             21,
&quot;unemploy&quot;: 15081 
},
{
 &quot;date&quot;: &quot;2010-12-01&quot;,
&quot;pce&quot;:        10436.1,
&quot;pop&quot;: 310853,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:           21.9,
&quot;unemploy&quot;: 14348 
},
{
 &quot;date&quot;: &quot;2011-01-01&quot;,
&quot;pce&quot;:        10474.7,
&quot;pop&quot;: 311042,
&quot;psavert&quot;:            6.2,
&quot;uempmed&quot;:           21.6,
&quot;unemploy&quot;: 14046 
},
{
 &quot;date&quot;: &quot;2011-02-01&quot;,
&quot;pce&quot;:        10512.4,
&quot;pop&quot;: 311205,
&quot;psavert&quot;:            6.4,
&quot;uempmed&quot;:           21.1,
&quot;unemploy&quot;: 13828 
},
{
 &quot;date&quot;: &quot;2011-03-01&quot;,
&quot;pce&quot;:        10583.5,
&quot;pop&quot;: 311367,
&quot;psavert&quot;:              6,
&quot;uempmed&quot;:           21.5,
&quot;unemploy&quot;: 13728 
},
{
 &quot;date&quot;: &quot;2011-04-01&quot;,
&quot;pce&quot;:        10624.6,
&quot;pop&quot;: 311548,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:           20.9,
&quot;unemploy&quot;: 13956 
},
{
 &quot;date&quot;: &quot;2011-05-01&quot;,
&quot;pce&quot;:        10653.1,
&quot;pop&quot;: 311729,
&quot;psavert&quot;:            5.9,
&quot;uempmed&quot;:           21.6,
&quot;unemploy&quot;: 13853 
},
{
 &quot;date&quot;: &quot;2011-06-01&quot;,
&quot;pce&quot;:        10676.4,
&quot;pop&quot;: 311923,
&quot;psavert&quot;:            6.1,
&quot;uempmed&quot;:           22.3,
&quot;unemploy&quot;: 13958 
},
{
 &quot;date&quot;: &quot;2011-07-01&quot;,
&quot;pce&quot;:        10727.1,
&quot;pop&quot;: 312139,
&quot;psavert&quot;:            6.3,
&quot;uempmed&quot;:             22,
&quot;unemploy&quot;: 13756 
},
{
 &quot;date&quot;: &quot;2011-08-01&quot;,
&quot;pce&quot;:        10745.6,
&quot;pop&quot;: 312355,
&quot;psavert&quot;:            6.2,
&quot;uempmed&quot;:           22.4,
&quot;unemploy&quot;: 13806 
},
{
 &quot;date&quot;: &quot;2011-09-01&quot;,
&quot;pce&quot;:        10790.6,
&quot;pop&quot;: 312587,
&quot;psavert&quot;:            5.7,
&quot;uempmed&quot;:             22,
&quot;unemploy&quot;: 13929 
},
{
 &quot;date&quot;: &quot;2011-10-01&quot;,
&quot;pce&quot;:        10827.6,
&quot;pop&quot;: 312810,
&quot;psavert&quot;:            5.5,
&quot;uempmed&quot;:           20.5,
&quot;unemploy&quot;: 13599 
},
{
 &quot;date&quot;: &quot;2011-11-01&quot;,
&quot;pce&quot;:        10828.7,
&quot;pop&quot;: 313003,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:           20.9,
&quot;unemploy&quot;: 13309 
},
{
 &quot;date&quot;: &quot;2011-12-01&quot;,
&quot;pce&quot;:        10827.3,
&quot;pop&quot;: 313191,
&quot;psavert&quot;:            6.4,
&quot;uempmed&quot;:           20.5,
&quot;unemploy&quot;: 13071 
},
{
 &quot;date&quot;: &quot;2012-01-01&quot;,
&quot;pce&quot;:        10905.5,
&quot;pop&quot;: 313373,
&quot;psavert&quot;:            6.6,
&quot;uempmed&quot;:             21,
&quot;unemploy&quot;: 12812 
},
{
 &quot;date&quot;: &quot;2012-02-01&quot;,
&quot;pce&quot;:        10979.2,
&quot;pop&quot;: 313537,
&quot;psavert&quot;:            6.7,
&quot;uempmed&quot;:           19.8,
&quot;unemploy&quot;: 12828 
},
{
 &quot;date&quot;: &quot;2012-03-01&quot;,
&quot;pce&quot;:        10994.3,
&quot;pop&quot;: 313705,
&quot;psavert&quot;:            6.9,
&quot;uempmed&quot;:           19.2,
&quot;unemploy&quot;: 12696 
},
{
 &quot;date&quot;: &quot;2012-04-01&quot;,
&quot;pce&quot;:        11030.2,
&quot;pop&quot;: 313881,
&quot;psavert&quot;:              7,
&quot;uempmed&quot;:           19.1,
&quot;unemploy&quot;: 12636 
},
{
 &quot;date&quot;: &quot;2012-05-01&quot;,
&quot;pce&quot;:          11029,
&quot;pop&quot;: 314052,
&quot;psavert&quot;:              7,
&quot;uempmed&quot;:           19.9,
&quot;unemploy&quot;: 12668 
},
{
 &quot;date&quot;: &quot;2012-06-01&quot;,
&quot;pce&quot;:        11032.5,
&quot;pop&quot;: 314247,
&quot;psavert&quot;:            7.1,
&quot;uempmed&quot;:           20.1,
&quot;unemploy&quot;: 12688 
},
{
 &quot;date&quot;: &quot;2012-07-01&quot;,
&quot;pce&quot;:        11074.8,
&quot;pop&quot;: 314449,
&quot;psavert&quot;:            6.6,
&quot;uempmed&quot;:           17.5,
&quot;unemploy&quot;: 12657 
},
{
 &quot;date&quot;: &quot;2012-08-01&quot;,
&quot;pce&quot;:        11104.8,
&quot;pop&quot;: 314673,
&quot;psavert&quot;:            6.4,
&quot;uempmed&quot;:           18.5,
&quot;unemploy&quot;: 12449 
},
{
 &quot;date&quot;: &quot;2012-09-01&quot;,
&quot;pce&quot;:        11179.6,
&quot;pop&quot;: 314909,
&quot;psavert&quot;:            6.5,
&quot;uempmed&quot;:           18.8,
&quot;unemploy&quot;: 12106 
},
{
 &quot;date&quot;: &quot;2012-10-01&quot;,
&quot;pce&quot;:        11199.9,
&quot;pop&quot;: 315129,
&quot;psavert&quot;:            7.1,
&quot;uempmed&quot;:           19.7,
&quot;unemploy&quot;: 12141 
},
{
 &quot;date&quot;: &quot;2012-11-01&quot;,
&quot;pce&quot;:        11222.8,
&quot;pop&quot;: 315341,
&quot;psavert&quot;:            8.2,
&quot;uempmed&quot;:           18.5,
&quot;unemploy&quot;: 12026 
},
{
 &quot;date&quot;: &quot;2012-12-01&quot;,
&quot;pce&quot;:        11245.2,
&quot;pop&quot;: 315532,
&quot;psavert&quot;:           10.5,
&quot;uempmed&quot;:           17.6,
&quot;unemploy&quot;: 12272 
},
{
 &quot;date&quot;: &quot;2013-01-01&quot;,
&quot;pce&quot;:        11303.2,
&quot;pop&quot;: 315701,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:           16.2,
&quot;unemploy&quot;: 12497 
},
{
 &quot;date&quot;: &quot;2013-02-01&quot;,
&quot;pce&quot;:        11371.4,
&quot;pop&quot;: 315869,
&quot;psavert&quot;:            4.7,
&quot;uempmed&quot;:           17.5,
&quot;unemploy&quot;: 11967 
},
{
 &quot;date&quot;: &quot;2013-03-01&quot;,
&quot;pce&quot;:        11378.8,
&quot;pop&quot;: 316041,
&quot;psavert&quot;:            4.9,
&quot;uempmed&quot;:           17.7,
&quot;unemploy&quot;: 11653 
},
{
 &quot;date&quot;: &quot;2013-04-01&quot;,
&quot;pce&quot;:        11373.3,
&quot;pop&quot;: 316220,
&quot;psavert&quot;:            5.1,
&quot;uempmed&quot;:           17.1,
&quot;unemploy&quot;: 11735 
},
{
 &quot;date&quot;: &quot;2013-05-01&quot;,
&quot;pce&quot;:        11407.1,
&quot;pop&quot;: 316395,
&quot;psavert&quot;:            5.2,
&quot;uempmed&quot;:             17,
&quot;unemploy&quot;: 11671 
},
{
 &quot;date&quot;: &quot;2013-06-01&quot;,
&quot;pce&quot;:        11462.4,
&quot;pop&quot;: 316594,
&quot;psavert&quot;:            5.3,
&quot;uempmed&quot;:           16.6,
&quot;unemploy&quot;: 11736 
},
{
 &quot;date&quot;: &quot;2013-07-01&quot;,
&quot;pce&quot;:        11484.7,
&quot;pop&quot;: 316799,
&quot;psavert&quot;:            5.1,
&quot;uempmed&quot;:           16.3,
&quot;unemploy&quot;: 11357 
},
{
 &quot;date&quot;: &quot;2013-08-01&quot;,
&quot;pce&quot;:        11511.6,
&quot;pop&quot;: 317019,
&quot;psavert&quot;:            5.3,
&quot;uempmed&quot;:           16.8,
&quot;unemploy&quot;: 11241 
},
{
 &quot;date&quot;: &quot;2013-09-01&quot;,
&quot;pce&quot;:        11559.6,
&quot;pop&quot;: 317253,
&quot;psavert&quot;:            5.2,
&quot;uempmed&quot;:           16.5,
&quot;unemploy&quot;: 11251 
},
{
 &quot;date&quot;: &quot;2013-10-01&quot;,
&quot;pce&quot;:        11602.1,
&quot;pop&quot;: 317470,
&quot;psavert&quot;:            4.7,
&quot;uempmed&quot;:           16.1,
&quot;unemploy&quot;: 11161 
},
{
 &quot;date&quot;: &quot;2013-11-01&quot;,
&quot;pce&quot;:        11671.5,
&quot;pop&quot;: 317679,
&quot;psavert&quot;:            4.3,
&quot;uempmed&quot;:             17,
&quot;unemploy&quot;: 10814 
},
{
 &quot;date&quot;: &quot;2013-12-01&quot;,
&quot;pce&quot;:        11686.3,
&quot;pop&quot;: 317867,
&quot;psavert&quot;:            4.1,
&quot;uempmed&quot;:             17,
&quot;unemploy&quot;: 10376 
},
{
 &quot;date&quot;: &quot;2014-01-01&quot;,
&quot;pce&quot;:        11663.9,
&quot;pop&quot;: 318032,
&quot;psavert&quot;:            4.9,
&quot;uempmed&quot;:           15.9,
&quot;unemploy&quot;: 10280 
},
{
 &quot;date&quot;: &quot;2014-02-01&quot;,
&quot;pce&quot;:        11714.4,
&quot;pop&quot;: 318200,
&quot;psavert&quot;:              5,
&quot;uempmed&quot;:           16.2,
&quot;unemploy&quot;: 10387 
},
{
 &quot;date&quot;: &quot;2014-03-01&quot;,
&quot;pce&quot;:        11807.1,
&quot;pop&quot;: 318373,
&quot;psavert&quot;:            4.8,
&quot;uempmed&quot;:           15.9,
&quot;unemploy&quot;: 10384 
},
{
 &quot;date&quot;: &quot;2014-04-01&quot;,
&quot;pce&quot;:        11825.2,
&quot;pop&quot;: 318552,
&quot;psavert&quot;:              5,
&quot;uempmed&quot;:           15.6,
&quot;unemploy&quot;: 9696 
},
{
 &quot;date&quot;: &quot;2014-05-01&quot;,
&quot;pce&quot;:        11864.3,
&quot;pop&quot;: 318728,
&quot;psavert&quot;:            5.1,
&quot;uempmed&quot;:           14.5,
&quot;unemploy&quot;: 9761 
},
{
 &quot;date&quot;: &quot;2014-06-01&quot;,
&quot;pce&quot;:        11922.6,
&quot;pop&quot;: 318927,
&quot;psavert&quot;:            5.1,
&quot;uempmed&quot;:           13.2,
&quot;unemploy&quot;: 9453 
},
{
 &quot;date&quot;: &quot;2014-07-01&quot;,
&quot;pce&quot;:        11944.4,
&quot;pop&quot;: 319133,
&quot;psavert&quot;:            5.1,
&quot;uempmed&quot;:           13.5,
&quot;unemploy&quot;: 9648 
},
{
 &quot;date&quot;: &quot;2014-08-01&quot;,
&quot;pce&quot;:          12017,
&quot;pop&quot;: 319354,
&quot;psavert&quot;:            4.7,
&quot;uempmed&quot;:           13.3,
&quot;unemploy&quot;: 9568 
},
{
 &quot;date&quot;: &quot;2014-09-01&quot;,
&quot;pce&quot;:        12044.6,
&quot;pop&quot;: 319588,
&quot;psavert&quot;:            4.6,
&quot;uempmed&quot;:           13.3,
&quot;unemploy&quot;: 9237 
},
{
 &quot;date&quot;: &quot;2014-10-01&quot;,
&quot;pce&quot;:        12096.4,
&quot;pop&quot;: 319804,
&quot;psavert&quot;:            4.6,
&quot;uempmed&quot;:           13.5,
&quot;unemploy&quot;: 8983 
},
{
 &quot;date&quot;: &quot;2014-11-01&quot;,
&quot;pce&quot;:        12142.2,
&quot;pop&quot;: 320013,
&quot;psavert&quot;:            4.5,
&quot;uempmed&quot;:           12.8,
&quot;unemploy&quot;: 9071 
},
{
 &quot;date&quot;: &quot;2014-12-01&quot;,
&quot;pce&quot;:          12122,
&quot;pop&quot;: 320201,
&quot;psavert&quot;:              5,
&quot;uempmed&quot;:           12.6,
&quot;unemploy&quot;: 8688 
},
{
 &quot;date&quot;: &quot;2015-01-01&quot;,
&quot;pce&quot;:        12080.8,
&quot;pop&quot;: 320367,
&quot;psavert&quot;:            5.5,
&quot;uempmed&quot;:           13.4,
&quot;unemploy&quot;: 8979 
},
{
 &quot;date&quot;: &quot;2015-02-01&quot;,
&quot;pce&quot;:        12095.9,
&quot;pop&quot;: 320534,
&quot;psavert&quot;:            5.7,
&quot;uempmed&quot;:           13.1,
&quot;unemploy&quot;: 8705 
},
{
 &quot;date&quot;: &quot;2015-03-01&quot;,
&quot;pce&quot;:        12161.5,
&quot;pop&quot;: 320707,
&quot;psavert&quot;:            5.2,
&quot;uempmed&quot;:           12.2,
&quot;unemploy&quot;: 8575 
},
{
 &quot;date&quot;: &quot;2015-04-01&quot;,
&quot;pce&quot;:        12158.9,
&quot;pop&quot;: 320887,
&quot;psavert&quot;:            5.6,
&quot;uempmed&quot;:           11.7,
&quot;unemploy&quot;: 8549 
} 
],
&quot;pointSize&quot;:              0,
&quot;lineWidth&quot;:              1,
&quot;id&quot;: &quot;chartfb02ecf686a&quot;,
&quot;labels&quot;: [ &quot;psavert&quot;, &quot;uempmed&quot; ] 
},
      chartType = &quot;Line&quot;
    new Morris[chartType](chartParams)
&lt;/script&gt;
    
    &lt;script&gt;&lt;/script&gt;    
  &lt;/body&gt;
&lt;/html&gt; ' scrolling='no' frameBorder='0' seamless class='rChart  morris  ' id='iframe-chartfb02ecf686a'> </iframe>
 <style>iframe.rChart{ width: 100%; height: 400px;}</style>

# NVD3 Plot Iframe

<iframe srcdoc=' &lt;!doctype HTML&gt;
&lt;meta charset = &#039;utf-8&#039;&gt;
&lt;html&gt;
  &lt;head&gt;
    
    &lt;script src=&#039;http://ramnathv.github.io/rCharts/libraries/widgets/polycharts/js/polychart2.standalone.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    &lt;style&gt;
    .rChart {
      display: block;
      margin-left: auto; 
      margin-right: auto;
      width: 800px;
      height: 400px;
    }  
    &lt;/style&gt;
    
  &lt;/head&gt;
  &lt;body &gt;
    
    &lt;div id = &#039;chartfb0c622ba&#039; class = &#039;rChart polycharts&#039;&gt;&lt;/div&gt;    
    &lt;script type=&#039;text/javascript&#039;&gt;
    var chartParams = {
 &quot;dom&quot;: &quot;chartfb0c622ba&quot;,
&quot;width&quot;:    800,
&quot;height&quot;:    400,
&quot;layers&quot;: [
 {
 &quot;x&quot;: &quot;wt&quot;,
&quot;y&quot;: &quot;mpg&quot;,
&quot;data&quot;: {
 &quot;mpg&quot;: [     21,     21,   22.8,   21.4,   18.7,   18.1,   14.3,   24.4,   22.8,   19.2,   17.8,   16.4,   17.3,   15.2,   10.4,   10.4,   14.7,   32.4,   30.4,   33.9,   21.5,   15.5,   15.2,   13.3,   19.2,   27.3,     26,   30.4,   15.8,   19.7,     15,   21.4 ],
&quot;cyl&quot;: [      6,      6,      4,      6,      8,      6,      8,      4,      4,      6,      6,      8,      8,      8,      8,      8,      8,      4,      4,      4,      4,      8,      8,      8,      8,      4,      4,      4,      8,      6,      8,      4 ],
&quot;disp&quot;: [    160,    160,    108,    258,    360,    225,    360,  146.7,  140.8,  167.6,  167.6,  275.8,  275.8,  275.8,    472,    460,    440,   78.7,   75.7,   71.1,  120.1,    318,    304,    350,    400,     79,  120.3,   95.1,    351,    145,    301,    121 ],
&quot;hp&quot;: [    110,    110,     93,    110,    175,    105,    245,     62,     95,    123,    123,    180,    180,    180,    205,    215,    230,     66,     52,     65,     97,    150,    150,    245,    175,     66,     91,    113,    264,    175,    335,    109 ],
&quot;drat&quot;: [    3.9,    3.9,   3.85,   3.08,   3.15,   2.76,   3.21,   3.69,   3.92,   3.92,   3.92,   3.07,   3.07,   3.07,   2.93,      3,   3.23,   4.08,   4.93,   4.22,    3.7,   2.76,   3.15,   3.73,   3.08,   4.08,   4.43,   3.77,   4.22,   3.62,   3.54,   4.11 ],
&quot;wt&quot;: [   2.62,  2.875,   2.32,  3.215,   3.44,   3.46,   3.57,   3.19,   3.15,   3.44,   3.44,   4.07,   3.73,   3.78,   5.25,  5.424,  5.345,    2.2,  1.615,  1.835,  2.465,   3.52,  3.435,   3.84,  3.845,  1.935,   2.14,  1.513,   3.17,   2.77,   3.57,   2.78 ],
&quot;qsec&quot;: [  16.46,  17.02,  18.61,  19.44,  17.02,  20.22,  15.84,     20,   22.9,   18.3,   18.9,   17.4,   17.6,     18,  17.98,  17.82,  17.42,  19.47,  18.52,   19.9,  20.01,  16.87,   17.3,  15.41,  17.05,   18.9,   16.7,   16.9,   14.5,   15.5,   14.6,   18.6 ],
&quot;vs&quot;: [      0,      0,      1,      1,      0,      1,      0,      1,      1,      1,      1,      0,      0,      0,      0,      0,      0,      1,      1,      1,      1,      0,      0,      0,      0,      1,      0,      1,      0,      0,      0,      1 ],
&quot;am&quot;: [      1,      1,      1,      0,      0,      0,      0,      0,      0,      0,      0,      0,      0,      0,      0,      0,      0,      1,      1,      1,      0,      0,      0,      0,      0,      1,      1,      1,      1,      1,      1,      1 ],
&quot;gear&quot;: [      4,      4,      4,      3,      3,      3,      3,      4,      4,      4,      4,      3,      3,      3,      3,      3,      3,      4,      4,      4,      3,      3,      3,      3,      3,      4,      5,      5,      5,      5,      5,      4 ],
&quot;carb&quot;: [      4,      4,      1,      1,      2,      1,      4,      2,      2,      4,      4,      3,      3,      3,      4,      4,      4,      1,      2,      1,      1,      2,      2,      4,      2,      1,      2,      2,      4,      6,      8,      2 ] 
},
&quot;facet&quot;: &quot;cyl&quot;,
&quot;color&quot;: &quot;gear&quot;,
&quot;type&quot;: &quot;point&quot; 
} 
],
&quot;facet&quot;: {
 &quot;type&quot;: &quot;wrap&quot;,
&quot;var&quot;: &quot;cyl&quot; 
},
&quot;guides&quot;: [],
&quot;coord&quot;: [],
&quot;id&quot;: &quot;chartfb0c622ba&quot; 
}
    _.each(chartParams.layers, function(el){
        el.data = polyjs.data(el.data)
    })
    var graph_chartfb0c622ba = polyjs.chart(chartParams);
&lt;/script&gt;
    
    &lt;script&gt;&lt;/script&gt;    
  &lt;/body&gt;
&lt;/html&gt; ' scrolling='no' frameBorder='0' seamless class='rChart  polycharts  ' id='iframe-chartfb0c622ba'> </iframe>
 <style>iframe.rChart{ width: 100%; height: 400px;}</style>

# DataTable

<!-- html table generated in R 3.2.3 by xtable 1.8-0 package -->
<!-- Sun May 22 13:33:40 2016 -->
<table border=1>
<tr> <th> Sepal.Length </th> <th> Sepal.Width </th> <th> Petal.Length </th> <th> Petal.Width </th> <th> Species </th>  </tr>
  <tr> <td align="right"> 5.10 </td> <td align="right"> 3.50 </td> <td align="right"> 1.40 </td> <td align="right"> 0.20 </td> <td> setosa </td> </tr>
  <tr> <td align="right"> 4.90 </td> <td align="right"> 3.00 </td> <td align="right"> 1.40 </td> <td align="right"> 0.20 </td> <td> setosa </td> </tr>
  <tr> <td align="right"> 4.70 </td> <td align="right"> 3.20 </td> <td align="right"> 1.30 </td> <td align="right"> 0.20 </td> <td> setosa </td> </tr>
  <tr> <td align="right"> 4.60 </td> <td align="right"> 3.10 </td> <td align="right"> 1.50 </td> <td align="right"> 0.20 </td> <td> setosa </td> </tr>
  <tr> <td align="right"> 5.00 </td> <td align="right"> 3.60 </td> <td align="right"> 1.40 </td> <td align="right"> 0.20 </td> <td> setosa </td> </tr>
  <tr> <td align="right"> 5.40 </td> <td align="right"> 3.90 </td> <td align="right"> 1.70 </td> <td align="right"> 0.40 </td> <td> setosa </td> </tr>
  <tr> <td align="right"> 4.60 </td> <td align="right"> 3.40 </td> <td align="right"> 1.40 </td> <td align="right"> 0.30 </td> <td> setosa </td> </tr>
  <tr> <td align="right"> 5.00 </td> <td align="right"> 3.40 </td> <td align="right"> 1.50 </td> <td align="right"> 0.20 </td> <td> setosa </td> </tr>
  <tr> <td align="right"> 4.40 </td> <td align="right"> 2.90 </td> <td align="right"> 1.40 </td> <td align="right"> 0.20 </td> <td> setosa </td> </tr>
  <tr> <td align="right"> 4.90 </td> <td align="right"> 3.10 </td> <td align="right"> 1.50 </td> <td align="right"> 0.10 </td> <td> setosa </td> </tr>
   </table>
<!--html_preserve--><div id="htmlwidget-7652" style="width:100%;height:auto;" class="datatables"></div>
<script type="application/json" data-for="htmlwidget-7652">{"x":{"data":[["Mazda RX4","Mazda RX4 Wag","Datsun 710","Hornet 4 Drive","Hornet Sportabout","Valiant","Duster 360","Merc 240D","Merc 230","Merc 280","Merc 280C","Merc 450SE","Merc 450SL","Merc 450SLC","Cadillac Fleetwood","Lincoln Continental","Chrysler Imperial","Fiat 128","Honda Civic","Toyota Corolla","Toyota Corona","Dodge Challenger","AMC Javelin","Camaro Z28","Pontiac Firebird","Fiat X1-9","Porsche 914-2","Lotus Europa","Ford Pantera L","Ferrari Dino","Maserati Bora","Volvo 142E"],[21,21,22.8,21.4,18.7,18.1,14.3,24.4,22.8,19.2,17.8,16.4,17.3,15.2,10.4,10.4,14.7,32.4,30.4,33.9,21.5,15.5,15.2,13.3,19.2,27.3,26,30.4,15.8,19.7,15,21.4],[6,6,4,6,8,6,8,4,4,6,6,8,8,8,8,8,8,4,4,4,4,8,8,8,8,4,4,4,8,6,8,4],[160,160,108,258,360,225,360,146.7,140.8,167.6,167.6,275.8,275.8,275.8,472,460,440,78.7,75.7,71.1,120.1,318,304,350,400,79,120.3,95.1,351,145,301,121],[110,110,93,110,175,105,245,62,95,123,123,180,180,180,205,215,230,66,52,65,97,150,150,245,175,66,91,113,264,175,335,109],[3.9,3.9,3.85,3.08,3.15,2.76,3.21,3.69,3.92,3.92,3.92,3.07,3.07,3.07,2.93,3,3.23,4.08,4.93,4.22,3.7,2.76,3.15,3.73,3.08,4.08,4.43,3.77,4.22,3.62,3.54,4.11],[2.62,2.875,2.32,3.215,3.44,3.46,3.57,3.19,3.15,3.44,3.44,4.07,3.73,3.78,5.25,5.424,5.345,2.2,1.615,1.835,2.465,3.52,3.435,3.84,3.845,1.935,2.14,1.513,3.17,2.77,3.57,2.78],[16.46,17.02,18.61,19.44,17.02,20.22,15.84,20,22.9,18.3,18.9,17.4,17.6,18,17.98,17.82,17.42,19.47,18.52,19.9,20.01,16.87,17.3,15.41,17.05,18.9,16.7,16.9,14.5,15.5,14.6,18.6],[0,0,1,1,0,1,0,1,1,1,1,0,0,0,0,0,0,1,1,1,1,0,0,0,0,1,0,1,0,0,0,1],[1,1,1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1,1,1,0,0,0,0,0,1,1,1,1,1,1,1],[4,4,4,3,3,3,3,4,4,4,4,3,3,3,3,3,3,4,4,4,3,3,3,3,3,4,5,5,5,5,5,4],[4,4,1,1,2,1,4,2,2,4,4,3,3,3,4,4,4,1,2,1,1,2,2,4,2,1,2,2,4,6,8,2]],"container":"<table class=\"display\">\n  <thead>\n    <tr>\n      <th> </th>\n      <th>mpg</th>\n      <th>cyl</th>\n      <th>disp</th>\n      <th>hp</th>\n      <th>drat</th>\n      <th>wt</th>\n      <th>qsec</th>\n      <th>vs</th>\n      <th>am</th>\n      <th>gear</th>\n      <th>carb</th>\n    </tr>\n  </thead>\n</table>","options":{"columnDefs":[{"className":"dt-right","targets":[1,2,3,4,5,6,7,8,9,10,11]},{"orderable":false,"targets":0}],"order":[],"autoWidth":false,"orderClasses":false},"callback":null,"filter":"none"},"evals":[]}</script><!--/html_preserve-->

<!-- html table generated in R 3.2.3 by xtable 1.8-0 package -->
<!-- Sun May 22 13:33:41 2016 -->
<table border=1>
<caption align="bottom"> A sideways table </caption>
<tr> <th>  </th> <th> 1 </th> <th> 2 </th> <th> 3 </th> <th> 4 </th> <th> 5 </th> <th> 6 </th> <th> 7 </th> <th> 8 </th> <th> 9 </th> <th> 10 </th>  </tr>
  <tr> <td align="right"> 1 </td> <td align="right"> 0.14 </td> <td align="right"> 0.43 </td> <td align="right"> -0.89 </td> <td align="right"> 1.65 </td> <td align="right"> 0.28 </td> <td align="right"> -0.52 </td> <td align="right"> 0.90 </td> <td align="right"> -0.93 </td> <td align="right"> 0.11 </td> <td align="right"> -0.65 </td> </tr>
  <tr> <td align="right"> 2 </td> <td align="right"> -0.27 </td> <td align="right"> 1.31 </td> <td align="right"> 0.34 </td> <td align="right"> -1.17 </td> <td align="right"> 0.09 </td> <td align="right"> 0.06 </td> <td align="right"> 1.92 </td> <td align="right"> 0.60 </td> <td align="right"> -0.01 </td> <td align="right"> 0.72 </td> </tr>
  <tr> <td align="right"> 3 </td> <td align="right"> 0.01 </td> <td align="right"> 0.38 </td> <td align="right"> 0.34 </td> <td align="right"> -0.07 </td> <td align="right"> 0.66 </td> <td align="right"> 0.30 </td> <td align="right"> -2.05 </td> <td align="right"> -0.57 </td> <td align="right"> -0.62 </td> <td align="right"> 0.89 </td> </tr>
  <tr> <td align="right"> 4 </td> <td align="right"> 1.24 </td> <td align="right"> 1.49 </td> <td align="right"> 0.58 </td> <td align="right"> -1.21 </td> <td align="right"> -3.27 </td> <td align="right"> 0.22 </td> <td align="right"> -0.60 </td> <td align="right"> -0.57 </td> <td align="right"> 1.37 </td> <td align="right"> 0.71 </td> </tr>
  <tr> <td align="right"> 5 </td> <td align="right"> -0.95 </td> <td align="right"> 0.75 </td> <td align="right"> 0.72 </td> <td align="right"> -2.23 </td> <td align="right"> -1.52 </td> <td align="right"> -0.35 </td> <td align="right"> 0.33 </td> <td align="right"> -0.30 </td> <td align="right"> 1.43 </td> <td align="right"> 0.08 </td> </tr>
  <tr> <td align="right"> 6 </td> <td align="right"> 0.96 </td> <td align="right"> 0.08 </td> <td align="right"> 0.14 </td> <td align="right"> -1.14 </td> <td align="right"> -0.46 </td> <td align="right"> 1.75 </td> <td align="right"> 1.24 </td> <td align="right"> 0.58 </td> <td align="right"> -0.50 </td> <td align="right"> 0.14 </td> </tr>
  <tr> <td align="right"> 7 </td> <td align="right"> -1.16 </td> <td align="right"> 1.14 </td> <td align="right"> 2.30 </td> <td align="right"> -0.11 </td> <td align="right"> 0.15 </td> <td align="right"> 1.33 </td> <td align="right"> 2.45 </td> <td align="right"> 0.45 </td> <td align="right"> 0.78 </td> <td align="right"> -0.37 </td> </tr>
  <tr> <td align="right"> 8 </td> <td align="right"> 0.85 </td> <td align="right"> 0.99 </td> <td align="right"> 0.86 </td> <td align="right"> 0.60 </td> <td align="right"> -0.82 </td> <td align="right"> -0.01 </td> <td align="right"> 0.02 </td> <td align="right"> 0.65 </td> <td align="right"> -1.01 </td> <td align="right"> -0.91 </td> </tr>
  <tr> <td align="right"> 9 </td> <td align="right"> -0.32 </td> <td align="right"> 2.19 </td> <td align="right"> -0.86 </td> <td align="right"> -0.67 </td> <td align="right"> -0.46 </td> <td align="right"> 0.20 </td> <td align="right"> -0.54 </td> <td align="right"> 0.05 </td> <td align="right"> -0.39 </td> <td align="right"> -1.61 </td> </tr>
  <tr> <td align="right"> 10 </td> <td align="right"> -1.16 </td> <td align="right"> 0.09 </td> <td align="right"> -1.53 </td> <td align="right"> 0.03 </td> <td align="right"> 1.47 </td> <td align="right"> -0.55 </td> <td align="right"> 0.14 </td> <td align="right"> 0.39 </td> <td align="right"> 1.44 </td> <td align="right"> -1.57 </td> </tr>
  <tr> <td align="right"> 11 </td> <td align="right"> -1.12 </td> <td align="right"> -0.17 </td> <td align="right"> 0.15 </td> <td align="right"> 0.56 </td> <td align="right"> -1.02 </td> <td align="right"> 0.57 </td> <td align="right"> -0.01 </td> <td align="right"> -1.36 </td> <td align="right"> -0.07 </td> <td align="right"> 1.11 </td> </tr>
  <tr> <td align="right"> 12 </td> <td align="right"> 1.72 </td> <td align="right"> 1.09 </td> <td align="right"> 0.56 </td> <td align="right"> 0.59 </td> <td align="right"> -1.71 </td> <td align="right"> -1.02 </td> <td align="right"> 0.74 </td> <td align="right"> -0.66 </td> <td align="right"> 1.67 </td> <td align="right"> -0.99 </td> </tr>
  <tr> <td align="right"> 13 </td> <td align="right"> 0.36 </td> <td align="right"> -1.23 </td> <td align="right"> -1.54 </td> <td align="right"> 0.61 </td> <td align="right"> -0.27 </td> <td align="right"> -0.17 </td> <td align="right"> -0.12 </td> <td align="right"> -1.37 </td> <td align="right"> -0.10 </td> <td align="right"> 0.78 </td> </tr>
  <tr> <td align="right"> 14 </td> <td align="right"> 0.07 </td> <td align="right"> 2.98 </td> <td align="right"> -0.51 </td> <td align="right"> -0.39 </td> <td align="right"> 0.15 </td> <td align="right"> -1.86 </td> <td align="right"> -0.30 </td> <td align="right"> -0.02 </td> <td align="right"> -0.54 </td> <td align="right"> 0.13 </td> </tr>
  <tr> <td align="right"> 15 </td> <td align="right"> -1.67 </td> <td align="right"> 0.14 </td> <td align="right"> 1.22 </td> <td align="right"> -0.36 </td> <td align="right"> -0.90 </td> <td align="right"> -0.26 </td> <td align="right"> -0.71 </td> <td align="right"> 2.02 </td> <td align="right"> 0.34 </td> <td align="right"> 0.74 </td> </tr>
  <tr> <td align="right"> 16 </td> <td align="right"> 1.69 </td> <td align="right"> 1.71 </td> <td align="right"> 1.26 </td> <td align="right"> 0.28 </td> <td align="right"> 0.85 </td> <td align="right"> -0.38 </td> <td align="right"> 0.86 </td> <td align="right"> 0.14 </td> <td align="right"> 1.56 </td> <td align="right"> -0.37 </td> </tr>
  <tr> <td align="right"> 17 </td> <td align="right"> 0.04 </td> <td align="right"> -1.89 </td> <td align="right"> 0.10 </td> <td align="right"> -0.27 </td> <td align="right"> 1.85 </td> <td align="right"> -0.78 </td> <td align="right"> -0.27 </td> <td align="right"> 0.60 </td> <td align="right"> 0.27 </td> <td align="right"> -1.73 </td> </tr>
  <tr> <td align="right"> 18 </td> <td align="right"> 0.97 </td> <td align="right"> -0.24 </td> <td align="right"> 0.82 </td> <td align="right"> -0.76 </td> <td align="right"> -0.23 </td> <td align="right"> 1.88 </td> <td align="right"> 1.26 </td> <td align="right"> 0.23 </td> <td align="right"> 0.31 </td> <td align="right"> -0.10 </td> </tr>
  <tr> <td align="right"> 19 </td> <td align="right"> -0.02 </td> <td align="right"> 0.75 </td> <td align="right"> -0.05 </td> <td align="right"> -1.24 </td> <td align="right"> 0.56 </td> <td align="right"> 2.01 </td> <td align="right"> -0.28 </td> <td align="right"> -0.50 </td> <td align="right"> -0.24 </td> <td align="right"> 1.29 </td> </tr>
  <tr> <td align="right"> 20 </td> <td align="right"> 0.80 </td> <td align="right"> -1.31 </td> <td align="right"> -1.02 </td> <td align="right"> 1.00 </td> <td align="right"> 2.37 </td> <td align="right"> 1.26 </td> <td align="right"> 0.13 </td> <td align="right"> 0.25 </td> <td align="right"> 0.20 </td> <td align="right"> -0.53 </td> </tr>
  <tr> <td align="right"> 21 </td> <td align="right"> -1.03 </td> <td align="right"> -0.39 </td> <td align="right"> -0.57 </td> <td align="right"> 0.31 </td> <td align="right"> 0.58 </td> <td align="right"> -0.76 </td> <td align="right"> 1.98 </td> <td align="right"> -0.82 </td> <td align="right"> 0.76 </td> <td align="right"> -0.76 </td> </tr>
  <tr> <td align="right"> 22 </td> <td align="right"> -0.45 </td> <td align="right"> 1.61 </td> <td align="right"> 0.96 </td> <td align="right"> -0.95 </td> <td align="right"> 0.89 </td> <td align="right"> -1.39 </td> <td align="right"> 0.91 </td> <td align="right"> -0.50 </td> <td align="right"> 0.17 </td> <td align="right"> 1.60 </td> </tr>
  <tr> <td align="right"> 23 </td> <td align="right"> -0.26 </td> <td align="right"> -0.82 </td> <td align="right"> 0.12 </td> <td align="right"> -0.13 </td> <td align="right"> -0.28 </td> <td align="right"> 0.93 </td> <td align="right"> 0.94 </td> <td align="right"> -0.26 </td> <td align="right"> 0.87 </td> <td align="right"> -1.18 </td> </tr>
  <tr> <td align="right"> 24 </td> <td align="right"> 0.58 </td> <td align="right"> -0.53 </td> <td align="right"> 1.43 </td> <td align="right"> 0.60 </td> <td align="right"> -2.21 </td> <td align="right"> 2.03 </td> <td align="right"> 0.93 </td> <td align="right"> 0.99 </td> <td align="right"> 0.34 </td> <td align="right"> -0.10 </td> </tr>
  <tr> <td align="right"> 25 </td> <td align="right"> -0.27 </td> <td align="right"> 1.56 </td> <td align="right"> 0.44 </td> <td align="right"> 0.41 </td> <td align="right"> 0.31 </td> <td align="right"> 0.53 </td> <td align="right"> 1.03 </td> <td align="right"> 1.33 </td> <td align="right"> -0.29 </td> <td align="right"> 1.05 </td> </tr>
  <tr> <td align="right"> 26 </td> <td align="right"> 0.34 </td> <td align="right"> 0.63 </td> <td align="right"> -0.76 </td> <td align="right"> 0.26 </td> <td align="right"> -0.85 </td> <td align="right"> -0.93 </td> <td align="right"> 0.51 </td> <td align="right"> -0.73 </td> <td align="right"> 0.52 </td> <td align="right"> -0.74 </td> </tr>
  <tr> <td align="right"> 27 </td> <td align="right"> 1.63 </td> <td align="right"> 0.52 </td> <td align="right"> 0.66 </td> <td align="right"> 0.78 </td> <td align="right"> 0.05 </td> <td align="right"> -0.31 </td> <td align="right"> -0.34 </td> <td align="right"> 2.50 </td> <td align="right"> -0.87 </td> <td align="right"> 0.74 </td> </tr>
  <tr> <td align="right"> 28 </td> <td align="right"> 1.42 </td> <td align="right"> -0.53 </td> <td align="right"> 0.12 </td> <td align="right"> -1.66 </td> <td align="right"> 1.22 </td> <td align="right"> 0.55 </td> <td align="right"> -0.84 </td> <td align="right"> 0.02 </td> <td align="right"> 0.95 </td> <td align="right"> -1.33 </td> </tr>
  <tr> <td align="right"> 29 </td> <td align="right"> 0.73 </td> <td align="right"> -0.39 </td> <td align="right"> -1.20 </td> <td align="right"> 1.18 </td> <td align="right"> 0.03 </td> <td align="right"> -0.01 </td> <td align="right"> -0.49 </td> <td align="right"> -0.75 </td> <td align="right"> -0.31 </td> <td align="right"> 0.91 </td> </tr>
  <tr> <td align="right"> 30 </td> <td align="right"> 0.74 </td> <td align="right"> -1.20 </td> <td align="right"> 0.32 </td> <td align="right"> 0.98 </td> <td align="right"> 1.02 </td> <td align="right"> 0.18 </td> <td align="right"> 1.83 </td> <td align="right"> 0.74 </td> <td align="right"> -0.40 </td> <td align="right"> -2.51 </td> </tr>
   </table>

<!-- html table generated in R 3.2.3 by xtable 1.8-0 package -->
<!-- Sun May 22 13:33:41 2016 -->
<table border=1>
<tr> <th>  </th> <th> Estimate </th> <th> Std. Error </th> <th> t value </th> <th> Pr(&gt;|t|) </th>  </tr>
  <tr> <td align="right"> (Intercept) </td> <td align="right"> -0.02 </td> <td align="right"> 0.10 </td> <td align="right"> -0.2 </td> <td align="right"> 0.88 </td> </tr>
  <tr> <td align="right"> x </td> <td align="right"> 1.97 </td> <td align="right"> 0.09 </td> <td align="right"> 21.6 </td> <td align="right"> 0.00 </td> </tr>
   </table>


<!--html_preserve--><div id="htmlwidget-2300" style="width:612px;height:378px;" class="plotly"></div>
<script type="application/json" data-for="htmlwidget-2300">{"x":{"data":[{"x":[0.2,0.2,0.2,0.2,0.2,0.4,0.3,0.2,0.2,0.1,0.2,0.2,0.1,0.1,0.2,0.4,0.4,0.3,0.3,0.3,0.2,0.4,0.2,0.5,0.2,0.2,0.4,0.2,0.2,0.2,0.2,0.4,0.1,0.2,0.2,0.2,0.2,0.1,0.2,0.2,0.3,0.3,0.2,0.6,0.4,0.3,0.2,0.2,0.2,0.2],"y":[5.1,4.9,4.7,4.6,5,5.4,4.6,5,4.4,4.9,5.4,4.8,4.8,4.3,5.8,5.7,5.4,5.1,5.7,5.1,5.4,5.1,4.6,5.1,4.8,5,5,5.2,5.2,4.7,4.8,5.4,5.2,5.5,4.9,5,5.5,4.9,4.4,5.1,5,4.5,4.4,5,5.1,4.8,5.1,4.6,5.3,5],"name":"setosa","text":[],"type":"scatter","mode":"markers","marker":{"opacity":null,"color":"rgb(248,118,109)","size":5.66929133858268,"symbol":"circle"},"xaxis":"x1","yaxis":"y1","showlegend":true},{"x":[1.4,1.5,1.5,1.3,1.5,1.3,1.6,1,1.3,1.4,1,1.5,1,1.4,1.3,1.4,1.5,1,1.5,1.1,1.8,1.3,1.5,1.2,1.3,1.4,1.4,1.7,1.5,1,1.1,1,1.2,1.6,1.5,1.6,1.5,1.3,1.3,1.3,1.2,1.4,1.2,1,1.3,1.2,1.3,1.3,1.1,1.3],"y":[7,6.4,6.9,5.5,6.5,5.7,6.3,4.9,6.6,5.2,5,5.9,6,6.1,5.6,6.7,5.6,5.8,6.2,5.6,5.9,6.1,6.3,6.1,6.4,6.6,6.8,6.7,6,5.7,5.5,5.5,5.8,6,5.4,6,6.7,6.3,5.6,5.5,5.5,6.1,5.8,5,5.6,5.7,5.7,6.2,5.1,5.7],"name":"versicolor","text":[],"type":"scatter","mode":"markers","marker":{"opacity":null,"color":"rgb(0,186,56)","size":5.66929133858268,"symbol":"circle"},"xaxis":"x1","yaxis":"y1","showlegend":true},{"x":[2.5,1.9,2.1,1.8,2.2,2.1,1.7,1.8,1.8,2.5,2,1.9,2.1,2,2.4,2.3,1.8,2.2,2.3,1.5,2.3,2,2,1.8,2.1,1.8,1.8,1.8,2.1,1.6,1.9,2,2.2,1.5,1.4,2.3,2.4,1.8,1.8,2.1,2.4,2.3,1.9,2.3,2.5,2.3,1.9,2,2.3,1.8],"y":[6.3,5.8,7.1,6.3,6.5,7.6,4.9,7.3,6.7,7.2,6.5,6.4,6.8,5.7,5.8,6.4,6.5,7.7,7.7,6,6.9,5.6,7.7,6.3,6.7,7.2,6.2,6.1,6.4,7.2,7.4,7.9,6.4,6.3,6.1,7.7,6.3,6.4,6,6.9,6.7,6.9,5.8,6.8,6.7,6.7,6.3,6.5,6.2,5.9],"name":"virginica","text":[],"type":"scatter","mode":"markers","marker":{"opacity":null,"color":"rgb(97,156,255)","size":5.66929133858268,"symbol":"circle"},"xaxis":"x1","yaxis":"y1","showlegend":true},{"x":[0.1,0.106329113924051,0.112658227848101,0.118987341772152,0.125316455696203,0.131645569620253,0.137974683544304,0.144303797468354,0.150632911392405,0.156962025316456,0.163291139240506,0.169620253164557,0.175949367088608,0.182278481012658,0.188607594936709,0.194936708860759,0.20126582278481,0.207594936708861,0.213924050632911,0.220253164556962,0.226582278481013,0.232911392405063,0.239240506329114,0.245569620253165,0.251898734177215,0.258227848101266,0.264556962025316,0.270886075949367,0.277215189873418,0.283544303797468,0.289873417721519,0.29620253164557,0.30253164556962,0.308860759493671,0.315189873417722,0.321518987341772,0.327848101265823,0.334177215189873,0.340506329113924,0.346835443037975,0.353164556962025,0.359493670886076,0.365822784810127,0.372151898734177,0.378481012658228,0.384810126582279,0.391139240506329,0.39746835443038,0.40379746835443,0.410126582278481,0.416455696202532,0.422784810126582,0.429113924050633,0.435443037974684,0.441772151898734,0.448101265822785,0.454430379746835,0.460759493670886,0.467088607594937,0.473417721518987,0.479746835443038,0.486075949367089,0.492405063291139,0.49873417721519,0.505063291139241,0.511392405063291,0.517721518987342,0.524050632911392,0.530379746835443,0.536708860759494,0.543037974683544,0.549367088607595,0.555696202531646,0.562025316455696,0.568354430379747,0.574683544303797,0.581012658227848,0.587341772151899,0.593670886075949,0.6,0.6,0.593670886075949,0.587341772151899,0.581012658227848,0.574683544303797,0.568354430379747,0.562025316455696,0.555696202531646,0.549367088607595,0.543037974683544,0.536708860759494,0.530379746835443,0.524050632911392,0.517721518987342,0.511392405063291,0.505063291139241,0.49873417721519,0.492405063291139,0.486075949367089,0.479746835443038,0.473417721518987,0.467088607594937,0.460759493670886,0.454430379746835,0.448101265822785,0.441772151898734,0.435443037974684,0.429113924050633,0.422784810126582,0.416455696202532,0.410126582278481,0.40379746835443,0.39746835443038,0.391139240506329,0.384810126582279,0.378481012658228,0.372151898734177,0.365822784810127,0.359493670886076,0.353164556962025,0.346835443037975,0.340506329113924,0.334177215189873,0.327848101265823,0.321518987341772,0.315189873417722,0.308860759493671,0.30253164556962,0.29620253164557,0.289873417721519,0.283544303797468,0.277215189873418,0.270886075949367,0.264556962025316,0.258227848101266,0.251898734177215,0.245569620253165,0.239240506329114,0.232911392405063,0.226582278481013,0.220253164556962,0.213924050632911,0.207594936708861,0.20126582278481,0.194936708860759,0.188607594936709,0.182278481012658,0.175949367088608,0.169620253164557,0.163291139240506,0.156962025316456,0.150632911392405,0.144303797468354,0.137974683544304,0.131645569620253,0.125316455696203,0.118987341772152,0.112658227848101,0.106329113924051,0.1,0.1,null,1,1.01012658227848,1.02025316455696,1.03037974683544,1.04050632911392,1.05063291139241,1.06075949367089,1.07088607594937,1.08101265822785,1.09113924050633,1.10126582278481,1.11139240506329,1.12151898734177,1.13164556962025,1.14177215189873,1.15189873417722,1.1620253164557,1.17215189873418,1.18227848101266,1.19240506329114,1.20253164556962,1.2126582278481,1.22278481012658,1.23291139240506,1.24303797468354,1.25316455696203,1.26329113924051,1.27341772151899,1.28354430379747,1.29367088607595,1.30379746835443,1.31392405063291,1.32405063291139,1.33417721518987,1.34430379746835,1.35443037974684,1.36455696202532,1.3746835443038,1.38481012658228,1.39493670886076,1.40506329113924,1.41518987341772,1.4253164556962,1.43544303797468,1.44556962025316,1.45569620253165,1.46582278481013,1.47594936708861,1.48607594936709,1.49620253164557,1.50632911392405,1.51645569620253,1.52658227848101,1.53670886075949,1.54683544303797,1.55696202531646,1.56708860759494,1.57721518987342,1.5873417721519,1.59746835443038,1.60759493670886,1.61772151898734,1.62784810126582,1.6379746835443,1.64810126582278,1.65822784810127,1.66835443037975,1.67848101265823,1.68860759493671,1.69873417721519,1.70886075949367,1.71898734177215,1.72911392405063,1.73924050632911,1.74936708860759,1.75949367088608,1.76962025316456,1.77974683544304,1.78987341772152,1.8,1.8,1.78987341772152,1.77974683544304,1.76962025316456,1.75949367088608,1.74936708860759,1.73924050632911,1.72911392405063,1.71898734177215,1.70886075949367,1.69873417721519,1.68860759493671,1.67848101265823,1.66835443037975,1.65822784810127,1.64810126582278,1.6379746835443,1.62784810126582,1.61772151898734,1.60759493670886,1.59746835443038,1.5873417721519,1.57721518987342,1.56708860759494,1.55696202531646,1.54683544303797,1.53670886075949,1.52658227848101,1.51645569620253,1.50632911392405,1.49620253164557,1.48607594936709,1.47594936708861,1.46582278481013,1.45569620253165,1.44556962025316,1.43544303797468,1.4253164556962,1.41518987341772,1.40506329113924,1.39493670886076,1.38481012658228,1.3746835443038,1.36455696202532,1.35443037974684,1.34430379746835,1.33417721518987,1.32405063291139,1.31392405063291,1.30379746835443,1.29367088607595,1.28354430379747,1.27341772151899,1.26329113924051,1.25316455696203,1.24303797468354,1.23291139240506,1.22278481012658,1.2126582278481,1.20253164556962,1.19240506329114,1.18227848101266,1.17215189873418,1.1620253164557,1.15189873417722,1.14177215189873,1.13164556962025,1.12151898734177,1.11139240506329,1.10126582278481,1.09113924050633,1.08101265822785,1.07088607594937,1.06075949367089,1.05063291139241,1.04050632911392,1.03037974683544,1.02025316455696,1.01012658227848,1,1,null,1.4,1.41392405063291,1.42784810126582,1.44177215189873,1.45569620253165,1.46962025316456,1.48354430379747,1.49746835443038,1.51139240506329,1.5253164556962,1.53924050632911,1.55316455696203,1.56708860759494,1.58101265822785,1.59493670886076,1.60886075949367,1.62278481012658,1.63670886075949,1.65063291139241,1.66455696202532,1.67848101265823,1.69240506329114,1.70632911392405,1.72025316455696,1.73417721518987,1.74810126582278,1.7620253164557,1.77594936708861,1.78987341772152,1.80379746835443,1.81772151898734,1.83164556962025,1.84556962025316,1.85949367088608,1.87341772151899,1.8873417721519,1.90126582278481,1.91518987341772,1.92911392405063,1.94303797468354,1.95696202531646,1.97088607594937,1.98481012658228,1.99873417721519,2.0126582278481,2.02658227848101,2.04050632911392,2.05443037974684,2.06835443037975,2.08227848101266,2.09620253164557,2.11012658227848,2.12405063291139,2.1379746835443,2.15189873417722,2.16582278481013,2.17974683544304,2.19367088607595,2.20759493670886,2.22151898734177,2.23544303797468,2.24936708860759,2.26329113924051,2.27721518987342,2.29113924050633,2.30506329113924,2.31898734177215,2.33291139240506,2.34683544303797,2.36075949367089,2.3746835443038,2.38860759493671,2.40253164556962,2.41645569620253,2.43037974683544,2.44430379746835,2.45822784810127,2.47215189873418,2.48607594936709,2.5,2.5,2.5,2.48607594936709,2.47215189873418,2.45822784810127,2.44430379746835,2.43037974683544,2.41645569620253,2.40253164556962,2.38860759493671,2.3746835443038,2.36075949367089,2.34683544303797,2.33291139240506,2.31898734177215,2.30506329113924,2.29113924050633,2.27721518987342,2.26329113924051,2.24936708860759,2.23544303797468,2.22151898734177,2.20759493670886,2.19367088607595,2.17974683544304,2.16582278481013,2.15189873417722,2.1379746835443,2.12405063291139,2.11012658227848,2.09620253164557,2.08227848101266,2.06835443037975,2.05443037974684,2.04050632911392,2.02658227848101,2.0126582278481,1.99873417721519,1.98481012658228,1.97088607594937,1.95696202531646,1.94303797468354,1.92911392405063,1.91518987341772,1.90126582278481,1.8873417721519,1.87341772151899,1.85949367088608,1.84556962025316,1.83164556962025,1.81772151898734,1.80379746835443,1.78987341772152,1.77594936708861,1.7620253164557,1.74810126582278,1.73417721518987,1.72025316455696,1.70632911392405,1.69240506329114,1.67848101265823,1.66455696202532,1.65063291139241,1.63670886075949,1.62278481012658,1.60886075949367,1.59493670886076,1.58101265822785,1.56708860759494,1.55316455696203,1.53924050632911,1.5253164556962,1.51139240506329,1.49746835443038,1.48354430379747,1.46962025316456,1.45569620253165,1.44177215189873,1.42784810126582,1.41392405063291,1.4,1.4,null,1,null,0.1,0.1],"y":[5.0375066861581,5.03862868035235,5.03982745512881,5.04111005734704,5.04248427234505,5.04395869422228,5.04554279705682,5.04724700433497,5.04908275270041,5.05106254467531,5.05319998328006,5.05550977954816,5.05800772196067,5.06071059510107,5.06363603381194,5.06680229944869,5.07022796723129,5.07393151894624,5.07793084385363,5.08224266251539,5.08688190233419,5.09186106766496,5.09718965823245,5.10287369375812,5.10891539752209,5.11531307648286,5.12206121271479,5.12915075488035,5.13656957484923,5.14430303822788,5.15233463101223,5.16064658759616,5.16922047552746,5.17803770624562,5.18707995526406,5.19632948750852,5.20576939259205,5.21538374049389,5.22515767086034,5.23507742969785,5.24513036634965,5.2553049019889,5.26559047890248,5.27597749789174,5.28645724935733,5.29702184214204,5.30766413299658,5.31837765858912,5.32915657126554,5.33999557924219,5.35088989153868,5.36183516769908,5.37282747217784,5.38386323315835,5.39493920550961,5.4060524375556,5.41720024132377,5.42838016594458,5.43958997388914,5.4508276197521,5.46209123131,5.47337909260888,5.48468962885877,5.49602139293485,5.50737305330641,5.51874338323414,5.53013125109393,5.54153561170133,5.55295549852527,5.56439001669247,5.57583833669505,5.5872996887245,5.59877335756343,5.61025867797508,5.62175503053691,5.63326183787119,5.64477856123068,5.65630469740221,5.6678397758954,5.67938335638708,4.99117893688744,4.99094817901693,4.99070891914792,4.99046071695725,4.99020310195454,4.98993557092662,4.98965758512625,4.9893685671757,4.98906789765243,4.98875491131968,4.98842889296007,4.98808907276506,4.98773462122681,4.987364643472,4.98697817296959,4.98657416453513,4.98615148654449,4.98570891225837,4.98524511014606,4.98475863308274,4.98424790627844,4.9837112137792,4.98314668336156,4.98255226962017,4.98192573502614,4.98126462870993,4.98056626269899,4.97982768531731,4.97904565143387,4.97821658923207,4.97733656316636,4.97640123278081,4.97540580709502,4.97434499432537,4.97321294681771,4.97200320124022,4.97070861434361,4.96932129497067,4.96783253352205,4.96623273079911,4.9645113290887,4.96265674956402,4.96065634156827,4.9584963511079,4.95616191782924,4.9536371117115,4.95090502236774,4.9479479147237,4.9447474642928,4.94128508251453,4.93754233693668,4.93350146195313,4.92914594355981,4.92446114736318,4.91943494523291,4.91405828583148,4.90832565123325,4.90223534839672,4.89578960060201,4.88899442757057,4.88185932902718,4.87439680932674,4.86662179587193,4.85855100922468,4.85020233864508,4.84159426591963,4.8327453662683,4.8236739010465,4.81439750509681,4.80493296300271,4.79529606324527,4.78550151685797,4.7755629268612,4.76549279577716,4.75530256024949,4.74500264376453,4.73460252040034,4.72411078425637,4.71353522067063,4.70288287650269,5.0375066861581,null,5.71224262663287,5.72120249349721,5.73021096495906,5.73927156476682,5.74838812669975,5.7575648238091,5.7668062000153,5.77611720404681,5.78550322561835,5.79497013362538,5.80452431596871,5.81417272040862,5.82392289557102,5.83378303087868,5.84376199374849,5.85386936187777,5.86411544783772,5.87451131251779,5.88506876325051,5.89580033175212,5.90671922643051,5.91783925326903,5.92917469956123,5.94074017544812,5.9525504097015,5.96461999867559,5.97696311088775,5.98959315419118,6.00252241763362,6.01576170525355,6.02931998341149,6.04320406584163,6.05741836059632,6.07196469995043,6.08684226821193,6.10204763396735,6.11757488383226,6.13341584578873,6.14956038306729,6.16599673522058,6.18271188186316,6.19969190622451,6.21692233944325,6.2343884714845,6.25207561978948,6.26996935156485,6.28805565955204,6.30632109400232,6.32475285543891,6.34333885375432,6.36206773946757,6.3809289127589,6.39991251539044,6.41900940995738,6.43821115019854,6.45750994540079,6.47689862129769,6.49637057931015,6.5159197555125,6.53554058032681,6.55522793964457,6.57497713783797,6.59478386294092,6.61464415414451,6.63455437165147,6.65451116886378,6.6745114668283,6.6945524308336,6.71463144903158,6.73474611294738,6.75489419973757,6.77507365605768,6.79528258340469,6.81551922480624,6.83578195273639,6.85606925814552,6.87637974050117,6.8967120987443,6.91706512307435,6.93743768748375,6.28675602924728,6.27824019507245,6.26970482081828,6.26114878047719,6.25257086424861,6.24396977107353,6.23534410041944,6.22669234323678,6.21801287199956,6.20930392973545,6.20056361794142,6.191789883273,6.18298050288675,6.17413306830782,6.16524496768812,6.15631336631621,6.14733518523895,6.13830707785831,6.12922540437704,6.12008620398621,6.11088516471976,6.10161759094984,6.09227836856797,6.0828619279962,6.07336220530888,6.06377260192691,6.05408594358384,6.04429443956656,6.03438964361388,6.02436241832098,6.01420290545002,6.0039005051812,5.99344386803356,5.98282090389962,5.97201881330259,5.96102414649374,5.94982289621449,5.93840062967152,5.92674266430604,5.91483429008316,5.90266103814152,5.89020899171059,5.87746513040493,5.86441769377717,5.85105654505785,5.83737351222905,5.82336268190633,5.80902062267621,5.79434651884668,5.7793422026926,5.76401208226631,5.74836297130203,5.73240383616024,5.71614548087945,5.69960019450739,5.68278138489725,5.66570322056641,5.64838029786907,5.63082734557705,5.61305897383135,5.59508946992552,5.5769326398429,5.55860169199139,5.54010915808724,5.52146684546297,5.50268581500803,5.48377637929362,5.46474811601705,5.44560989259523,5.42636989845091,5.40703568221002,5.38761419163283,5.36811181462014,5.34853442006743,5.32888739768941,5.30917569621454,5.28940385956324,5.26957606078678,5.24969613366441,5.22976760194452,5.71224262663287,null,6.6206606726097,6.62150251050204,6.62237512112132,6.62328032402127,6.62422007694442,6.62519648828732,6.6262118308156,6.62726855675685,6.62836931441063,6.62951696642562,6.63071460990497,6.6319655985104,6.63327356674365,6.63464245658852,6.63607654669778,6.63758048430274,6.63915932000849,6.64081854560994,6.6425641350193,6.64440258832793,6.64634097892886,6.64838700349092,6.65054903439194,6.65283617397495,6.65525830967424,6.65782616865451,6.66055137010236,6.66344647269638,6.66652501405554,6.66980153813516,6.6732916056314,6.67701178152385,6.68097959302127,6.68521345051401,6.68973252386418,6.69455656671472,6.69970568273406,6.70520003008969,6.71105946414556,6.71730312343669,6.72394897017295,6.73101330332689,6.73851026889264,6.7464513970284,6.75484519830993,6.76369685024162,6.77300800004402,6.78277670087371,6.79299748715089,6.80366158229831,6.8147572208738,6.82627005849571,6.83818363817062,6.85047988087963,6.86313957105528,6.8761428128714,6.88946943986385,6.90309936718142,6.91701288188542,6.93119087166525,6.94561499592476,6.96026780546623,6.97513281815044,6.99019455819925,7.00543856649396,7.02085138853742,7.03642054587376,7.05213449582675,7.0679825835146,7.08395498927653,7.10004267392933,7.11623732366825,7.13253129593167,7.14891756715303,7.16538968301303,7.18194171156727,7.19856819944526,7.21526413118523,7.23202489167485,7.2488462316031,6.54414116085401,6.54414116085401,6.54283810480665,6.54147446932066,6.54004600508501,6.53854809698739,6.53697572956602,6.5353234494504,6.53358532469615,6.53175490098396,6.52982515474726,6.52778844342445,6.52563645321076,6.52336014492299,6.52094969890037,6.51839446026111,6.51568288632895,6.51280249864804,6.50973984272125,6.50648045942984,6.5030088729957,6.49930860127959,6.49536219508381,6.49115131381219,6.48665684515415,6.48185907617098,6.47673792201149,6.47127321621153,6.46544506294492,6.45923424664422,6.45262268829051,6.4455939308904,6.4381336300622,6.43023002036376,6.42187432521785,6.41306107904463,6.40378833500071,6.39405774030662,6.38387447246677,6.37324704205691,6.36218697923523,6.35070842999588,6.33882769331139,6.32656273139165,6.31393268277167,6.30095740281539,6.28765704969032,6.27405172706488,6.260161188582,6.24600460410381,6.23160038402065,6.21696605554127,6.20211818364528,6.18707232902883,6.17184303564723,6.15644384111946,6.14088730412412,6.1251850438478,6.10934778745519,6.0933854223806,6.07730705096705,6.06112104559236,6.04483510292538,6.02845629635913,6.01199112598497,5.9954455657151,5.97882510734444,5.96213480147809,5.94537929534735,5.92856286760498,5.91168946023481,5.89476270773854,5.87778596377791,5.86076232545608,5.84369465542172,5.82658560197438,5.80943761734167,5.79225297428921,5.77503378121355,5.75778199585721,5.74049943777394,6.6206606726097,null,5.71224262663287,null,5.0375066861581,5.0375066861581],"name":null,"text":[null],"type":"scatter","mode":"lines","line":{"dash":"solid","color":"transparent","width":7.55905511811024},"fill":"tozerox","fillcolor":"rgba(153,153,153,0.2)","xaxis":"x1","yaxis":"y1","showlegend":false},{"x":[0.1,0.106329113924051,0.112658227848101,0.118987341772152,0.125316455696203,0.131645569620253,0.137974683544304,0.144303797468354,0.150632911392405,0.156962025316456,0.163291139240506,0.169620253164557,0.175949367088608,0.182278481012658,0.188607594936709,0.194936708860759,0.20126582278481,0.207594936708861,0.213924050632911,0.220253164556962,0.226582278481013,0.232911392405063,0.239240506329114,0.245569620253165,0.251898734177215,0.258227848101266,0.264556962025316,0.270886075949367,0.277215189873418,0.283544303797468,0.289873417721519,0.29620253164557,0.30253164556962,0.308860759493671,0.315189873417722,0.321518987341772,0.327848101265823,0.334177215189873,0.340506329113924,0.346835443037975,0.353164556962025,0.359493670886076,0.365822784810127,0.372151898734177,0.378481012658228,0.384810126582279,0.391139240506329,0.39746835443038,0.40379746835443,0.410126582278481,0.416455696202532,0.422784810126582,0.429113924050633,0.435443037974684,0.441772151898734,0.448101265822785,0.454430379746835,0.460759493670886,0.467088607594937,0.473417721518987,0.479746835443038,0.486075949367089,0.492405063291139,0.49873417721519,0.505063291139241,0.511392405063291,0.517721518987342,0.524050632911392,0.530379746835443,0.536708860759494,0.543037974683544,0.549367088607595,0.555696202531646,0.562025316455696,0.568354430379747,0.574683544303797,0.581012658227848,0.587341772151899,0.593670886075949,0.6],"y":[4.87019478133039,4.87608195051149,4.88196911969259,4.88785628887369,4.89374345805479,4.89963062723589,4.90551779641699,4.91140496559809,4.91729213477919,4.92317930396029,4.92906647314139,4.93495364232249,4.94084081150359,4.94672798068469,4.95261514986579,4.95850231904689,4.96438948822798,4.97027665740908,4.97616382659018,4.98205099577128,4.98793816495238,4.99382533413348,4.99971250331458,5.00559967249568,5.01148684167678,5.01737401085788,5.02326118003898,5.02914834922008,5.03503551840118,5.04092268758228,5.04680985676338,5.05269702594448,5.05858419512558,5.06447136430668,5.07035853348778,5.07624570266888,5.08213287184998,5.08802004103108,5.09390721021218,5.09979437939328,5.10568154857438,5.11156871775548,5.11745588693658,5.12334305611768,5.12923022529877,5.13511739447987,5.14100456366097,5.14689173284207,5.15277890202317,5.15866607120427,5.16455324038537,5.17044040956647,5.17632757874757,5.18221474792867,5.18810191710977,5.19398908629087,5.19987625547197,5.20576342465307,5.21165059383417,5.21753776301527,5.22342493219637,5.22931210137747,5.23519927055857,5.24108643973967,5.24697360892077,5.25286077810187,5.25874794728297,5.26463511646407,5.27052228564517,5.27640945482627,5.28229662400737,5.28818379318847,5.29407096236957,5.29995813155067,5.30584530073176,5.31173246991286,5.31761963909396,5.32350680827506,5.32939397745616,5.33528114663726],"name":"setosa","text":[null],"type":"scatter","mode":"lines","line":{"dash":"solid","color":"rgb(248,118,109)","width":7.55905511811024},"xaxis":"x1","yaxis":"y1","showlegend":false},{"x":[1,1.01012658227848,1.02025316455696,1.03037974683544,1.04050632911392,1.05063291139241,1.06075949367089,1.07088607594937,1.08101265822785,1.09113924050633,1.10126582278481,1.11139240506329,1.12151898734177,1.13164556962025,1.14177215189873,1.15189873417722,1.1620253164557,1.17215189873418,1.18227848101266,1.19240506329114,1.20253164556962,1.2126582278481,1.22278481012658,1.23291139240506,1.24303797468354,1.25316455696203,1.26329113924051,1.27341772151899,1.28354430379747,1.29367088607595,1.30379746835443,1.31392405063291,1.32405063291139,1.33417721518987,1.34430379746835,1.35443037974684,1.36455696202532,1.3746835443038,1.38481012658228,1.39493670886076,1.40506329113924,1.41518987341772,1.4253164556962,1.43544303797468,1.44556962025316,1.45569620253165,1.46582278481013,1.47594936708861,1.48607594936709,1.49620253164557,1.50632911392405,1.51645569620253,1.52658227848101,1.53670886075949,1.54683544303797,1.55696202531646,1.56708860759494,1.57721518987342,1.5873417721519,1.59746835443038,1.60759493670886,1.61772151898734,1.62784810126582,1.6379746835443,1.64810126582278,1.65822784810127,1.66835443037975,1.67848101265823,1.68860759493671,1.69873417721519,1.70886075949367,1.71898734177215,1.72911392405063,1.73924050632911,1.74936708860759,1.75949367088608,1.76962025316456,1.77974683544304,1.78987341772152,1.8],"y":[5.4710051142887,5.48544931358081,5.49989351287292,5.51433771216503,5.52878191145714,5.54322611074925,5.55767031004136,5.57211450933348,5.58655870862559,5.6010029079177,5.61544710720981,5.62989130650192,5.64433550579404,5.65877970508615,5.67322390437826,5.68766810367037,5.70211230296248,5.71655650225459,5.73100070154671,5.74544490083882,5.75988910013093,5.77433329942304,5.78877749871515,5.80322169800726,5.81766589729937,5.83211009659149,5.8465542958836,5.86099849517571,5.87544269446782,5.88988689375993,5.90433109305204,5.91877529234416,5.93321949163627,5.94766369092838,5.96210789022049,5.9765520895126,5.99099628880471,6.00544048809683,6.01988468738894,6.03432888668105,6.04877308597316,6.06321728526527,6.07766148455738,6.0921056838495,6.10654988314161,6.12099408243372,6.13543828172583,6.14988248101794,6.16432668031005,6.17877087960217,6.19321507889428,6.20765927818639,6.2221034774785,6.23654767677061,6.25099187606272,6.26543607535483,6.27988027464695,6.29432447393906,6.30876867323117,6.32321287252328,6.33765707181539,6.3521012711075,6.36654547039962,6.38098966969173,6.39543386898384,6.40987806827595,6.42432226756806,6.43876646686017,6.45321066615229,6.4676548654444,6.48209906473651,6.49654326402862,6.51098746332073,6.52543166261284,6.53987586190496,6.55432006119707,6.56876426048918,6.58320845978129,6.5976526590734,6.61209685836551],"name":"versicolor","text":[null],"type":"scatter","mode":"lines","line":{"dash":"solid","color":"rgb(0,186,56)","width":7.55905511811024},"xaxis":"x1","yaxis":"y1","showlegend":false},{"x":[1.4,1.41392405063291,1.42784810126582,1.44177215189873,1.45569620253165,1.46962025316456,1.48354430379747,1.49746835443038,1.51139240506329,1.5253164556962,1.53924050632911,1.55316455696203,1.56708860759494,1.58101265822785,1.59493670886076,1.60886075949367,1.62278481012658,1.63670886075949,1.65063291139241,1.66455696202532,1.67848101265823,1.69240506329114,1.70632911392405,1.72025316455696,1.73417721518987,1.74810126582278,1.7620253164557,1.77594936708861,1.78987341772152,1.80379746835443,1.81772151898734,1.83164556962025,1.84556962025316,1.85949367088608,1.87341772151899,1.8873417721519,1.90126582278481,1.91518987341772,1.92911392405063,1.94303797468354,1.95696202531646,1.97088607594937,1.98481012658228,1.99873417721519,2.0126582278481,2.02658227848101,2.04050632911392,2.05443037974684,2.06835443037975,2.08227848101266,2.09620253164557,2.11012658227848,2.12405063291139,2.1379746835443,2.15189873417722,2.16582278481013,2.17974683544304,2.19367088607595,2.20759493670886,2.22151898734177,2.23544303797468,2.24936708860759,2.26329113924051,2.27721518987342,2.29113924050633,2.30506329113924,2.31898734177215,2.33291139240506,2.34683544303797,2.36075949367089,2.3746835443038,2.38860759493671,2.40253164556962,2.41645569620253,2.43037974683544,2.44430379746835,2.45822784810127,2.47215189873418,2.48607594936709,2.5],"y":[6.18058005519182,6.18964225317962,6.19870445116743,6.20776664915524,6.21682884714305,6.22589104513085,6.23495324311866,6.24401544110647,6.25307763909427,6.26213983708208,6.27120203506989,6.28026423305769,6.2893264310455,6.29838862903331,6.30745082702111,6.31651302500892,6.32557522299673,6.33463742098453,6.34369961897234,6.35276181696015,6.36182401494795,6.37088621293576,6.37994841092357,6.38901060891137,6.39807280689918,6.40713500488699,6.41619720287479,6.4252594008626,6.43432159885041,6.44338379683822,6.45244599482602,6.46150819281383,6.47057039080164,6.47963258878944,6.48869478677725,6.49775698476506,6.50681918275286,6.51588138074067,6.52494357872848,6.53400577671628,6.54306797470409,6.5521301726919,6.5611923706797,6.57025456866751,6.57931676665532,6.58837896464313,6.59744116263093,6.60650336061874,6.61556555860655,6.62462775659435,6.63368995458216,6.64275215256997,6.65181435055777,6.66087654854558,6.66993874653339,6.67900094452119,6.688063142509,6.69712534049681,6.70618753848461,6.71524973647242,6.72431193446023,6.73337413244803,6.74243633043584,6.75149852842365,6.76056072641145,6.76962292439926,6.77868512238707,6.78774732037487,6.79680951836268,6.80587171635049,6.8149339143383,6.8239961123261,6.83305831031391,6.84212050830172,6.85118270628952,6.86024490427733,6.86930710226514,6.87836930025294,6.88743149824075,6.89649369622856],"name":"virginica","text":[null],"type":"scatter","mode":"lines","line":{"dash":"solid","color":"rgb(97,156,255)","width":7.55905511811024},"xaxis":"x1","yaxis":"y1","showlegend":false}],"layout":{"xaxis":{"tickcolor":"rgb(0,0,0)","gridcolor":"rgb(229,229,229)","showgrid":true,"ticks":"outside","showticklabels":true,"tickangle":-0,"tickfont":{"family":"","size":9.6,"color":"rgb(0,0,0)"},"titlefont":{"family":"","size":12,"color":"rgb(0,0,0)"},"type":"linear","title":"Petal.Width","zeroline":false,"showline":true,"linecolor":"rgb(127,127,127)"},"yaxis":{"tickcolor":"rgb(0,0,0)","gridcolor":"rgb(229,229,229)","showgrid":true,"ticks":"outside","showticklabels":true,"tickangle":-0,"tickfont":{"family":"","size":9.6,"color":"rgb(0,0,0)"},"titlefont":{"family":"","size":12,"color":"rgb(0,0,0)"},"type":"linear","title":"Sepal.Length","zeroline":false,"showline":true,"linecolor":"rgb(127,127,127)"},"plot_bgcolor":"rgb(255,255,255)","margin":{"b":40,"l":60,"t":25,"r":10},"legend":{"bordercolor":"transparent","x":1.01,"y":0.7125,"xref":"paper","yref":"paper","xanchor":"left","yanchor":"top","font":{"family":""},"bgcolor":"rgb(255,255,255)"},"showlegend":true,"annotations":[{"text":"<b>Species</b>","x":1.025554,"y":0.8125,"showarrow":false,"xref":"paper","yref":"paper","xanchor":"left","yanchor":"top","textangle":0}],"titlefont":{"family":""},"paper_bgcolor":"rgb(255,255,255)"},"world_readable":true},"evals":[]}</script><!--/html_preserve-->

# Slide 4

![plot of chunk unnamed-chunk-7](/assets/Rfig/unnamed-chunk-7-1.svg)


Authored by [Robert Loudon](mailto:robert.loudon@deancare.com)
