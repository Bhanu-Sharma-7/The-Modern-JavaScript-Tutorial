# An Introduction to JavaScript 🌐

Chalo dekhe JavaScript ke baare me ki usme kya special hai, hum usse kya achieve kar skte hai, aur kaun si other technologies hai jo iske saath achhe se kaam karti hai.

---

## What is JavaScript?

**JavaScript** ko web pages ko jivit (yani alive) karne ke liye banaya gaya tha.

Jo bhi programs JavaScript me likhe jaate hai unko **script** kehte hai. Isko hum directly HTML page me likh skte hai aur jese hi page load hota hai ye automatically run ho jaata hai.

Scripts ko plain text ke roop me diya (yani provided) ya chalaya (yani executed) jata hai. Isko run karne ke liye koi bhi special compilation ya preparation (yani tayyaari) ki zarurat nahi hoti.

Isi karan se JavaScript, Java language se bohot alag hai.

---

## Why is it called JavaScript?

Jab JavaScript banayi gayi thi to uska naam **"LiveScript"** rakha gaya tha. Us samay Java language bohot popular thi, to JavaScript ke developers ne socha ki isko Java language ke chhote bhai ke roop me present (yani positioning) karenge.

But jese jese JavaScript ka vikas hua (yani jese jese ye evolved hui), JavaScript ek independent language (swatantr bhasha) ban gayi jiske apne kuch niyam-kayde (yani specification) the jisko hum **ECMAScript** kehte hai. Aur iske baad ye Java se ek dum alag ho gayi.

---

## JavaScript Engines

Aaj ke samay me JavaScript sirf browser pe nahi, kisi bhi aise device me chal sakti hai jisme JavaScript naam ka engine ho.

Jo browsers me engine hote hai unhe kabhi kabhi **"JavaScript Virtual Machine"** bhi bolte hai.

Alag alag engines ke paas alag alag codenames hote hai, jese:

- **V8** — Chrome, Opera aur Edge me
- **SpiderMonkey** — Firefox me
- ...Aur bhi kuch codenames hai jese "Chakra" for IE, "JavaScriptCore", "Nitro" aur "SquirrelFish" for Safari

> **Note:** Upar bataye gaye naam yaad rakhoge to achha hoga, kyunki ye internet par developer articles me use hote hai aur hum bhi inka istemal karenge. Jese agar V8 engine kisi feature X ko support karta hai to vo shayad Chrome, Opera aur Edge me bhi kaam karega.

---

## How do Engines Work?

Engines jatil hote hai (yaani complicated hote hai). But inki buniyaad bohot easy hoti hai (yaani inke basics bohot easy hote hai).

1. Engine script ko padhta hai (yaani "parse" karta hai)
2. Phir script ko machine code me convert karta hai — machine code me isliye convert karte hai kyunki computer only machine code hi samajhta hai, to hum programming language ko machine code me convert karte hai compiler ki help se
3. Aur phir machine code bohot fast run hota hai

Engine process ke har charan par optimization laagu karta hai (yaani har process ke steps par optimization apply keta hai). Chalte hue (yaani run hote hue) ye jo compiled script hai uspe bhi nazar rakhta hai, har ek data ko analyze karta hai, aur jo jaankari milti hai in sab chizo se uske aadhar par ye machine code ko optimize karta hai (yani code ko behtar banata hai).

---

## What can in-browser JavaScript do?

Modern JavaScript **"safe"** (yaani surakshit) programming language hai. JavaScript memory aur CPU ko low-level access nahi deti kyunki isko starting me browser ke liye banaya gaya tha, jisko low-level access ki zarurat nahi hoti.

JavaScript ki capabilities (yaani shamatayen) uske environment pe depend karti hai jisme vo chal raha hota hai. Jese **Node.js** aise functions ko support karta hai jo JavaScript ko kisi bhi arbitrary files ko padhne ya likhne, network requests karne aadi ki suvidha deta hai.

In-browser JavaScript kuch bhi kar sakta hai jese webpage manipulation (yaani webpages ko badalna), interaction with the user (yaani user ke saath interact karna), aur webserver se related kaam.

In-browser JavaScript niche likhe hue kaam kar sakti hai:

- Naya HTML page me jodna (yaani add karna), maujuda content ko badalna, style ko badalna
- Network ke zariye remote server ko request send karna, files ko download aur upload karna
- Cookies ko set ya get karna, visitor se question karna, messages show karna
- Client side ka data yaad rakhna (basically client side hum data **local storage** me store karte hai)

---

## What CAN'T in-browser JavaScript do?

Browser me JavaScript ki abilities limited hoti hai — user safety ko lekar — kyunki isi wajah se user ka private data ya information ko koi khatra nahi hota.

Niche kuch examples hai:

- Browser par maujud JavaScript user ki local hard disk ki files ko na to read kar sakta hai, na hi write kar sakta hai, na hi unhe copy kar sakta hai. Browser pe maujud JavaScript ko local OS ke kisi bhi function ka access nahi hota. Aaj kal ke modern browsers me aap user ki local files ka access maang sakte ho, **but iske liye user ki explicit permission chahiye hogi** — jese user khud file ko browser window me drop kare ya ek `<input>` tag ke zariye file select kare. (Sirf "website pe upload karne se permission milti hai" waali baat thodi incomplete hai — specific action chahiye hota hai.)

- Agar user ek browser par multiple tabs ko khol rakha hai, to ek tab ki JavaScript doosre tab ki JavaScript ko access nahi kar sakti. Ise **"Same Origin Policy"** kehte hai. But agar aap chahte hai ki 2 tabs ek doosre ki information share kare, to **dono pages** par woh JavaScript code hona chahiye jo is data exchange ke liye zaruri hai. Note: ye policy sirf different domain, **protocol ya port** wale pages ke beech lagti hai — matlab ek hi origin ke tabs aapas me communicate kar sakte hai agar code likha ho.

> Agar JavaScript ka istemal browser se bahar kiya jaaye (jese server side par), to iski koi bhi limitation nahi hoti.

---

## What makes JavaScript unique?

JavaScript ke baare me **3 behtareen baatein** (yaani great things):

- Ye easily HTML/CSS ke saath integrate ho jaata hai
- Aasaan kaam aasaani se ho jaate hai (jese C language me aapko ek line "Hello World" print karne ke liye bohot lines likhni padti hai — isme wesa kuch nahi hota)
- Sabhi **major** browsers isko support karte hai aur ye default se enabled hota hai

Inhi karano se JavaScript ek unique language hai aur isi liye ye industry me widely use hoti hai. Iska istemal hum mobile applications banane me, servers banane me aur bohot chizo me karte hai.

---

## Languages "over" JavaScript

**JavaScript ki syntax har kisi ki needs ko satisfy nahi karti.** Alag alag log alag alag features chahte hai.

To, recently kai nayi languages aayi hain jo **browser me run hone se pehle transpile (yaani convert) ho jaati hain JavaScript me**. Ye transpilation browser me automatically nahi hoti — ye build tools ke zariye development ke time hoti hai. Browser tak sirf converted JavaScript hi pahunchti hai.

> **Transpilation** = ek language ke source code ko doosri language ke source code me convert karna (yahan: kisi bhi language → JavaScript)

Kuch languages ke examples:

| Language | Kya khaas hai? |
|---|---|
| **TypeScript** | Strict data typing add karta hai — Microsoft ne banaya hai |
| **Kotlin** | Modern, concise aur safe language — browser ya Node pe run kar sakti hai |
| **Flow** | Data typing add karta hai, but alag tarike se — Facebook ne banaya |
| **Dart** | Apna khud ka engine hai (jese mobile apps ke liye), JavaScript me bhi transpile ho sakti hai — Google ne banaya |
| **Brython** | Python ko JavaScript me transpile karta hai — pure Python me apps likhne deta hai |
| **CoffeeScript** | JavaScript ka "syntactic sugar" hai — shorter syntax, zyada saaf code — Ruby developers ko pasand aata hai |

---

## Summary

- JavaScript was initially created as a browser-only language, but it is now used in many other environments as well.
- Today, JavaScript has a unique position as the most widely-adopted browser language, fully integrated with HTML/CSS.
- There are many languages that get "transpiled" to JavaScript and provide certain features. It is recommended to take a look at them, at least briefly, after mastering JavaScript.
