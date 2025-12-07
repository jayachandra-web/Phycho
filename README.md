<!DOCTYPE html>
<html>
<head>
<title>Phycho (Jai)</title>
<style>
body{
    font-family: Arial;
    background: #f2f2f2;
    text-align: center;
    padding: 20px;
}

.box{
    background: white;
    padding: 20px;
    border-radius: 10px;
    width: 90%;
    margin: auto;
    max-width: 350px;
    box-shadow: 0 0 10px #aaa;
}

button{
    width: 100%;
    padding: 12px;
    background: black;
    color: white;
    border: none;
    border-radius: 6px;
    margin-top: 10px;
}

input, textarea{
    width: 100%;
    padding: 10px;
    margin-top: 10px;
    border-radius: 6px;
    border: 1px solid #aaa;
}
</style>

<script>
function show(page){
    document.querySelectorAll(".page").forEach(p => p.style.display="none");
    document.getElementById(page).style.display="block";
}
</script>

</head>

<body>

<!-- LOGIN PAGE -->
<div class="page" id="login">
    <div class="box">
        <h2>Phycho (Jai)</h2>
        <h3>Login</h3>
        <input placeholder="Enter Email">
        <input placeholder="Enter Password" type="password">
        <button onclick="show('home')">Login</button>
        <p>Don't have an account?</p>
        <button onclick="show('signup')">Create Account</button>
    </div>
</div>

<!-- SIGNUP PAGE -->
<div class="page" id="signup" style="display:none;">
    <div class="box">
        <h2>Create Account</h2>
        <input placeholder="Name">
        <input placeholder="Email">
        <input placeholder="Password" type="password">
        <button onclick="show('login')">Sign Up</button>
        <button onclick="show('login')">Back to Login</button>
    </div>
</div>

<!-- HOME PAGE -->
<div class="page" id="home" style="display:none;">
    <div class="box">
        <h2>Welcome User</h2>
        <h3>Select Your Problem</h3>

        <button onclick="show('gf')">Girlfriend / Boyfriend Cheated</button>
        <button onclick="show('wife')">Wife / Husband Cheated</button>

        <button onclick="show('login')">Logout</button>
    </div>
</div>

<!-- COMPLAINT PAGE 1 -->
<div class="page" id="gf" style="display:none;">
    <div class="box">
        <h2>GF / BF Cheated</h2>
        <textarea rows="5" placeholder="Enter your complaint here..."></textarea>
        <button onclick="alert('Complaint Submitted (UI only).')">Submit</button>
        <button onclick="show('home')">Back</button>
    </div>
</div>

<!-- COMPLAINT PAGE 2 -->
<div class="page" id="wife" style="display:none;">
    <div class="box">
        <h2>Wife / Husband Cheated</h2>
        <textarea rows="5" placeholder="Enter your complaint here..."></textarea>
        <button onclick="alert('Complaint Submitted (UI only).')">Submit</button>
        <button onclick="show('home')">Back</button>
    </div>
</div>

</body>
</html>
