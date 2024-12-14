## Contact Form

Have a question or project in mind? We're happy to help. Drop us a message below.

{{< rawhtml >}}

<script type="text/javascript">
var submitted = false;

function handleSubmit(form) {
    const button = form.querySelector('button[type="submit"]');
    button.disabled = true;
    button.classList.add('loading');
    submitted = true;
    return true;
}
</script>

<style>
/* Spinner Animation */
@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

/* Loading Spinner */
.loading::after {
    content: '';
    display: inline-block;
    width: 1em;
    height: 1em;
    margin-left: 0.5em;
    border: 2px solid #ffffff;
    border-radius: 50%;
    border-top-color: transparent;
    animation: spin 0.6s linear infinite;
    vertical-align: middle;
}

/* Disabled button styles */
button[type="submit"]:disabled {
    opacity: 0.7;
    cursor: not-allowed;
}
</style>

<iframe name="hidden_iframe" id="hidden_iframe" style="display:none;" 
onload="if(submitted) {window.location='/thank-you';}"></iframe>

<form
    action="https://docs.google.com/forms/u/3/d/e/1FAIpQLScrKW7siL3Tqh1ze_WdOpbtGrnGzUxFPPQ3WZWyWsKxodPWww/formResponse"
    method="post"
    target="hidden_iframe"
    onsubmit="return handleSubmit(this);"
>
    <label class="required">Email</label>
    <input type="email" placeholder="Your Email" class="form-input" name="entry.1045781291" required>
    <label>Name</label>
    <input type="text" placeholder="Your Name" class="form-input" name="entry.2005620554">
    <label>Subject</label>
    <input type="text" placeholder="Subject" class="form-input" name="entry.1065046570">
    <label class="required">Message</label>
    <textarea rows="10" placeholder="Message" class="form-input" name="entry.839337160" required></textarea>
    <button type="submit">Send</button>
</form>

<link rel="stylesheet" href="/css/form.css">
<link rel="stylesheet" href="/css/vars.css">

{{< /rawhtml >}}
