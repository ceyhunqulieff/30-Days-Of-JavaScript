<div align="center">
  <h1> 30 Günlük JavaScript: Məlumat növləri</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

<sub>Müəllif:
<a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
<small> Yanvar, 2020</small>
</sub>

</div>
</div>

[<< Gün 1](../README.md) | [Gün 3 >>](../03_Day_Booleans_operators_date/03_booleans_operators_date.md)

![Thirty Days Of JavaScript](../../images/banners/day_1_2.png)

- [📔 Gün 2](#-day-2)
  - [Məlumat növləri «Data Types»](#data-types)
    - [Primitiv məlumat növləri «Primitive Data Types»](#primitive-data-types)
    - [Primitiv olmayan məlumat növləri «Non-Primitive Data Types»](#non-primitive-data-types)
  - [Ədədlər «Numbers»](#numbers)
    - [Ədəd məlumat növlərinin bildirilməsi](#declaring-number-data-types)
    - [Riyazi obyekt «Math Object»](#math-object)
      - [Təsadüfi rəqəm hazırlayıcı](#random-number-generator)
  - [Sətirlər «Strings»](#strings)
    - [Sətir birləşdirmə](#string-concatenation)
      - [Toplama operatorundan istifadə edərək birləşdirmə](#concatenating-using-addition-operator)
      - [Uzun dəyişilməyən sətirlər](#long-literal-strings)
      - [Sətirlərdəki qaçış simvolu](#escape-sequences-in-strings)
      - [Şablon Sətirləri](#template-literals-template-strings)
    - [Sətir üsulları «String Methods»](#string-methods)
  - [Məlumat növlərinin yoxlanılması və dərc edilməsi](#checking-data-types-and-casting)
    - [Məlumat növlərinin yoxlanılması](#checking-data-types)
    - [Məlumat növünün dəyişdirilməsi(Casting)](#changing-data-type-casting)
      - [String-dən Integerə çevirmək](#string-to-int)
      - [String-dən Floata çevirmək](#string-to-float)
      - [Float-dan Integerə çevirmək](#float-to-int)
  - [💻 Gün 2: Məşqlər](#-day-2-exercises)
    - [Məşq: Səviyyə 1](#exercise-level-1)
    - [Məşq: Səviyyə 2](#exercise-level-2)
    - [Məşqlər: Səviyyə 3](#exercises-level-3)

# 📔 Gün 2

## Məlumat növləri «Data Types»

Əvvəlki bölmədə məlumat növləri haqqında bir az bəhs etdik. Məlumat və ya dəyərlərin məlumat növləri var. Məlumat növləri verilənlərin xüsusiyyətlərini təsvir edir. Məlumat növlərini iki yerə bölmək olar:

1. Primitiv məlumat növləri «Primitive Data Types»
2. Primitiv olmayan məlumat növləri(Obyekt Referansları) «Non-Primitive Data Types(Object References)»

### Primitiv məlumat növləri «Primitive Data Types»

JavaScript-də primitiv(ibtidai) məlumat növlərinə aşağıdakılar daxildir:

1.  Numbers - Integers, floats(Ədədlər - Tam ədədlər, Onluq qiymətlər)
2.  Strings - Tək dırnaq, cüt dırnaq və ya geri işarə içərisində olan hər hansı məlumat
3.  Booleans - doğru və ya yanlış dəyər
4.  Null - boş dəyər və ya dəyər yoxdur
5.  Undefined - dəyəri olmayan elan edilmiş dəyişən

JavaScriptdə Primitiv olmayan məlumat növlərinə aşağıdakılar daxildir:

1. Obyektlər
2. Funksiyalar
3. Massivlər

İndi gəlin görək primitiv və primitiv olmayan məlumat növlərinin tam olaraq nə demək olduğunu. _Primitiv_ məlumat növləri dəyişməz (dəyişdirilə bilməyən) məlumat növləridir. Primitiv məlumat növü yaradıldıqdan sonra onu dəyişdirə bilmərik.

**Misal:**

```js
let word = "JavaScript";
```

Dəyişən _word_ saxlanılan sətri dəyişdirməyə çalışsaq, JavaScript xəta yaratmalıdır. Tək dırnaq, cüt dırnaq və ya geri işarə arasında olan istənilən məlumat növü sətir məlumat növüdür.

```js
word[0] = "Y";
```

Bu ifadə dəyişən _word_ saxlanılan sətri dəyişmir. Beləliklə, deyə bilərik ki, sətirlər dəyişdirilə bilməz və ya başqa sözlə dəyişməzdir. Primitiv məlumat növləri dəyərləri ilə müqayisə edilir. Fərqli məlumat dəyərlərini müqayisə edək. Aşağıdakı nümunəyə baxın:

```js
let numOne = 3;
let numTwo = 3;

console.log(numOne == numTwo); // true(doğru)

let js = "JavaScript";
let py = "Python";

console.log(js == py); //false(yanlış)

let lightOn = true;
let lightOff = false;

console.log(lightOn == lightOff); // false(yanlış)
```

### Primitiv olmayan məlumat növləri «Non-Primitive Data Types»

_Qeyri-primitiv_ məlumat növləri dəyişdirilə bilən və ya dəyişkəndir. Primitiv olmayan məlumat növləri yaradıldıqdan sonra onların dəyərini dəyişdirə bilərik. Bir massiv yaradaraq baxaq. Massiv kvadrat mötərizədə verilənlər dəyərlərinin siyahısıdır. Massivlər eyni və ya fərqli məlumat növlərini özündə saxlaya bilər. Massiv dəyərlərinə onların indeksi ilə istinad edilir. JavaScript-də massiv indeksi sıfırdan başlayır. Yəni, massivin birinci elementi indeks sıfırda, ikinci elementi isə birinci indeksdə, üçüncü element isə ikinci indeksdə və s.

```js
let nums = [1, 2, 3];
nums[0] = 10;

console.log(nums); // [10, 2, 3]
```

Gördüyünüz kimi, primitiv olmayan məlumat növü olan massiv dəyişkəndir. Primitiv olmayan məlumat növləri dəyərlə müqayisə edilə bilməz. İki qeyri-primitiv məlumat növü eyni xassələrə və dəyərlərə malik olsa belə, onlar ciddi şəkildə bərabər deyillər.

```js
let nums = [1, 2, 3];
let numbers = [1, 2, 3];

console.log(nums == numbers); // false(yanlış)

let userOne = {
  name: "Asabeneh",
  role: "teaching",
  country: "Finland",
};

let userTwo = {
  name: "Asabeneh",
  role: "teaching",
  country: "Finland",
};

console.log(userOne == userTwo); // false(yanlış)
```

Əsas qayda, biz primitiv olmayan məlumat növlərini müqayisə etmirik. Massivləri, funksiyaları və ya obyektləri müqayisə etməyin. Qeyri-primitiv dəyərlərə istinad növləri deyilir, çünki onlar dəyər əvəzinə istinadla müqayisə edilir. İki obyekt yalnız eyni əsas obyektə istinad etdikdə ciddi şəkildə bərabərdir.

```js
let nums = [1, 2, 3];
let numbers = nums;

console.log(nums == numbers); // true(doğru)

let userOne = {
  name: "Asabeneh",
  role: "teaching",
  country: "Finland",
};

let userTwo = userOne;

console.log(userOne == userTwo); // true(doğru)
```

Primitiv məlumat növləri ilə qeyri-primitiv məlumat növləri arasındakı fərqi anlamaqda çətinlik çəkirsinizsə, tək siz deyilsiniz. Sakitləşin və sadəcə növbəti hissəyə keçin və bir müddət sonra geri qayıtmağa çalışın. İndi ədəd tipinə görə məlumat növlərinə başlayaq.

## Ədədlər «Numbers»

Ədədlər bütün riyazi əməliyyatları yerinə yetirə bilən tam ədədlər və onluq qiymətlərdir. Ədədlərin bəzi nümunələrinə baxaq.

### Ədəd məlumat növlərinin bildirilməsi

```js
let age = 35;
const gravity = 9.81; // dəyişməyən qiymətlər üçün const-dan istifadə edirik, m/s2-də qravitasiya sabiti
let mass = 72; // kiloqramda kütlə
const PI = 3.14; // pi həndəsi sabitdir

// More Examples
const boilingPoint = 100; // oC-də temperatur, sabit olan suyun qaynama nöqtəsi
const bodyTemp = 37; // oC sabit olan orta insan bədən istiliyi

console.log(age, gravity, mass, PI, boilingPoint, bodyTemp);
```

### Riyazi obyekt «Math Object»

JavaScript-də Riyaziyyat Obyekti rəqəmlərlə işləmək üçün çoxlu üsullar təqdim edir.

```js
const PI = Math.PI;

console.log(PI); // 3.141592653589793

// Ən yaxın nömrəyə yuvarlaqlaşdırma
// Əgər .5 -dirsə və ya 0.5-dən yuxarıdırsa yuxarı yavarlaşdırılır

console.log(Math.round(PI)); // Dəyərləri ən yaxın ədədə yuvarlaqlaşdırmaq üçün 3

console.log(Math.round(9.81)); // 10

console.log(Math.floor(PI)); // aşağı yuvarlaşdırır 3

console.log(Math.ceil(PI)); // yuxarı yuvarlaşdırır 4

console.log(Math.min(-5, 3, 20, 4, 5, 10)); // -5, minimum dəyəri qaytarır

console.log(Math.max(-5, 3, 20, 4, 5, 10)); // 20, maksimum dəyəri qaytarır

const randNum = Math.random(); // 0 ilə 0,999999 arasında təsadüfi ədəd yaradır
console.log(randNum);

// Gəlin 0 ilə 10 arasında təsadüfi ədəd yaradaq

const num = Math.floor(Math.random() * 11); // 0 ilə 10 arasında təsadüfi ədəd yaradır
console.log(num);

//Mütləq dəyər - Modul
console.log(Math.abs(-10)); // 10

//Kvadrat kök
console.log(Math.sqrt(100)); // 10

console.log(Math.sqrt(2)); // 1.4142135623730951

// Qüvvətə yüksəltmə
console.log(Math.pow(3, 2)); // 9

console.log(Math.E); // 2.718

// Loqarifm
// x, Math.log(x) E əsası ilə natural loqarifmanı qaytarır
console.log(Math.log(2)); // 0.6931471805599453
console.log(Math.log(10)); // 2.302585092994046

// Triqonometriya
Math.sin(0);
Math.sin(60);

Math.cos(0);
Math.cos(60);
```

#### Təsadüfi rəqəm hazırlayıcı

JavaScript Riyaziyyat Obyektində 0-dan 0,999999999-a qədər rəqəm yaradan random() metodu ilə ədəd generatoru var...

```js
let randomNum = Math.random(); // 0-dan 0.999-a qədər yaradır...
```

İndi gəlin görək 0 ilə 10 arasında təsadüfi ədəd yaratmaq üçün random() metodundan necə istifadə edə bilərik:

```js
let randomNum = Math.random(); // 0-dan 0.999-a qədər yaradır
let numBtnZeroAndTen = randomNum * 11;

console.log(numBtnZeroAndTen); // bu verir: min 0 və maksimum 10,99

let randomNumRoundToFloor = Math.floor(numBtnZeroAndTen);
console.log(randomNumRoundToFloor); // bu isə 0 ilə 10 arasında verir
```

## Sətirlər «Strings»

Strings(Sətirlər) **_tək dırnaq_**, **_cüt dırnaq_**, **_geri işarəsi_** altında olan mətnlərdir. Sətiri elan etmək üçün bizə dəyişən adı, təyin operatoru, tək dırnaq altındakı dəyər, cüt dırnaq və ya geri işarə simvolları lazımdır.
Bir neçə sətir nümunəsinə baxaq:

```js
let space = " "; // boş
let firstName = "Asabeneh";
let lastName = "Yetayeh";
let country = "Finland";
let city = "Helsinki";
let language = "JavaScript";
let job = "teacher";
let quote = "The saying,'Seeing is Believing' is not correct in 2020."; //* Cüt dırnaq daxilində tək dırnaq istifadə etmək olar, qaçış simvolu istifadə etmədən. Bunun əksidə doğrudur - '"Bunun kimi"'. */
let quotWithBackTick = `The saying,'Seeing is Believing' is not correct in 2020.`;
```

### Sətir birləşdirmə

İki və ya daha çox sətirin bir-birinə bağlanmasına birləşmə deyilir. Əvvəlki String bölməsində elan edilmiş sətirlərdən istifadə etməklə:

```js
let fullName = firstName + space + lastName; // birləşdirmək, iki və daha çox string-i birləşdirmək.
console.log(fullName);
```

```sh
Asabeneh Yetayeh
```

Biz sətirləri müxtəlif yollarla birləşdirə bilərik.

#### Toplama operatorundan istifadə edərək birləşdirmə

Toplama operatorundan istifadə edərək birləşmə köhnə üsuldur. Bu birləşmə üsulu yorucu və səhvlərə meyllidir. Bu şəkildə necə birləşdiriləcəyini bilmək yaxşıdır, lakin mən ES6(ECMA Script 6) şablon sətirlərindən istifadə etməyi şiddətlə təklif edirəm (daha sonra izah ediləcək).

```js
// Müxtəlif məlumat növlərinin müxtəlif dəyişənlərinin elan(bəyan) edilməsi
let space = " ";
let firstName = "Asabeneh";
let lastName = "Yetayeh";
let country = "Finland";
let city = "Helsinki";
let language = "JavaScript";
let job = "teacher";
let age = 250;

let fullName = firstName + space + lastName;
let personInfoOne = fullName + ". I am " + age + ". I live in " + country; // ES5(ECMA Script 5) - string əlavə etmə üsulu

console.log(personInfoOne);
```

```sh
Asabeneh Yetayeh. I am 250. I live in Finland
```

#### Uzun dəyişilməyən sətirlər

Sətir tək simvol, paraqraf və ya daha çox uzunluqda ola bilər. Əgər string uzunluğu çox böyükdürsə, o, bir xəttə uyğun gəlmir. Sətirin növbəti sətirdə davam edəcəyini göstərmək üçün hər sətrin sonunda əks slash işarəsindən (\) istifadə edə bilərik.
**Misal:**

```js
const paragraph =
  "My name is Asabeneh Yetayeh. I live in Finland, Helsinki.\
I am a teacher and I love teaching. I teach HTML, CSS, JavaScript, React, Redux, \
Node.js, Python, Data Analysis and D3.js for anyone who is interested to learn. \
In the end of 2019, I was thinking to expand my teaching and to reach \
to global audience and I started a Python challenge from November 20 - December 19.\
It was one of the most rewarding and inspiring experience.\
Now, we are in 2020. I am enjoying preparing the 30DaysOfJavaScript challenge and \
I hope you are enjoying too.";

console.log(paragraph);
```

#### Sətirlərdəki qaçış simvolu

JavaScript və digər proqramlaşdırma dillərində \ simvolun ardınca yazılan simvollar qaçış rolun oynuyur. Ən çox yayılmış qaçış simvollarına baxaq:

- \n: yeni sətir
- \t: Tab
- \\\\: Tərs əyri xətt
- \\': tək dırnaq (')
- \\": cüt dırnaq (")

```js
console.log(
  "I hope everyone is enjoying the 30 Days Of JavaScript challenge.\nDo you ?"
); // sətir sonu
console.log("Days\tTopics\tExercises");
console.log("Day 1\t3\t5");
console.log("Day 2\t3\t5");
console.log("Day 3\t3\t5");
console.log("Day 4\t3\t5");
console.log("This is a backslash  symbol (\\)"); // Tərs əyri xətt yazmaq üçün
console.log('In every programming language it starts with "Hello, World!"');
console.log("In every programming language it starts with 'Hello, World!'");
console.log("The saying 'Seeing is Believing' isn't correct in 2020");
```

Konsolda çıxış:

```sh
I hope everyone is enjoying the 30 Days Of JavaScript challenge.
Do you ?
Days  Topics  Exercises
Day 1 3 5
Day 2 3 5
Day 3 3 5
Day 4 3 5
This is a backslash  symbol (\)
In every programming language it starts with "Hello, World!"
In every programming language it starts with 'Hello, World!'
The saying 'Seeing is Believing' isn't correct in 2020
```

#### Şablon Sətirləri

Şablon sətirləri yaratmaq üçün iki geri işarədən istifadə edirik. Şablon sətirinə ifadələr kimi verilənləri yeridə bilərik. Məlumatı daxil etmək üçün ifadəni qarşısında $ işarəsi olan əyri mötərizə ({}) ilə əhatə edirik. Aşağıdakı sintaksisə baxın.

```js
//Sintaksis
`String literal text``String literal text ${expression}`;
```

**Misal: 1**

```js
console.log(`The sum of 2 and 3 is 5`); // məlumatların statik şəkildə yazılması
let a = 2;
let b = 3;
console.log(`The sum of ${a} and ${b} is ${a + b}`); // məlumatların dinamik şəkildə yeridilməsi
```

**Misal: 2**

```js
let firstName = "Asabeneh";
let lastName = "Yetayeh";
let country = "Finland";
let city = "Helsinki";
let language = "JavaScript";
let job = "teacher";
let age = 250;
let fullName = firstName + " " + lastName;

let personInfoTwo = `I am ${fullName}. I am ${age}. I live in ${country}.`; //ES6 - String interpolyasiya üsulu
let personInfoThree = `I am ${fullName}. I live in ${city}, ${country}. I am a ${job}. I teach ${language}.`;
console.log(personInfoTwo);
console.log(personInfoThree);
```

```sh
I am Asabeneh Yetayeh. I am 250. I live in Finland.
I am Asabeneh Yetayeh. I live in Helsinki, Finland. I am a teacher. I teach JavaScript.
```

Bir sətir şablonu və ya sətir interpolyasiyası metodundan istifadə edərək, biz ifadələr əlavə edə bilərik, bunlar dəyər ola bilər və ya bəzi əməliyyatlar (müqayisə, riyazi əməliyyatlar, üçlü əməliyyat).

```js
let a = 2;
let b = 3;
console.log(`${a} is greater than ${b}: ${a > b}`);
```

```sh
2 is greater than 3: false
```

### Sətir üsulları «String Methods»

JavaScript-də hər şey bir obyektdir. Sətir primitiv məlumat növüdür ki, onu yaradıldıqdan sonra dəyişdirə bilməyəcəyik. Sətir obyekti çoxlu sətir metodlarına malikdir. Sətirlərlə işləməkdə bizə kömək edə biləcək müxtəlif string üsulları var.

1. _length_: Sətir _uzunluğu_ metodu daxil edilmiş String-in simvolların sayını qaytarır.

**Misal:**

```js
let js = "JavaScript";
console.log(js.length); // 10
let firstName = "Asabeneh";
console.log(firstName.length); // 8
```

2. _Sətirdəki simvollara daxil olmaq:_ Biz onun indeksindən istifadə edərək sətirdəki hər simvola daxil ola bilərik. Proqramlaşdırmada sayma 0-dan başlayır. Sətirin birinci indeksi sıfıra, sonuncu indeks isə sətirin uzunluğu çıxılsın birə bərabərdir.

![Accessing sting by index](../../images/string_indexes.png)

'JavaScript' sətirində müxtəlif simvollara daxil olaq.

```js
let string = "JavaScript";
let firstLetter = string[0];

console.log(firstLetter); // J

let secondLetter = string[1]; // a
let thirdLetter = string[2];
let lastLetter = string[9];

console.log(lastLetter); // t

let lastIndex = string.length - 1;

console.log(lastIndex); // 9
console.log(string[lastIndex]); // t
```

3. _toUpperCase():_ bu üsul sətri böyük hərflərə dəyişir.

```js
let string = "JavaScript";

console.log(string.toUpperCase()); // JAVASCRIPT

let firstName = "Asabeneh";

console.log(firstName.toUpperCase()); // ASABENEH

let country = "Finland";

console.log(country.toUpperCase()); // FINLAND
```

4. _toLowerCase()_: bu üsul sətri kiçik hərflərə dəyişir.

```js
let string = "JavasCript";

console.log(string.toLowerCase()); // javascript

let firstName = "Asabeneh";

console.log(firstName.toLowerCase()); // asabeneh

let country = "Finland";

console.log(country.toLowerCase()); // finland
```

5. _substr()_: Dilimləmək üçün iki arqument, başlanğıc indeksi və simvolların sayı lazımdır.

```js
let string = "JavaScript";
console.log(string.substr(4, 6)); // Script

let country = "Finland";
console.log(country.substr(3, 4)); // land
```

6. _substring()_: O, iki arqument tələb edir, başlanğıc indeksi və dayanma indeksi, lakin dayanma indeksindəki simvolu daxil etmir.

```js
let string = "JavaScript";

console.log(string.substring(0, 4)); // Java
console.log(string.substring(4, 10)); // Script
console.log(string.substring(4)); // Script

let country = "Finland";

console.log(country.substring(0, 3)); // Fin
console.log(country.substring(3, 7)); // land
console.log(country.substring(3)); // land
```

7. _split()_: Split metodu sətri müəyyən edilmiş yerdə bölür.

```js
let string = "30 Days Of JavaScript";

console.log(string.split()); // Massivlə dəyişdirin -> ["30 Days Of JavaScript"]
console.log(string.split(" ")); // Boşluq vasitəsi ilə massivlərə bölün -> ["30", "Days", "Of", "JavaScript"]

let firstName = "Asabeneh";

console.log(firstName.split()); // Massivlə dəyişdirin- > ["Asabeneh"]
console.log(firstName.split("")); // Hər hərfdən bir massivlərə bölün ->  ["A", "s", "a", "b", "e", "n", "e", "h"]

let countries = "Finland, Sweden, Norway, Denmark, and Iceland";

console.log(countries.split(",")); // vergüllə massivə bölün -> ["Finland", " Sweden", " Norway", " Denmark", " and Iceland"]
console.log(countries.split(", ")); //  ["Finland", "Sweden", "Norway", "Denmark", "and Iceland"]
```

8. _trim()_: Sətirin əvvəlində və ya sonundakı boşluqları silir.

```js
let string = "   30 Days Of JavaScript   ";

console.log(string);
console.log(string.trim(" "));

let firstName = " Asabeneh ";

console.log(firstName);
console.log(firstName.trim()); //sətirin əvvəlində və sonunda boşluqları silir
```

```sh
   30 Days Of JavasCript
30 Days Of JavasCript
  Asabeneh
Asabeneh
```

9. _includes()_: O, alt sətir arqumentini götürür və sətirdə alt sətir arqumentinin olub olmadığını yoxlayır. _includes()_ boolean qaytarır. Əgər sətirdə arqument kimi verdiyimiz sətir varsa, o, doğru, əks halda isə yalan qaytarır.

```js
let string = "30 Days Of JavaScript";

console.log(string.includes("Days")); // true
console.log(string.includes("days")); // false - hərflərə həssasdır!
console.log(string.includes("Script")); // true
console.log(string.includes("script")); // false
console.log(string.includes("java")); // false
console.log(string.includes("Java")); // true

let country = "Finland";

console.log(country.includes("fin")); // false
console.log(country.includes("Fin")); // true
console.log(country.includes("land")); // true
console.log(country.includes("Land")); // false
```

10. _replace()_: parametr kimi köhnə alt sətir və yeni alt sətir götürür.

```js
string.replace(oldsubstring, newsubstring);
```

```js
let string = "30 Days Of JavaScript";
console.log(string.replace("JavaScript", "Python")); // 30 Days Of Python

let country = "Finland";
console.log(country.replace("Fin", "Noman")); // Nomanland
```

11. _charAt()_: İndeks götürür və həmin indeksdəki dəyəri qaytarır

```js
string.charAt(index);
```

```js
let string = "30 Days Of JavaScript";
console.log(string.charAt(0)); // 3

let lastIndex = string.length - 1;
console.log(string.charAt(lastIndex)); // t
```

12. _charCodeAt()_: İndeksi götürür və həmin indeksdəki dəyərin simvol kodunu (ASCII nömrəsi) qaytarır

```js
string.charCodeAt(index);
```

```js
let string = "30 Days Of JavaScript";
console.log(string.charCodeAt(3)); // D ASCII number is 68

let lastIndex = string.length - 1;
console.log(string.charCodeAt(lastIndex)); // t ASCII is 116
```

13. _indexOf()_: Alt sətir götürür və əgər alt sətir sətirdə mövcuddursa başlanğıcdan index nömrəsini və yaxud mövcud deyilsə, alt sətirin ilk mövqeyini qaytarır -1

```js
string.indexOf(substring);
```

```js
let string = "30 Days Of JavaScript";

console.log(string.indexOf("D")); // 3
console.log(string.indexOf("Days")); // 3
console.log(string.indexOf("days")); // -1
console.log(string.indexOf("a")); // 4
console.log(string.indexOf("JavaScript")); // 11
console.log(string.indexOf("Script")); //15
console.log(string.indexOf("script")); // -1
```

14. _lastIndexOf()_: Alt sətir götürür və əgər alt sətir sətirdə mövcuddursa sondan index nömrəsini və yaxud mövcud deyilsə, alt sətirin son mövqeyini qaytarır -1

```js
//sintaksis
string.lastIndexOf(substring);
```

```js
let string =
  "I love JavaScript. If you do not love JavaScript what else can you love.";

console.log(string.lastIndexOf("love")); // 67
console.log(string.lastIndexOf("you")); // 63
console.log(string.lastIndexOf("JavaScript")); // 38
```

15. _concat()_: çoxlu alt sətirləri götürür mövcud sətirə birləşdirir.

```js
string.concat(substring, substring, substring);
```

```js
let string = "30";
console.log(string.concat("Days", "Of", "JavaScript")); // 30DaysOfJavaScript

let country = "Fin";
console.log(country.concat("land")); // Finland
```

16. _startsWith_: O, arqument kimi bir alt sətir götürür və sətirin həmin göstərilən alt sətirlə başlamasını yoxlayır. Boolean (doğru və ya yanlış) qaytarır.

```js
//sintaksis
string.startsWith(substring);
```

```js
let string = "Love is the best to in this world";

console.log(string.startsWith("Love")); // true
console.log(string.startsWith("love")); // false
console.log(string.startsWith("world")); // false

let country = "Finland";

console.log(country.startsWith("Fin")); // true
console.log(country.startsWith("fin")); // false
console.log(country.startsWith("land")); //  false
```

17. _endsWith_: o, arqument kimi alt sətir götürür və sətirin həmin göstərilən alt sətirlə bitib-bitmədiyini yoxlayır. Boolean (doğru və ya yanlış) qaytarır.

```js
string.endsWith(substring);
```

```js
let string = "Love is the most powerful feeling in the world";

console.log(string.endsWith("world")); // true
console.log(string.endsWith("love")); // false
console.log(string.endsWith("in the world")); // true

let country = "Finland";

console.log(country.endsWith("land")); // true
console.log(country.endsWith("fin")); // false
console.log(country.endsWith("Fin")); //  false
```

18. _search_: arqument kimi alt sətir götürür və ilk uyğunluğun indeksini qaytarır. Axtarış dəyəri sətir və ya qaydalı ifadə nümunəsi ola bilər.

```js
string.search(substring);
```

```js
let string =
  "I love JavaScript. If you do not love JavaScript what else can you love.";
console.log(string.search("love")); // 2
console.log(string.search(/javascript/gi)); // 7
```

19. _match_: o, arqument kimi alt sətir və ya qaydalı ifadə nümunəsini götürür və uyğunluq varsa massivi qaytarır, yoxsa null qaytarır. Gəlin qaydalı ifadə nümunəsinin necə göründüyünü görək. / işarəsi ilə başlayır və / işarəsi ilə bitir.

```js
let string = "love";
let patternOne = /love/; // heç bir bayraq olmadan
let patternTwo = /love/gi; // g-bütün mətndə axtarış deməkdir, i - hərflərə həssas deyil
```

Sintaksisi uyğunlaşdırın - Match syntax

```js
// sintaksis
string.match(substring);
```

```js
let string =
  "I love JavaScript. If you do not love JavaScript what else can you love.";
console.log(string.match("love"));
```

```sh
["love", index: 2, input: "I love JavaScript. If you do not love JavaScript what else can you love.", groups: undefined]
```

```js
let pattern = /love/gi;
console.log(string.match(pattern)); // ["love", "love", "love"]
```

Qaydalı ifadədən istifadə edərək mətndən rəqəmləri çıxaraq. Bu qaydalı ifadə bölməsi deyil, panik etməyin! Daha sonra qaydalı ifadələrə toxunacağıq.

```js
let txt =
  "In 2019, I ran 30 Days of Python. Now, in 2020 I am super exited to start this challenge";
let regEx = /\d+/;

// qaçış simvolu ilə d hərfi - normal d hərfi demək deyil, rəqəmlər üçün fəaliyyət göstərir.
// + bir və ya bir neçə rəqəmli rəqəm deməkdir,
// əgər ondan sonra g varsa, bu qlobal deməkdir, hər yerdə axtarın.

console.log(txt.match(regEx)); // ["2", "0", "1", "9", "3", "0", "2", "0", "2", "0"]
console.log(txt.match(/\d+/g)); // ["2019", "30", "2020"]
```

20. _repeat()_: o, arqument kimi bir ədəd götürür və həmin ədəd qədər ifadəni təkrarlayır.

```js
string.repeat(n);
```

```js
let string = "love";
console.log(string.repeat(10)); // lovelovelovelovelovelovelovelovelovelove
```

## Məlumat növlərinin yoxlanılması və dərc edilməsi

### Məlumat növlərinin yoxlanılması

Müəyyən bir dəyişənin məlumat tipini yoxlamaq üçün _typeof_ metodundan istifadə edirik.

**Misal:**

```js
// Müxtəlif javascript məlumat növləri
// Müxtəlif məlumat növlərini elan edək

let firstName = "Asabeneh"; // string
let lastName = "Yetayeh"; // string
let country = "Finland"; // string
let city = "Helsinki"; // string
let age = 250; // number, mənim əsl yaşım deyil, ona görə narahat olmayın
let job; // undefined, çünki dəyər təyin olunmayıb

console.log(typeof "Asabeneh"); // string
console.log(typeof firstName); // string
console.log(typeof 10); // number
console.log(typeof 3.14); // number
console.log(typeof true); // boolean
console.log(typeof false); // boolean
console.log(typeof NaN); // number
console.log(typeof job); // undefined
console.log(typeof undefined); // undefined
console.log(typeof null); // object
```

### Məlumat növünün dəyişdirilməsi(Casting)

- Casting : Bir məlumat növünün digər məlumat növünə çevrilməsi. Biz _parseInt()_, _parseFloat()_, _Number()_, _+ sign_, _str()_ funksiyalarından istifadə edirik. Hesab əməliyyatları edərkən sətir daxilindəki ədədlər əvvəlcə tam ədədə(integer) çevrilməlidir və ya xəta qaytarmırsa onluq kəsrlərə(float).

#### String-dən Integerə çevirmək

Biz sətir daxilindəki ədədləri, ədəd məlumat növünə çevirə bilərik. İfadə daxilindəki hər hansı bir ədəd sətir ədəddir. Sətir ədədlərinə misal: '10', '5' və s. Biz aşağıdakı üsullardan istifadə edərək sətrləri ədədlərə çevirə bilərik:

- parseInt()
- Number()
- Plus sign(+)

```js
let num = "10";
let numInt = parseInt(num);
console.log(numInt); // 10
```

```js
let num = "10";
let numInt = Number(num);

console.log(numInt); // 10
```

```js
let num = "10";
let numInt = +num;

console.log(numInt); // 10
```

#### String-dən Floata çevirmək

Biz sətirlərdəki kəsr ədədləri float məlumat növünə çevirə bilərik. Sətir daxilindəki hər hansı float ədədi sətir float ədədidir. Sətir float ədədlərinə nümunə: '9.81', '3.14', '1.44' və s.

- parseFloat()
- Number()
- Plus sign(+)

```js
let num = "9.81";
let numFloat = parseFloat(num);

console.log(numFloat); // 9.81
```

```js
let num = "9.81";
let numFloat = Number(num);

console.log(numFloat); // 9.81
```

```js
let num = "9.81";
let numFloat = +num;

console.log(numInt); // 9.81
```

#### Float-dan Integerə çevirmək

Biz float ədədləri tam ədədlərə çevirə bilərik. floatı int-ə çevirmək üçün aşağıdakı üsuldan istifadə edirik:

- parseInt()

```js
let num = 9.81;
let numInt = parseInt(num);

console.log(numInt); // 9
```

🌕 Möhtəşəmsiz. 2-ci günü yenicə tamamladınız və mükəmməlliyə doğru gedirsiniz. İndi beyniniz və əzələniz üçün aşağıdakı məşqlər edin.

## 💻 Gün 2: Məşqlər

### Məşq edin: Səviyyə 1

1. Çağırış adlı dəyişəni elan edin və onu **“30 Days Of JavaScript”** ilkin dəyərinə təyin edin.
2. **console.log()** istifadə edərək brauzer konsolunda sətri çap edin
3. _console.log()_ istifadə edərək brauzer konsolunda sətir **uzunluğunu** çap edin
4. **toUpperCase()** metodundan istifadə edərək bütün sətir simvollarını böyük hərflərə dəyişdirin
5. **toLowerCase()** metodundan istifadə edərək bütün sətir simvollarını kiçik hərflərə dəyişdirin
6. **Substr()** və ya **substring()** metodundan istifadə edərək sətirin ilk sözünü kəsin (dilimləyin).
7. **"Günlük JavaScript"** ifadəsini **"30 Günlük JavaScript"**-dən kəsin.
8. **includes()** metodundan istifadə edərək sətirdə _Script_ sözünün olub olmadığını yoxlayın
9. **Split()** metodundan istifadə edərək sətri massivə bölün
10. **Split()** metodundan istifadə edərək _"30 Günlük JavaScript"_ sətrini hər-hərfdən bir massivlərə bölün.
11. 'Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon' sətrini vergüllərə görə massivlərə bölün.
12. **replace()** metodundan istifadə edərək 30 Günlük JavaScript-i 30 Günlük Python-a dəyişdirin.
13. '30 Günlük JavaScript' sətirində 15-ci indeksdəki simvol nədir? **charAt()** metodundan istifadə edin.
14. **charCodeAt()** istifadə edərək '30 Günlük JavaScript' sətirində J simvol kodu nədir
15. "30 Günlük JavaScript" yazısında **a**-simvolunun ilk harda yerləşdiyini müəyyən etmək üçün **IndexOf**-dan istifadə edin.
16. JavaScript-in 30 günündə **a**-nın son baş verməsinin mövqeyini müəyyən etmək üçün **lastIndexOf**-dan istifadə edin
17. **indexOf**-dan istifadə edərək cümlədə "**çünki**" sözünün ilk dəfə yazıldığı yeri tapın. Cümlə: **"JavaScript öyrənirəm çünki ən populyar dillərdən biridir və çünki, öyrənməkdə asantdır."**
18. **lastIndexOf**-dan istifadə edərək cümlədə "**çünki**" sözünün son dəfə yazıldığı yeri tapın. Cümlə: **"JavaScript öyrənirəm çünki ən populyar dillərdən biridir və çünki, öyrənməkdə asantdır."**
19. **search**-dan istifadə edərək cümlədə "**çünki**" sözünün ilk dəfə yazıldığı yeri axtarışa verin. Cümlə: **"JavaScript öyrənirəm çünki ən populyar dillərdən biridir və çünki, öyrənməkdə asantdır."**
20. Sətirin əvvəlində və sonundakı boşluqları silmək üçün **trim()** funksiyasından istifadə edin. Məsələn, ' 30 Days Of JavaScript '.
21. "30 Days Of JavaScript" sətri ilə **startsWith()** metodundan istifadə edin və nəticəni true olsun
22. "30 Days Of JavaScript" sətri ilə **endsWith()** metodundan istifadə edin və nəticəni true olsun
23. 30 Günlük JavaScript-də bütün a-ları tapmaq üçün **match()** metodundan istifadə edin
24. **concat()** istifadə edin və '30 Days of' və 'JavaScript'i bir sətirə birləşdirin, '30 Days Of JavaScript' alınsın.
25. 30 Günlük JavaScript-i 2 dəfə çap etmək üçün **repeat()** metodundan istifadə edin

### Məşq edin: Səviyyə 2

1. console.log() istifadə edərək aşağıdakı ifadəni çap edin:

   ```sh
   İfadə: 'There is no exercise better for the heart than reaching down and lifting people up.' John Holmes bizə bir-birimizə kömək etməyi öyrədir.
   ```

2. console.log() istifadə edərək Tereza Ananın aşağıdakı ifadəsini çap edin:

   ```sh
   "Love is not patronizing and charity isn't about pity, it is about love. Charity and love are the same -- with charity you give love, so don't just give money but reach out your hand instead."
   ```

3. '10' məlumat tipinin 10-a tam bərabər olub olmadığını yoxlayın. Əgər deyilsə, onu tam bərabər edin.
4. parseFloat('9.8') 10-a bərabər olub olmadığını yoxlayın. Əgər deyilsə, onu 10-a tam bərabərləşdirin.
5. Həm pitonda, həm də jarqonda sözlərində '**on**' yazısının olub olmadığını yoxlayın
6. _Ümid edirəm ki, bu kurs jarqonla dolu deyil._ Cümlədə _jarqon_ -nun olub olmadığını yoxlayın.
7. 0 və 100 daxil olmaqla təsadüfi bir ədəd yaradın.
8. 50 ilə 100 arasında təsadüfi bir ədəd yaradın.
9. 0 ilə 255 arasında təsadüfi bir ədəd yaradın.
10. Təsadüfi ədədlərdən istifadə edərək 'JavaScript' sətir simvollarına daxil olun.
11. Aşağıdakı nümunəni çap etmək üçün console.log() və qaçış simvollarından istifadə edin.

    ```js
    1 1 1 1 1
    2 1 2 4 8
    3 1 3 9 27
    4 1 4 16 64
    5 1 5 25 125
    ```

12. Cümləni kəsmək üçün _substr_ istifadə edin. 'çünki' sözündən ikinci 'çünki' sözünə kimi aralığı kəsin çıxarın. Cümlə: **"JavaScript öyrənirəm çünki ən populyar dillərdən biridir və çünki, öyrənməkdə asantdır."**

### Məşqlər: Səviyyə 3

1. 'Love is the best thing in this world. Some found their love and some are still looking for their love.' Bu cümlədəki 'love' sözlərinin sayını sayın.
2. 'çünki' sözlerinin hamının sayını hesablamaq üçün match() funksiyasından istifadə edin. Cümlə: **"JavaScript öyrənirəm çünki ən populyar dillərdən biridir və çünki, öyrənməkdə asantdır."**
3. Aşağıdakı mətni təmizləyin və ən çox rast gəlinən sözü tapın (ipucu, replace və qaydalı ifadələrdən istifadə edin).

   ```js
   const sentence =
     "%I $am@% a %tea@cher%, &and& I lo%#ve %te@a@ching%;. The@re $is no@th@ing; &as& mo@re rewarding as educa@ting &and& @emp%o@weri@ng peo@ple. ;I found tea@ching m%o@re interesting tha@n any ot#her %jo@bs. %Do@es thi%s mo@tiv#ate yo@u to be a tea@cher!? %Th#is 30#Days&OfJavaScript &is al@so $the $resu@lt of &love& of tea&ching";
   ```

4. Aşağıdakı mətndən rəqəmləri çıxararaq şəxsin ümumi illik gəlirini hesablayın. 'O, ayda maaşdan 5000 avro, illik 10000 avro bonus, ayda 15000 avro onlayn kurslardan qazanır'

🎉 TƏBRİK EDİRİK! ! 🎉

[<< Gün 1](../readMe.md) | [Gün 3 >>](../03_Day_Booleans_operators_date/03_booleans_operators_date.md)
