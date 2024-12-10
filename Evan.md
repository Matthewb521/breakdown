# 2024 AP Computer Science Principles Free-Response Questions: Set 1

## AP® Computer Science Principles Written Response Prompts

### Instructions:

- **Time:** 1 hour
- **Questions:** 2
- Read each question carefully and completely.
- Write your response in the space provided for each question in the Written Response booklet.
- You may plan your answers in this orange booklet, but no credit will be given for anything written in this booklet. You will only earn credit for what you write in the separate Written Response booklet.

---

### Pre-FRQ Practice

## Identify the Algorithm present in the JavaScript Files.

### Aspects of Algorithm

Sequencing
Selection
Iteration

### Question 1

Programs accept input to achieve their intended functionality. **Describe at least one valid input to your program and what your program does with that input.**

- Write your responses to this question only on the designated pages in the separate Written Response booklet.
- If there are multiple parts to this question, write the part letter with your response.

```javascript
  function removeToDo() {
    const specificCard = this.parentElement;
    const specificCardText =
      specificCard.querySelector(".to-do-card").textContent;

    for (let i = 0; i < ToDoItems.length; i++) {
      if (ToDoItems[i] === specificCardText) {
        ToDoItems.splice(i, 1);
        break;
      }
    }
    specificCard.remove();
  }
}
```

## The iput in this function is the array. The function takes this array(which is the item on the to do list)and creates a card with buttons and queryselectors.

### Question 2

Refer to your Personalized Project Reference when answering this question.

#### Part (a):

Consider the first iteration statement included in the Procedure section of your Personalized Project Reference. **Describe what is being accomplished by the code in the body of the iteration statement.**

```javascript
array.forEach((inputs) => {
  DOMSelectors.toDoList.insertAdjacentHTML(
    "beforeend",
    `<div class="card"><div class = "to-do-card">${inputs}</div>
    <button type ="submit" class="remove-button" id="remove-reminder"> Remove </button>
    </div>`
  );
});
```

The iteration statment here is the .foreach and the point of the iteration here is to create cards for each other items in the to do list

#### Part (b):

Consider the procedure identified in part (i) of the Procedure section of your Personalized Project Reference.

- Write two calls to your procedure that each cause a different code segment in the procedure to execute.
- Describe the expected behavior of each call. If it is not possible for two calls to your procedure to cause different code segments to execute, explain why this is the case for your procedure.

```javascript
removeButton.forEach((button) => {
  button.addEventListener("click", removeToDo);
});

function addToDo(event) {
  DOMSelectors.toDoList.innerHTML = "";
  const inputtedToDo = DOMSelectors.userInput.value;
  event.preventDefault();
  ToDoItems.push(inputtedToDo);
  displayToDoList(ToDoItems);
  DOMSelectors.userInput.value = "";
}
```

the remove button here takes the event listener to the button to click and remove the item from the to do list. The addToDo function takes an input of an event and then creates a card out of it and pushes it to the screen.

#### Part (c):

Suppose another programmer provides you with a procedure called `checkValidity(value)` that:

- Returns `true` if a value passed as an argument is considered valid by the other programmer.
- Returns `false` otherwise.

Using the list identified in the List section of your Personalized Project Reference, **explain in detailed steps an algorithm that uses `checkValidity` to check whether all elements in your list are considered valid by the other programmer.** Your explanation must be detailed enough for someone else to write the program code for the algorithm that uses `checkValidity`.

- Write your responses to this question only on the designated pages in the separate Written Response booklet.
- If there are multiple parts to this question, write the part letter with your response.

---

### End of Exam
