---
description: Il riavvio&\# 8194; Il metodo della classe WMI arresta il sistema del computer e lo riavvia.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Metodo Reboot della classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 700d497650e8950c72467bbad8e11cf450b2302f0b68ef762e8a11e3c6aaceee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752731"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Metodo Reboot della classe OperatingSystem Win32 \_

Il **metodo reboot** della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) arresta il sistema del computer e lo riavvia.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Reboot();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per i codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Altro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

La possibilità di riavviare un computer a livello di codice consente agli amministratori di eseguire molte attività di gestione dei computer in modalità remota.

Ad esempio, se si crea uno script per installare software o apportare una modifica di configurazione che richiede il riavvio di un computer, è possibile includere il comando restart nello script ed eseguire l'intera operazione in modalità remota. Il **metodo Reboot** può essere usato per riavviare un computer. Analogamente al [**metodo Win32Shutdown,**](win32shutdown-method-in-class-win32-operatingsystem.md) il metodo **Reboot** richiede all'utente le cui credenziali di sicurezza vengono usate dallo script di disporre del privilegio Shutdown.

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente richiama il metodo Reboot della [**classe \_ OperatingSystem Win32.**](win32-operatingsystem.md)

> [!Note]  
> Per richiamare correttamente il metodo Shutdown, è necessario disporre del privilegio Shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



Il codice Perl seguente richiama il metodo Reboot della [**classe \_ OperatingSystem Win32.**](win32-operatingsystem.md)

> [!Note]  
> Per richiamare correttamente il metodo Shutdown, è necessario disporre del privilegio Shutdown.

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
  if (!defined $RetVal || $RetVal != 0)
  {
   print Win32::OLE->LastError, "\n"; 
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



Il codice VBScript seguente richiama il metodo Reboot della [**classe \_ OperatingSystem Win32**](win32-operatingsystem.md) in un sistema remoto. Compilare REMOTE \_ SYSTEM NAME con il nome del sistema remoto da \_ riavviare.

> [!Note]  
> Per richiamare correttamente il metodo Reboot, è necessario disporre del privilegio RemoteShutdown

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



segue Perl richiama il metodo Reboot della [**classe \_ OperatingSystem Win32**](win32-operatingsystem.md) in un sistema remoto. Compilare REMOTE \_ SYSTEM NAME con il nome del sistema remoto da \_ riavviare.

> [!Note]  
> Per richiamare correttamente il metodo Reboot, è necessario disporre del privilegio RemoteShutdown.

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Sistema operativo \_ Win32**](win32-operatingsystem.md)
</dt> <dt>

[**Metodo CIM \_ OperatingSystem.Shutdown**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[Attività WMI: Gestione desktop](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

