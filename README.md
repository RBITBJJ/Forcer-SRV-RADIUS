# Forcer-SRV-RADIUS
Win+R
Gpedit.msc ctrl+shift+enter
Modele d'administration
Système 
Device guard
Desactiver les deux éléments 

# Désactiver "Déployer le contrôle d'application Windows Defender"
Set-ItemProperty -Path "HKLM:\SOFTWARE\Policies\Microsoft\Windows Defender\Device Guard" -Name "EnableApplicationControl" -Value 0 -Force

# Désactiver "Activer la sécurité basée sur la virtualisation"
Set-ItemProperty -Path "HKLM:\SOFTWARE\Policies\Microsoft\Windows Defender\Device Guard" -Name "EnableVirtualizationBasedSecurity" -Value 0 -Force

# Appliquer la mise à jour de la stratégie de groupe
gpupdate /force
