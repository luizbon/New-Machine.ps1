Got that new machine smell? Run this:

    if (([Security.Principal.WindowsPrincipal][Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] "Administrator")) { Set-ExecutionPolicy RemoteSigned; iex ((new-object net.webclient).DownloadString('https://raw.githubusercontent.com/tathamoddie/New-Machine.ps1/master/New-Machine.ps1')); } else { throw "You need to run this from an elevated PS prompt" }

You trust me, right?
