<!DOCTYPE html>
<html lang="en">
<head>
    <title>List of works</title>
    <meta charset="UTF-8">
    <link href="https://fonts.googleapis.com/css?family=Roboto+Slab:300,400,700|Roboto:300,400,400i,700,700i" rel="stylesheet">
    <link rel="stylesheet" href="/static/style.css" />
    <style>
    ul {list-style: none;} li {font-family: 'Roboto Slab', serif;} hr {border-bottom: 1px solid #ca987a;}
</style>
    
<script>
function add_book() {
    fetch('/api/create_work')
        .then(function(response){window.location.reload(false);})
}
function add_publication(work_id) {
    let name = document.getElementById('name_'+work_id).value;
    let data = {work_id: work_id, name: name}; console.log(data);
    fetch('/api/add_publication', 
        {method: 'POST', body: JSON.stringify(data), headers:{'Content-Type': 'application/json'}})
        .then(function(){window.location.reload(false);})
}
</script>

</head>

<body>
    <header><div class="wrap">
        <img id="logo" src="/static/logo.png">
        <nav id="menu"><a>Home</a><a>About</a><a>FAQ</a><a>Contribute</a><a>Contact us</a></nav>
        <a id="search"><div id="search-icon"></div>Search</a>
        <nav id="tabs"><a class="active">Tab</a><a>Another tab</a></nav>
    </div></header>
    <main><div class="wrap">
        
    <h1></h1>
     <img style="padding: 0 15px; float: left;"src= 
        "https://images-na.ssl-images-amazon.com/images/I/51FMxz1kEUL._SX317_BO1,204,203,200_.jpg" alt="Romeo and Juliet" width="100">
        
         <ul>
        
            <li>Romeo and Juliet</li>
        
        
        </ul>
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Genre: Tragedy</span>
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Genre: Stage Play</span>
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Era: 13th Century</span>
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Location: Verona (city)</span>
        
        <br>
        <br>
       
    <button onclick="document.getElementById('work_1').style.display='block';">add publication</button>
    <div id="work_1" style="display:none;">
        <input type="text" name="name" id="name_1" placeholder="title">
        <button onclick="add_publication(1);">save</button>
    </div>
    <hr><br>
    
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Genre: Children&#39; Literature</span>
        
        <ul>
        
            <li>Alice&#39;s Adventures in Wonderland</li>
        
        
        </ul>
    <button onclick="document.getElementById('work_2').style.display='block';">add publication</button>
    <div id="work_2" style="display:none;">
        <input type="text" name="name" id="name_2" placeholder="title">
        <button onclick="add_publication(2);">save</button>
    </div>
    <hr><br>
    
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Genre: Science Fiction</span>
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Era: 80s</span>
        
        <ul>
        
            <li>Jurassic Park</li>
        
        </ul>
    <button onclick="document.getElementById('work_3').style.display='block';">add publication</button>
    <div id="work_3" style="display:none;">
        <input type="text" name="name" id="name_3" placeholder="title">
        <button onclick="add_publication(3);">save</button>
    </div>
    <hr><br>
    
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Genre: Fantasy</span>
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Genre: Children&#39; Literature</span>
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Genre: Mystery</span>
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Setting: Boarding School</span>
        
             <span style="padding: 5px; border: 1px solid black; border-radius: 5px;">Era: 90s</span>
        
        <ul>
        
            <li>Harry Potter and the Philosopher&#39;s Stone</li>
        
        
        </ul>
    <button onclick="document.getElementById('work_4').style.display='block';">add publication</button>
    <div id="work_4" style="display:none;">
        <input type="text" name="name" id="name_4" placeholder="title">
        <button onclick="add_publication(4);">save</button>
    </div>
    <hr><br>
    
        
        <ul>
        
        </ul>
    <button onclick="document.getElementById('work_5').style.display='block';">add publication</button>
    <div id="work_5" style="display:none;">
        <input type="text" name="name" id="name_5" placeholder="title">
        <button onclick="add_publication(5);">save</button>
    </div>
    <hr><br>
    
    <button onclick="add_book();">add book</button>

    </div></main>
</body>
</html>
