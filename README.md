<!DOCTYPE html> 
<html>
<head>
	<title>Add (2-4) matrix</title>
</head>
<body>
<script>
	// Initialising arrays with pre-set values.
	var temp = [[0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0]];
	var a = [[8, 3, 3, 6], [2, 4, 4, 9], [3, 6, 5, 2], [3, 6, 5, 2]];
    var b = [[1, 2, 3, 1], [4, 6, 8, 1], [2, 4, 4, 7], [2, 4, 4, 9]];
	var c = [[12, 2, 8, 8], [3, 1, 2, 2], [7, 8, 1, 0], [2, 4, 4, 9]];
	var d = [[1, 2, 3, 1], [4, 6, 8, 1], [2, 4, 4, 7], [2, 4, 4, 9]];
	
	function add() {
	var args = document.getElementById("numArrays").value;
	// Call appropriate functions with number of arguments.
	if (args == 2) twoArguments(a, b); 
	if (args == 3) threeArguments(a, b, c);
	if (args == 4) fourArguments(a, b, c, d);
	}
	// This function uses two number of ARGUMENTS passed to it as length of array.
	function twoArguments() {
	var len = arguments.length;
		for (var i = 0; i < len; i++) {
		temp[i].pop();temp[i].pop(); // Pops the last two '0' of the array.
			for (var j= 0; j < len; j++) {
			temp[i][j] = a[i][j] + b[i][j]; 
			}
		}
		for (var i = 0; i < len; i++){
		document.write("<br>" + temp[i]);
		}
	}
	// This function uses three number of ARGUMENTS passed to it as length of array.
	function threeArguments() {
	var len = arguments.length;
		for (var i = 0; i < len; i++) {
		temp[i].pop(); // Pops the last '0' of the array.
			for (var j= 0; j < len; j++) {
			temp[i][j] = a[i][j] + b[i][j] + c[i][j]; 
			}
		}
		for (var i = 0; i < len; i++){
		document.write("<br>" + temp[i]);
		}
	}
	// This function uses four number of ARGUMENTS passed to it as length of array.
	function fourArguments() {
	var len = arguments.length;
		for (var i = 0; i < len; i++) {
			for (var j= 0; j < len; j++) {
			temp[i][j] = a[i][j] + b[i][j] + c[i][j] + d[i][j]; 
			}
		}
		for (var i = 0; i < len; i++){
		document.write("<br>" + temp[i]);
		}
	}	
</script>

<p>There are four preset arrays (a,b,c,d). Enter the number of these arrays you wish to add (2-4).</p>
<!--The input will have an ID of numArrays and will be called by getElementById("numArrays") within the function options -->
<input id="numArrays">
<form name=myform><br> 
	<button type="button" onclick="add(2,4)">Enter Number of Arrays (2-4)</button>
</form>
</body>
</html>
