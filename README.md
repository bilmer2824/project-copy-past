# Class Number

## 1 Method
```
function numberSum(N) {
    var total = 0;
    for (var i = 1; i <= N; i++) {
        total += i;
    }
    return total;
}
console.log(numberSum(100));

// answer 5050
```
## 2 Method
```
var total = 0;
for (var i = 1; i <= 100; i++) {
    total += i;
}
console.log(total);

// answer 5050
```

## 3 Method
```
const numSum = (n) => n * (n + 1) / 2;
console.log(numSum(100));

// answer 5050
```

## 4 Method
```
var sum = 0;
for (var i = 1; i <= 100; i += 2) {
    sum += i;
}
console.log(sum);

// answer 2500
```

## 5 Method
```
function sumOddEven(n) {
    const floor = Math.floor(n / 2);
    const ceil = Math.ceil(n / 2);
    return [ceil * ceil, floor * (1 + floor)];
}
console.log(sumOddEven(100)[1], sumOddEven(100)[0])

// answer 2550 2500
```

## 6 Method
```
let even_sum = 0;
let odd_sum = 0;
for (let i = 0; i <= 100; i++) {
    if (i % 2 == 0)
        even_sum += i;
    else
        odd_sum += i;
}
console.log(even_sum, odd_sum)

// answer 2550 2500
```

## 7 Method
```
m = [0, 0]; for (i = 0; i < 101; i++) m[i % 2] += i; console.log(m[0], m[1]);

// answer 2550 2500
```

## 8 Method
```
let maz = 0, kaz = 0;
for (let i = 0; i <= 100; i++) if (i % 2 == 0) maz += i; else kaz += i; console.log(maz, kaz);

// answer 2550 2500
```

## 9 Method
```
let maz = 0, kaz = 0;
function learnJavaScript(f) {
    let count = 0
    while (count < f) {
        count + ' '
        count++
    }
    return count * (count + 1) / 2;
}
console.log(learnJavaScript(100));

// answer 5050
```
# Class Material ui

## 1 Method

```
<Button
    style={{
        borderRadius: 35,
        backgroundColor: "#21b6ae",
        padding: "18px 36px",
        fontSize: "18px"
    }}
    variant="contained"
    >
    Submit
</Button>
```

# Time Medhod

## 1 Medhod
```
let number = 0;

function updateClock() {
    const hoursElement = document.getElementById('hrs');
    const minutesElement = document.getElementById('min');
    const secondsElement = document.getElementById('sec');
    
    const update = () => {
        const hours = String(Math.floor(number / 3600)).padStart(2, '0');
        const minutes = String(Math.floor((number % 3600) / 60)).padStart(2, '0');
        const seconds = String(number % 60).padStart(2, '0');
        
        hoursElement.textContent = hours;
        minutesElement.textContent = minutes;
        secondsElement.textContent = seconds;
        
        console.log(seconds);
        number++;
        
        if (number <= 60) {
            setTimeout(update, 1000);
        }
    };

    update();
}

updateClock();
```

## 2 Medhod 

```
let number = 0;

function Time() {
    if (number <= 60) {
        const hours = String(Math.floor(number / 3600)).padStart(2, '0');
        const minutes = String(Math.floor((number % 3600) / 60)).padStart(2, '0');
        const seconds = String(number % 60).padStart(2, '0');
        
        document.getElementById('hrs').textContent = hours;
        document.getElementById('min').textContent = minutes;
        document.getElementById('sec').textContent = seconds;
        
        console.log(seconds);
        number++;
        
        if (number <= 60) {
            setTimeout(Time, 1000);
        }
    }
    return number;
}

Time();
```

## 3 Medhod
```
function updateTime() {
    const now = new Date();
    const hours = String(now.getHours()).padStart(2, '0');
    const minutes = String(now.getMinutes()).padStart(2, '0');
    const seconds = String(now.getSeconds()).padStart(2, '0');
    
    document.getElementById('hrs').textContent = hours;
    document.getElementById('min').textContent = minutes;
    document.getElementById('sec').textContent = seconds;
}

setInterval(updateTime, 1000); // Vaqt o'zgarishini har 1 sekundda yangilash
updateTime();
```
## 4 Medhod Parallax
```
attribute: data-speed="2.5"
function:
let img = document.querySelector(".images")

window.addEventListener("scroll", () =>{
    console.log(this.scrollY);
    let speed  = +img.getAttribute("data-speed")
    
    img.style.transform = `translateX(${scrollY * speed}px)`
})
```
