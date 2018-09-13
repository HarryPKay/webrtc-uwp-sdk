INSTRUCTIONS
=======

From your terminal, recursively clone this repo to obtain all the source code needed to build WebRTC for UWP:
git clone --recursive https://github.com/webrtc-uwp/webrtc-uwp-sdk.git

This repository will yield the WebRtc SDK and dependency libraries.

Directory structure:

- webrtc-uwp-sdk\bin          	contains scripts for preparing an environment for the Windows
- webrtc-uwp-sdk\common         contains samples applications (ChatterBox and PeerCC)
- webrtc-uwp-sdk\webrtc    		contains WebRtc code
- webrtc-uwp-sdk\docs			contains documentation

Prerequisites:

- Visual Studio 2017 (latest tested version tested 15.6)
- Windows SDK 16299 (available from archive page https://developer.microsoft.com/en-us/windows/downloads/sdk-archive)
- When installing the SDK, include the feature "Debugging Tools for Windows" which is required to run prepare.bat. Note that the SDK install as part of Visual Studio does not include this feature.


How to Build:

WINDOWS BUILD :
----------------------------

1) Run prepare script, from your terminal:
<br />
<pre>
<code>
cd webrtc-uwp-sdk
bin\prepare.bat
</code>
</pre>
<br />
This script will prepare environment but it won't build webrtc projects. In this case webrtc project will be built from Visual Studio once you try to build Org.WebRtc.

2) From VS2017, load webrtc\windows\solutions\WebRtc.sln for WebRtc development.

3) Now you can build winrt libraries for WebRtc and deploy sample apps ChatterBox and PeerCC.

IMPORTANT NOTES:
----------------------------
Ensure that Git is properly configured to handle line endings. 
Git setting for core.autocrlf MUST be set to true; 
BEFORE running bin\prepare.bat, check current setting for core.autocrlf using command: 'git config -l', or 'git config core.autocrlf', and you can change setting to true using 'git config --global core.autocrlf true'. 

Usefull links: https://help.github.com/articles/dealing-with-line-endings/ https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration#__code_core_autocrlf_code (section core.autocrlf)

====
