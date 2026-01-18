🔗 Exam Portal – File Connection Summary
📁 Project Structure
index.html        → Landing page  
test-entry.html   → Test entry form  
exam.html         → Exam interface  
results.html      → Results page  

style.css / script.js  
test-entry.css / test-entry.js  
exam.css / exam.js  
results.css / results.js  

🔄 Page Flow (Navigation)
index.html
   ↓
test-entry.html
   ↓
exam.html
   ↓
results.html
   ↓
(Home / Retake)

🔗 Page Connections
1️⃣ index.html (Landing)

Links to test-entry.html

Signup success → redirects to test-entry.html

Uses: style.css, script.js

2️⃣ test-entry.html (Test Entry)

From: index.html

To: exam.html (after validation)

Stores student data in sessionStorage

Uses: test-entry.css, test-entry.js

3️⃣ exam.html (Exam)

From: test-entry.html

To: results.html (after submit / auto-submit)

Reads student data from sessionStorage

Stores exam results in sessionStorage

Uses: exam.css, exam.js

4️⃣ results.html (Results)

From: exam.html

Options:

Retake → exam.html

Home → index.html

Reads test + result data from sessionStorage

Uses: results.css, results.js

🔐 Data Flow (SessionStorage)
Stored in Test Entry
testData = {
  studentName,
  testId,
  email,
  startTime
}

Stored in Exam
examResults = {
  score,
  correct,
  wrong,
  unanswered,
  answers,
  timeTaken
}

Read in Results
testData + examResults

✅ Features Working

✔ All page redirects

✔ SessionStorage data flow

✔ Exam timer & auto-submit

✔ Question navigation & palette

✔ Result calculation & review

✔ Retake and home navigation

✔ Responsive design

🎯 Final Status

✅ Fully connected & functional exam portal

Clean navigation

Proper data flow

Separate exam & results pages

Ready for deployment 🚀
