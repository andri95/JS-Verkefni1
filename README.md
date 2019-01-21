# JS-Verkefni1 - Andri Fannar Pétursson

**1. Hvað er null og undefined?**
Ef breytu er gefið gildið null hefur breytan ekkert gildi en er samt ekki tóm (null er ekki það sama og 0, þar sem 0 er gildi). undefined þýðir að breytan er til en ekkert gildi hefur verið sett á hana.

**2. Hvað gerir 'use strict' í JavaScript kóða?**
Use strict neyðir translatorinn í vafranum til að stilla sig inn á ECMA-script 6 og þær reglur sem gilda þar.

**3. Hver er munurinn á let, var, const?**
var er global breyta. Eins og ég skildi þetta er let er takmarkað við blokkina sem það er skilgreint í. const er ekki hægt að update-a. Ég gæti td. ekki gert const nafn = "andri" og svo const nafn = "fannar". 

**4. Endurskrifaðu kóðann með for lykkjunni.**
	```javascript	
	let x; //Virkaði nákvæmlega eins með eða án let x;
	
	
	for(x = 9; x >= 1; x--){
		console.log("hello" + x);
	};
	```
**5. Skilgreindu sama fallið á þrjá mismunandi vegu.**
	```javascript
	function leggjaSaman(tala){
		return tala + tala;
	};

	var x = function (tala) {return tala + tala};

	const bla = () => {tala + tala};
	```
**6. Útskýrðu hvað eftirfarandi kóði gerir, hvað gera svigarnir?**
Náði þessu ekki alveg í tímanum, reyndi að finna eitthvað um þetta á netinu og eins og ég skil það eru ytri svigarnir fall, fallið að innan er parameter fyrir það fall. Man ekki hvað () í endan gerir.

**7. Af hverju birtist 1 en ekki 10? ....**
Átti í smá vandræðum með þetta. Ef ég keyri þetta svona:
	
	```javascript
	"use strict";
	let a = 1;
	function b(){
		a = 10;
		return;
	};
	b();
	console.log(a);
	```
	Fæ ég 10. Þegar function a er inní er eins og fallið virki ekki þar sem a er nú þegar til sem breyta. Veit ekki hvernig ég gæti endurraðað þessu til að virka þar sem a er skilgreint sem fall og breyta.

**8. Liður 20 í lesson 6:**
	
	```javascript
		var test = [12, 929, 11, 3, 199, 1000, 7, 1, 24, 37, 4,
	    19, 300, 3775, 299, 36, 209, 148, 169, 299,
	    6, 109, 20, 58, 139, 59, 3, 1, 139];

	// Write your code here

	test.forEach(function(testTala, index){
	    if (testTala % 3 === 0){
	        test[index] = testTala + 100;
	    }
	});

	console.log(test);
	```
**9. Liður 22 í lesson 6:**
	
	```javascript
	var bills = [50.23, 19.12, 34.01,
    100.11, 12.15, 9.90, 29.11, 12.99,
    10.00, 99.22, 102.20, 100.10, 6.77, 2.22];

	var totals = bills.map(function(totalsTala){
	    totalsTala *= 1.15;
	    totalsTala = parseFloat(totalsTala.toFixed(2));
	    return totalsTala;
	});

	console.log(totals);
	```
**10. Stack Overflow:**
	
	Eitthvað í þessa áttina held ég:
	
	```javascript
		function a () {
		let nafn = "andri ";
		return nafn + b();
	};

	function b () {
		let millinafn = "fannar ";
		return millinafn + c();
	};

	function c () {
		let eftirnafn = "petursson ";
		return eftirnafn + d();
	};

	function d () {
		let gerir = "er i tækniskolanum ";
		return gerir + e();
	};

	function e() {
		let vinna = "og vinnur hjá ISAL ";
		return vinna + f();
	};

	function f () {
		let broskall = ":)"
		return broskall;
	};
	```
