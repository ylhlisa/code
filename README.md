<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>IFE JavaScript Task 22</title>
    <style>
        #dic{
            width: 400px;
            height: 500px;
            border: 1px solid red;
        }
    </style>
</head>
<body>
<input type="text" id="num">
<button id="btn">插入</button>
<div id="dic">

</div>
<script type="text/javascript" >

    function Btn(){
        var date=new  Array();
        var use=new Array();

        date=document.getElementById('num').value;
        var value=date.split(' ');
        var j=0;
        for(var i=0;i<value.length;i+=2){
            var n=value[i];
            var m=value[i+1];
            var tital=0.0;
            if((n!=0)&&(m!=0)){
                tital=sum(n,m);
                var div=document.getElementById('dic');
                j++;
                var span=document.createElement('span');
                span.innerHTML='Case '+j+':  '+tital.toFixed(5)+'<br>';
                div.appendChild(span);
            }
        }
    }
    function sum(n,m) {
        var sum=0.0;
        for(var i= n;i<=m;i++){
            sum+=(1.0/(i*i));
        }
        return sum;
    }
    function init(){
        document.getElementById('btn').onclick=function(){
            Btn();
        }
    }
    init();
</script>
</body>
</html>
