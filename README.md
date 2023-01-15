# !!UNDER CONSTRUCTION!!

[API REF](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/API)

List of features that need to be catered to:
- support for potential use of authentication (username:password declared in backend config), needs a way to send/store user information in situations where this occurs.
- support for potential changes in CKPT models that require different settings (clip_skip etc) need to have their requirements met. This means we need to include a tab for setting these things (see [here](https://rentry.org/voldy#-novelai-setup-) for an example of the settings that need changing for NovelAI.

General idea is to have the initial tab set up as "login", allowing users to enter: IP and port of target SD session, a username and password if required by their backend. Tab two will be the prompt, negative prompt, a choice between two radio buttons for Steps ("28" and "48") and the same for CFG scale ("11" and "12"). An option for "Create a batch?" which will set the batch size to 8 while it is ticked, a seed textbox and an optional square button to enable the hr fix. The final tab will be for displaying the generated images and related information such as generated seed and information from tab 2.

Also needs download functionality. The only feature this app is aiming to support is the text to image features. Other tabs such as img2img and the rest are beyond the scope of this project. The aim is to simply have a clean material ui interface on the mobile device which simply sends and recieves to and from the API.







supposed needed API stuff is:
- GET /login_check
- POST /login
- POST /sdapi/v1/txt2img
- ???
