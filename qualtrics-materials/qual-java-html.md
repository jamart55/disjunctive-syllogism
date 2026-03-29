## Center HTML IMAGE - NEED CHANGE LINK
<div>

  <img src="LINK_HERE" 
       style="width: 1200px; height: 720px; max-width: 100%; height: auto; display: block; margin: 0 auto; border: none; outline: none;" />

</div>

## JavaScript

### NO NEXT button & AUTOPROCEED
Qualtrics.SurveyEngine.addOnload(function() {
  this.hideNextButton(); // hides NextButton early, before it's shown
});

Qualtrics.SurveyEngine.addOnReady(function() {
  var video = jQuery("#vidid");
  var preview = false;

  if (/^\/jfe[0-9]?\/preview/.test(window.location.pathname)) preview = true;

  if (preview) {
    if (jQuery('.MobilePreviewFrame:first').length > 0) {
      var vidEl = video.get(0);
      vidEl.muted = true;
      vidEl.width = "300";
    }
  }

  video.on('ended', function(event) {
    $('NextButton').click(); // auto-advance after video ends
  });
});

Qualtrics.SurveyEngine.addOnUnload(function() {
  // Optional: any cleanup
});

### SHOW NEXT button after video
Qualtrics.SurveyEngine.addOnReady(function() {
    var video = jQuery("#vidid");
    var preview = false;

    // Check if in preview mode
    if(/^\/jfe[0-9]?\/preview/.test(window.location.pathname)) preview = true;  
    
    if(preview) {
        if(jQuery('.MobilePreviewFrame:first').length > 0) {
            var vidEl = video.get(0);
            vidEl.muted = true;
            vidEl.width = "300";
        }
    }  

    // Hide the Next button immediately
    jQuery('#NextButton').hide();

    // Show the Next button when the video ends
    video.on('ended', function(event) {          
        jQuery('#NextButton').show();  
    });
});




## Center HTML VIDEO - NEED CHANGE LINK

### For signature box

<div style="text-align: center; line-height: 0; margin-bottom: 0; padding-bottom: 0;">
    <video id="vidid" autoplay="autoplay" width="1200" class="qmedia" height="auto" preload="auto" style="display: block; margin: 0 auto;">
        <source src="LINK_HERE" type="video/mp4">
        <embed align="middle" autoplay="true" bgcolor="white" class="qmedia" controller="true" height="auto" src="LINK_HERE" type="video/quicktime" width="1200">
    </video>
</div>

### General
<div style="text-align: center;">
    <video id="vidid" autoplay="autoplay" width="1200" class="qmedia" height="720" preload="auto">
        <source src="LINK_HERE" type="video/mp4">
        <embed align="middle" autoplay="true" bgcolor="white" class="qmedia" controller="true" height="720" pluginspage="http://www.apple.com/quicktime/download/" src="LINK_HERE" type="video/quicktime" width="1200">
    </video>
</div>

## Links

### intro trial links
**rachel-vid:** https://nyu.qualtrics.com/CP/File.php?F=F_39ieyZznekmsCGh
**after-rachel:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_XX7GNikZMA2pvGz
**consent-007-no-sig-box:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_enTxVHUZBqzSo9E
**setup-01:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_qFwqcAFyMUm7Xb8
**setup-02:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_vCMK1TKcxFOyMd1
**setup-03:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_fTYYmM9UunSNueJ

### trial links
**01-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_12TJ0SmIpkaAPZ6
**01-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_ka2oxS4FNAcRk9O

**02-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_0vwJ56DtaV5s0Vg
**02-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_5nhYXZtb5BYR6Vn

**03-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_PpQKTeFNUHnVEnJ
**03-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_yaSsX94CkPixK52

**04-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_QALYzlhkTP8JP7E
**04-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_5jJejxLUPEXxXKC

**05-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_rSydfAUmPP3XlU4
**05-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_W2r3qy5uXjfkxJI

**06-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_kir0SRapCYf4GrE
**06-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_amxHYKivwoCp4Oc

**07-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_13hRChP5hWoWk3P
**07-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_t0CSxZkTsMxtW28

**08-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_9ujcULSaaxDeZXx
**08-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_7zziUuRPpk38lne

**09-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_fYUeU933L6qDqpn
**09-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_7kF8N88N9ZAWZPJ

**10-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_flYrTUjb0UbdWED
**10-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_fw1jgIMZIPFQVfa

**11-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_EOo5YdLi1z6AvsE
**11-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_o0vvSc9OLKZ0juy

**12-trial:**     https://nyu.qualtrics.com/ControlPanel/File.php?F=F_a8gN7lCWrkHWYea
**12-attention:** https://nyu.qualtrics.com/ControlPanel/File.php?F=F_oZHMFnWnZfBdtPj
