<div align="center">
  <h1> 30 Günlük JavaScript - Giriş</h1>
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

  <div>

  🇬🇧 [English](../readMe.md)
  🇪🇸 [Spanish](../Spanish/readme.md)
  🇷🇺 [Russian](./README.md)
  🇦🇿 [Azerbaijan](./AZ/README.md)

  </div>

</div>

[Gün 2 >>](./02_Day_Data_types/02_day_data_types.md)

![Thirty Days Of JavaScript](../images/day_1_1.png)

- [📔 Gün 1](#-gün-1)
  - [Giriş](#giriş)
  - [Tələblər](#tələblər)
  - [Qurmaq](#qurmaq)
    - [Node.js quraşdırın](#nodejs-quraşdırın)
    - [Brauzer](#brauzer)
      - [Google Chrome-un quraşdırılması](#google-chrome-un-quraşdırılması)
      - [Google Chrome konsol açılışı](#google-chrome-konsol-açılışı)
      - [Brauzer konsolunda kodun yazılması](#brauzer-konsolunda-kodun-yazılması)
        - [Console.log](#consolelog)
        - [Console.log - Çox arqumentli ](#consolelog---%C3%A7ox-arqumentli)
        - [Şərhlər](#%C5%9F%C9%99rhl%C9%99r)
        - [Sintaksis «Syntax»](#sintaksis)
      - [Hesablama](#hesablama)
    - [Kod redaktoru](#kod-redaktoru)
      - [Visual Studio Code yüklənməsi](#visual-studio-code-qura%C5%9Fd%C4%B1r%C4%B1lmas%C4%B1)
      - [VS Code necə istifadə edilir](#visual-studio-code-nec%C9%99-istifad%C9%99-edilir)
  - [Veb səhifəyə JavaScript əlavə edilməsi](#veb-s%C9%99hif%C9%99y%C9%99-javascript-%C9%99lav%C9%99-edilm%C9%99si)
    - [Sətir içi «Inline» skript](#s%C9%99tir-i%C3%A7i-inline-skript)
    - [Daxili «Internal» skript](#daxili-internal-skript)
    - [Xarici «External» skript](#xarici-external-skript)
    - [Çoxlu xarici «Multiple External» skript](#%C3%A7oxlu-xarici-multiple-external-skriptl%C9%99r)
  - [Məlumat növlərinə «Data Types» giriş](#m%C9%99lumat-n%C3%B6vl%C9%99rin%C9%99-data-types-giri%C5%9F)
    - [Rəqəmlər «Numbers»](#r%C9%99q%C9%99ml%C9%99r-numbers)
    - [Sətirlər «Strings»](#s%C9%99tirl%C9%99r-strings)
    - [Booleanlar(məntiqi) növ «boolean»](#booleanlarm%C9%99ntiqi-n%C3%B6v-boolean)
    - [Qeyri-müəyyən «undefined»](#qeyri-m%C3%BC%C9%99yy%C9%99n-undefined)
    - [Boş dəyər «null»](#bo%C5%9F-d%C9%99y%C9%99r-null)
  - [Məlumat növlərinin yoxlanılması](#m%C9%99lumat-n%C3%B6vl%C9%99rinin-yoxlan%C4%B1lmas%C4%B1)
  - [Yenə şərhlər](#yen%C9%99-%C5%9F%C9%99rhl%C9%99r)
  - [Dəyişənlər «Variables»](#d%C9%99yi%C5%9F%C9%99nl%C9%99r-variables)
- [💻 Gün 1: Məşqlər](#-g%C3%BCn-1-m%C9%99%C5%9Fql%C9%99r)

# 📔 Gün 1

## Giriş

30 günlük JavaScript proqramlaşdırma çağırışında iştirak etmək qərarına gəldiyiniz üçün sizi **təbrik edirik**. Bu çağırışda siz JavaScript proqramçısı olmaq üçün lazım olan hər şeyi və ümumiyyətlə, proqramlaşdırmanın bütün konsepsiyasını öyrənəcəksiniz. Müsabiqənin sonunda siz 30DaysOfJavaScript proqramlaşdırma testini tamamlama sertifikatı alacaqsınız.Yardıma ehtiyacınız olarsa və ya başqalarına kömək etmək istəyirsinizsə, [telegram qrupuna](https://t.me/ThirtyDaysOfJavaScript) qoşula bilərsiniz.

**30DaysOfJavaScript** çağırışı həm yeni başlayanlar, həm də qabaqcıl JavaScript tərtibatçıları üçün bələdçidir. JavaScript-ə xoş gəlmisiniz. JavaScript internetin dilidir. Mən JavaScript-dən istifadə etməkdən və öyrətməkdən həzz alıram və ümid edirəm ki, siz də bunu edəcəksiniz..

Bu addım-addım JavaScript çağırışında siz bəşəriyyət tarixində ən populyar proqramlaşdırma dili olan JavaScript-i öyrənəcəksiniz.
JavaScript veb-saytlara **interaktivlik əlavə etmək, mobil proqramlar, masa üstü proqramlar, oyunlar** hazırlamaq üçün istifadə olunur və hazırda JavaScript **maşın öyrənməsi(machine learning)** və **AI** üçün istifadə edilə bilər.
**JavaScript (JS)** son illərdə populyarlığı artıb və altı il ardıcıl olaraq lider proqramlaşdırma dili olub və Github-da ən çox istifadə olunan proqramlaşdırma dilidir.

## Tələblər

Bu çağırışı yerinə yetirmək üçün proqramlaşdırma üzrə əvvəlcədən bilik tələb olunmur. Sizə yalnız lazımdır:

1. Motivasiya
2. Kompüter
3. İnternet
4. Brauzer
5. Kod redaktoru

## Qurmaq

İnanıram ki, sizdə inkişaf etdirici(Developer) olmaq üçün kompüter, internet, motivasiya və güclü istəyiniz var. Bunlara sahibsinizsə, başlamaq üçün hər şeyiniz var.

### Node.js quraşdırın

Hazırda Node.js-ə ehtiyacınız olmasada, lakin daha sonra ehtiyacınız ola bilər. [Node.js](https://nodejs.org/en/) quraşdırın.

![Node download](../images/download_node.png)

Yüklədikdən sonra iki dəfə klikləyin və quraşdırın

![Install node](../images/install_node.png)

Cihaz terminalımızı(Command Prompt) və ya əmr sətirini açaraq yerli maşınımızda node quraşdırılıb-quraşdırılmadığını yoxlaya bilərik.

```sh
asabeneh $ node -v
v12.14.0
```

Bu dərsliyi hazırlayarkən mən Node 12.14.0 versiyasından istifadə edirdim, lakin indi yükləmək üçün Node.js-in tövsiyə olunan versiyası v16.13.2-dır

### Brauzer

Orada bir çox brauzer var. Bununla belə, mən Google Chrome-u şiddətlə tövsiyə edirəm.

#### Google Chrome-un quraşdırılması

Əgər hələ də yoxdursa, [Google Chrome](https://www.google.com/chrome/) quraşdırın.
Install [Google Chrome](https://www.google.com/chrome/) if you do not have one yet. Biz brauzer konsolunda kiçik JavaScript kodu yaza bilərik, lakin proqramların hazırlanması üçün brauzer konsolundan istifadə etmirik.

![Google Chrome](../images/google_chrome.png)

#### Google Chrome konsol açılışı

Siz Google Chrome konsolunu brauzerin yuxarı sağ küncündəki üç nöqtəyə klikləməklə, Daha çox alətlər -> Developer alətləri seçməklə və ya klaviatura qısa yolundan istifadə etməklə aça bilərsiniz. Qısayollardan istifadə etməyi üstün tuturam.

![Opening chrome](../images/opening_developer_tool.png)

Klaviatura qısa yolundan istifadə edərək Chrome konsolunu açmaq üçün.

```sh
Mac
Command+Option+J

Windows/Linux:
Ctl+Shift+J
```

![Opening console](../images/opening_chrome_console_shortcut.png)

Google Chrome konsolunu açdıqdan sonra işarələnmiş düymələri araşdırmağa çalışın. Biz vaxtımızın çox hissəsini Konsolda keçirəcəyik. Konsol JavaScript kodunuzun getdiyi yerdir. Google Console V8 mühərriki JavaScript kodunuzu maşın koduna çevirir. Gəlin Google Chrome konsolunda JavaScript kodu yazaq:

![write code on console](../images/js_code_on_chrome_console.png)

#### Brauzer Konsolunda Kodun Yazılması

Biz istənilən JavaScript kodunu Google konsolunda və ya istənilən brauzer konsolunda yaza bilərik. Bununla belə, bu çağırış üçün biz yalnız Google Chrome konsoluna diqqət yetiririk. Konsolu aşağıdakılardan istifadə edərək açın:

```sh
Mac
Command+Option+I

Windows:
Ctl+Shift+I
```

##### Console.log

İlk JavaScript kodumuzu yazmaq üçün biz daxili funksiyadan istifadə etdik **console.log()**. Biz arqumenti giriş məlumatları kimi ötürdük və funksiya çıxışı göstərir. Biz console.log() funksiyasında giriş məlumatı və ya arqument kimi "Salam, Dünya"nı seçdik.

```js
console.log('Hello, World!')
```

##### Console.log - Çox arqumentli 

**console.log()** funksiyası vergüllə ayrılmış çoxlu parametrləri qəbul edə bilər. Sintaksis aşağıdakı kimi görünür:**console.log(param1, param2, param3)**

![console log multiple arguments](../images/console_log_multipl_arguments.png)

```js
console.log('Hello', 'World', '!')
console.log('HAPPY', 'NEW', 'YEAR', 2020)
console.log('Welcome', 'to', 30, 'Days', 'Of', 'JavaScript')
```

Yuxarıdakı kod parçasından göründüyü kimi, _console.log()_ çoxlu arqumentlər qəbul edə bilər.

Təbrik edirik! Siz ilk JavaScript kodunuzu _console.log()_ istifadə edərək yazdınız.

##### Şərhlər

Kodumuza şərhlər əlavə edirik. Kodu daha oxunaqlı etmək və kodumuzda qeydlər buraxmaq üçün şərhlər çox vacibdir. JavaScript kodumuzun şərh hissəsini icra etmir, JavaScript-də // ilə başlayan hər hansı mətn sətri şərhdir və bu kimi /\* \*/ simvolların arasına yazılmış çox sətirli yazılarda şərhdir.

**Misal: Tək sətirli şərh**

// Bu ilk şərhdir  
 // Bu ikinci şərhdir  
 // Mən tək sətirli şərhəm

**Misal: Çox sətirli şərh**

/\*
Bu çox sətirli şərhdir, çox sətirli şərhlər 
bir neçə sətirdən ibarət ola bilər
JavaScript internetin dilidir 
 \*/

##### Sintaksis

Proqramlaşdırma dilləri insan dillərinə bənzəyir. Azərbaycan və ya bir çox başqa dillər mənalı mesajı çatdırmaq üçün sözlər, ifadələr, cümlələr, mürəkkəb cümlələr və sair istifadə edir. Sintaksisin Azərbaycanca mənası _bir dilə xas olan cümlə quruluşu və cümlədə sözlərin birləşməsi üsuludur._ Sintaksisin texniki tərifi kompüter dilində ifadələrin strukturudur. Proqramlaşdırma dillərində sintaksis var. JavaScript proqramlaşdırma dilidir və digər proqramlaşdırma dilləri kimi onun da öz sintaksisi var. JavaScript-in başa düşdüyü sintaksisi yazmasaq, o, müxtəlif növ xətaları artıracaq. Müxtəlif növ JavaScript xətalarını daha sonra araşdıracağıq. Hələlik gəlin sintaksis səhvlərinə baxaq.

![Error](../images/raising_syntax_error.png)

Mən qəsdən səhv etdim. Nəticədə, konsol sintaksis səhvlərini artırır. Əslində, sintaksis çox informativdir. Hansı növ səhvə yol verildiyini bildirir. Səhv rəyi təlimatını oxumaqla biz sintaksisi düzəldə və problemi həll edə bilərik. Proqramdakı xətaların müəyyən edilməsi və aradan qaldırılması prosesi sazlama(debugging) adlanır. Gəlin səhvləri düzəldək:

```js
console.log('Hello, World!')
console.log('Hello, World!')
```

İndiyə qədər biz _console.log()_ vasitəsilə mətnin necə göstərildiyini gördük. Əgər biz mətni və ya sətri _console.log()_ istifadə edərək çap ediriksə, mətn tək dırnaqlar, qoşa dırnaqlar və ya geri işarə(backtick) içərisində olmalıdır. 

**Əlavə qeyd:** Alternativ olaraq kəskin, geri işarə, sol sitat və ya açıq sitat kimi tanınan arxa sitat və ya əks sitat durğu işarəsidir (\`). Geri sitat yaratmaq üçün birbaşa Esc düyməsinin altında yerləşən (\`) düyməsini basın. Bu düymə həm də Shift düyməsi basılarkən saxlanılırsa, buruqlu ( ~ ) simvolunu yazmaq üçün istifadə olunur.

**Misal:**

```js
console.log('Hello, World!')
console.log("Hello, World!")
console.log(`Hello, World!`)
```

#### Hesablama

İndi gəlin rəqəm(Number) məlumat növləri üçün Google Chrome konsolunda _console.log()_ istifadə edərək JavaScript kodlarının yazılmasını daha çox məşq edək. Yazılardan əlavə JavaScript-dən istifadə edərək riyazi hesablamalar da edə bilərik. Aşağıdakı sadə hesablamaları aparaq. Konsol birbaşa **_console.log()_** funksiyası olmadan arqumentləri qəbul edə bilər. Bununla belə, bu misalda girişə daxil edilmişdir, çünki bu problemin əksəriyyəti funksiyadan istifadənin məcburi olduğu mətn redaktorunda baş verəcəkdir. Konsoldakı təlimatları birbaşa dəyişə bilərsiniz.

![Arithmetic](../images/arithmetic.png)

```js
console.log(2 + 3) // Addition - Toplama 
console.log(3 - 2) // Subtraction - Çıxarma
console.log(2 * 3) // Multiplication - Vurma
console.log(3 / 2) // Division - Bölmə
console.log(3 % 2) // Modulus(finding remainder) - Modul(qalıq tapmaq)
console.log(3 ** 2) // Exponentiation 3 ** 2 == 3 * 3 - Qüvvətə yüksəltmə
```

### Kod redaktoru

Kodlarımızı brauzer konsolunda yaza bilərik, lakin bu, daha böyük layihələr üçün yetərsizdir. Həqiqi iş mühitində tərtibatçılar kodlarını yazmaq üçün müxtəlif kod redaktorlarından istifadə edirlər. Bu 30 günlük JavaScript çağırışında biz Visual Studio Kodundan istifadə edəcəyik.

#### Visual Studio Code quraşdırılması

Visual studio kodu çox məşhur açıq mənbəli mətn redaktorudur. Mən [Visual Studio Kodunu endirməyi](https://code.visualstudio.com/) tövsiyə edərdim, lakin digər redaktorların tərəfdarısınızsa, əlinizdə olanlardan da istifadə edə bilərsiniz.

![Vscode](../images/vscode.png)

Əgər siz Visual Studio Kodunu quraşdırmısınızsa, ondan istifadə etməyə başlayaq.

#### Visual Studio Code necə istifadə edilir

Simgesini iki dəfə klikləməklə Visual Studio Kodunu açın. Onu açdığınız zaman belə bir interfeys əldə edəcəksiniz. İşarələnmiş yerlərə diqqət yetirin.

![Vscode ui](../images/vscode_ui.png)

![Vscode add project](../images/adding_project_to_vscode.png)

![Vscode open project](../images/opening_project_on_vscode.png)

![script file](../images/scripts_on_vscode.png)

![Installing Live Server](../images/vsc_live_server.png)

![running script](../images/running_script.png)

![coding running](../images/launched_on_new_tab.png)

## Veb səhifəyə JavaScript əlavə edilməsi

JavaScript veb-səhifəyə üç müxtəlif yolla əlavə edilə bilər:

- **_Sətir içi(Inline) skript_**
- **_Daxili(Internal) skript_**
- **_Xarici(External) skript_**
- **_Çoxlu Xarici(Multiple External) skriptlər_**

Aşağıdakı bölmələr veb səhifənizə JavaScript kodu əlavə etməyin müxtəlif yollarını göstərir.

### Sətir içi «Inline» skript

İş masanızda və ya istənilən yerdə layihə qovluğu yaradın, onu 30DaysOfJS adlandırın və layihə qovluğunda index.html faylı yaradın. Sonra aşağıdakı kodu yapışdırın və onu brauzerdə, məsələn, [Chrome](https://www.google.com/chrome/) - da açın.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>30 Günlük JavaScript:Sətir içi Skript</title>
  </head>
  <body>
    <button onclick="alert('30 Günlük JavaScript-ə xoş gəlmisiniz!')">Click Me</button>
  </body>
</html>
```

İndi siz ilk daxili skriptinizi yazdınız. _alert()_ daxili funksiyasından istifadə edərək pop-up xəbərdarlıq mesajı yarada bilərik.

### Daxili «Internal» skript

Daxili skript _head(baş)_ və ya _body(gövdə)_ yazıla bilər, lakin onu HTML sənədinin body(gövdəsində) yazmağa üstünlük verilir. Əvvəlcə səhifənin head(baş) hissəsinə yazaq

```html
<!DOCTYPE html>
<html>
  <head>
    <title>30 Günlük JavaScript:Daxili Skript</title>
    <script>
      console.log('30 Günlük JavaScript-ə xoş gəlmisiniz!')
    </script>
  </head>
  <body></body>
</html>
```

Çox vaxt daxili skripti belə yazırıq. JavaScript kodunu gövdə bölməsinə yazmaq ən çox seçilən seçimdir. console.log()-dakı çıxışı görmək üçün brauzer konsolunu açın

```html
<!DOCTYPE html>
<html>
  <head>
    <title>30 Günlük JavaScript:Daxili Skript</title>
  </head>
  <body>
    <button onclick="alert('30 Günlük JavaScript-ə xoş gəlmisiniz!');">Mənə klikləyin</button>
    <script>
      console.log('30 Günlük JavaScript-ə xoş gəlmisiniz!')
    </script>
  </body>
</html>
```

console.log()-dakı çıxışı görmək üçün brauzer konsolunu açın

![js code from vscode](../images/js_code_vscode.png)

### Xarici «External» skript

Daxili skriptə bənzər şəkildə, xarici skript bağlantısı başlıqda və ya gövdədə ola bilər, lakin onu gövdəyə yerləşdirməyə üstünlük verilir. Əvvəlcə .js uzantılı xarici JavaScript faylı yaratmalıyıq. .js uzantısı ilə bitən bütün fayllar JavaScript fayllarıdır. Layihə kataloqunuzda introduction.js adlı fayl yaradın və aşağıdakı kodu yazın və bu .js faylını gövdənin aşağı hissəsində əlaqələndirin.

```js
console.log('30 Günlük JavaScript-ə xoş gəlmisiniz!')
```

_Başdakı(head)_ xarici skriptlər:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>30 Günlük JavaScript:Xarici Skript</title>
    <script src="introduction.js"></script>
  </head>
  <body></body>
</html>
```

_Gövdədəki(body)_ xarici skriptlər:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>30 Günlük JavaScript: Xarici skript</title>
  </head>
  <body>
    <!-- başlıqda və ya gövdədə ola bilər --> 
    <!-- Xarici skripti yerləşdirmək üçün tövsiyə olunan yer budur -->
    <script src="introduction.js"></script>
  </body>
</html>
```

console.log() çıxışını görmək üçün brauzer konsolunu açın

### Çoxlu Xarici «Multiple External» skriptlər

Biz həmçinin bir neçə xarici JavaScript faylını veb səhifəyə bağlaya bilərik. 30DaysOfJS qovluğunda helloworld.js faylı yaradın və aşağıdakı kodu yazın.

```js
console.log('Hello, World!')
```

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Çoxlu Xarici skriptlər</title>
  </head>
  <body>
    <script src="./helloworld.js"></script>
    <script src="./introduction.js"></script>
  </body>
</html>
```

_main.js(əsas js) faylınız bütün digər skriptlərin altında olmalıdır._ Bunu xatırlamaq çox vacibdir.

![Multiple Script](../images/multiple_script.png)

## Məlumat növlərinə «Data Types» giriş

JavaScript-də və digər proqramlaşdırma dillərində müxtəlif növ məlumat növləri mövcuddur. Aşağıdakılar JavaScript primitiv məlumat növləridir:_String, Number, Boolean, undefined, Null_ və _Symbol_.

### Rəqəmlər «Numbers»

- Tam ədədlər: Tam (mənfi, sıfır və müsbət) ədədlər Misal:
  ... -3, -2, -1, 0, 1, 2, 3 ...
- Float-nöqtəli ədədlər: Ondalıq ədəd Misal
  ... -3.5, -2.25, -1.0, 0.0, 1.1, 2.2, 3.5 ...

### Sətirlər «Strings»

İki tək dırnaq(single quotes), qoşa dırnaq(double quotes) və ya geri işarələr(backticks) arasında bir və ya daha çox simvol toplusu. **Misal:**

```js
'Asabeneh'
'Finland'
'JavaScript gözəl proqramlaşdırma dilidir'
'Mən öyrətməyi sevirəm'
'Ümid edirəm ilk gündən zövq alırsınız'
`Biz həmçinin geri işarədən istifadə edərək sətir yarada bilərik - bunun kimi.`
'Bir sətir bir simvol qədər kiçik və bir çox səhifə qədər böyük ola bilər'
```

### Booleanlar(məntiqi) növ «boolean»

Boolean dəyəri doğru və ya yanlışdır. İstənilən müqayisə doğru və ya yalan olan boolean dəyəri qaytarır.

Boolean məlumat növü ya doğru, ya da yanlış dəyərdir.

**Misal:**

```js
true // işıq yanırsa, dəyər doğrudur(true)
false // işıq sönübsə, dəyər yanlışdır(false)
```

### Qeyri-müəyyən «undefined»

JavaScript-də dəyişənə dəyər təyin etməsək, dəyər müəyyən edilmir. Bundan əlavə, əgər funksiya heç nə qaytarmırsa, o, müəyyən edilməmiş şəkildə qaytarır.

```js
let firstName
console.log(firstName) // qeyri-müəyyən(undefined), çünki ona, hələ bir dəyər təyin edilməyib
```

### Boş dəyər «null»

JavaScript-də null boş dəyər deməkdir.

```js
let emptyValue = null
```

## Məlumat növlərinin yoxlanılması

Müəyyən dəyişənin məlumat tipini yoxlamaq üçün **typeof** operatorundan istifadə edirik. Aşağıdakı nümunəyə baxın.

```js
console.log(typeof 'Asabeneh') // string - sətir
console.log(typeof 5) // number - rəqəm
console.log(typeof true) // boolean - məntiqi(true,false)
console.log(typeof null) // object type - obyekt növü
console.log(typeof undefined) // undefined - qeyri-müəyyən
```

## Yenə şərhlər

Unutmayın ki, JavaScript-də şərh yazmaq digər proqramlaşdırma dillərinə bənzəyir. Kodunuzu daha oxunaqlı etmək üçün şərhlər vacibdir. Şərh bildirməyin iki yolu var:

- _Tək sətir şərh_
- _Çox sətirli şərh_

```js
// kodun özünü bir şərhlə şərh etmək
// let firstName = 'Asabeneh'; tək sətirli şərh
// let soyadı = 'Yetayeh'; tək sətirli şərh
```

Çox sətirli şərh:

```js
/*
  let location = 'Helsinki';
  let age = 100;
  let isMarried = true;
  Bu Çoxsətirli şərhdir

*/
```

## Dəyişənlər «Variables»

Dəyişənlər məlumat _konteynerləridir_. Dəyişənlər məlumatları yaddaşda _saxlamaq_ üçün istifadə olunur. Dəyişən elan edildikdə, yaddaşda yer ayrılır. Dəyişən dəyərə (məlumata) təyin edildikdə, yaddaş sahəsi həmin verilənlərlə doldurulacaq. Dəyişən elan etmək üçün _var_, _let_ və ya _const_ açar sözlərindən istifadə edirik.

Fərqli vaxtlarda dəyişilən dəyərlər üçün biz _let_ açar sözündən istifadə edirik. Məlumatlar heç dəyişməzsə, _const_ istifadə edirik. Məsələn, PI, ölkə adı, qravitasiya dəyişmir və biz const istifadə edə bilərik. Bu çağırışda var istifadə etməyəcəyik və mən sizə ondan istifadə etməyi tövsiyə etmirəm. Bu, çox sızıntısı olan bir dəyişəni elan etməyin səhvə meylli yoludur. Var, let və const haqqında digər bölmələrdə (əhatə dairəsi - scope) ətraflı danışacağıq. Hələlik yuxarıdakı izahat kifayətdir.

Etibarlı JavaScript dəyişəni adı aşağıdakı qaydalara əməl etməlidir:

- JavaScript dəyişəninin adı nömrə ilə başlamamalıdır.
- JavaScript dəyişən adı dollar işarəsi və alt xəttdən(underscore) başqa xüsusi simvollara icazə vermir.
- JavaScript dəyişəni adı camelCase qaydasına uyğundur.
- JavaScript dəyişən adında sözlər arasında boşluq olmamalıdır.

Aşağıda etibarlı JavaScript dəyişənlərinin nümunələri verilmişdir.

```js
firstName
lastName
country
city
capitalCity
age
isMarried

first_name
last_name
is_married
capital_city

num1
num_1
_num_1
$num1
year2020
year_2020
```

Siyahıdakı birinci və ikinci dəyişənlər JavaScript-də bəyan etmək üçün camelCase qaydasına uyğundur. Bu materialda biz camelCase dəyişənlərindən istifadə edəcəyik.

Etibarsız dəyişənlərə misal:

```sh
  first-name
  1_num
  num_#_1
```

Müxtəlif məlumat növləri ilə dəyişənləri elan edək. Dəyişən elan etmək üçün dəyişən adından əvvəl _let_ və ya _const_ açar sözlərindən istifadə etməliyik. Dəyişən adından sonra bərabər işarə(təyinat operatoru) və dəyər(təyin edilmiş verilənlər) yazırıq.

```js
// Syntax
let nameOfVariable = value
```

**Elan edilmiş dəyişənlərin nümunələri**

```js
// Müxtəlif məlumat növlərinin müxtəlif dəyişənlərinin elan edilməsi
let firstName = 'Asabeneh' // bir şəxsin adı
let lastName = 'Yetayeh' // bir şəxsin soyadı
let country = 'Finland' // ölkə
let city = 'Helsinki' // paytaxt
let age = 100 // illərlə yaş
let isMarried = true

console.log(firstName, lastName, country, city, age, isMarried)
```

```sh
Asabeneh Yetayeh Finland Helsinki 100 true
```

```js
// Dəyişənlərin ədədi qiymətlərlə elan edilməsi
let age = 100 // illərlə yaş
const gravity = 9.81 // m/s2 ilə yerin cazibə qüvvəsi
const boilingPoint = 100 // suyun qaynama nöqtəsi, temperatur °C
const PI = 3.14 // həndəsi sabit
console.log(gravity, boilingPoint, PI)
```

```sh
9.81 100 3.14
```

```js
// Dəyişənlər də vergüllə ayrılmış bir sətirdə elan edilə bilər
let name = 'Asabeneh', // bir şəxsin adı
job = 'teacher',
live = 'Finland'
console.log(name, job, live)
```

```sh
Asabeneh teacher Finland
```

01 Günlük qovluqda _index.html_ faylını işə saldığınız zaman bunu əldə etməlisiniz:

![Day one](../images/day_1.png)

🌕 Möhtəşəmsiz! 1-ci günü yenicə tamamladınız və mükəmməlliyə doğru gedirsiniz. İndi beyniniz və əzələniz üçün bəzi məşqlər edin.

# 💻 Gün 1: Məşqlər

1. _Şərhlərin kodu oxunaqlı edə biləcəyini_ deyən tək sətirli şərh yazın
2. _"30DaysOfJavaScript-ə xoş gəlmisiniz"_ deyən başqa bir şərh yazın
3. _Şərhlərin kodu oxunaqlı, təkrar istifadəsi asan və məlumatlandırıcı edə biləcəyini_ deyən çoxsətirli şərh yazın

4. Variable.js faylı yaradın və dəyişənləri elan edin və sətir, boolean, qeyri-müəyyən və null məlumat növlərini təyin edin
5. Datatypes.js faylı yaradın və müxtəlif məlumat növlərini yoxlamaq üçün JavaScript **typeof** operatorundan istifadə edin. Hər dəyişənin məlumat növünü yoxlayın
6. Dəyər təyin etmədən dörd dəyişəni elan edin
7. Təyin edilmiş dəyərləri olan dörd dəyişəni elan edin
8. Adınızı, soyadınızı, ailə vəziyyətinizi, ölkənizi və yaşınızı bir neçə sətirdə saxlamaq üçün dəyişənləri elan edin
9. Adınızı, soyadınızı, ailə vəziyyətinizi, ölkənizi və yaşınızı bir sətirdə saxlamaq üçün dəyişənləri elan edin
10. İki _myAge_ və _yourAge_ dəyişənini elan edin və onlara ilkin dəyərlər təyin edin və brauzer konsoluna daxil olun.

```sh
Mənim 25 yaşım var.
Sənin 30 yaşın var.
```

🎉 TƏBRİK EDİRİK ! 🎉

[Gün 2 >>](./02_Day_Data_types/02_day_data_types.md)
