Bilkul! Chalo CSS ki **positions** ko ekdum simple aur mazedaar tareeqe se samajhte hain — jaise tum 5th class ke student ho. 🎒✏️

---

### 💡 Socho ke tumhare paas ek **drawing copy** hai (webpage), aur usme tum kuch **stickers** (HTML elements) lagana chahte ho.

CSS mein **position** batata hai ke ye stickers (yaani boxes) **kahaan aur kaise chipkayenge**.

---

## 🖼️ 1. `static` (Default — apni jagah pe seedha)

**Socho ke tumne sticker ko copy mein jahan rakh diya, woh wahi chipak gaya.**

```css
position: static;
```

* Ye **default** hoti hai.
* Tum isse **move** nahi kar sakte `top`, `left`, `right`, `bottom` se.

✍️ *Example:*

```html
<div style="position: static;">Main apni line mein hoon</div>
```

---

## 🧲 2. `relative` (Thoda idhar-udhar le jao, par jagah reserved rahegi)

**Socho ke sticker ko thoda idhar-udhar sarka diya, lekin asli jagah khaali chhor di.**

```css
position: relative;
```

* Tum `top`, `left`, `right`, `bottom` se usse thoda move kar sakte ho.
* Uski **original jagah** fir bhi wahan rahegi.

✍️ *Example:*

```css
position: relative;
top: 20px;
left: 30px;
```

---

## 🎈 3. `absolute` (Jahan chaho, wahan chipka do)

**Socho ke sticker hawa mein le jaake kahi bhi chipka diya — kisi doosri jagah ke hisaab se.**

```css
position: absolute;
```

* Ye **parent** ke hisaab se move hota hai (agar parent `relative` ya `absolute` ho).
* Agar parent kuch bhi set nahi kiya toh **poore page (body)** ke hisaab se move karega.

✍️ *Example:*

```css
position: absolute;
top: 50px;
left: 100px;
```

---

## 🧊 4. `fixed` (Page scroll ho ya na ho, sticker wahi chipka rahega)

**Socho ke sticker ko tumne screen pe chipka diya, ab chahe copy upar neeche ho, sticker wahi chipka rahega.**

```css
position: fixed;
```

* Page scroll karne par bhi wahi rahta hai.
* Mostly **navbar** ya **scroll-to-top button** ke liye use hota hai.

✍️ *Example:*

```css
position: fixed;
top: 0;
left: 0;
```

---

## 🎯 5. `sticky` (Thoda sa smart — pehle line mein, phir chipak jaata hai)

**Socho ke sticker normal line mein hai, lekin jaise hi tum copy scroll karte ho, woh upar chipak jaata hai.**

```css
position: sticky;
```

* Normal flow mein hota hai.
* Lekin jab **scroll** hoti hai to woh ek jagah pe **chipak jaata hai**.
* `top: 0;` likhna zaroori hai batane ke liye kahaan chipakna hai.

✍️ *Example:*

```css
position: sticky;
top: 0;
```

---

## 🔁 Ek chhoti si table:

| Position | Move kar sakte ho? | Parent ke hisaab se? | Scroll pe chipakta? |
| -------- | ------------------ | -------------------- | ------------------- |
| static   | ❌ Nahi             | ❌ Nahi               | ❌ Nahi              |
| relative | ✅ Haan             | ❌ Nahi               | ❌ Nahi              |
| absolute | ✅ Haan             | ✅ Haan               | ❌ Nahi              |
| fixed    | ✅ Haan             | ❌ (screen ke hisaab) | ✅ Haan              |
| sticky   | ✅ Haan             | ❌ Nahi               | ✅ (scroll pe)       |

---

Agar chaho to mein ek chhoti demo page bana ke dikha doon jisme ye sab positions kaam karti hoon?
