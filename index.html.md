<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Social Hostel Chennai - Registration</title>  
    <style>  
        body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif; background: #f0f2f5; padding: 15px; display: flex; justify-content: center; }  
        .form-card { background: white; padding: 25px; border-radius: 12px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); width: 100%; max-width: 480px; }  
        h2 { color: #075E54; margin: 0 0 10px 0; text-align: center; }  
        p.subtitle { text-align: center; color: #666; font-size: 13px; margin-bottom: 20px; }  
        label { display: block; margin-top: 15px; font-weight: 600; color: #444; font-size: 14px; }  
        input, select, textarea { width: 100%; padding: 12px; margin-top: 5px; border: 1px solid #ccc; border-radius: 8px; box-sizing: border-box; font-size: 16px; }  
        .row { display: flex; gap: 10px; }  
        .row div { flex: 1; }  
        .upload-section { background: #f9f9f9; padding: 15px; border: 1.5px dashed #25D366; border-radius: 8px; margin-top: 15px; }  
        button { background: #25D366; color: white; border: none; padding: 16px; width: 100%; border-radius: 8px; cursor: pointer; font-size: 18px; font-weight: bold; margin-top: 25px; transition: 0.3s; }  
        button:hover { background: #128C7E; }  
    </style>  
</head>  
<body>  
  
<div class="form-card">  
    <h2>Hostel Registration</h2>  
    <p class="subtitle">Social Hostel Chennai</p>  
      
    <form id="registrationForm" action="https://formsubmit.co/YOUR_EMAIL@gmail.com" method="POST" enctype="multipart/form-data">  
          
        <input type="hidden" name="_captcha" value="false">  
        <input type="hidden" name="_template" value="table">  
  
        <div class="row">  
            <div>  
                <label>First Name</label>  
                <input type="text" name="First_Name" id="fname" required>  
            </div>  
            <div>  
                <label>Last Name</label>  
                <input type="text" name="Last_Name" id="lname" required>  
            </div>  
        </div>  
  
        <label>Phone Number</label>  
        <input type="tel" name="Phone" id="phone_num" placeholder="E.g. 9876543210" required>  
  
        <label>Email Address</label>  
        <input type="email" name="Email" id="email_addr" required>  
  
        <div class="row">  
            <div>  
                <label>Check-in Date</label>  
                <input type="date" name="Check_in_Date" id="cdate" required>  
            </div>  
            <div>  
                <label>Arrival Time</label>  
                <input type="time" name="Arrival_Time" id="ctime">  
            </div>  
        </div>  
  
        <label>Identity Proof Type</label>  
        <select name="ID_Type" id="idtype">  
            <option value="Aadhaar Card">Aadhaar Card</option>  
            <option value="PAN Card">PAN Card</option>  
            <option value="Voter ID">Voter ID</option>  
            <option value="Passport">Passport</option>  
            <option value="ID Card">ID Card</option>  
        </select>  
  
        <div class="upload-section">  
            <label>Upload ID Document</label>  
            <input type="file" name="Attachment" accept="image/*,.pdf" required>  
        </div>  
  
        <button type="submit">Submit to Email & WhatsApp</button>  
    </form>  
</div>  
  
<script>  
    document.getElementById('registrationForm').onsubmit = function() {  
        // 1. Get values for WhatsApp message  
        let fname = document.getElementById('fname').value;  
        let lname = document.getElementById('lname').value;  
        let pnum = document.getElementById('phone_num').value;  
        let cdate = document.getElementById('cdate').value;  
        let ctime = document.getElementById('ctime').value;  
        let idtype = document.getElementById('idtype').value;  
  
        // 2. Your WhatsApp Number (Change this!)  
        let myWhatsApp = "918098566636";  
  
        // 3. Format the WhatsApp Text  
        let message = `*New Registration - Social Hostel*%0A%0A` +  
                      `*Name:* ${fname} ${lname}%0A` +  
                      `*Phone:* ${pnum}%0A` +  
                      `*Check-in:* ${cdate}%0A` +  
                      `*Time:* ${ctime}%0A` +  
                      `*ID Provided:* ${idtype}%0A%0A` +  
                      `_Note: I have uploaded my ID proof via the form._`;  
  
        // 4. Construct the WhatsApp URL  
        let waURL = `https://wa.me/${8098566636}?text=${message}`;  
  
        // 5. Change the FormSubmit 'next' URL dynamically to your WhatsApp link  
        let nextInput = document.createElement("input");  
        nextInput.type = "hidden";  
        nextInput.name = "_next";  
        nextInput.value = waURL;  
        this.appendChild(nextInput);  
  
        return true; // Allows the form to submit to email first, then redirect to WA  
    };  
</script>  
  
</body>  
</html>  
  
