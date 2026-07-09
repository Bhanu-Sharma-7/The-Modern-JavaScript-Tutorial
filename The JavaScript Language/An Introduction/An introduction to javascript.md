# An Introduction to JavaScript 🌐

Chalo dekhe JavaScript ke baare mein ki usme kya special hai, hum usse kya achieve kar sakte hain, aur kaun si other technologies hain jo iske saath achhe se kaam karti hain.

---

## What is JavaScript?

**JavaScript** ko web pages ko jivit (yani alive) karne ke liye banaya gaya tha.

Jo bhi programs JavaScript mein likhe jaate hain unko **script** kehte hain. Inhe hum directly HTML page mein likh sakte hain aur jaise hi page load hota hai ye automatically run ho jaate hain.

Scripts ko plain text ke roop mein diya (yani provided) ya chalaya (yani executed) jaata hai. Inhe run karne ke liye koi bhi special compilation ya preparation (yani tayyaari) ki zarurat nahi hoti.

Isi karan se JavaScript, Java language se bohot alag hai.

---

## Why is it Called JavaScript?

Jab JavaScript banayi gayi thi to uska naam **"LiveScript"** rakha gaya tha. Us samay Java language bohot popular thi, to JavaScript ke developers ne socha ki isko Java language ke chhote bhai ke roop mein present (yani positioning) karenge.

Jaise jaise JavaScript ka vikas hua (yani jaise jaise ye evolved hui), JavaScript ek independent language (swatantr bhasha) ban gayi jiske apne kuch niyam-kayde (yani specification) the, jisko hum **ECMAScript** kehte hain. Aur iske baad ye Java se bilkul alag ho gayi — ab dono ka aapas mein koi bhi relation nahi hai.

---

## JavaScript Engines

Aaj ke samay mein JavaScript sirf browser pe nahi, kisi bhi aise device mein chal sakti hai jisme **JavaScript engine** naam ka ek special program ho.

Jo browsers mein engine hote hain unhe kabhi kabhi **"JavaScript Virtual Machine"** bhi bolte hain.

Alag alag engines ke paas alag alag codenames hote hain, jaise:

- **V8** — Chrome, Opera aur Edge mein
- **SpiderMonkey** — Firefox mein
- ...Aur bhi kuch codenames hain jaise "Chakra" for IE, "JavaScriptCore", "Nitro" aur "SquirrelFish" for Safari

> **Note:** Upar bataye gaye naam yaad rakhoge to achha hoga, kyunki ye internet par developer articles mein use hote hain aur hum bhi inका istemal karenge. Jaise agar V8 engine kisi feature X ko support karta hai to vo shayad Chrome, Opera aur Edge mein bhi kaam karega.

---

## How do Engines Work?

Engines jatil hote hain (yaani complicated hote hain). But inki buniyaad bohot easy hoti hai (yaani inke basics bohot easy hote hain).

1. Engine script ko padhta hai (yaani "parse" karta hai)
2. Phir script ko machine code mein convert karta hai (yaani "compile" karta hai) — machine code mein isliye convert karte hain kyunki computer only machine code hi samajhta hai
3. Aur phir machine code bohot fast run hota hai

Engine process ke har charan par optimization laagu karta hai (yaani har process ke steps par optimization apply karta hai). Chalte hue (yaani run hote hue) ye jo compiled script hai uspe bhi nazar rakhta hai, us mein se flow hone wale data ko analyze karta hai, aur jo jaankari milti hai in sab chizo se uske aadhar par ye machine code ko aur optimize karta hai (yani code ko behtar banata hai).

---

## What can In-Browser JavaScript do?

Modern JavaScript **"safe"** (yaani surakshit) programming language hai. JavaScript memory aur CPU ko low-level access nahi deti kyunki isko starting mein browser ke liye banaya gaya tha, jisko low-level access ki zarurat nahi hoti.

JavaScript ki capabilities (yaani shamatayen) uske environment pe depend karti hain jisme vo chal raha hota hai. Jaise **Node.js** aise functions ko support karta hai jo JavaScript ko kisi bhi arbitrary files ko padhne ya likhne, network requests karne aadi ki suvidha deta hai.

In-browser JavaScript kuch bhi kar sakta hai jaise webpage manipulation (yaani webpages ko badalna), interaction with the user (yaani user ke saath interact karna), aur webserver se related kaam.

In-browser JavaScript niche likhe hue kaam kar sakti hai:

- Naya HTML page mein jodna (yaani add karna), maujuda content ko badalna, style ko badalna
- User ke actions par react karna — jaise mouse clicks, pointer movements, key presses
- Network ke zariye remote server ko request send karna, files ko download aur upload karna (AJAX aur COMET technologies)
- Cookies ko set ya get karna, visitor se question karna, messages show karna
- Client side ka data yaad rakhna (basically client side hum data **local storage** mein store karte hain)

---

## What CAN'T In-Browser JavaScript do?

Browser mein JavaScript ki abilities limited hoti hain — user safety ko lekar — kyunki isi wajah se user ka private data ya information ko koi khatra nahi hota.

Niche kuch examples hain:

- Browser par maujud JavaScript user ki local hard disk ki files ko na to read kar sakta hai, na hi write kar sakta hai, na hi unhe copy kar sakta hai, na hi programs execute kar sakta hai. Browser pe maujud JavaScript ko local OS ke kisi bhi function ka direct access nahi hota. Aaj kal ke modern browsers mein aap user ki local files ka access maang sakte ho, **but iske liye user ki explicit permission chahiye hogi** — jaise user khud file ko browser window mein drop kare ya ek `<input>` tag ke zariye file select kare.

- Agar user ek browser par multiple tabs ko khol rakha hai, to ek tab ki JavaScript doosre tab ki JavaScript ko generally access nahi kar sakti. Ise **"Same Origin Policy"** kehte hain. But agar aap chahte hain ki 2 tabs ek doosre ki information share karein, to **dono pages** par woh JavaScript code hona chahiye jo is data exchange ke liye zaruri hai. Note: ye policy sirf different domain, **protocol ya port** wale pages ke beech lagti hai — matlab same origin ke tabs aapas mein communicate kar sakte hain agar code likha ho.

- JavaScript aasaani se us server se communicate kar sakti hai jisse current page aayi hai. But doosre sites/domains se data receive karne ki uski ability severely limited hoti hai — ye possible hai, lekin remote side ki taraf se explicit agreement (HTTP headers mein expressed) zaroori hoti hai.

> Agar JavaScript ka istemal browser se bahar kiya jaaye (jaise server side par), to iski koi bhi limitation nahi hoti. Modern browsers plugins/extensions bhi allow karte hain jo extended permissions maang sakte hain.

---

## What makes JavaScript Unique?

JavaScript ke baare mein **teen behtareen baatein** (yaani great things):

- HTML/CSS ke saath full integration
- Aasaan kaam aasaani se ho jaate hain
- Sabhi **major** browsers isko support karte hain aur ye default se enabled hota hai

JavaScript **akela** browser technology hai jo yeh teeno cheezein ek saath combine karti hai. Inhi karanon se JavaScript ek unique language hai aur isi liye ye industry mein widely use hoti hai. Iska istemal hum mobile applications banane mein, servers banane mein aur bohot chizo mein karte hain.

---

## Languages "over" JavaScript

**JavaScript ki syntax har kisi ki needs ko satisfy nahi karti.** Alag alag log alag alag features chahte hain.

To, recently kai nayi languages aayi hain jo **browser mein run hone se pehle transpile (yaani convert) ho jaati hain JavaScript mein**. Modern tools is transpilation ko bohot fast aur transparent banate hain — developers kisi aur language mein code likhte hain aur "under the hood" automatically JavaScript mein convert ho jaata hai.

> **Transpilation** = ek language ke source code ko doosri language ke source code mein convert karna (yahan: kisi bhi language → JavaScript)

Kuch languages ke examples:

| Language | Kya khaas hai? |
|---|---|
| **CoffeeScript** | JavaScript ka "syntactic sugar" hai — shorter syntax, zyada saaf code — Ruby developers ko pasand aata hai |
| **TypeScript** | Strict data typing add karta hai — Microsoft ne banaya hai |
| **Flow** | Data typing add karta hai, but alag tarike se — Facebook ne banaya |
| **Dart** | Apna khud ka engine hai (jaise mobile apps ke liye), JavaScript mein bhi transpile ho sakti hai — Google ne banaya |
| **Brython** | Python ko JavaScript mein transpile karta hai — pure Python mein apps likhne deta hai |
| **Kotlin** | Modern, concise aur safe language — browser ya Node pe run kar sakti hai |

---

## Summary

- JavaScript was initially created as a browser-only language, but it is now used in many other environments as well.
- Today, JavaScript has a unique position as the most widely-adopted browser language, fully integrated with HTML/CSS.
- There are many languages that get "transpiled" to JavaScript and provide certain features. It is recommended to take a look at them, at least briefly, after mastering JavaScript.
