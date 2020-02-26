# GazeCloud
Real-Time online Eye-Tracking

GazeCloudAPI Integration details:  

Register origin domain address of your web page:  https://api.gazerecorder.com/register/

Include JavaScript 
<script src="https://api.gazerecorder.com/GazeCloudAPI.js" ></script>

1. Start eye tracking
GazeCloudAPI.StartEyeTracking(); 

2.  Define your  results  data  callback
GazeCloudAPI.OnResult = 
function (GazeData) {
GazeData.state //  0: valid gaze data;     -1 : face tracking lost,     1 : gaze data uncalibrated
GazeData.docX // gaze x in document coordinates
GazeData.docY // gaze y in document coordinates 
GazeData.time // timestamp
}

3.  After you finish your test stop eye tracking
GazeCloudAPI.StopEyeTracking();

optional callbacks:
GazeCloudAPI.OnCalibrationComplete =function(){ console.log('gaze Calibration Complete')  }

GazeCloudAPI.OnCamDenied =  function(){ console.log('camera  access denied')  }

GazeCloudAPI.OnError =  function(msg){ console.log('err: ' + msg)  }

Disable/Enable click recalibration
GazeCloudAPI.UseClickRecalibration = true;

Simple Example: https://api.gazerecorder.com/ 

Supported browsers: Chrome 53+ | Edge 12+ | Firefox 42+ | Opera 40+ | Safari 11+   

Read More:
https://gazerecorder.com/gazecloudapi/
