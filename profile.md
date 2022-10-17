oh-my-posh init pwsh --config 'https://raw.githubusercontent.com/tobiashungwe/my-custom-posh-theme/9a3b0c8f77263ea2882f7499566eeac0c95cad14/Theme/tobiashungwe.omp.json' | Invoke-Expression

Enable-PoshTransientPrompt
Enable-PoshTooltips
#ChocolateyProfile
$ChocolateyProfile = "$env:ChocolateyInstall\helpers\chocolateyProfile.psm1"
if(Test-Path($ChocolateyProfile))
{
    Import-Module "$ChocolateyProfile"
}
$env:POSH_GIT_ENABLED = $true

Import-Module -Name Terminal-Icons

Import-Module -Name PSReadLine
Set-PSReadLineOption -PredictionViewStyle ListView
Set-PSReadLineOption -PredictionSource History
Set-PSReadLineOption -EditMode Windows

Install-Module z -AllowClobber


