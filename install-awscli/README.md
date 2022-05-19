## Instalación y Configuración de AWSCLI Python
# NECESARIO
1. Usuario administrador local (para instalacion de todos los usuarios)

### Cambiar a user ansible
```
$cred = Get-Credential -UserName 'ansible' -Message ' '
Start-Process Powershell.exe -Credential $cred `
  -ArgumentList '-noprofile -command &{Start-Process Powershell -verb runas}'
```

### Refrescar sesion 
```
 $env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path","User")
 ```

 ### Lanzar Playbooks
 ```
 ansible-playbook playbook.yml -i inventory
 ```