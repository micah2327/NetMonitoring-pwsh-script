# NetMonitoring-pwsh-script

This is a tool im thinking of employing, NetMonitor is a powershell script with a cmd line gui, That checks for network connectivity and Wec forwarding for windows specific boxes 

the only thing i had in mind when making this was security if i am in a small customer network and i have the ability to have constant tabs on when hosts are reachable/forwarding/stale i think it would somewhat of a usefull tool to employ temporarily.

This should be placed on a wec collector internal to a siem

This works by first and foremost checking hosts every 60 seconds or whatever time interval you want to make it.

This tool looks at 3 things when "checking" a host

Wec log forwarding
  using cmdlet Get-winevent
      this will measure the time inbetween intervals of logging and will populate a stale/notforwarding depending on the time 



This will also check tcp reachability

Light connection check to a port like
445
5985



And finally an optional ping my main goal with this will be to have constant servallaince instead of finding out something isnt forwarding through detections/activemonitoring
