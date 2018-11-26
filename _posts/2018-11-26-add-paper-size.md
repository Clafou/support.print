---
layout: post
title: Adding a New Paper Size
categories: [Troubleshooting]
---

I have included most standard paper sizes to Print to Size's built-in list. But if you find that your paper size is missing you can use this page to add it to the app.

* View this page on your iPhone/iPad
* Fill-in the form below with your paper size
* Tap on the Add Size button
* Tap Open Print to Size
* The app now includes your size at the bottom of the paper size list 

<script>
function addPaper() {
    var fields = document.getElementById("customPaperSize").elements;
    var w = fields["width"].value;
    var h = fields["height"].value;
    var unit = fields["unit"].value;
    var url = "print-to-size://x-callback-url/addPaper?w=" + w + "&h=" + h + "&unit=" + unit;
    window.open(url);
    return false;
}
</script>
<form class="uk-form" id="customPaperSize">
    <fieldset data-uk-margin>
        <legend>Paper Size to Add</legend>
        <input type="text" name="width" placeholder="width">
        x
        <input type="text" name="height" placeholder="height">
        <select name="unit">
            <option value="in">Inches</option>
            <option value="cm">Centimeters</option>
        </select>
        <div class="uk-form-row">
            <button class="uk-button-primary" onclick="return addPaper()">Add Size</button>
        </div>
    </fieldset>
</form>

Once added I cannot promise that your printer will accept this new paper size: some printers only accept standard sizes and reject any other size. But if this works and you think the size should be included for everyone, please let me know and I will look into it – thank you!


