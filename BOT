<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Task Bot</title>
  <style>
    body {
      background: #0f172a;
      color: #f1f5f9;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }
    .bot-container {
      background: #1e293b;
      padding: 2rem;
      border-radius: 1rem;
      width: 90%;
      max-width: 500px;
      text-align: center;
    }
    .progress-circle {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      border: 10px solid #334155;
      border-top-color: #3b82f6;
      margin: 1rem auto;
      animation: spin 1s linear infinite;
    }
    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
    input, button {
      margin-top: 1rem;
      padding: 0.5rem;
      font-size: 1rem;
      border-radius: 0.5rem;
      border: none;
    }
    input {
      width: 80%;
    }
    button {
      background: #3b82f6;
      color: white;
      cursor: pointer;
    }
    button:hover {
      background: #2563eb;
    }
  </style>
</head>
<body>
  <div class="bot-container">
    <h2>🎯 Добро пожаловать в Задачный Бот</h2>
    <div class="progress-circle"></div>
    <p id="task">Загрузка задания...</p>
    <input type="text" id="checkWord" placeholder="Введите проверочное слово">
    <button onclick="nextTask()">Проверить и продолжить</button>
  </div>

  <script>
    const tasks = [
      { text: "Найди в комнате 3 предмета синего цвета", code: "синий" },
      { text: "Сделай 10 приседаний и напиши слово: фитнес", code: "фитнес" },
      { text: "Подойди к зеркалу и подмигни себе. Напиши слово: герой", code: "герой" },
      { text: "Открой окно и вдохни глубже. Напиши: воздух", code: "воздух" },
      { text: "Поставь будильник на завтрашний день. Введи: готово", code: "готово" }
    ];

    let currentTask = 0;

    function showTask() {
      document.getElementById('task').innerText = tasks[currentTask].text;
    }

    function nextTask() {
      const input = document.getElementById('checkWord').value.trim().toLowerCase();
      if (input === tasks[currentTask].code) {
        currentTask++;
        if (currentTask < tasks.length) {
          document.getElementById('checkWord').value = '';
          showTask();
        } else {
          document.querySelector('.bot-container').innerHTML = "<h2>🎉 Поздравляем! Все задания выполнены.</h2>";
        }
      } else {
        alert('Неправильное проверочное слово!');
      }
    }

    window.onload = showTask;
  </script>
</body>
</html>
