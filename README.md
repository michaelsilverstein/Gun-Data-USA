# Gun-Data-USA
Taking a look at the correlations between certain features and gun murder per state

```html
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>GunData</title>
        
<link rel="stylesheet" href="https://cdn.pydata.org/bokeh/release/bokeh-0.12.3.min.css" type="text/css" />
        
<script type="text/javascript" src="https://cdn.pydata.org/bokeh/release/bokeh-0.12.3.min.js"></script>
<script type="text/javascript">
    Bokeh.set_log_level("info");
</script>
        <style>
          html {
            width: 100%;
            height: 100%;
          }
          body {
            width: 90%;
            height: 100%;
            margin: auto;
          }
        </style>
    </head>
    <body>
        
        <div class="bk-root">
            <div class="plotdiv" id="4f16faab-611b-4ded-aaed-1c9fb09460b7"></div>
        </div>
        
        <script type="text/javascript">
            Bokeh.$(function() {
            Bokeh.safely(function() {
                var docs_json = {"93f20acc-7877-4754-9c54-97b1a883e5d1":{"roots":{"references":[{"attributes":{"callback":null,"plot":{"id":"3be12f1f-dd5b-48e1-8ec0-158c1aa69ef5","subtype":"Figure","type":"Plot"},"tooltips":[["State","@states"],["Ownership, Income","@x%, @y"],["Gun Murders","@c"]]},"id":"4badc33a-2622-4eac-80a3-ee5b63ea8edf","type":"HoverTool"},{"attributes":{"plot":{"id":"3be12f1f-dd5b-48e1-8ec0-158c1aa69ef5","subtype":"Figure","type":"Plot"},"ticker":{"id":"875d6047-117c-4800-b9b9-c316e2ddbf5c","type":"BasicTicker"}},"id":"56b0d72c-0568-408f-8ea7-574d7b666859","type":"Grid"},{"attributes":{},"id":"875d6047-117c-4800-b9b9-c316e2ddbf5c","type":"BasicTicker"},{"attributes":{"plot":null,"text":null},"id":"30ae3a05-85f9-43ea-a0e1-fbd1849b455f","type":"Title"},{"attributes":{"axis_label":"Gun Ownership (%)","axis_label_text_color":{"value":"snow"},"formatter":{"id":"2b73a7d7-a0c4-4807-bb26-dd77ab5518f7","type":"BasicTickFormatter"},"major_label_text_color":{"value":"snow"},"plot":{"id":"3be12f1f-dd5b-48e1-8ec0-158c1aa69ef5","subtype":"Figure","type":"Plot"},"ticker":{"id":"875d6047-117c-4800-b9b9-c316e2ddbf5c","type":"BasicTicker"}},"id":"45596902-973d-4fdf-95aa-ef03a348f4c5","type":"LinearAxis"},{"attributes":{"callback":null,"column_names":["states","y","c","x","line_color","fill_color"],"data":{"c":[135.0,19.0,232.0,93.0,1257.0,65.0,97.0,38.0,99.0,669.0,376.0,7.0,12.0,364.0,142.0,21.0,63.0,116.0,351.0,11.0,118.0,413.0,53.0,120.0,321.0,12.0,32.0,84.0,5.0,246.0,67.0,517.0,286.0,4.0,310.0,111.0,36.0,457.0,16.0,207.0,8.0,219.0,805.0,22.0,2.0,250.0,93.0,27.0,97.0,5.0],"fill_color":["#000003","#FBFCBF","#B53679","#000003","#FBFCBF","#FB8660","#FBFCBF","#FB8660","#FBFCBF","#4F117B","#4F117B","#FBFCBF","#4F117B","#FB8660","#4F117B","#B53679","#B53679","#000003","#000003","#4F117B","#FBFCBF","#4F117B","#FBFCBF","#000003","#4F117B","#4F117B","#B53679","#B53679","#FBFCBF","#FBFCBF","#000003","#FB8660","#4F117B","#FB8660","#4F117B","#000003","#B53679","#B53679","#FB8660","#000003","#B53679","#000003","#B53679","#FB8660","#FB8660","#FBFCBF","#FB8660","#000003","#B53679","#FB8660"],"line_color":["#000003","#FBFCBF","#B53679","#000003","#FBFCBF","#FB8660","#FBFCBF","#FB8660","#FBFCBF","#4F117B","#4F117B","#FBFCBF","#4F117B","#FB8660","#4F117B","#B53679","#B53679","#000003","#000003","#4F117B","#FBFCBF","#4F117B","#FBFCBF","#000003","#4F117B","#4F117B","#B53679","#B53679","#FBFCBF","#FBFCBF","#000003","#FB8660","#4F117B","#FB8660","#4F117B","#000003","#B53679","#B53679","#FB8660","#000003","#B53679","#000003","#B53679","#FB8660","#FB8660","#FBFCBF","#FB8660","#000003","#B53679","#FB8660"],"states":["Alabama","Alaska","Arizona","Arkansas","California","Colorado","Connecticut","Delaware","District of Columbia","Florida","Georgia","Hawaii","Idaho","Illinois","Indiana","Iowa","Kansas","Kentucky","Louisiana","Maine","Massachusetts","Michigan","Minnesota","Mississippi","Missouri","Montana","Nebraska","Nevada","New Hampshire","New Jersey","New Mexico","New York","North Carolina","North Dakota","Ohio","Oklahoma","Oregon","Pennsylvania","Rhode Island","South Carolina","South Dakota","Tennessee","Texas","Utah","Vermont","Virginia","Washington","West Virginia","Wisconsin","Wyoming"],"x":[48.9,61.7,32.3,57.9,20.1,34.3,16.6,5.2,25.9,32.5,31.6,45.1,56.9,26.2,33.8,33.8,32.2,42.4,44.5,22.6,22.6,28.8,36.7,42.8,27.1,52.3,19.8,37.5,14.4,11.3,49.9,10.3,28.7,47.9,19.6,31.2,26.6,27.1,5.8,44.4,35.0,39.4,35.7,31.9,28.8,29.3,27.7,54.2,34.7,53.8],"y":[41415,60287,46709,38758,67458,55387,65753,57954,65124,44299,46007,62814,43341,53234,46438,49427,48964,41141,41734,46033,64859,45981,61814,36919,45247,44222,50296,48927,64712,69825,41963,55246,43916,51704,45749,43225,46816,50228,53636,42367,48321,41693,49392,55869,52776,62881,57835,38482,50395,56322]}},"id":"c06e7ccf-a5de-44c8-bbfd-b8023ffbf243","type":"ColumnDataSource"},{"attributes":{"callback":null},"id":"53ba4488-0aa6-4b58-8c93-e07bcc99bf96","type":"DataRange1d"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"value":"#1f77b4"},"line_alpha":{"value":0.1},"line_color":{"value":"#1f77b4"},"size":{"units":"screen","value":10},"x":{"field":"x"},"y":{"field":"y"}},"id":"63c9a41b-4035-4563-be3a-0085a79e665c","type":"Circle"},{"attributes":{"background_fill_alpha":{"value":0.6},"background_fill_color":{"value":"slategray"},"below":[{"id":"45596902-973d-4fdf-95aa-ef03a348f4c5","type":"LinearAxis"}],"border_fill_color":{"value":"slategray"},"left":[{"id":"46d938e2-65fa-4cc1-92e6-504c6051d928","type":"LinearAxis"}],"outline_line_alpha":{"value":0.8},"outline_line_color":{"value":"black"},"outline_line_width":{"value":7},"plot_width":800,"renderers":[{"id":"45596902-973d-4fdf-95aa-ef03a348f4c5","type":"LinearAxis"},{"id":"56b0d72c-0568-408f-8ea7-574d7b666859","type":"Grid"},{"id":"46d938e2-65fa-4cc1-92e6-504c6051d928","type":"LinearAxis"},{"id":"1ea95567-7d52-47e5-ba06-8aff9cf6d99f","type":"Grid"},{"id":"389300a5-187f-4aec-831f-54f340507229","type":"GlyphRenderer"}],"title":{"id":"30ae3a05-85f9-43ea-a0e1-fbd1849b455f","type":"Title"},"tool_events":{"id":"beb70bbd-2889-47a8-acd9-dc9b84062102","type":"ToolEvents"},"toolbar":{"id":"904cb854-17cb-4cc6-8e10-f5ce1a33f297","type":"Toolbar"},"x_range":{"id":"53ba4488-0aa6-4b58-8c93-e07bcc99bf96","type":"DataRange1d"},"y_range":{"id":"4cccbf9c-2824-4ac2-9faf-cfb8525cdd86","type":"DataRange1d"}},"id":"3be12f1f-dd5b-48e1-8ec0-158c1aa69ef5","subtype":"Figure","type":"Plot"},{"attributes":{"fill_alpha":{"value":0.5},"fill_color":{"field":"fill_color"},"line_alpha":{"value":0.5},"line_color":{"field":"line_color"},"size":{"units":"screen","value":10},"x":{"field":"x"},"y":{"field":"y"}},"id":"94af0559-86c7-42f2-b706-0c3830418367","type":"Circle"},{"attributes":{"axis_label":"Median Income ($)","axis_label_text_color":{"value":"snow"},"formatter":{"id":"7cf306d0-3483-4540-bd72-2a13889e6b9f","type":"BasicTickFormatter"},"major_label_text_color":{"value":"snow"},"plot":{"id":"3be12f1f-dd5b-48e1-8ec0-158c1aa69ef5","subtype":"Figure","type":"Plot"},"ticker":{"id":"5ec34d6e-8062-49a2-9e43-b2a6c53a5152","type":"BasicTicker"}},"id":"46d938e2-65fa-4cc1-92e6-504c6051d928","type":"LinearAxis"},{"attributes":{"dimension":1,"plot":{"id":"3be12f1f-dd5b-48e1-8ec0-158c1aa69ef5","subtype":"Figure","type":"Plot"},"ticker":{"id":"5ec34d6e-8062-49a2-9e43-b2a6c53a5152","type":"BasicTicker"}},"id":"1ea95567-7d52-47e5-ba06-8aff9cf6d99f","type":"Grid"},{"attributes":{"callback":null},"id":"4cccbf9c-2824-4ac2-9faf-cfb8525cdd86","type":"DataRange1d"},{"attributes":{"data_source":{"id":"c06e7ccf-a5de-44c8-bbfd-b8023ffbf243","type":"ColumnDataSource"},"glyph":{"id":"94af0559-86c7-42f2-b706-0c3830418367","type":"Circle"},"hover_glyph":null,"nonselection_glyph":{"id":"63c9a41b-4035-4563-be3a-0085a79e665c","type":"Circle"},"selection_glyph":null},"id":"389300a5-187f-4aec-831f-54f340507229","type":"GlyphRenderer"},{"attributes":{},"id":"beb70bbd-2889-47a8-acd9-dc9b84062102","type":"ToolEvents"},{"attributes":{},"id":"2b73a7d7-a0c4-4807-bb26-dd77ab5518f7","type":"BasicTickFormatter"},{"attributes":{},"id":"7cf306d0-3483-4540-bd72-2a13889e6b9f","type":"BasicTickFormatter"},{"attributes":{"active_drag":"auto","active_scroll":"auto","active_tap":"auto","tools":[{"id":"4badc33a-2622-4eac-80a3-ee5b63ea8edf","type":"HoverTool"}]},"id":"904cb854-17cb-4cc6-8e10-f5ce1a33f297","type":"Toolbar"},{"attributes":{},"id":"5ec34d6e-8062-49a2-9e43-b2a6c53a5152","type":"BasicTicker"}],"root_ids":["3be12f1f-dd5b-48e1-8ec0-158c1aa69ef5"]},"title":"Bokeh Application","version":"0.12.3"}};
                var render_items = [{"docid":"93f20acc-7877-4754-9c54-97b1a883e5d1","elementid":"4f16faab-611b-4ded-aaed-1c9fb09460b7","modelid":"3be12f1f-dd5b-48e1-8ec0-158c1aa69ef5"}];
                
                Bokeh.embed.embed_items(docs_json, render_items);
            });
        });
        </script>
    </body>
</html>
```
