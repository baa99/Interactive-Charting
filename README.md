# Interactive-Charting
<!DOCTYPE html>
<html>
<head>
    
    

<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
<script type="text/javascript">
      google.charts.load('current', {'packages':['corechart']});
      google.charts.setOnLoadCallback(drawChart);
      google.charts.setOnLoadCallback(drawChart2);
      
 
//first chart    
    function drawChart() {
    
     mymagnitude = document.getElementById("thedropdown").value;
     
     
     info = [{magnitude: "5-5.9", year2000: 1344, year2001: 1224, year2002: 1201, year2003: 1203, year2004: 1515, year2005: 1693 , year2006: 1712 , year2007: 2074 , year2008: 1768 , year2009: 1896 , year2010: 2209 , year2011: 2276 , year2012: 1401 , year2013: 1453 , year2014: 1574 , year2015: 1419 , year2016: 1550 , year2017: 1455 , year2018: 1674 , year2019: 1492},
     {magnitude: "6-6.9", year2000: 146 , year2001: 121 , year2002: 127 , year2003: 140 , year2004: 141 , year2005: 140 , year2006: 142 , year2007:  178 , year2008:  168 , year2009:  144 , year2010:  150 , year2011:  185 , year2012:  108 , year2013:  123 , year2014:  143 , year2015:  127 , year2016:  130 , year2017:  104 , year2018:  117 , year2019:  135},
     {magnitude: "7-7.9", year2000: 14 , year2001: 15 , year2002: 13 , year2003: 14 , year2004: 14 , year2005: 10 , year2006: 9 , year2007: 14 , year2008: 12 , year2009: 16 , year2010: 23 , year2011: 19 , year2012: 12 , year2013: 17 , year2014: 11 , year2015: 18 , year2016: 16 , year2017: 6 , year2018: 16 , year2019: 9},
     {magnitude: "8.0+", year2000: 1 , year2001: 1 , year2002: 0 , year2003: 1 , year2004: 2 , year2005: 1 , year2006: 2 , year2007: 4 , year2008: 0 , year2009: 1 , year2010: 1 , year2011: 1 , year2012: 2 , year2013: 2 , year2014: 1 , year2015: 1 , year2016: 0 , year2017: 1 , year2018: 1 , year2019: 1}
     ];
    
    
    for(i=0; i<info.length; i++) { 
    
    
    if(mymagnitude == info[i].magnitude) {
       year2000 = info[i].year2000;
       year2001 = info[i].year2001;
       year2002 = info[i].year2002;
       year2003 = info[i].year2003;
       year2004 = info[i].year2004;
       year2005 = info[i].year2005;
       year2006 = info[i].year2006;
       year2007 = info[i].year2007;
       year2008 = info[i].year2008;
       year2009 = info[i].year2009;
       year2010 = info[i].year2010;
       year2011 = info[i].year2011;
       year2012 = info[i].year2012;
       year2013 = info[i].year2013;
       year2014 = info[i].year2014;
       year2015 = info[i].year2015;
       year2016 = info[i].year2016;
       year2017 = info[i].year2017;
       year2018 = info[i].year2018;
       year2019 = info[i].year2019;
    
    }// end if
    } // end for
    
    var data = google.visualization.arrayToDataTable([
          ['Task', 'Hours per Week'],
          ['2000',     year2000],
          ['2001',      year2001],
          ['2002',  year2002],
          ['2003', year2003],
          ['2004',    year2004],
          ['2005',     year2005],
          ['2006',      year2006],
          ['2007',  year2007],
          ['2008', year2008],
          ['2009',    year2009],
          ['2010',     year2010],
          ['2011',      year2011],
          ['2012',  year2012],
          ['2013', year2013],
          ['2014',    year2014],
          ['2015',     year2015],
          ['2016',      year2016],
          ['2017',  year2017],
          ['2018', year2018],
          ['2019',    year2019]
        ]);
        var options = {
          title: 'Earthquakes World Wide'
        };
        var chart = new google.visualization.PieChart(document.getElementById('piechart'));
        chart.draw(data, options);        
      }  
      
      
//second chart - function needs a unique name   
function drawChart2() {
      
      myusa = document.getElementById("thedropdown2").value;
     
     
     info = [{usa: "5-5.9", year2000: 63, year2001: 41, year2002: 63, year2003: 54, year2004: 25, year2005: 47, year2006: 51, year2007: 72, year2008: 85, year2009: 58, year2010: 89, year2011: 51, year2012: 27},
     {usa: "6-6.9", year2000: 6, year2001: 5, year2002: 4, year2003: 7, year2004: 2, year2005: 4, year2006: 7, year2007: 9, year2008: 9, year2009: 4, year2010: 8, year2011: 3, year2012: 5},
     {usa: "7-7.9", year2000: 0, year2001: 1, year2002: 1, year2003: 2, year2004: 0, year2005: 1, year2006: 0, year2007: 1, year2008: 0, year2009: 0, year2010: 1, year2011: 1, year2012: 0},
     {usa: "8.0+", year2000: 0, year2001: 0, year2002: 0, year2003: 0, year2004: 0, year2005: 0, year2006: 0, year2007: 0, year2008: 0, year2009: 0, year2010: 0, year2011: 0, year2012: 0}
     ];
     
     for(i=0; i<info.length; i++) { 
    if(myusa == info[i].usa) {
      year2000 = info[i].year2000;
       year2001 = info[i].year2001;
       year2002 = info[i].year2002;
       year2003 = info[i].year2003;
       year2004 = info[i].year2004;
       year2005 = info[i].year2005;
       year2006 = info[i].year2006;
       year2007 = info[i].year2007;
       year2008 = info[i].year2008;
       year2009 = info[i].year2009;
       year2010 = info[i].year2010;
       year2011 = info[i].year2011;
       year2012 = info[i].year2012;
    
    }// end if
    } // end for
    
        var data = google.visualization.arrayToDataTable([
          ['Element', 'Year'],
          ['2000',     year2000],
          ['2001',      year2001],
          ['2002',  year2002],
          ['2003', year2003],
          ['2004',    year2004],
          ['2005',     year2005],
          ['2006',      year2006],
          ['2007',  year2007],
          ['2008', year2008],
          ['2009',    year2009],
          ['2010',     year2010],
          ['2011',      year2011],
          ['2012',  year2012]
        ]);

        var options = {
       
            title: 'Earthquakes in USA',
        };

        var chart = new google.visualization.ColumnChart(document.getElementById('div_chart'));
        chart.draw(data, options);
      }
    
    // this function makes the chart responsive; include the name of the proper drawChart function; This is an example with more than one chart.   
    window.onresize = function() {
    drawChart();
    drawChart2();
    }
     
</script>
    
<style>
    .class {
    width: 100%;
    }
    
    #piechart {
   height: 600px;
    }
    
     #div_chart {
    height: 400px;
    }

body {
background-color:  #4ddbff;
font-family: Helvetica;
}

#main {
width: 80%;
max-width: 950px;
border: 1px gray solid;
margin: auto;
padding: 10px;
background-color: white;
border-radius: 10px;
}

#header {
margin-top: 0;
border: 2px solid black;
padding: 5px;
height: 250px;
background: beige;
background-image: url("earth3.jpg");
color: white;
}

label {
display: block;
}

input {
width: 30px;
margin-left: 20px;
}

h2 {
clear: both;
padding-top: 20px;
}

button {
width: 100px;
margin-top: 20px;
}

</style>
    
    
</head>
<body>
 
<div id="main">
<div id="header">
<h1>Earthquake Data 2000-2019</h1>
</div>

    <h2>Data Charts </h2>
    
 <!-- First Chart in HTML, calls drawChart -->
  <form id="form1" onchange="drawChart()" >
     
     <select id="thedropdown">
     <option value="5-5.9">5-5.9</option>
     <option value="6-6.9">6-6.9</option>
     <option value="7-7.9">7-7.9</option>
     <option value="8.0+">8.0+</option>
     </select>
    
  </form>
  
    <div id="piechart" class="chart"></div>
    
    <p>This pie chart is a visualization of the number of earthquakes that occured world wide from the years 2000-2019. It is split between four diffrent charts that cna be changed showing the varying strength of magnitude earthquakes.</p>

 
 
 <!-- 2nd Chart in HTML, calls drawChart2 -->
 <!-- needs unique ids for form and dropdown -->   

<form id="form2" onchange="drawChart2()" >
     
     <select id="thedropdown2">
     <option value="5-5.9">5-5.9</option>
     <option value="6-6.9">6-6.9</option>
     <option value="7-7.9">7-7.9</option>
     <option value="8.0+">8.0+</option>
     </select>
    
  </form>

    <div id="div_chart" class="chart"></div>
    
    <p>This Column chart is similar to the pie chart where it is using and comparing earthquake numbers by the maginitude range and can adjust what magnitude range s shown on the chart. What is different is this data is meant for the USA specially instead of the whole world so you can see the amount of earthquakes we have and can compare to the world.</p>
 
    </div>
      
</body>
</html>



