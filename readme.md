# Code Quiz

- [Demo](#Demo)
- [Code-Quiz](#Coding-Quiz)
- [Diagram](#Diagram)
- [End](#End)

![photo of quiz application](code-quiz.png)

# Coding Quiz

```javascript

function getQuestion() {
  // get current question object from array
  var currentQuestion = questions[currentQuestionIndex];

  // update title with current question
  var titleEl = document.getElementById("question-title");
  titleEl.textContent = currentQuestion.title;

  // clear out any old question choices
  choicesEl.innerHTML = "";

  // loop over choices
  currentQuestion.choices.forEach(function(choice, i) {
    // create new button for each choice
    var choiceNode = document.createElement("button");
    choiceNode.setAttribute("class", "choice");
    choiceNode.setAttribute("value", choice);

    choiceNode.textContent = i + 1 + ". " + choice;

    // attach click event listener to each choice
    choiceNode.onclick = questionClick;

    // display on the page
    choicesEl.appendChild(choiceNode);
  });
}
function printHighscores() {
    // either get scores from localstorage or set to empty array
    var highscores = JSON.parse(window.localStorage.getItem("highscores")) || [];
  
    // sort highscores by score property in descending order
    highscores.sort(function(a, b) {
      return b.score - a.score;
    });
  ```
# Demo

* Quiz In Action
- [https://drive.google.com/file/d/1nfTT2Hxz6PvkoXAdkv7pNkCsY4fz8roX/view]; ![demo of quiz application]

# Diagram

![photo of mermaid diagram](diagram.png)
https://mermaid.ink/img/eyJjb2RlIjoiZ3JhcGggVERcbiAgICBBW1N0YXJ0IFF1aXpdIC0tPiBCKFN0YXJ0IFRpbWVyKVxuICAgIEJbU3RhcnQgVGltZXJdIC0tPiBDKFF1ZXN0aW9uIDEpLS0-IEQoQ29ycmVjdCEpXG4gICAgQ1tRdWVzdGlvbiAxXS0tPiBFKFdyb25nISktLT4gRihkZWR1Y3QgMzAgc2Vjb25kcylcbiAgICBEW0NvcnJlY3QhXS0tPiBNKGZ1bmN0aW9uIC5wbGF5KSAtLT5HKEdvIHRvIFF1ZXN0aW9uIDIpXG4gICAgRihkZWR1Y3QgMzAgc2Vjb25kcyktLT5MKGZ1bmN0aW9uIC5wbGF5KS0tPkdcbiAgICBHLS0-SChDb3JyZWN0ISktLT5KKGZ1bmN0aW9uIC5wbGF5KVxuICAgIEctLT5JKFdyb25nISktLT4gSyhkZWR1Y3QgMzAgc2Vjb25kcyktLT5OKGZ1bmN0aW9uIC5wbGF5KSBcbiAgICBKLS0-TyhHbyB0byBOZXh0IFF1ZXN0aW9uKVxuICAgIE4tLT5PKEdvIHRvIE5leHQgUXVlc3Rpb24pLS0-UChSZXBlYXQgU2VxdWVuY2UpXG4gICAgUC0tPlEoZnVuY3Rpb24gdG8gc2F2ZUhpZ2hzY29yZSktLT5VKHNldCB0byB0byBlbXB0eSBhcnJheSBpZiBub25lKVxuICAgIFAtLT5SKGluaXRpYWxzIGVsZW1lbnQgdG8gbG9jYWwgc3RvcmFnZSlcbiAgICBSLS0-UyhPbmNsaWNrIFNhdmUgSGlnaCBTY29yZSlcbiAgICBSLS0-VChPbmNsaWNrIFN0YXJ0IFF1aXopXG4gICAgXG5cbiAgICAiLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCJ9LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ

# End
- [Back To Top](#Code-Quiz)
