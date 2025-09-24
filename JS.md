let stack = []
// let stp = []

const stackopr = document.getElementById("stack")
const step = document.getElementById("stp")

document.getElementById("push").addEventListener("click", () => {
    let num = prompt("Enter number to be pushed into stack")
    if (num) {
        stack.push(num)
        updateStack()
        step.innerHTML += `<li style = "font-size:35px; font-weight = "bold">Pushing ${num} in the stack</li>`
    }
})

document.getElementById("pop").addEventListener("click", () => {
    if (stack.length == 0) {
        step.innerHTML += `<li style = "font-size:35px; font-weight = "bold";> Checking if any element to pop</li>`
        alert("Stack is empty. Try again after inserting elements")
    }
    else {
        let elementpopped = stack.pop()
        deleteStack()
        step.innerHTML += `<li style = "font-size:35px; font-weight = "bold";> Popping ${elementpopped} from the stack</li>`
        
        
    }
})

document.getElementById("empty").addEventListener("click", () => {
    if (stack.length == 0) {
        alert("Stack is empty")
    }
    else {
       alert("Stack is not empty.")
    }
})
document.getElementById("size").addEventListener("click", () => {
    alert("Current stack size " + stack.length)
})
document.getElementById("top").addEventListener("click", () => {
    if (stack.length == 0) {
        alert("No element found. Stack is empty ")
    }
    else {
        alert("Top most element of stack is " + stack[stack.length - 1])
    }
})

function updateStack() {
    stackopr.innerHTML = ""
    for (let index = stack.length - 1; index >= 0; index--) {
        let div = document.createElement("div")
        div.className = "box1"
        div.textContent = stack[index]
        //  stackopr.firstChild.classList.add("popAnimation")
         stackopr.appendChild(div)
    }
   
}

function deleteStack() {
    if (stackopr.firstChild) {
        stackopr.firstChild.classList.add("boxAnimation")
        setTimeout(() => {
            stackopr.removeChild(stackopr.firstChild)
        }, 300);
    }
}
