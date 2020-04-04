# Pandas Holoviz

- [Installation](#Installation)
- [Basic Plotting](#Basic-Plotting)
- [Plot Types](#Plot-Types)
- [Getting Help](#Getting-Help)
- [Customization](#Customization)
- [Coloring](#Coloring)
- [Composing Plots](#Composing-Plots)
- [Holoviews Objects](#Holoviews-Objects)
- [Saving Plots](#Saving-Plots)
  
[hvplot](https://hvplot.holoviz.org/user_guide/index.html) - replaces `pandas.plot` api  
[holoviews](http://holoviews.org/user_guide/index.html) - high level plotting library  
[holoviz](http://holoviz.org/) - holoviz project with all kind of visualization libraries

### Installation

```
conda install -c pyviz holoviz
```

If using JupyterLab:
```
conda install jupyterlab
jupyter labextension install @pyviz/jupyterlab_pyviz
```

See: http://holoviz.org/installation.html


```python
import pandas as pd
import hvplot.pandas
df = pd.read_csv("https://raw.githubusercontent.com/holoviz/hvplot/master/examples/data/crime.csv", index_col="Year")
```









### Basic Plotting
Just use `df.hvplot()` instead of `df.plot()`


```python
df.hvplot(y=['Robbery', 'Burglary'])
```






<div id='1001'>





  <div class="bk-root" id="c6e00f0c-c4cf-470f-9991-c66c5a7ded07" data-root-id="1001"></div>
</div>
<script type="application/javascript">
    function msg_handler(msg) {
      var metadata = msg.metadata;
      var buffers = msg.buffers;
      var msg = msg.content.data;
      if ((metadata.msg_type == "Ready")) {
        if (metadata.content) {
          console.log("Python callback returned following output:", metadata.content);
        }
      } else if (metadata.msg_type == "Error") {
        console.log("Python failed with the following traceback:", metadata.traceback)
      } else {

var plot_id = "1001";

if ((plot_id in window.PyViz.plot_index) && (window.PyViz.plot_index[plot_id] != null)) {
  var plot = window.PyViz.plot_index[plot_id];
} else if ((Bokeh !== undefined) && (plot_id in Bokeh.index)) {
  var plot = Bokeh.index[plot_id];
}

if (plot == null) {
  return
}

if (plot_id in window.PyViz.receivers) {
  var receiver = window.PyViz.receivers[plot_id];
} else {
  var receiver = new Bokeh.protocol.Receiver();
  window.PyViz.receivers[plot_id] = receiver;
}

if ((buffers != undefined) && (buffers.length > 0)) {
  receiver.consume(buffers[0].buffer)
} else {
  receiver.consume(msg)
}

const comm_msg = receiver.message;
if ((comm_msg != null) && (Object.keys(comm_msg.content).length > 0)) {
  plot.model.document.apply_json_patch(comm_msg.content, comm_msg.buffers)
}

      }
    }
    if ((window.PyViz == undefined) || (!window.PyViz.comm_manager)) {
      console.log("Could not find comm manager")
    } else {
      window.PyViz.comm_manager.register_target('1001', '2854c156560c48668dd081632f64a894', msg_handler);
    }

(function(root) {
  function embed_document(root) {
  var docs_json = {"94584295-61ba-4a7e-a89c-4dfa8a9d218a":{"roots":{"references":[{"attributes":{"line_alpha":0.1,"line_color":"#1f77b3","line_width":2,"x":{"field":"Year"},"y":{"field":"value"}},"id":"1045","type":"Line"},{"attributes":{"data":{"Variable":["Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery","Robbery"],"Year":[1960,1961,1962,1963,1964,1965,1966,1967,1968,1969,1970,1971,1972,1973,1974,1975,1976,1977,1978,1979,1980,1981,1982,1983,1984,1985,1986,1987,1988,1989,1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014],"value":[107840,106670,110860,116470,130390,138690,157990,202910,262840,298850,349860,387700,376290,384220,442400,470500,427810,412610,426930,480700,565840,592910,553130,506567,485008,497874,542775,517704,542968,578326,639271,687732,672478,659870,618949,580509,535594,498534,447186,409371,408016,423557,420806,414235,401470,417438,449246,447324,443563,408742,369089,354772,355051,345095,325802]},"selected":{"id":"1042"},"selection_policy":{"id":"1071"}},"id":"1041","type":"ColumnDataSource"},{"attributes":{"source":{"id":"1041"}},"id":"1048","type":"CDSView"},{"attributes":{"callback":null,"renderers":[{"id":"1047"},{"id":"1063"}],"tags":["hv_created"],"tooltips":[["Variable","@{Variable}"],["Year","@{Year}"],["value","@{value}"]]},"id":"1005","type":"HoverTool"},{"attributes":{"children":[{"id":"1002"},{"id":"1007"},{"id":"1154"}],"margin":[0,0,0,0],"name":"Row01546","tags":["embedded"]},"id":"1001","type":"Row"},{"attributes":{},"id":"1082","type":"UnionRenderers"},{"attributes":{},"id":"1012","type":"LinearScale"},{"attributes":{"end":2014.0,"reset_end":2014.0,"reset_start":1960.0,"start":1960.0,"tags":[[["Year","Year",null]]]},"id":"1003","type":"Range1d"},{"attributes":{"line_alpha":0.1,"line_color":"#ff7e0e","line_width":2,"x":{"field":"Year"},"y":{"field":"value"}},"id":"1061","type":"Line"},{"attributes":{},"id":"1014","type":"LinearScale"},{"attributes":{"label":{"value":"Robbery"},"renderers":[{"id":"1047"}]},"id":"1056","type":"LegendItem"},{"attributes":{"text":"","text_color":{"value":"black"},"text_font_size":{"value":"12pt"}},"id":"1008","type":"Title"},{"attributes":{"end":4164053.0,"reset_end":4164053.0,"reset_start":-262183.0,"start":-262183.0,"tags":[[["value","value",null]]]},"id":"1004","type":"Range1d"},{"attributes":{},"id":"1025","type":"PanTool"},{"attributes":{"line_alpha":0.2,"line_color":"#1f77b3","line_width":2,"x":{"field":"Year"},"y":{"field":"value"}},"id":"1046","type":"Line"},{"attributes":{"axis":{"id":"1016"},"grid_line_color":null,"ticker":null},"id":"1019","type":"Grid"},{"attributes":{},"id":"1026","type":"WheelZoomTool"},{"attributes":{},"id":"1042","type":"Selection"},{"attributes":{"bottom_units":"screen","fill_alpha":0.5,"fill_color":"lightgrey","left_units":"screen","level":"overlay","line_alpha":1.0,"line_color":"black","line_dash":[4,4],"line_width":2,"render_mode":"css","right_units":"screen","top_units":"screen"},"id":"1029","type":"BoxAnnotation"},{"attributes":{"line_alpha":0.2,"line_color":"#ff7e0e","line_width":2,"x":{"field":"Year"},"y":{"field":"value"}},"id":"1062","type":"Line"},{"attributes":{},"id":"1024","type":"SaveTool"},{"attributes":{"overlay":{"id":"1029"}},"id":"1027","type":"BoxZoomTool"},{"attributes":{"line_color":"#ff7e0e","line_width":2,"x":{"field":"Year"},"y":{"field":"value"}},"id":"1060","type":"Line"},{"attributes":{"align":null,"below":[{"id":"1016"}],"center":[{"id":"1019"},{"id":"1023"}],"left":[{"id":"1020"}],"margin":null,"min_border_bottom":10,"min_border_left":10,"min_border_right":10,"min_border_top":10,"plot_height":300,"plot_width":700,"renderers":[{"id":"1047"},{"id":"1063"}],"right":[{"id":"1055"}],"sizing_mode":"fixed","title":{"id":"1008"},"toolbar":{"id":"1030"},"x_range":{"id":"1003"},"x_scale":{"id":"1012"},"y_range":{"id":"1004"},"y_scale":{"id":"1014"}},"id":"1007","subtype":"Figure","type":"Plot"},{"attributes":{},"id":"1028","type":"ResetTool"},{"attributes":{"axis":{"id":"1020"},"dimension":1,"grid_line_color":null,"ticker":null},"id":"1023","type":"Grid"},{"attributes":{"click_policy":"mute","items":[{"id":"1056"},{"id":"1073"}],"location":[0,0],"title":"Variable"},"id":"1055","type":"Legend"},{"attributes":{"active_drag":"auto","active_inspect":"auto","active_multi":null,"active_scroll":"auto","active_tap":"auto","tools":[{"id":"1005"},{"id":"1024"},{"id":"1025"},{"id":"1026"},{"id":"1027"},{"id":"1028"}]},"id":"1030","type":"Toolbar"},{"attributes":{"data_source":{"id":"1057"},"glyph":{"id":"1060"},"hover_glyph":null,"muted_glyph":{"id":"1062"},"nonselection_glyph":{"id":"1061"},"selection_glyph":null,"view":{"id":"1064"}},"id":"1063","type":"GlyphRenderer"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer01550","sizing_mode":"stretch_width"},"id":"1002","type":"Spacer"},{"attributes":{},"id":"1021","type":"BasicTicker"},{"attributes":{"source":{"id":"1057"}},"id":"1064","type":"CDSView"},{"attributes":{"line_color":"#1f77b3","line_width":2,"x":{"field":"Year"},"y":{"field":"value"}},"id":"1044","type":"Line"},{"attributes":{"axis_label":"","bounds":"auto","formatter":{"id":"1040"},"major_label_orientation":"horizontal","ticker":{"id":"1021"}},"id":"1020","type":"LinearAxis"},{"attributes":{"axis_label":"Year","bounds":"auto","formatter":{"id":"1038"},"major_label_orientation":"horizontal","ticker":{"id":"1017"}},"id":"1016","type":"LinearAxis"},{"attributes":{},"id":"1071","type":"UnionRenderers"},{"attributes":{},"id":"1040","type":"BasicTickFormatter"},{"attributes":{"data_source":{"id":"1041"},"glyph":{"id":"1044"},"hover_glyph":null,"muted_glyph":{"id":"1046"},"nonselection_glyph":{"id":"1045"},"selection_glyph":null,"view":{"id":"1048"}},"id":"1047","type":"GlyphRenderer"},{"attributes":{"label":{"value":"Burglary"},"renderers":[{"id":"1063"}]},"id":"1073","type":"LegendItem"},{"attributes":{},"id":"1017","type":"BasicTicker"},{"attributes":{},"id":"1058","type":"Selection"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer01551","sizing_mode":"stretch_width"},"id":"1154","type":"Spacer"},{"attributes":{"data":{"Variable":["Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary","Burglary"],"Year":[1960,1961,1962,1963,1964,1965,1966,1967,1968,1969,1970,1971,1972,1973,1974,1975,1976,1977,1978,1979,1980,1981,1982,1983,1984,1985,1986,1987,1988,1989,1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014],"value":[912100,949600,994300,1086400,1213200,1282500,1410100,1632100,1858900,1981900,2205000,2399300,2375500,2565500,3039200,3265300,3108700,3071500,3128300,3327700,3795200,3779700,3447100,3129851,2984434,3073348,3241410,3236184,3218077,3168170,3073909,3157150,2979884,2834808,2712774,2593784,2506400,2460526,2332735,2100739,2050992,2116531,2151252,2154834,2144446,2155448,2194993,2190198,2228887,2203313,2168459,2185140,2109932,1931835,1729806]},"selected":{"id":"1058"},"selection_policy":{"id":"1082"}},"id":"1057","type":"ColumnDataSource"},{"attributes":{},"id":"1038","type":"BasicTickFormatter"}],"root_ids":["1001"]},"title":"Bokeh Application","version":"2.0.1"}};
  var render_items = [{"docid":"94584295-61ba-4a7e-a89c-4dfa8a9d218a","root_ids":["1001"],"roots":{"1001":"c6e00f0c-c4cf-470f-9991-c66c5a7ded07"}}];
  root.Bokeh.embed.embed_items_notebook(docs_json, render_items);
  }
if (root.Bokeh !== undefined) {
    embed_document(root);
  } else {
    var attempts = 0;
    var timer = setInterval(function(root) {
      if (root.Bokeh !== undefined) {
        clearInterval(timer);
        embed_document(root);
      } else if (document.readyState == "complete") {
        attempts++;
        if (attempts > 100) {
          clearInterval(timer);
          console.log("Bokeh: ERROR: Unable to run BokehJS code because BokehJS library is missing");
        }
      }
    }, 10, root)
  }
})(window);</script>



### Plot Types
Use `df.hvplot.<TAB>`

### Getting Help
Multiple options
```python
df.hvplot.scatter(<Tab>)
df.hvplot.scatter(<Shift + Tab>)
df.hvplot.scatter?
```

### Customization

Just use arguments when calling `.plot()`. Type `df.hvplot.plot(<Tab>)` to get a list of arguments and `df.hvplot.plot(<Shift + Tab>)` to get a more detailed description.

See: https://hvplot.holoviz.org/user_guide/Customization.html

### Coloring
Use either `color=<color>` to color everything with same color or use `c=<color column>` (and optionally `cmap=<colormap>`) arguments.

List of colormaps: http://holoviews.org/user_guide/Colormaps.html


```python
df.hvplot.scatter(y='Robbery', c='Robbery', cmap='bgy')
```






<div id='1206'>





  <div class="bk-root" id="306f939f-73de-4f3e-926c-52c5036d35af" data-root-id="1206"></div>
</div>
<script type="application/javascript">
    function msg_handler(msg) {
      var metadata = msg.metadata;
      var buffers = msg.buffers;
      var msg = msg.content.data;
      if ((metadata.msg_type == "Ready")) {
        if (metadata.content) {
          console.log("Python callback returned following output:", metadata.content);
        }
      } else if (metadata.msg_type == "Error") {
        console.log("Python failed with the following traceback:", metadata.traceback)
      } else {

var plot_id = "1206";

if ((plot_id in window.PyViz.plot_index) && (window.PyViz.plot_index[plot_id] != null)) {
  var plot = window.PyViz.plot_index[plot_id];
} else if ((Bokeh !== undefined) && (plot_id in Bokeh.index)) {
  var plot = Bokeh.index[plot_id];
}

if (plot == null) {
  return
}

if (plot_id in window.PyViz.receivers) {
  var receiver = window.PyViz.receivers[plot_id];
} else {
  var receiver = new Bokeh.protocol.Receiver();
  window.PyViz.receivers[plot_id] = receiver;
}

if ((buffers != undefined) && (buffers.length > 0)) {
  receiver.consume(buffers[0].buffer)
} else {
  receiver.consume(msg)
}

const comm_msg = receiver.message;
if ((comm_msg != null) && (Object.keys(comm_msg.content).length > 0)) {
  plot.model.document.apply_json_patch(comm_msg.content, comm_msg.buffers)
}

      }
    }
    if ((window.PyViz == undefined) || (!window.PyViz.comm_manager)) {
      console.log("Could not find comm manager")
    } else {
      window.PyViz.comm_manager.register_target('1206', 'a7b5f797e90747ec94fdb68e37ae7853', msg_handler);
    }

(function(root) {
  function embed_document(root) {
  var docs_json = {"dda31fa6-2831-47ad-9de8-b5f3540c8169":{"roots":{"references":[{"attributes":{},"id":"1243","type":"Selection"},{"attributes":{"bottom_units":"screen","fill_alpha":0.5,"fill_color":"lightgrey","left_units":"screen","level":"overlay","line_alpha":1.0,"line_color":"black","line_dash":[4,4],"line_width":2,"render_mode":"css","right_units":"screen","top_units":"screen"},"id":"1233","type":"BoxAnnotation"},{"attributes":{"axis":{"id":"1224"},"dimension":1,"grid_line_color":null,"ticker":null},"id":"1227","type":"Grid"},{"attributes":{"align":null,"below":[{"id":"1220"}],"center":[{"id":"1223"},{"id":"1227"}],"left":[{"id":"1224"}],"margin":null,"min_border_bottom":10,"min_border_left":10,"min_border_right":10,"min_border_top":10,"plot_height":300,"plot_width":700,"renderers":[{"id":"1250"}],"right":[{"id":"1253"}],"sizing_mode":"fixed","title":{"id":"1212"},"toolbar":{"id":"1234"},"x_range":{"id":"1208"},"x_scale":{"id":"1216"},"y_range":{"id":"1209"},"y_scale":{"id":"1218"}},"id":"1211","subtype":"Figure","type":"Plot"},{"attributes":{"axis_label":"Robbery","bounds":"auto","formatter":{"id":"1258"},"major_label_orientation":"horizontal","ticker":{"id":"1225"}},"id":"1224","type":"LinearAxis"},{"attributes":{"high":687732.0,"low":106670.0,"palette":["#000c7c","#000c7e","#000d80","#000d82","#000e83","#000e85","#000f87","#000f89","#00108b","#00108c","#00118e","#001290","#001292","#001393","#001395","#001497","#001598","#00159a","#00169c","#00179d","#00179f","#0018a0","#0019a2","#001aa3","#001aa5","#001ba6","#001ca8","#001da9","#001eab","#001eac","#001fad","#0020af","#0021b0","#0022b1","#0023b2","#0024b3","#0025b4","#0026b5","#0027b6","#0028b7","#0029b8","#002ab8","#002bb9","#002cba","#002eba","#002fba","#0030bb","#0031bb","#0033bb","#0034bb","#0035bb","#0036bb","#0037bb","#0039bb","#003abb","#003bbb","#003cbb","#003dbb","#003fba","#0040ba","#0041ba","#0042b9","#0043b9","#0045b8","#0046b8","#0047b7","#0048b6","#0049b6","#004ab5","#004cb4","#004db3","#004eb2","#004fb2","#0050b1","#0052b0","#0053ae","#0054ad","#0055ac","#0056ab","#0057aa","#0059a9","#005aa8","#005ba7","#005ca5","#005da4","#005fa3","#0060a2","#0061a1","#0062a0","#00639e","#00649d","#00659c","#00679b","#00689a","#006998","#006a97","#006b96","#006c95","#006d93","#006f92","#007091","#00718f","#00728e","#00738d","#00748b","#00758a","#007689","#007887","#007986","#007a84","#007b83","#007c81","#007d80","#007e7e","#007f7d","#00807b","#008279","#008377","#008476","#028574","#068672","#098770","#0d886e","#10896c","#128a6a","#158b68","#178c66","#198d63","#1b8e61","#1d905f","#1f915c","#20925a","#229358","#239455","#259552","#269650","#28974d","#29984a","#2a9948","#2b9a45","#2c9b43","#2c9c40","#2d9d3e","#2d9e3b","#2e9f39","#2ea037","#2fa135","#2fa232","#2fa330","#30a52e","#30a62c","#30a72a","#30a828","#30a926","#31aa25","#31ab23","#31ac21","#31ad20","#31ae1f","#31af1d","#31b01c","#31b11b","#31b21a","#32b31a","#32b41a","#32b519","#32b619","#32b719","#32b819","#32b919","#32ba19","#32bb19","#33bc19","#33bd19","#33be19","#33bf19","#33c019","#33c119","#33c219","#33c319","#34c519","#34c619","#34c719","#34c819","#34c919","#34ca19","#35cb19","#35cc19","#35cd19","#35ce19","#35cf19","#35d019","#36d119","#36d219","#36d319","#36d419","#37d519","#38d619","#3bd719","#3dd819","#40d919","#44da19","#47da19","#4bdb19","#4fdc1a","#53dd1a","#57de1a","#5ade1a","#5edf1a","#62e01a","#66e01a","#6ae11a","#6ee21a","#72e21a","#76e31a","#7ae31b","#7ee41b","#82e51b","#86e51b","#8ae61b","#8ee61b","#91e71b","#95e71b","#99e81c","#9de81c","#a1e91c","#a4e91c","#a8ea1c","#acea1c","#b0ea1c","#b3eb1d","#b7eb1d","#bbec1d","#beec1d","#c2ec1d","#c6ed1e","#c9ed1e","#cded1e","#d1ee1e","#d4ee1e","#d8ee1f","#dcee1f","#dfef1f","#e3ef1f","#e7ef20","#eaef20","#eef020","#f2f020","#f5f021","#f9f021","#fcf021","#fff021","#fff022","#fff122","#fff122","#fff123"]},"id":"1241","type":"LinearColorMapper"},{"attributes":{"axis":{"id":"1220"},"grid_line_color":null,"ticker":null},"id":"1223","type":"Grid"},{"attributes":{"active_drag":"auto","active_inspect":"auto","active_multi":null,"active_scroll":"auto","active_tap":"auto","tools":[{"id":"1210"},{"id":"1228"},{"id":"1229"},{"id":"1230"},{"id":"1231"},{"id":"1232"}]},"id":"1234","type":"Toolbar"},{"attributes":{},"id":"1256","type":"BasicTickFormatter"},{"attributes":{"axis_label":"Year","bounds":"auto","formatter":{"id":"1256"},"major_label_orientation":"horizontal","ticker":{"id":"1221"}},"id":"1220","type":"LinearAxis"},{"attributes":{"end":2016.3142857142857,"reset_end":2016.3142857142857,"reset_start":1957.6857142857143,"start":1957.6857142857143,"tags":[[["Year","Year",null]]]},"id":"1208","type":"Range1d"},{"attributes":{},"id":"1232","type":"ResetTool"},{"attributes":{},"id":"1252","type":"BasicTicker"},{"attributes":{"bar_line_color":{"value":"black"},"color_mapper":{"id":"1241"},"formatter":{"id":"1262"},"label_standoff":8,"location":[0,0],"major_tick_line_color":"black","ticker":{"id":"1252"}},"id":"1253","type":"ColorBar"},{"attributes":{"text":"","text_color":{"value":"black"},"text_font_size":{"value":"12pt"}},"id":"1212","type":"Title"},{"attributes":{"data":{"Robbery":[107840,106670,110860,116470,130390,138690,157990,202910,262840,298850,349860,387700,376290,384220,442400,470500,427810,412610,426930,480700,565840,592910,553130,506567,485008,497874,542775,517704,542968,578326,639271,687732,672478,659870,618949,580509,535594,498534,447186,409371,408016,423557,420806,414235,401470,417438,449246,447324,443563,408742,369089,354772,355051,345095,325802],"Year":[1960,1961,1962,1963,1964,1965,1966,1967,1968,1969,1970,1971,1972,1973,1974,1975,1976,1977,1978,1979,1980,1981,1982,1983,1984,1985,1986,1987,1988,1989,1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014],"color":[107840,106670,110860,116470,130390,138690,157990,202910,262840,298850,349860,387700,376290,384220,442400,470500,427810,412610,426930,480700,565840,592910,553130,506567,485008,497874,542775,517704,542968,578326,639271,687732,672478,659870,618949,580509,535594,498534,447186,409371,408016,423557,420806,414235,401470,417438,449246,447324,443563,408742,369089,354772,355051,345095,325802]},"selected":{"id":"1243"},"selection_policy":{"id":"1266"}},"id":"1242","type":"ColumnDataSource"},{"attributes":{},"id":"1230","type":"WheelZoomTool"},{"attributes":{"overlay":{"id":"1233"}},"id":"1231","type":"BoxZoomTool"},{"attributes":{"data_source":{"id":"1242"},"glyph":{"id":"1245"},"hover_glyph":{"id":"1248"},"muted_glyph":{"id":"1249"},"nonselection_glyph":{"id":"1246"},"selection_glyph":{"id":"1247"},"view":{"id":"1251"}},"id":"1250","type":"GlyphRenderer"},{"attributes":{},"id":"1262","type":"BasicTickFormatter"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer01958","sizing_mode":"stretch_width"},"id":"1268","type":"Spacer"},{"attributes":{},"id":"1216","type":"LinearScale"},{"attributes":{},"id":"1229","type":"PanTool"},{"attributes":{},"id":"1225","type":"BasicTicker"},{"attributes":{},"id":"1228","type":"SaveTool"},{"attributes":{},"id":"1266","type":"UnionRenderers"},{"attributes":{"children":[{"id":"1207"},{"id":"1211"},{"id":"1268"}],"margin":[0,0,0,0],"name":"Row01953","tags":["embedded"]},"id":"1206","type":"Row"},{"attributes":{"end":745838.2,"reset_end":745838.2,"reset_start":48563.799999999996,"start":48563.799999999996,"tags":[[["Robbery","Robbery",null]]]},"id":"1209","type":"Range1d"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer01957","sizing_mode":"stretch_width"},"id":"1207","type":"Spacer"},{"attributes":{"source":{"id":"1242"}},"id":"1251","type":"CDSView"},{"attributes":{"callback":null,"renderers":[{"id":"1250"}],"tags":["hv_created"],"tooltips":[["Year","@{Year}"],["Robbery","@{Robbery}"]]},"id":"1210","type":"HoverTool"},{"attributes":{"fill_color":{"field":"color","transform":{"id":"1241"}},"line_color":{"field":"color","transform":{"id":"1241"}},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1245","type":"Scatter"},{"attributes":{},"id":"1218","type":"LinearScale"},{"attributes":{"fill_color":{"field":"color","transform":{"id":"1241"}},"line_color":{"field":"color","transform":{"id":"1241"}},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1247","type":"Scatter"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"field":"color","transform":{"id":"1241"}},"line_alpha":{"value":0.1},"line_color":{"field":"color","transform":{"id":"1241"}},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1246","type":"Scatter"},{"attributes":{},"id":"1258","type":"BasicTickFormatter"},{"attributes":{"fill_color":{"field":"color","transform":{"id":"1241"}},"line_color":{"field":"color","transform":{"id":"1241"}},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1248","type":"Scatter"},{"attributes":{},"id":"1221","type":"BasicTicker"},{"attributes":{"fill_alpha":{"value":0.2},"fill_color":{"field":"color","transform":{"id":"1241"}},"line_alpha":{"value":0.2},"line_color":{"field":"color","transform":{"id":"1241"}},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1249","type":"Scatter"}],"root_ids":["1206"]},"title":"Bokeh Application","version":"2.0.1"}};
  var render_items = [{"docid":"dda31fa6-2831-47ad-9de8-b5f3540c8169","root_ids":["1206"],"roots":{"1206":"306f939f-73de-4f3e-926c-52c5036d35af"}}];
  root.Bokeh.embed.embed_items_notebook(docs_json, render_items);
  }
if (root.Bokeh !== undefined) {
    embed_document(root);
  } else {
    var attempts = 0;
    var timer = setInterval(function(root) {
      if (root.Bokeh !== undefined) {
        clearInterval(timer);
        embed_document(root);
      } else if (document.readyState == "complete") {
        attempts++;
        if (attempts > 100) {
          clearInterval(timer);
          console.log("Bokeh: ERROR: Unable to run BokehJS code because BokehJS library is missing");
        }
      }
    }, 10, root)
  }
})(window);</script>



### Composing Plots
See: http://holoviews.org/user_guide/Composing_Elements.html

#### Overlay
Put one plot over another


```python
robbery = df.hvplot.scatter(y='Robbery')
burglary = df.hvplot.scatter(y='Burglary')

robbery * burglary
```






<div id='1315'>





  <div class="bk-root" id="5efeb748-f139-4f76-b2a5-e8e87565fb97" data-root-id="1315"></div>
</div>
<script type="application/javascript">
    function msg_handler(msg) {
      var metadata = msg.metadata;
      var buffers = msg.buffers;
      var msg = msg.content.data;
      if ((metadata.msg_type == "Ready")) {
        if (metadata.content) {
          console.log("Python callback returned following output:", metadata.content);
        }
      } else if (metadata.msg_type == "Error") {
        console.log("Python failed with the following traceback:", metadata.traceback)
      } else {

var plot_id = "1315";

if ((plot_id in window.PyViz.plot_index) && (window.PyViz.plot_index[plot_id] != null)) {
  var plot = window.PyViz.plot_index[plot_id];
} else if ((Bokeh !== undefined) && (plot_id in Bokeh.index)) {
  var plot = Bokeh.index[plot_id];
}

if (plot == null) {
  return
}

if (plot_id in window.PyViz.receivers) {
  var receiver = window.PyViz.receivers[plot_id];
} else {
  var receiver = new Bokeh.protocol.Receiver();
  window.PyViz.receivers[plot_id] = receiver;
}

if ((buffers != undefined) && (buffers.length > 0)) {
  receiver.consume(buffers[0].buffer)
} else {
  receiver.consume(msg)
}

const comm_msg = receiver.message;
if ((comm_msg != null) && (Object.keys(comm_msg.content).length > 0)) {
  plot.model.document.apply_json_patch(comm_msg.content, comm_msg.buffers)
}

      }
    }
    if ((window.PyViz == undefined) || (!window.PyViz.comm_manager)) {
      console.log("Could not find comm manager")
    } else {
      window.PyViz.comm_manager.register_target('1315', '12b6f43bd5b943a4ab132c3eb1308b29', msg_handler);
    }

(function(root) {
  function embed_document(root) {
  var docs_json = {"d94c4c4e-7448-4f50-9fce-02c027b7d419":{"roots":{"references":[{"attributes":{},"id":"1380","type":"UnionRenderers"},{"attributes":{"children":[{"id":"1316"},{"id":"1321"},{"id":"1452"}],"margin":[0,0,0,0],"name":"Row02178","tags":["embedded"]},"id":"1315","type":"Row"},{"attributes":{"callback":null,"renderers":[{"id":"1370"}],"tags":["hv_created"],"tooltips":[["Year","@{Year}"],["Burglary","@{Burglary}"]]},"id":"1320","type":"HoverTool"},{"attributes":{},"id":"1357","type":"Selection"},{"attributes":{"end":2016.3142857142857,"reset_end":2016.3142857142857,"reset_start":1957.6857142857143,"start":1957.6857142857143,"tags":[[["Year","Year",null]]]},"id":"1317","type":"Range1d"},{"attributes":{"axis_label":"Robbery","bounds":"auto","formatter":{"id":"1355"},"major_label_orientation":"horizontal","ticker":{"id":"1335"}},"id":"1334","type":"LinearAxis"},{"attributes":{"fill_alpha":{"value":0.2},"fill_color":{"value":"#1f77b3"},"line_alpha":{"value":0.2},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1361","type":"Scatter"},{"attributes":{},"id":"1328","type":"LinearScale"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"value":"#1f77b3"},"line_alpha":{"value":0.1},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1360","type":"Scatter"},{"attributes":{},"id":"1338","type":"SaveTool"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer02182","sizing_mode":"stretch_width"},"id":"1316","type":"Spacer"},{"attributes":{},"id":"1339","type":"PanTool"},{"attributes":{"callback":null,"renderers":[{"id":"1362"}],"tags":["hv_created"],"tooltips":[["Year","@{Year}"],["Robbery","@{Robbery}"]]},"id":"1319","type":"HoverTool"},{"attributes":{"fill_color":{"value":"#1f77b3"},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1359","type":"Scatter"},{"attributes":{"overlay":{"id":"1343"}},"id":"1341","type":"BoxZoomTool"},{"attributes":{"axis_label":"Year","bounds":"auto","formatter":{"id":"1353"},"major_label_orientation":"horizontal","ticker":{"id":"1331"}},"id":"1330","type":"LinearAxis"},{"attributes":{"source":{"id":"1356"}},"id":"1363","type":"CDSView"},{"attributes":{},"id":"1340","type":"WheelZoomTool"},{"attributes":{},"id":"1378","type":"UnionRenderers"},{"attributes":{"data_source":{"id":"1356"},"glyph":{"id":"1359"},"hover_glyph":null,"muted_glyph":{"id":"1361"},"nonselection_glyph":{"id":"1360"},"selection_glyph":null,"view":{"id":"1363"}},"id":"1362","type":"GlyphRenderer"},{"attributes":{},"id":"1331","type":"BasicTicker"},{"attributes":{},"id":"1326","type":"LinearScale"},{"attributes":{"fill_color":{"value":"#ff7e0e"},"line_color":{"value":"#ff7e0e"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Burglary"}},"id":"1367","type":"Scatter"},{"attributes":{"text":"","text_color":{"value":"black"},"text_font_size":{"value":"12pt"}},"id":"1322","type":"Title"},{"attributes":{"data_source":{"id":"1364"},"glyph":{"id":"1367"},"hover_glyph":null,"muted_glyph":{"id":"1369"},"nonselection_glyph":{"id":"1368"},"selection_glyph":null,"view":{"id":"1371"}},"id":"1370","type":"GlyphRenderer"},{"attributes":{"end":4164053.0,"reset_end":4164053.0,"reset_start":-262183.0,"start":-262183.0,"tags":[[["Robbery","Robbery",null]]]},"id":"1318","type":"Range1d"},{"attributes":{"align":null,"below":[{"id":"1330"}],"center":[{"id":"1333"},{"id":"1337"}],"left":[{"id":"1334"}],"margin":null,"min_border_bottom":10,"min_border_left":10,"min_border_right":10,"min_border_top":10,"plot_height":300,"plot_width":700,"renderers":[{"id":"1362"},{"id":"1370"}],"sizing_mode":"fixed","title":{"id":"1322"},"toolbar":{"id":"1344"},"x_range":{"id":"1317"},"x_scale":{"id":"1326"},"y_range":{"id":"1318"},"y_scale":{"id":"1328"}},"id":"1321","subtype":"Figure","type":"Plot"},{"attributes":{"axis":{"id":"1330"},"grid_line_color":null,"ticker":null},"id":"1333","type":"Grid"},{"attributes":{"bottom_units":"screen","fill_alpha":0.5,"fill_color":"lightgrey","left_units":"screen","level":"overlay","line_alpha":1.0,"line_color":"black","line_dash":[4,4],"line_width":2,"render_mode":"css","right_units":"screen","top_units":"screen"},"id":"1343","type":"BoxAnnotation"},{"attributes":{"fill_alpha":{"value":0.2},"fill_color":{"value":"#ff7e0e"},"line_alpha":{"value":0.2},"line_color":{"value":"#ff7e0e"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Burglary"}},"id":"1369","type":"Scatter"},{"attributes":{},"id":"1342","type":"ResetTool"},{"attributes":{"active_drag":"auto","active_inspect":"auto","active_multi":null,"active_scroll":"auto","active_tap":"auto","tools":[{"id":"1319"},{"id":"1320"},{"id":"1338"},{"id":"1339"},{"id":"1340"},{"id":"1341"},{"id":"1342"}]},"id":"1344","type":"Toolbar"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"value":"#ff7e0e"},"line_alpha":{"value":0.1},"line_color":{"value":"#ff7e0e"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Burglary"}},"id":"1368","type":"Scatter"},{"attributes":{},"id":"1355","type":"BasicTickFormatter"},{"attributes":{"axis":{"id":"1334"},"dimension":1,"grid_line_color":null,"ticker":null},"id":"1337","type":"Grid"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer02183","sizing_mode":"stretch_width"},"id":"1452","type":"Spacer"},{"attributes":{"data":{"Burglary":[912100,949600,994300,1086400,1213200,1282500,1410100,1632100,1858900,1981900,2205000,2399300,2375500,2565500,3039200,3265300,3108700,3071500,3128300,3327700,3795200,3779700,3447100,3129851,2984434,3073348,3241410,3236184,3218077,3168170,3073909,3157150,2979884,2834808,2712774,2593784,2506400,2460526,2332735,2100739,2050992,2116531,2151252,2154834,2144446,2155448,2194993,2190198,2228887,2203313,2168459,2185140,2109932,1931835,1729806],"Year":[1960,1961,1962,1963,1964,1965,1966,1967,1968,1969,1970,1971,1972,1973,1974,1975,1976,1977,1978,1979,1980,1981,1982,1983,1984,1985,1986,1987,1988,1989,1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014]},"selected":{"id":"1365"},"selection_policy":{"id":"1380"}},"id":"1364","type":"ColumnDataSource"},{"attributes":{},"id":"1353","type":"BasicTickFormatter"},{"attributes":{},"id":"1365","type":"Selection"},{"attributes":{"data":{"Robbery":[107840,106670,110860,116470,130390,138690,157990,202910,262840,298850,349860,387700,376290,384220,442400,470500,427810,412610,426930,480700,565840,592910,553130,506567,485008,497874,542775,517704,542968,578326,639271,687732,672478,659870,618949,580509,535594,498534,447186,409371,408016,423557,420806,414235,401470,417438,449246,447324,443563,408742,369089,354772,355051,345095,325802],"Year":[1960,1961,1962,1963,1964,1965,1966,1967,1968,1969,1970,1971,1972,1973,1974,1975,1976,1977,1978,1979,1980,1981,1982,1983,1984,1985,1986,1987,1988,1989,1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014]},"selected":{"id":"1357"},"selection_policy":{"id":"1378"}},"id":"1356","type":"ColumnDataSource"},{"attributes":{},"id":"1335","type":"BasicTicker"},{"attributes":{"source":{"id":"1364"}},"id":"1371","type":"CDSView"}],"root_ids":["1315"]},"title":"Bokeh Application","version":"2.0.1"}};
  var render_items = [{"docid":"d94c4c4e-7448-4f50-9fce-02c027b7d419","root_ids":["1315"],"roots":{"1315":"5efeb748-f139-4f76-b2a5-e8e87565fb97"}}];
  root.Bokeh.embed.embed_items_notebook(docs_json, render_items);
  }
if (root.Bokeh !== undefined) {
    embed_document(root);
  } else {
    var attempts = 0;
    var timer = setInterval(function(root) {
      if (root.Bokeh !== undefined) {
        clearInterval(timer);
        embed_document(root);
      } else if (document.readyState == "complete") {
        attempts++;
        if (attempts > 100) {
          clearInterval(timer);
          console.log("Bokeh: ERROR: Unable to run BokehJS code because BokehJS library is missing");
        }
      }
    }, 10, root)
  }
})(window);</script>



#### Side by Side


```python
robbery + burglary
```






<div id='1504'>





  <div class="bk-root" id="d8242f5f-bb94-4a88-b10f-706c860a98bf" data-root-id="1504"></div>
</div>
<script type="application/javascript">
    function msg_handler(msg) {
      var metadata = msg.metadata;
      var buffers = msg.buffers;
      var msg = msg.content.data;
      if ((metadata.msg_type == "Ready")) {
        if (metadata.content) {
          console.log("Python callback returned following output:", metadata.content);
        }
      } else if (metadata.msg_type == "Error") {
        console.log("Python failed with the following traceback:", metadata.traceback)
      } else {

var plot_id = "1504";

if ((plot_id in window.PyViz.plot_index) && (window.PyViz.plot_index[plot_id] != null)) {
  var plot = window.PyViz.plot_index[plot_id];
} else if ((Bokeh !== undefined) && (plot_id in Bokeh.index)) {
  var plot = Bokeh.index[plot_id];
}

if (plot == null) {
  return
}

if (plot_id in window.PyViz.receivers) {
  var receiver = window.PyViz.receivers[plot_id];
} else {
  var receiver = new Bokeh.protocol.Receiver();
  window.PyViz.receivers[plot_id] = receiver;
}

if ((buffers != undefined) && (buffers.length > 0)) {
  receiver.consume(buffers[0].buffer)
} else {
  receiver.consume(msg)
}

const comm_msg = receiver.message;
if ((comm_msg != null) && (Object.keys(comm_msg.content).length > 0)) {
  plot.model.document.apply_json_patch(comm_msg.content, comm_msg.buffers)
}

      }
    }
    if ((window.PyViz == undefined) || (!window.PyViz.comm_manager)) {
      console.log("Could not find comm manager")
    } else {
      window.PyViz.comm_manager.register_target('1504', '1e4f2d6144d54dc0bf2a54b7ac42501a', msg_handler);
    }

(function(root) {
  function embed_document(root) {
  var docs_json = {"8c0b7786-f1fa-4680-b51a-9f84387e3cd8":{"roots":{"references":[{"attributes":{"children":[{"id":"1615"},{"id":"1613"}]},"id":"1616","type":"Column"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"value":"#1f77b3"},"line_alpha":{"value":0.1},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1543","type":"Scatter"},{"attributes":{},"id":"1592","type":"BasicTickFormatter"},{"attributes":{"data_source":{"id":"1583"},"glyph":{"id":"1586"},"hover_glyph":null,"muted_glyph":{"id":"1588"},"nonselection_glyph":{"id":"1587"},"selection_glyph":null,"view":{"id":"1590"}},"id":"1589","type":"GlyphRenderer"},{"attributes":{"children":[{"id":"1505"},{"id":"1616"},{"id":"1745"}],"margin":[0,0,0,0],"name":"Row02510","tags":["embedded"]},"id":"1504","type":"Row"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer02515","sizing_mode":"stretch_width"},"id":"1745","type":"Spacer"},{"attributes":{"fill_alpha":{"value":0.2},"fill_color":{"value":"#1f77b3"},"line_alpha":{"value":0.2},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1544","type":"Scatter"},{"attributes":{},"id":"1594","type":"BasicTickFormatter"},{"attributes":{},"id":"1572","type":"WheelZoomTool"},{"attributes":{"end":4083510.0,"reset_end":4083510.0,"reset_start":623790.0,"start":623790.0,"tags":[[["Burglary","Burglary",null]]]},"id":"1551","type":"Range1d"},{"attributes":{"active_drag":"auto","active_inspect":"auto","active_multi":null,"active_scroll":"auto","active_tap":"auto","tools":[{"id":"1508"},{"id":"1526"},{"id":"1527"},{"id":"1528"},{"id":"1529"},{"id":"1530"}]},"id":"1532","type":"Toolbar"},{"attributes":{"fill_color":{"value":"#1f77b3"},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Burglary"}},"id":"1586","type":"Scatter"},{"attributes":{},"id":"1571","type":"PanTool"},{"attributes":{"end":2016.3142857142857,"reset_end":2016.3142857142857,"reset_start":1957.6857142857143,"start":1957.6857142857143,"tags":[[["Year","Year",null]]]},"id":"1506","type":"Range1d"},{"attributes":{"bottom_units":"screen","fill_alpha":0.5,"fill_color":"lightgrey","left_units":"screen","level":"overlay","line_alpha":1.0,"line_color":"black","line_dash":[4,4],"line_width":2,"render_mode":"css","right_units":"screen","top_units":"screen"},"id":"1531","type":"BoxAnnotation"},{"attributes":{},"id":"1570","type":"SaveTool"},{"attributes":{"end":745838.2,"reset_end":745838.2,"reset_start":48563.799999999996,"start":48563.799999999996,"tags":[[["Robbery","Robbery",null]]]},"id":"1507","type":"Range1d"},{"attributes":{"callback":null,"renderers":[{"id":"1545"}],"tags":["hv_created"],"tooltips":[["Year","@{Year}"],["Robbery","@{Robbery}"]]},"id":"1508","type":"HoverTool"},{"attributes":{},"id":"1540","type":"Selection"},{"attributes":{"toolbar":{"id":"1614"},"toolbar_location":"above"},"id":"1615","type":"ToolbarBox"},{"attributes":{"callback":null,"renderers":[{"id":"1589"}],"tags":["hv_created"],"tooltips":[["Year","@{Year}"],["Burglary","@{Burglary}"]]},"id":"1552","type":"HoverTool"},{"attributes":{"source":{"id":"1583"}},"id":"1590","type":"CDSView"},{"attributes":{"toolbars":[{"id":"1532"},{"id":"1576"}],"tools":[{"id":"1508"},{"id":"1526"},{"id":"1527"},{"id":"1528"},{"id":"1529"},{"id":"1530"},{"id":"1552"},{"id":"1570"},{"id":"1571"},{"id":"1572"},{"id":"1573"},{"id":"1574"}]},"id":"1614","type":"ProxyToolbar"},{"attributes":{"overlay":{"id":"1531"}},"id":"1529","type":"BoxZoomTool"},{"attributes":{"axis_label":"Burglary","bounds":"auto","formatter":{"id":"1594"},"major_label_orientation":"horizontal","ticker":{"id":"1567"}},"id":"1566","type":"LinearAxis"},{"attributes":{"axis":{"id":"1566"},"dimension":1,"grid_line_color":null,"ticker":null},"id":"1569","type":"Grid"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer02514","sizing_mode":"stretch_width"},"id":"1505","type":"Spacer"},{"attributes":{"axis":{"id":"1562"},"grid_line_color":null,"ticker":null},"id":"1565","type":"Grid"},{"attributes":{"align":null,"below":[{"id":"1518"}],"center":[{"id":"1521"},{"id":"1525"}],"left":[{"id":"1522"}],"margin":null,"min_border_bottom":10,"min_border_left":10,"min_border_right":10,"min_border_top":10,"plot_height":300,"plot_width":700,"renderers":[{"id":"1545"}],"sizing_mode":"fixed","title":{"id":"1510"},"toolbar":{"id":"1532"},"toolbar_location":null,"x_range":{"id":"1506"},"x_scale":{"id":"1514"},"y_range":{"id":"1507"},"y_scale":{"id":"1516"}},"id":"1509","subtype":"Figure","type":"Plot"},{"attributes":{},"id":"1563","type":"BasicTicker"},{"attributes":{},"id":"1567","type":"BasicTicker"},{"attributes":{"data_source":{"id":"1539"},"glyph":{"id":"1542"},"hover_glyph":null,"muted_glyph":{"id":"1544"},"nonselection_glyph":{"id":"1543"},"selection_glyph":null,"view":{"id":"1546"}},"id":"1545","type":"GlyphRenderer"},{"attributes":{"text":"","text_color":{"value":"black"},"text_font_size":{"value":"12pt"}},"id":"1510","type":"Title"},{"attributes":{"source":{"id":"1539"}},"id":"1546","type":"CDSView"},{"attributes":{},"id":"1558","type":"LinearScale"},{"attributes":{"fill_color":{"value":"#1f77b3"},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1542","type":"Scatter"},{"attributes":{},"id":"1514","type":"LinearScale"},{"attributes":{"axis_label":"Year","bounds":"auto","formatter":{"id":"1592"},"major_label_orientation":"horizontal","ticker":{"id":"1563"}},"id":"1562","type":"LinearAxis"},{"attributes":{},"id":"1516","type":"LinearScale"},{"attributes":{"axis_label":"Year","bounds":"auto","formatter":{"id":"1548"},"major_label_orientation":"horizontal","ticker":{"id":"1519"}},"id":"1518","type":"LinearAxis"},{"attributes":{"text":"","text_color":{"value":"black"},"text_font_size":{"value":"12pt"}},"id":"1554","type":"Title"},{"attributes":{"children":[[{"id":"1509"},0,0],[{"id":"1553"},0,1]]},"id":"1613","type":"GridBox"},{"attributes":{},"id":"1548","type":"BasicTickFormatter"},{"attributes":{},"id":"1560","type":"LinearScale"},{"attributes":{},"id":"1519","type":"BasicTicker"},{"attributes":{"axis":{"id":"1518"},"grid_line_color":null,"ticker":null},"id":"1521","type":"Grid"},{"attributes":{"data":{"Burglary":[912100,949600,994300,1086400,1213200,1282500,1410100,1632100,1858900,1981900,2205000,2399300,2375500,2565500,3039200,3265300,3108700,3071500,3128300,3327700,3795200,3779700,3447100,3129851,2984434,3073348,3241410,3236184,3218077,3168170,3073909,3157150,2979884,2834808,2712774,2593784,2506400,2460526,2332735,2100739,2050992,2116531,2151252,2154834,2144446,2155448,2194993,2190198,2228887,2203313,2168459,2185140,2109932,1931835,1729806],"Year":[1960,1961,1962,1963,1964,1965,1966,1967,1968,1969,1970,1971,1972,1973,1974,1975,1976,1977,1978,1979,1980,1981,1982,1983,1984,1985,1986,1987,1988,1989,1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014]},"selected":{"id":"1584"},"selection_policy":{"id":"1610"}},"id":"1583","type":"ColumnDataSource"},{"attributes":{"axis_label":"Robbery","bounds":"auto","formatter":{"id":"1550"},"major_label_orientation":"horizontal","ticker":{"id":"1523"}},"id":"1522","type":"LinearAxis"},{"attributes":{},"id":"1530","type":"ResetTool"},{"attributes":{"align":null,"below":[{"id":"1562"}],"center":[{"id":"1565"},{"id":"1569"}],"left":[{"id":"1566"}],"margin":null,"min_border_bottom":10,"min_border_left":10,"min_border_right":10,"min_border_top":10,"plot_height":300,"plot_width":700,"renderers":[{"id":"1589"}],"sizing_mode":"fixed","title":{"id":"1554"},"toolbar":{"id":"1576"},"toolbar_location":null,"x_range":{"id":"1506"},"x_scale":{"id":"1558"},"y_range":{"id":"1551"},"y_scale":{"id":"1560"}},"id":"1553","subtype":"Figure","type":"Plot"},{"attributes":{"fill_alpha":{"value":0.2},"fill_color":{"value":"#1f77b3"},"line_alpha":{"value":0.2},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Burglary"}},"id":"1588","type":"Scatter"},{"attributes":{"axis":{"id":"1522"},"dimension":1,"grid_line_color":null,"ticker":null},"id":"1525","type":"Grid"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"value":"#1f77b3"},"line_alpha":{"value":0.1},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Burglary"}},"id":"1587","type":"Scatter"},{"attributes":{},"id":"1610","type":"UnionRenderers"},{"attributes":{},"id":"1526","type":"SaveTool"},{"attributes":{},"id":"1527","type":"PanTool"},{"attributes":{},"id":"1584","type":"Selection"},{"attributes":{"bottom_units":"screen","fill_alpha":0.5,"fill_color":"lightgrey","left_units":"screen","level":"overlay","line_alpha":1.0,"line_color":"black","line_dash":[4,4],"line_width":2,"render_mode":"css","right_units":"screen","top_units":"screen"},"id":"1575","type":"BoxAnnotation"},{"attributes":{"data":{"Robbery":[107840,106670,110860,116470,130390,138690,157990,202910,262840,298850,349860,387700,376290,384220,442400,470500,427810,412610,426930,480700,565840,592910,553130,506567,485008,497874,542775,517704,542968,578326,639271,687732,672478,659870,618949,580509,535594,498534,447186,409371,408016,423557,420806,414235,401470,417438,449246,447324,443563,408742,369089,354772,355051,345095,325802],"Year":[1960,1961,1962,1963,1964,1965,1966,1967,1968,1969,1970,1971,1972,1973,1974,1975,1976,1977,1978,1979,1980,1981,1982,1983,1984,1985,1986,1987,1988,1989,1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014]},"selected":{"id":"1540"},"selection_policy":{"id":"1601"}},"id":"1539","type":"ColumnDataSource"},{"attributes":{"active_drag":"auto","active_inspect":"auto","active_multi":null,"active_scroll":"auto","active_tap":"auto","tools":[{"id":"1552"},{"id":"1570"},{"id":"1571"},{"id":"1572"},{"id":"1573"},{"id":"1574"}]},"id":"1576","type":"Toolbar"},{"attributes":{},"id":"1523","type":"BasicTicker"},{"attributes":{},"id":"1550","type":"BasicTickFormatter"},{"attributes":{},"id":"1528","type":"WheelZoomTool"},{"attributes":{"overlay":{"id":"1575"}},"id":"1573","type":"BoxZoomTool"},{"attributes":{},"id":"1601","type":"UnionRenderers"},{"attributes":{},"id":"1574","type":"ResetTool"}],"root_ids":["1504"]},"title":"Bokeh Application","version":"2.0.1"}};
  var render_items = [{"docid":"8c0b7786-f1fa-4680-b51a-9f84387e3cd8","root_ids":["1504"],"roots":{"1504":"d8242f5f-bb94-4a88-b10f-706c860a98bf"}}];
  root.Bokeh.embed.embed_items_notebook(docs_json, render_items);
  }
if (root.Bokeh !== undefined) {
    embed_document(root);
  } else {
    var attempts = 0;
    var timer = setInterval(function(root) {
      if (root.Bokeh !== undefined) {
        clearInterval(timer);
        embed_document(root);
      } else if (document.readyState == "complete") {
        attempts++;
        if (attempts > 100) {
          clearInterval(timer);
          console.log("Bokeh: ERROR: Unable to run BokehJS code because BokehJS library is missing");
        }
      }
    }, 10, root)
  }
})(window);</script>



#### Stacked


```python
(robbery + burglary).cols(1)
```






<div id='1827'>





  <div class="bk-root" id="44fb4261-86c9-4671-8ab2-a8cc3b599c0b" data-root-id="1827"></div>
</div>
<script type="application/javascript">
    function msg_handler(msg) {
      var metadata = msg.metadata;
      var buffers = msg.buffers;
      var msg = msg.content.data;
      if ((metadata.msg_type == "Ready")) {
        if (metadata.content) {
          console.log("Python callback returned following output:", metadata.content);
        }
      } else if (metadata.msg_type == "Error") {
        console.log("Python failed with the following traceback:", metadata.traceback)
      } else {

var plot_id = "1827";

if ((plot_id in window.PyViz.plot_index) && (window.PyViz.plot_index[plot_id] != null)) {
  var plot = window.PyViz.plot_index[plot_id];
} else if ((Bokeh !== undefined) && (plot_id in Bokeh.index)) {
  var plot = Bokeh.index[plot_id];
}

if (plot == null) {
  return
}

if (plot_id in window.PyViz.receivers) {
  var receiver = window.PyViz.receivers[plot_id];
} else {
  var receiver = new Bokeh.protocol.Receiver();
  window.PyViz.receivers[plot_id] = receiver;
}

if ((buffers != undefined) && (buffers.length > 0)) {
  receiver.consume(buffers[0].buffer)
} else {
  receiver.consume(msg)
}

const comm_msg = receiver.message;
if ((comm_msg != null) && (Object.keys(comm_msg.content).length > 0)) {
  plot.model.document.apply_json_patch(comm_msg.content, comm_msg.buffers)
}

      }
    }
    if ((window.PyViz == undefined) || (!window.PyViz.comm_manager)) {
      console.log("Could not find comm manager")
    } else {
      window.PyViz.comm_manager.register_target('1827', '674b45c579ee402ea77a1c3e70190002', msg_handler);
    }

(function(root) {
  function embed_document(root) {
  var docs_json = {"fa02b320-7a94-4e0f-b577-14f4ec411364":{"roots":{"references":[{"attributes":{"children":[{"id":"1938"},{"id":"1936"}]},"id":"1939","type":"Column"},{"attributes":{},"id":"1871","type":"BasicTickFormatter"},{"attributes":{"fill_alpha":{"value":0.2},"fill_color":{"value":"#1f77b3"},"line_alpha":{"value":0.2},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Burglary"}},"id":"1911","type":"Scatter"},{"attributes":{"active_drag":"auto","active_inspect":"auto","active_multi":null,"active_scroll":"auto","active_tap":"auto","tools":[{"id":"1875"},{"id":"1893"},{"id":"1894"},{"id":"1895"},{"id":"1896"},{"id":"1897"}]},"id":"1899","type":"Toolbar"},{"attributes":{"data_source":{"id":"1906"},"glyph":{"id":"1909"},"hover_glyph":null,"muted_glyph":{"id":"1911"},"nonselection_glyph":{"id":"1910"},"selection_glyph":null,"view":{"id":"1913"}},"id":"1912","type":"GlyphRenderer"},{"attributes":{"text":"","text_color":{"value":"black"},"text_font_size":{"value":"12pt"}},"id":"1833","type":"Title"},{"attributes":{"bottom_units":"screen","fill_alpha":0.5,"fill_color":"lightgrey","left_units":"screen","level":"overlay","line_alpha":1.0,"line_color":"black","line_dash":[4,4],"line_width":2,"render_mode":"css","right_units":"screen","top_units":"screen"},"id":"1898","type":"BoxAnnotation"},{"attributes":{},"id":"1873","type":"BasicTickFormatter"},{"attributes":{},"id":"1895","type":"WheelZoomTool"},{"attributes":{"align":null,"below":[{"id":"1841"}],"center":[{"id":"1844"},{"id":"1848"}],"left":[{"id":"1845"}],"margin":null,"min_border_bottom":10,"min_border_left":10,"min_border_right":10,"min_border_top":10,"plot_height":300,"plot_width":700,"renderers":[{"id":"1868"}],"sizing_mode":"fixed","title":{"id":"1833"},"toolbar":{"id":"1855"},"toolbar_location":null,"x_range":{"id":"1829"},"x_scale":{"id":"1837"},"y_range":{"id":"1830"},"y_scale":{"id":"1839"}},"id":"1832","subtype":"Figure","type":"Plot"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"value":"#1f77b3"},"line_alpha":{"value":0.1},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Burglary"}},"id":"1910","type":"Scatter"},{"attributes":{"source":{"id":"1906"}},"id":"1913","type":"CDSView"},{"attributes":{},"id":"1850","type":"PanTool"},{"attributes":{"bottom_units":"screen","fill_alpha":0.5,"fill_color":"lightgrey","left_units":"screen","level":"overlay","line_alpha":1.0,"line_color":"black","line_dash":[4,4],"line_width":2,"render_mode":"css","right_units":"screen","top_units":"screen"},"id":"1854","type":"BoxAnnotation"},{"attributes":{},"id":"1924","type":"UnionRenderers"},{"attributes":{},"id":"1907","type":"Selection"},{"attributes":{"axis":{"id":"1889"},"dimension":1,"grid_line_color":null,"ticker":null},"id":"1892","type":"Grid"},{"attributes":{},"id":"1842","type":"BasicTicker"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer02800","sizing_mode":"stretch_width"},"id":"2068","type":"Spacer"},{"attributes":{"fill_color":{"value":"#1f77b3"},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Burglary"}},"id":"1909","type":"Scatter"},{"attributes":{"active_drag":"auto","active_inspect":"auto","active_multi":null,"active_scroll":"auto","active_tap":"auto","tools":[{"id":"1831"},{"id":"1849"},{"id":"1850"},{"id":"1851"},{"id":"1852"},{"id":"1853"}]},"id":"1855","type":"Toolbar"},{"attributes":{},"id":"1933","type":"UnionRenderers"},{"attributes":{"end":2016.3142857142857,"reset_end":2016.3142857142857,"reset_start":1957.6857142857143,"start":1957.6857142857143,"tags":[[["Year","Year",null]]]},"id":"1829","type":"Range1d"},{"attributes":{"fill_alpha":{"value":0.2},"fill_color":{"value":"#1f77b3"},"line_alpha":{"value":0.2},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1867","type":"Scatter"},{"attributes":{"axis_label":"Year","bounds":"auto","formatter":{"id":"1915"},"major_label_orientation":"horizontal","ticker":{"id":"1886"}},"id":"1885","type":"LinearAxis"},{"attributes":{"callback":null,"renderers":[{"id":"1868"}],"tags":["hv_created"],"tooltips":[["Year","@{Year}"],["Robbery","@{Robbery}"]]},"id":"1831","type":"HoverTool"},{"attributes":{"overlay":{"id":"1898"}},"id":"1896","type":"BoxZoomTool"},{"attributes":{},"id":"1915","type":"BasicTickFormatter"},{"attributes":{},"id":"1893","type":"SaveTool"},{"attributes":{"axis_label":"Year","bounds":"auto","formatter":{"id":"1871"},"major_label_orientation":"horizontal","ticker":{"id":"1842"}},"id":"1841","type":"LinearAxis"},{"attributes":{"end":745838.2,"reset_end":745838.2,"reset_start":48563.799999999996,"start":48563.799999999996,"tags":[[["Robbery","Robbery",null]]]},"id":"1830","type":"Range1d"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"value":"#1f77b3"},"line_alpha":{"value":0.1},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1866","type":"Scatter"},{"attributes":{},"id":"1917","type":"BasicTickFormatter"},{"attributes":{},"id":"1837","type":"LinearScale"},{"attributes":{"end":4083510.0,"reset_end":4083510.0,"reset_start":623790.0,"start":623790.0,"tags":[[["Burglary","Burglary",null]]]},"id":"1874","type":"Range1d"},{"attributes":{},"id":"1839","type":"LinearScale"},{"attributes":{"children":[{"id":"1828"},{"id":"1939"},{"id":"2068"}],"margin":[0,0,0,0],"name":"Row02795","tags":["embedded"]},"id":"1827","type":"Row"},{"attributes":{"callback":null,"renderers":[{"id":"1912"}],"tags":["hv_created"],"tooltips":[["Year","@{Year}"],["Burglary","@{Burglary}"]]},"id":"1875","type":"HoverTool"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer02799","sizing_mode":"stretch_width"},"id":"1828","type":"Spacer"},{"attributes":{},"id":"1897","type":"ResetTool"},{"attributes":{"toolbar":{"id":"1937"},"toolbar_location":"above"},"id":"1938","type":"ToolbarBox"},{"attributes":{"source":{"id":"1862"}},"id":"1869","type":"CDSView"},{"attributes":{"overlay":{"id":"1854"}},"id":"1852","type":"BoxZoomTool"},{"attributes":{},"id":"1846","type":"BasicTicker"},{"attributes":{"align":null,"below":[{"id":"1885"}],"center":[{"id":"1888"},{"id":"1892"}],"left":[{"id":"1889"}],"margin":null,"min_border_bottom":10,"min_border_left":10,"min_border_right":10,"min_border_top":10,"plot_height":300,"plot_width":700,"renderers":[{"id":"1912"}],"sizing_mode":"fixed","title":{"id":"1877"},"toolbar":{"id":"1899"},"toolbar_location":null,"x_range":{"id":"1829"},"x_scale":{"id":"1881"},"y_range":{"id":"1874"},"y_scale":{"id":"1883"}},"id":"1876","subtype":"Figure","type":"Plot"},{"attributes":{"data_source":{"id":"1862"},"glyph":{"id":"1865"},"hover_glyph":null,"muted_glyph":{"id":"1867"},"nonselection_glyph":{"id":"1866"},"selection_glyph":null,"view":{"id":"1869"}},"id":"1868","type":"GlyphRenderer"},{"attributes":{"text":"","text_color":{"value":"black"},"text_font_size":{"value":"12pt"}},"id":"1877","type":"Title"},{"attributes":{"axis":{"id":"1841"},"grid_line_color":null,"ticker":null},"id":"1844","type":"Grid"},{"attributes":{},"id":"1881","type":"LinearScale"},{"attributes":{"fill_color":{"value":"#1f77b3"},"line_color":{"value":"#1f77b3"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"1865","type":"Scatter"},{"attributes":{},"id":"1883","type":"LinearScale"},{"attributes":{"toolbars":[{"id":"1855"},{"id":"1899"}],"tools":[{"id":"1831"},{"id":"1849"},{"id":"1850"},{"id":"1851"},{"id":"1852"},{"id":"1853"},{"id":"1875"},{"id":"1893"},{"id":"1894"},{"id":"1895"},{"id":"1896"},{"id":"1897"}]},"id":"1937","type":"ProxyToolbar"},{"attributes":{"axis":{"id":"1885"},"grid_line_color":null,"ticker":null},"id":"1888","type":"Grid"},{"attributes":{"data":{"Robbery":[107840,106670,110860,116470,130390,138690,157990,202910,262840,298850,349860,387700,376290,384220,442400,470500,427810,412610,426930,480700,565840,592910,553130,506567,485008,497874,542775,517704,542968,578326,639271,687732,672478,659870,618949,580509,535594,498534,447186,409371,408016,423557,420806,414235,401470,417438,449246,447324,443563,408742,369089,354772,355051,345095,325802],"Year":[1960,1961,1962,1963,1964,1965,1966,1967,1968,1969,1970,1971,1972,1973,1974,1975,1976,1977,1978,1979,1980,1981,1982,1983,1984,1985,1986,1987,1988,1989,1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014]},"selected":{"id":"1863"},"selection_policy":{"id":"1924"}},"id":"1862","type":"ColumnDataSource"},{"attributes":{},"id":"1863","type":"Selection"},{"attributes":{},"id":"1886","type":"BasicTicker"},{"attributes":{},"id":"1853","type":"ResetTool"},{"attributes":{"axis":{"id":"1845"},"dimension":1,"grid_line_color":null,"ticker":null},"id":"1848","type":"Grid"},{"attributes":{"children":[[{"id":"1832"},0,0],[{"id":"1876"},1,0]]},"id":"1936","type":"GridBox"},{"attributes":{},"id":"1894","type":"PanTool"},{"attributes":{},"id":"1849","type":"SaveTool"},{"attributes":{},"id":"1890","type":"BasicTicker"},{"attributes":{},"id":"1851","type":"WheelZoomTool"},{"attributes":{"data":{"Burglary":[912100,949600,994300,1086400,1213200,1282500,1410100,1632100,1858900,1981900,2205000,2399300,2375500,2565500,3039200,3265300,3108700,3071500,3128300,3327700,3795200,3779700,3447100,3129851,2984434,3073348,3241410,3236184,3218077,3168170,3073909,3157150,2979884,2834808,2712774,2593784,2506400,2460526,2332735,2100739,2050992,2116531,2151252,2154834,2144446,2155448,2194993,2190198,2228887,2203313,2168459,2185140,2109932,1931835,1729806],"Year":[1960,1961,1962,1963,1964,1965,1966,1967,1968,1969,1970,1971,1972,1973,1974,1975,1976,1977,1978,1979,1980,1981,1982,1983,1984,1985,1986,1987,1988,1989,1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014]},"selected":{"id":"1907"},"selection_policy":{"id":"1933"}},"id":"1906","type":"ColumnDataSource"},{"attributes":{"axis_label":"Burglary","bounds":"auto","formatter":{"id":"1917"},"major_label_orientation":"horizontal","ticker":{"id":"1890"}},"id":"1889","type":"LinearAxis"},{"attributes":{"axis_label":"Robbery","bounds":"auto","formatter":{"id":"1873"},"major_label_orientation":"horizontal","ticker":{"id":"1846"}},"id":"1845","type":"LinearAxis"}],"root_ids":["1827"]},"title":"Bokeh Application","version":"2.0.1"}};
  var render_items = [{"docid":"fa02b320-7a94-4e0f-b577-14f4ec411364","root_ids":["1827"],"roots":{"1827":"44fb4261-86c9-4671-8ab2-a8cc3b599c0b"}}];
  root.Bokeh.embed.embed_items_notebook(docs_json, render_items);
  }
if (root.Bokeh !== undefined) {
    embed_document(root);
  } else {
    var attempts = 0;
    var timer = setInterval(function(root) {
      if (root.Bokeh !== undefined) {
        clearInterval(timer);
        embed_document(root);
      } else if (document.readyState == "complete") {
        attempts++;
        if (attempts > 100) {
          clearInterval(timer);
          console.log("Bokeh: ERROR: Unable to run BokehJS code because BokehJS library is missing");
        }
      }
    }, 10, root)
  }
})(window);</script>



### Holoviews Objects
`df.hvplot` returns a [holoviews](https://holoviews.org/) plot object. Those objects can be further customized. You can get help for styling and plotting options by importing `holoviews` and calling its `help` function.


```python
import holoviews as hv
plot = df.hvplot()
hv.help(plot)
```

Holoviews objects are customized by calling the `.opts()` method on them:


```python
robbery.opts(color='red')
```






<div id='2150'>





  <div class="bk-root" id="702eb327-a9fc-413b-9c9e-0c19ec29f075" data-root-id="2150"></div>
</div>
<script type="application/javascript">
    function msg_handler(msg) {
      var metadata = msg.metadata;
      var buffers = msg.buffers;
      var msg = msg.content.data;
      if ((metadata.msg_type == "Ready")) {
        if (metadata.content) {
          console.log("Python callback returned following output:", metadata.content);
        }
      } else if (metadata.msg_type == "Error") {
        console.log("Python failed with the following traceback:", metadata.traceback)
      } else {

var plot_id = "2150";

if ((plot_id in window.PyViz.plot_index) && (window.PyViz.plot_index[plot_id] != null)) {
  var plot = window.PyViz.plot_index[plot_id];
} else if ((Bokeh !== undefined) && (plot_id in Bokeh.index)) {
  var plot = Bokeh.index[plot_id];
}

if (plot == null) {
  return
}

if (plot_id in window.PyViz.receivers) {
  var receiver = window.PyViz.receivers[plot_id];
} else {
  var receiver = new Bokeh.protocol.Receiver();
  window.PyViz.receivers[plot_id] = receiver;
}

if ((buffers != undefined) && (buffers.length > 0)) {
  receiver.consume(buffers[0].buffer)
} else {
  receiver.consume(msg)
}

const comm_msg = receiver.message;
if ((comm_msg != null) && (Object.keys(comm_msg.content).length > 0)) {
  plot.model.document.apply_json_patch(comm_msg.content, comm_msg.buffers)
}

      }
    }
    if ((window.PyViz == undefined) || (!window.PyViz.comm_manager)) {
      console.log("Could not find comm manager")
    } else {
      window.PyViz.comm_manager.register_target('2150', '6e8c9af1e93341d4ab12c55ea87251f0', msg_handler);
    }

(function(root) {
  function embed_document(root) {
  var docs_json = {"dd5f390e-9c8f-4191-bba4-cb19ea6ebdca":{"roots":{"references":[{"attributes":{"axis":{"id":"2164"},"grid_line_color":null,"ticker":null},"id":"2167","type":"Grid"},{"attributes":{"end":745838.2,"reset_end":745838.2,"reset_start":48563.799999999996,"start":48563.799999999996,"tags":[[["Robbery","Robbery",null]]]},"id":"2153","type":"Range1d"},{"attributes":{"children":[{"id":"2151"},{"id":"2155"},{"id":"2205"}],"margin":[0,0,0,0],"name":"Row03923","tags":["embedded"]},"id":"2150","type":"Row"},{"attributes":{"axis_label":"Year","bounds":"auto","formatter":{"id":"2194"},"major_label_orientation":"horizontal","ticker":{"id":"2165"}},"id":"2164","type":"LinearAxis"},{"attributes":{},"id":"2165","type":"BasicTicker"},{"attributes":{},"id":"2176","type":"ResetTool"},{"attributes":{},"id":"2169","type":"BasicTicker"},{"attributes":{},"id":"2203","type":"UnionRenderers"},{"attributes":{"fill_color":{"value":"red"},"line_color":{"value":"red"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"2188","type":"Scatter"},{"attributes":{"source":{"id":"2185"}},"id":"2192","type":"CDSView"},{"attributes":{"bottom_units":"screen","fill_alpha":0.5,"fill_color":"lightgrey","left_units":"screen","level":"overlay","line_alpha":1.0,"line_color":"black","line_dash":[4,4],"line_width":2,"render_mode":"css","right_units":"screen","top_units":"screen"},"id":"2177","type":"BoxAnnotation"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"value":"red"},"line_alpha":{"value":0.1},"line_color":{"value":"red"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"2189","type":"Scatter"},{"attributes":{"callback":null,"renderers":[{"id":"2191"}],"tags":["hv_created"],"tooltips":[["Year","@{Year}"],["Robbery","@{Robbery}"]]},"id":"2154","type":"HoverTool"},{"attributes":{},"id":"2174","type":"WheelZoomTool"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer03927","sizing_mode":"stretch_width"},"id":"2151","type":"Spacer"},{"attributes":{},"id":"2162","type":"LinearScale"},{"attributes":{"fill_alpha":{"value":0.2},"fill_color":{"value":"red"},"line_alpha":{"value":0.2},"line_color":{"value":"red"},"size":{"units":"screen","value":5.477225575051661},"x":{"field":"Year"},"y":{"field":"Robbery"}},"id":"2190","type":"Scatter"},{"attributes":{"overlay":{"id":"2177"}},"id":"2175","type":"BoxZoomTool"},{"attributes":{"align":null,"below":[{"id":"2164"}],"center":[{"id":"2167"},{"id":"2171"}],"left":[{"id":"2168"}],"margin":null,"min_border_bottom":10,"min_border_left":10,"min_border_right":10,"min_border_top":10,"plot_height":300,"plot_width":700,"renderers":[{"id":"2191"}],"sizing_mode":"fixed","title":{"id":"2156"},"toolbar":{"id":"2178"},"x_range":{"id":"2152"},"x_scale":{"id":"2160"},"y_range":{"id":"2153"},"y_scale":{"id":"2162"}},"id":"2155","subtype":"Figure","type":"Plot"},{"attributes":{"axis":{"id":"2168"},"dimension":1,"grid_line_color":null,"ticker":null},"id":"2171","type":"Grid"},{"attributes":{"text":"","text_color":{"value":"black"},"text_font_size":{"value":"12pt"}},"id":"2156","type":"Title"},{"attributes":{"axis_label":"Robbery","bounds":"auto","formatter":{"id":"2196"},"major_label_orientation":"horizontal","ticker":{"id":"2169"}},"id":"2168","type":"LinearAxis"},{"attributes":{},"id":"2160","type":"LinearScale"},{"attributes":{},"id":"2194","type":"BasicTickFormatter"},{"attributes":{"active_drag":"auto","active_inspect":"auto","active_multi":null,"active_scroll":"auto","active_tap":"auto","tools":[{"id":"2154"},{"id":"2172"},{"id":"2173"},{"id":"2174"},{"id":"2175"},{"id":"2176"}]},"id":"2178","type":"Toolbar"},{"attributes":{"data_source":{"id":"2185"},"glyph":{"id":"2188"},"hover_glyph":null,"muted_glyph":{"id":"2190"},"nonselection_glyph":{"id":"2189"},"selection_glyph":null,"view":{"id":"2192"}},"id":"2191","type":"GlyphRenderer"},{"attributes":{"margin":[5,5,5,5],"name":"HSpacer03928","sizing_mode":"stretch_width"},"id":"2205","type":"Spacer"},{"attributes":{},"id":"2173","type":"PanTool"},{"attributes":{},"id":"2196","type":"BasicTickFormatter"},{"attributes":{},"id":"2186","type":"Selection"},{"attributes":{},"id":"2172","type":"SaveTool"},{"attributes":{"data":{"Robbery":[107840,106670,110860,116470,130390,138690,157990,202910,262840,298850,349860,387700,376290,384220,442400,470500,427810,412610,426930,480700,565840,592910,553130,506567,485008,497874,542775,517704,542968,578326,639271,687732,672478,659870,618949,580509,535594,498534,447186,409371,408016,423557,420806,414235,401470,417438,449246,447324,443563,408742,369089,354772,355051,345095,325802],"Year":[1960,1961,1962,1963,1964,1965,1966,1967,1968,1969,1970,1971,1972,1973,1974,1975,1976,1977,1978,1979,1980,1981,1982,1983,1984,1985,1986,1987,1988,1989,1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014]},"selected":{"id":"2186"},"selection_policy":{"id":"2203"}},"id":"2185","type":"ColumnDataSource"},{"attributes":{"end":2016.3142857142857,"reset_end":2016.3142857142857,"reset_start":1957.6857142857143,"start":1957.6857142857143,"tags":[[["Year","Year",null]]]},"id":"2152","type":"Range1d"}],"root_ids":["2150"]},"title":"Bokeh Application","version":"2.0.1"}};
  var render_items = [{"docid":"dd5f390e-9c8f-4191-bba4-cb19ea6ebdca","root_ids":["2150"],"roots":{"2150":"702eb327-a9fc-413b-9c9e-0c19ec29f075"}}];
  root.Bokeh.embed.embed_items_notebook(docs_json, render_items);
  }
if (root.Bokeh !== undefined) {
    embed_document(root);
  } else {
    var attempts = 0;
    var timer = setInterval(function(root) {
      if (root.Bokeh !== undefined) {
        clearInterval(timer);
        embed_document(root);
      } else if (document.readyState == "complete") {
        attempts++;
        if (attempts > 100) {
          clearInterval(timer);
          console.log("Bokeh: ERROR: Unable to run BokehJS code because BokehJS library is missing");
        }
      }
    }, 10, root)
  }
})(window);</script>



`plot.opts()` modifies the plot object in place. If you want a copy use `plot.options()`

See: http://holoviews.org/user_guide/Applying_Customizations.html

### Saving Plots

See: http://holoviews.org/user_guide/Exporting_and_Archiving.html  
And: https://docs.bokeh.org/en/latest/docs/user_guide/export.html

#### Html


```python
hv.save(robbery, 'robbery.html')
```

#### PNG
The simplest way is just to click on the `Save` tool in the toolbar of the plot.

Alternatively you can use the `matplotlib` backend
```
hv.save(robbery, 'robbery.png', backend='matplotlib')
```

Or convert the interactive plots to png by first installing:
```
conda install -c conda-forge firefox geckodriver
```
And then using the code below:


```python
def remove_toolbar(figure):
    """Removes the toolbar from a bokeh figure"""
    from bokeh.models.tools import ToolbarBox
    if hasattr(figure, 'children'):
        for child in figure.children:
            if isinstance(child, ToolbarBox):
                figure.children.remove(child)
        if hasattr(figure, 'toolbar'):
            figure.toolbar.logo = None
        if hasattr(figure, 'toolbar_location'):
            figure.toolbar_location = None

def save_png(plot, filename, toolbar=False):
    """Renders a holoviews plot using bokeh and saves it as png file"""
    from bokeh.io import export_png
    figure = hv.render(plot, backend='bokeh')
    if toolbar is False:
        remove_toolbar(figure)
    export_png(figure, filename=filename)
    
save_png(robbery, 'robbery.png')
```

#### SVG

Either using `matplotlib` backend:
```
hv.save(robbery, 'robbery.svg', backend='matplotlib')
```

Or by converting the interactive plots to svg. This does only work for simple plots, not overlays and layouts.
Install:
```
conda install -c conda-forge firefox geckodriver
```
And then use the code below


```python
def save_svg(plot, filename, toolbar=False):
    """Renders a holoviews plot using bokeh and saves it as png file
    Does 
    """
    from bokeh.io import export_svgs
    figure = hv.render(plot, backend='bokeh')
    if hasattr(figure, 'output_backend'):
        figure.output_backend = 'svg'
    else:
        print('Cannot convert this plot to svg.')
    export_svgs(figure, filename=filename)
    
save_svg(robbery, 'robbery.svg')
```
