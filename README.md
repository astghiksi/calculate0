<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<style>
	body{
		background-color: #4196E1;
		user-select: none;
	}
	.cal{
		display: grid;
		grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
		grid-gap:20px;
		background-color:#6495ED;
		padding: 8px;
		border-radius: 8px;
		max-width: 720px;
		font-family: Tahoma;
	}
	.one{
	background-color: #4169E1;
	color: #000;
	padding: 20px;
	display: flex;
	justify-content: center;
	align-items: center;
	font-size: 20px;
	cursor:pointer;
	font-weight: bold;	
	}
	form{
		max-width: 100%;
	}
	input{
		width: 100%;
		height: 70%;
		border: none;
		font-size: 20px;
		outline: none;
		text-align: right;

	}
	.input{
		grid-column: 1/-1;
		padding: 0;

	}
</style>
<body>
	<div class="cal">
<div class="one input"><form name="form"><input type="text" name="txtview" readonly></div>
	<div class="one" onclick="insert('1')" >1</div>
<div class="one" onclick="insert('2')" >2</div>
<div class="one" onclick="insert('3')">3</div>
<div class="one" onclick="insert('+')">+</div>
<div class="one" onclick="insert('-')">-</div>
<div class="one" onclick="insert('*')">&times;</div>
<div class="one" onclick="clean()">C</div>
<div class="one" onclick="insert('4')">4</div>
<div class="one" onclick="insert('5')">5</div>
<div class="one" onclick="insert('6')">6</div>
<div class="one" onclick="insert('/')">&divide;</div>
<div class="one" onclick="insert('%')">%</div>
<div class="one" onclick="sqrt()">√</div>
<div class="one" onclick="back()">&larr;</div>
<div class="one" onclick="insert('7')">7</div>
<div class="one" onclick="insert('8')">8</div>
<div class="one" onclick="insert('9')">9</div>
<div class="one" onclick="sinclicked()">sin</div>
<div class="one" onclick="cosclicked()">cos</div>
<div class="one" onclick="tanclicked()">tg</div>
<div class="one" onclick="ctgclicked()">ctg</div>
<div class="one" onclick="insert('.')">.</div>
<div class="one" onclick="insert('0')">0</div>
<div class="one" onclick="insert('**')">^</div>
<div class="one" onclick="insert('(')">(</div>
<div class="one" onclick="insert(')')">)</div>
<div class="one" onclick="equal()">=</div>
<script type="text/javascript">
	function insert(num){
		document.form.txtview.value=document.form.txtview.value+num;
	}
	function clean(){
		document.form.txtview.value="";
	}
	function back(){
		var exp=document.form.txtview.value;
		document.form.txtview.value=exp.substring(0, exp.length-1);
	}
	function equal(){
		var exp=document.form.txtview.value;
		if(exp){
			document.form.txtview.value=eval(exp);
		}
	}
function sinclicked(){
	document.form.txtview.value=Math.sin(document.form.txtview.value);

}
function cosclicked(){
	document.form.txtview.value=Math.cos(document.form.txtview.value);

}
function tanclicked(){
	document.form.txtview.value=Math.tan(document.form.txtview.value);
} 
 function ctgclicked() {
 	document.form.txtview.value= 1 / Math.tan(document.form.txtview.value);
 	 }
function sqrt(){
 document.form.txtview.value=Math.sqrt(document.form.txtview.value);
}

</script>



		

</html>
