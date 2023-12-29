<h1 align="center" paddin> МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</h1>

<p align="center">Лабораторная работа №8. «Разработка серверных скриптов». </p>

<p align="right">Выполнил: Рогаль Сергей Александрович</p>
<p align="right">Проверил: Соболев Е. И.</p>

<p align="center">г. Южно-Сахалинск <br> 2023 год</p>

<h2 align="center">Введение</h2>
<p align="justify">PHP — язык программирования, который наиболее распространён в сфере веб-разработки.
В настоящее время PHP является одним из лидеров среди серверных языков программирования, применяющихся для создания динамических веб-сайтов и веб-приложений. Большая часть коробочных систем управления сайтами написана именно на PHP, язык поддерживается подавляющим большинством хостинг-провайдеров, Язык получил широкое распространение благодаря своей простоте, скорости, мультипарадигмальности, богатой функциональности и кроссплатформенности.
</p>

<h2 align="center">Цели и задачи</h2>
<palign="justify">Цели: решить задачи с применением языка PHP</p>
<palign="justify">Задачи: применить технологии PHP.</p>

<h2>Решение задач</h2>

```php
<!DOCTYPE html>
<html>
<head>
<title>Лабораторная работа №8</title>
<meta charset="utf-8">
</head>
<body>
<h3>Задание1</h3>
<?php
//Меня зовут Сергей.
/*Дата выполнения работы:
28.12.2023
*/
echo "Здравствуй, это моя Лабораторная работа №8. Прошу любить и жаловать.";
?>
<h3>Задание2</h3>
<?php
echo "\$tvChannel";
echo "<br>";
echo "\$productionAddress";
echo "<br>";
echo "\$automobileColor";
echo "<br>";
echo "\$waterTemperature";
echo "<br>";
echo "\$telephoneModel";
?>
<h3>Задание3</h3>
<?php
$a = 3;
$b = 5;
$c = 8;
echo "Переменные \$a,\$b,\$c, их значения соответственно $a, $b, $c";
echo "<br>";
$res = $a+$b+$c;
echo "Их сумма $res";
echo "<br>";
$result = 2+6+2/5-1;
echo "result = $result";
?>
<h3>Задание4</h3>
<?php
$a = 1;
$b = 2;
echo "\$a = $a,\$b = $b";
echo "<br>";
$c = $a;
$d = &$b;
echo "\$c = $c,\$d = $d";
echo "<br>";
$a = 3;
$b = 4;
echo "Итог: \$a = $a,\$b = $b" . "\$c = $c,\$d = $d";
?>

<h3>Задание5</h3>
<?php
const a = 41;
const b = 33;
echo "a+b = ". $a+$b
?>
<h3>Задание6</h3>
<?php
$a = 152;
$b = '152';
$c = 'London';
$d = array(152);
$e = 15.2;
$f = false;
$g = true;
echo "Тип \$a - " . gettype($a);
echo "<br>";
echo "Тип \$b - " . gettype($b);
echo "<br>";
echo "Тип \$c - " . gettype($c);
echo "<br>";
echo "Тип \$d - " . gettype($d);
echo "<br>";
echo "Тип \$e - " . gettype($e);
echo "<br>";
echo "Тип \$f - " . gettype($f);
echo "<br>";
echo "Тип \$g - " . gettype($g);
?>
<h3>Задание7</h3>
<?php
$a = "Привет,";
$b = "мир";
echo "$a $b";
?>
<h3>Задание8</h3>
<?php
$a = "Доброе утро";
$b = "дамы";
$c = "и господа";
echo "\$a = $a, \$b = $b, \$c = $c <br>";
echo $a . ", " . $b . " " . $c;
?>
<h3>Задание9</h3>
<?php
$nums1 = [1, 2, 3, 4, 5];
$nums2 = [6, 7, 8, 9, 10];
$nums1['!'] = 0;
unset($nums2[0]);
echo "\$nums1[2] = " . $nums1[2] . " \$nums1[2] = " . $nums2[2] . "<br>";
echo "Массив1:<br>";
print_r($nums1);
echo "<br>";
echo "Массив2:<br>";
print_r($nums2);
echo "<br>";
echo "Количество элементов в массиве1: " . count($nums1);
echo "<br>";
echo "Количество элементов в массиве2: " . count($nums2);
?>
<h3>Задание10</h3>
<?php
$N = 5;
echo "$N случайных чисел от -21 до 35<br>";
for ($i = 0; $i < $N; $i++) {
    echo rand(-21, 35) . "<br>";
}
?>
<h3>Задание11</h3>
<?php
$N = 2;
$sum = 0;
for ($i = 0; $i < $N; $i++) {
    $sum+=rand(0, 10);
}
echo "Сумма $N случайных чисел равна $sum";
?>
<h3>Задание12</h3>
<?php
$N = 7;
$num1 = rand(0,20);
echo "$num1<br>";
for ($i = 1; $i < $N; $i++) {
    $num2 = rand(0,20);
	if($num2>$num1) echo "$num2 > $num1";
	if($num2<$num1) echo "$num2 < $num1";
	if($num2==$num1) echo "$num2 = $num1";
	$num1 = $num2;
	echo "<br>";
}
?>
<h3>Задание13</h3>
<?php
$N = 7;
$num1 = 1;
$num2 = 1;
$res = 0;
for ($i = 0; $i < $N-2; $i++) {
    $res = $num1+$num2;
	$num1 = $num2;
	$num2 = $res;
}
echo "$N число Фибоначчи равно " . $res;
?>
<h3>Задание14</h3>
<?php
$num = 1234;
echo "Дано число $num, вот число наоборот: ";
while($num>=1){
	echo $num%10;
	$num/=10;
}
?>
<h3>Задание15</h3>
<?php
$num = 1234;
$flag = false;
echo "Дано число $num, его нечетные цифры: ";
while($num>=1){
	$digit = $num%10;
	if($digit%2!=0){
		echo $digit . " ";
		$flag = true;
	}
	$num/=10;
}
if ($flag==false) "Нечетных цифр не обнаружено!"
?>
<h3>Задание16</h3>
<?php
$len = 7;
$arr = [];
for ($i = 0; $i < $len; $i++) {
    $arr[$i] = rand(0,10);
}
echo "Итоговый массив: ";
for ($i = 0; $i < $len; $i++) {
    echo $arr[$i]. " ";
}
?>
<h3>Задание17</h3>
<?php
$m = 7;
$n = 5;
$arr = array();
for ($i = 0; $i < $m; $i++) {
    for ($j = 0; $j < $n; $j++) {
    $arr[$i][$j] = rand(0,10);
}
}
echo "Итоговый массив:<br>";
for ($i = 0; $i < $m; $i++) {
    for ($j = 0; $j < $n; $j++) {
		echo $arr[$i][$j] . " ";
	}
echo "<br>";
}
?>
<h3>Задание18</h3>
<?php
$arr = range(1,10);
$count = 1;
$ind = 1;
for ($i = 0; $i < count($arr); $i++) {
    echo $arr[$i]. " ";
	if ($ind==$count) 
	{
		echo "<br>";
		$ind=0;
		$count+=1;
	}
	$ind++;
}
$count = 1;
$ind = 1;
for ($i = 1; $i <= 10; $i++) {
    echo $i. " ";
	if ($ind==$count) 
	{
		echo "<br>";
		$ind=0;
		$count+=1;
	}
	$ind++;
}
?>
<h3>Задание19</h3>
<?php
$len = 7;
$arr = [];
echo "Массив: ";
for ($i = 0; $i < $len; $i++) {
    $arr[$i] = rand(0,100);
	echo $arr[$i] . " ";
}
echo "<br>";
echo "Максимальное число в массиве: " . max($arr);
?>
<h3>Задание20</h3>
<?php
$len = 20;
$arr = [];
echo "Массив: ";
for ($i = 0; $i < $len; $i++) {
    $arr[$i] = rand(0,100);
	echo $arr[$i] . " ";
}
echo "<br>";
echo "Минимальное число в массиве: " . min($arr);
?>
<h3>Задание21</h3>
<?php
$len = 20;
$arr1 = [];
$arr2 = [];
echo "Массив1: ";
for ($i = 0; $i < $len; $i++) {
    $arr1[$i] = rand(-10,10);
	echo $arr1[$i] . " ";
}
echo "<br>Массив2: ";
for ($i = 0; $i < $len; $i++) {
    $arr2[$i] = rand(-10,10);
	echo $arr2[$i] . " ";
}
echo "<br>";
for ($i = 1; $i*3 < $len; $i++) {
    if($arr1[$i*3]>$arr2[$i*2]) echo $arr1[$i] . " > " . $arr2[$i];
	if($arr1[$i*3]<$arr2[$i*2]) echo $arr1[$i] . " < " . $arr2[$i];
	if($arr1[$i*3]==$arr2[$i*2]) echo $arr1[$i] . " = " . $arr2[$i];
	echo "<br>";
}
?>
<h3>Задание22</h3>
<?php
function foo($arr)
{
	for ($i = 0; $i < count($arr); $i++) {
		switch ($arr[$i]) {
    case 5:
        echo "пять";
        break;
    case 6:
        echo "шесть";
        break;
    case 7:
        echo "семь";
        break;
	 default:
       echo "какое-то другое число";
}
echo "<br>";
}
}
$len = 7;
$array = [];
echo "Массив: ";
for ($i = 0; $i < $len; $i++) {
    $array[$i] = rand(5,12);
	echo $array[$i] . " ";
}
echo "<br>Его интерпретация<br>";
foo($array);
?>
<h3>Задание23</h3>
<?php
$a = [];
$b = [12, 5, 17, 6, 4];
echo "Массив a: ";
for ($i = 0; $i < 10; $i++) {
    $a[$i] = rand(0,20);
	echo $a[$i] . " ";
}
echo "<br>Массив b: ";
for ($i = 0; $i < count($b); $i++) {
	echo $b[$i] . " ";
}
echo "<br>Элементы, которые не содержатся в массиве b (без in_array)<br>";
for ($i = 0; $i < 10; $i++) {
	$flag = false;
	for ($j = 0; $j < count($b); $j++) {
		if($a[$i]==$b[$j]){
			$flag = true;
		} 
	}
	if ($flag==false) echo $a[$i] . " ";
}
echo "<br>Элементы, которые не содержатся в массиве b (с in_array)<br>";
for ($i = 0; $i < 10; $i++) {
	if(!in_array($a[$i],$b)) echo $a[$i] . " ";
}
?>

</body>
</html>

```
<p>Реализуйте функцию, которая будет парсить JSON-файлы и выводить их содержимое в консоль.</p>

```javascript
let data = require('./users.json');
let string = JSON.stringify(data);
let res = JSON.parse(string);
for (var key in res){
    var value = res[key];
    console.log(key + ": " + value);
}
```
<p>Напишите скрипт, который будет перебирать файлы в заданной директории и выводить их имена в консоль.</p>

```javascript

const fs = require('fs');

fs.readdir('./', (err, files) => {
  if (err) throw err;
  console.log(files);
});

```

<p>Реализуйте функцию, которая будет отправлять email-уведомления при определенных событиях.</p>

```javascript
const express = require('express');
const nodemailer = require('nodemailer');
const app = express();

app.use(express.static(__dirname)); 

app.get('/mail', async (req, res) => {
    mail();
});

app.listen(3000, () => {
  console.log(`Сервер запущен на порту 3000`);
});

function mail(){
    console.log('нажали кнопку')
    let transporter = nodemailer.createTransport({
        host: 'hostname',
        port: port,
        secure: false,
        auth: {
            user:"mail",
            pass: "password",
        },
    });
    
    let result = transporter.sendMail({
        from: 'mail',
        to: 'mail',
        subject: 'Вы зачем на кнопку нажали?',
        text: 'В следующий раз не нажимайте'
    });
    console.log(result);
}

```

<p>Создайте модуль для работы с API сторонних сервисов.</p>

```javascript
function breakChocolate(n,m) {
  if(n*m-1<0) return 0;
  return n*m-1;
}
```

<p>Playing with digits</p>

```javascript
const express = require('express');
const app = express();
const getFact = require('./api.js');

app.use(express.static(__dirname)); 

app.listen(3000, () => {
  console.log(`Сервер запущен на порту 3000`);
});

app.get('/getFact', async (req, res) => {
  getFact.getFact().then(function(result){
    console.log(result);
    res.json({
      text: result
      });
  });
  
});
```
<p>api.js</p>

```javascript
const axios = require('axios');

async function getFact(){

        const response = await axios.get("https://uselessfacts.jsph.pl/api/v2/facts/random");
        const interestingFact = response.data; 
        return interestingFact.text;
}
module.exports = {getFact};
```

<p>Создайте модуль для работы с графическими изображениями (обработка, изменение размеров и т.д.).</p>

```javascript
const Jimp = require('jimp');

async function resizeImage(inputPath, outputPath, width, height) {
    try {
        const image = await Jimp.read(inputPath);
        await image.resize(width, height);
        await image.writeAsync(outputPath);
        console.log(`Изображение успешно изменено: ${outputPath}`);
    } catch (error) {
        console.error(`Ошибка при изменении размеров изображения: ${error.message}`);
        throw error;
    }
}

module.exports = {
    resizeImage,
};

```


<h2 align="center">Вывод</h2>
<p align="justify">Таким образом, я освежил в памяти работу с PHP, поработал со скриптами, написал модуль для отправки email, модуль для работы с изображениями, для работы с каталогами и JSON-файлами, все поставленные цели были выполнены. </p>
