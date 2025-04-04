oh-my-posh init pwsh | Invoke-Expression
Enable-PoshTransientPrompt Enable-PoshTooltips #ChocolateyProfile $ChocolateyProfile = "$env:ChocolateyInstall\helpers\chocolateyProfile.psm1" if(Test-Path($ChocolateyProfile)) { Import-Module "$ChocolateyProfile" } $env:POSH_GIT_ENABLED = $true clear #remove to see all output Import-Module -Name Terminal-Icons

Import-Module -Name PSReadLine 
Set-PSReadLineOption -PredictionViewStyle ListView 
Set-PSReadLineOption -PredictionSource History 
Set-PSReadLineOption -EditMode Windows 

#Install-Module z
Set-PSReadLineOption -PredictionSource History 
Set-PSReadLineOption -PredictionViewStyle ListView 
Set-PSReadLineOption -EditMode Windows
clear

