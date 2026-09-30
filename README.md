<!DOCTYPE html>
<html>
<head>
    <title>My To-Do List</title>
    <style>
        body {
            font-family: Arial;
            text-align: center;
            background: #f2f2f2;
            padding: 50px;
        }

        .box {
            background: white;
            padding: 30px;
            max-width: 500px;
            margin: auto;
            border-radius: 10px;
        }

        input {
            padding: 10px;
            width: 65%;
        }

        button {
            padding: 10px;
            background: #333;
            color: white;
            border: none;
            cursor: pointer;
        }

        li {
            list-style: none;
            padding: 10px;
            margin: 5px;
            background: #eee;
        }
    </style>
</head>

<body>

<div class="box">
    <h1>My To-Do List</h1>

    <input id="task" placeholder="Enter a task">
    <button onclick="addTask()">Add</button>

    <ul id="list"></ul>
</div>

<script>
function addTask() {
    let task = document.getElementById("task").value;

    if (task == "") {
        alert("Please enter a task");
        return;
    }

    let li = document.createElement("li");
    li.innerHTML = task + 
        ' <button onclick="this.parentElement.remove()">Delete</button>';

    document.getElementById("list").appendChild(li);
    document.getElementById("task").value = "";
}
</script>

</body>
</html>
