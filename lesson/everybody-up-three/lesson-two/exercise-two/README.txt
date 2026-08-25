LASIN — Everybody Up 3
Unit 1: Things to Eat
Lesson 2: Vegetables
Exercise 2: Listen and Choose

CONTENTS
- index.html
- assets/images/        12 positive/negative picture choices
- assets/audio/questions/ 6 question MP3s
- assets/audio/answers/   12 answer MP3s
- assets/ui/bravo.gif
- assets/ui/success-chime.wav

LOCKED FLOW IMPLEMENTED
- 24 questions total.
- Each positive/negative vegetable target appears twice.
- Two picture choices per question.
- Headphones button above the choices.
- First question audio begins after 1.5 seconds.
- Each later question audio begins after 1.7 seconds.
- Headphones click cancels pending automatic playback and plays immediately.
- Playback sequence: question MP3, 1.7-second gap, then answer MP3.
- Correct answer: 0.5-second delay -> light-green full-screen Bravo -> uploaded Bravo GIF + gold Bravo text + clean success chime -> 2 seconds -> next question.
- Wrong answer stays on the same question and allows retry.

COMBINING LATER
The CSS is scoped under #lasin-ex2-root and the JavaScript is exposed only as window.LASINExercise2.
The component can be mounted into a parent LASIN project with:

  LASINExercise2.mount(document.getElementById('your-container'), {
    assetBase: './path-to-ex2-assets/'
  });
  LASINExercise2.start();

It also dispatches a bubbling custom event named:
  lasin-exercise-complete
when question 24 is completed.
