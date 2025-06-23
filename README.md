<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>A9LH Guide - 2025 Edition</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://fonts.cdnfonts.com/css/press-start-2p" rel="stylesheet">
  <style>
    body {
      background: #000;
      color: #0f0;
      font-family: 'Press Start 2P', monospace;
      padding: 20px;
      font-size: 10px;
      line-height: 1.8;
    }
    a { color: #0ff; text-decoration: none; }
    a:hover { text-decoration: underline; }
    h1, h2, h3 {
      border-bottom: 1px dashed #0f0;
      padding-bottom: 4px;
      margin-top: 2em;
    }
    pre, code {
      background: #111;
      border: 1px solid #0f0;
      padding: 4px;
      display: block;
      margin: 10px 0;
      overflow-x: auto;
    }
    .warning {
      border: 2px solid #f00;
      background: #200;
      padding: 10px;
      color: #f55;
      margin: 20px 0;
    }
    ul, ol { margin-left: 20px; }
    li { margin-bottom: 8px; }
  </style>
</head>
<body>

  <h1>A9LH Guide - 2025 Edition</h1>
  <p>A simple guide to install A9LH in 2025.</p>
  <p>Note that my English isn't that good, I'm sorry if I make mistakes.</p>
  <p>Alright, want to install A9LH on your 3DS for whatever reason? I gotcha.</p>

  <div class="warning">
    <strong>IF YOU DO NOT KNOW WHAT YOU'RE DOING, GET THE FUCK OUT OF HERE</strong><br>
    This guide is only intended for users who know what they are doing. Myself haven't installed A9LH in the past, and i bricked my console a few times before finding the right way to do it. Please make backups and do have a NTRBoot flashcard (if you don't know what i'm talking about, you shouldn't even be here)<br>
    I am not responsible if you brick your 3DS because i warned you.
  </div>

  <div class="warning">
    <strong>PLEASE, REALLY</strong><br>
    I'm insisting. If you truly want CFW for daily use, go to <a href="https://3ds.hacks.guide">3ds.hacks.guide</a> and install boot9strap.
  </div>

  <p>If you want to show me you succeeded, or tell me what i could do to improve this guide you can email me: maylina53uwu@gmail.com 
or DM on Discord: maylina53_uwu<br>(You can ask for help as well, but you better have read instructions)</p>

  <h2>Summary</h2>
  <ul>
    <li><a href="#prerequisites">Requirements</a></li>
    <li><a href="#downgrade">Downgrade</a></li>
    <li><a href="#removing-b9s">Removing B9S</a></li>
    <li><a href="#installing-a9lh">Installing A9LH</a></li>
    <li><a href="#installing-luma">Installing Luma</a></li>
  </ul>

  <h2 id="prerequisites">1. Prerequisites</h2>
  <ul>
    <li>Any 3DS family console running boot9strap (used to dump otp.bin, we'll remove it, if stock, hack it using 3ds.hacks.guide)</li>
    <li>A few braincells</li>
  </ul>

  <h2>Required Files</h2>
  <ul>
    <li>Soundhax audio: <a href="http://soundhax.com">soundhax.com</a></li>
    <li>otherapp: <a href="https://smealum.github.io/3ds/#otherapp">smealum.github.io</a></li>
    <li>OTP.bin (dumped yourself, should be in /boot9strap/)</li>
    <li>Luma v6.6: <a href="https://github.com/LumaTeam/Luma3DS/releases/download/v6.6/Luma3DSv6.6.7z">download</a></li>
    <li>SafeA9LH Installer: <a href="https://github.com/AuroraWright/SafeA9LHInstaller/releases/tag/v2.6.7">download</a></li>
    <li>Arm9LoaderHax: <a href="https://github.com/AuroraWright/arm9loaderhax/releases">download</a></li>
    <li>udsploit: <a href="https://github.com/smealum/udsploit/releases/tag/1.0">download</a></li>
    <li>safehax: <a href="https://github.com/TiniVi/safehax/releases/tag/r27">download</a></li>
    <li>data_input_v4.zip (search for it manually, I can't provide it)</li>
  </ul>

  <h2 id="downgrade">2. Downgrade (if on newer firmware)</h2>
  <p><strong>BACKUP EVERYTHING! (Also backup NAND with NANDManager as it'll let you do a full backup in case you horribly fuck up)</strong> Get firmware files for a version between 9.0.0 and 11.2(updates folder, not CTRTransfer) region and model SHOULD match (or you'll brick.).</p>
  <ol>
    <li>Put <code>updates</code> folder on SD root</li>
    <li>Install sysUpdater CIA: <a href="https://github.com/profi200/sysUpdater/releases/tag/0.4.3b">download</a></li>
    <li>Run and press Y to downgrade</li>
  </ol>
  <p><em>Alternate method (GodMode9):</em></p>
  <ul>
    <li>Go to GodMode9, press the HOME Button, go to More → System info to find original system version</li>
    <li>Get matching <code>updates</code> folder</li>
    <li>On GM9 with the <code>updates</code> folder correctly placed at the root of the sd card: Uninstall all NAND titles via Title Manager (Press Home Button → Title Manager → NAND/TWL Titles</li>
    <li>Go to SD, select every cia file (L+RIGHT) in sd/updates Press A → CIA Image options → Install image</li>
    <li>Reboot and verify</li>
  </ul>

  <h2 id="removing-b9s">3. Removing Boot9Strap</h2>
  <p><strong>Make sure you haven't done a region change or use a custom keyboard! (Or used a dsiware exploit like bannerbomb with the japanese flipnote)</strong></p>
  <ol>
    <li>Boot GodMode9</li>
    <li>HOME → Scripts → GM9Megascript → Hax Options → Uninstall CFW</li>
    <li>Follow prompts, reboot, if it boots without any issue, continue the guide, Otherwise, go restore that nand backup and go get this flashcard.</li>
  </ol>

  <h2 id="installing-a9lh">4. Installing A9LH</h2>
  <p>Place files:</p>
  <ul>
    <li>otherapp, soundhax mp3 file, and boot.3dsx in root</li>
    <li>udsploit + safehax in <code>/3ds/</code></li>
    <li>SafeA9LHInstaller’s <code>arm9loaderhax.bin</code> in root</li>
    <li><code>a9lh</code> OTP goes in root + merge data_input_v4's a9lh folder with the one on your sd</li>
  </ul>
  <p>Then:</p>
  <ol>
    <li>Boot HBL via SoundHax</li>
    <li>Run udsploit → Start to exit</li>
    <li>Run safehax → SafeA9LHInstaller appears</li>
    <li>Press SELECT to install</li>
    <li>Shutdown with any button, insert SD into PC</li>
  </ol>

  <h2 id="installing-luma">5. Installing Luma (Well, technically you could install others cfw as long as it's compatible with your version, but i'll use luma this time)</h2>
  <ol>
    <li>Replace installer <code>arm9loaderhax.bin</code> with Luma v6.6’s</li>
    <li>Boot — you should see Luma config</li>
    <li>Enable Autoboot SysNAND (if no EmuNAND)</li>
    <li>Reboot — you're done!</li>
  </ol>

  <p style="margin-top: 2em;">Guide by <a href="https://github.com/Maylina53uwu">Maylina53uwu</a></p>

</body>
</html>
