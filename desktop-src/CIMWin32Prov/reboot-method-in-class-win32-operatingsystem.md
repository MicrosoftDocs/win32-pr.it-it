---
description: Il riavvio&\# 8194; Il metodo della classe WMI arresta il sistema del computer e quindi lo riavvia.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Metodo reboot della classe Win32_OperatingSystem
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
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966279"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Metodo reboot della \_ classe Win32 OperatingSystem

Il metodo **Riavvia** la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) arresta il sistema del computer e quindi lo riavvia.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Reboot();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per i codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Altro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

La possibilità di riavviare a livello di codice un computer consente agli amministratori di eseguire molte attività di gestione dei computer in modalità remota.

Se, ad esempio, si crea uno script per installare il software o apportare una modifica alla configurazione che richiede il riavvio di un computer, è possibile includere il comando Riavvia nello script ed eseguire l'intera operazione in modalità remota. Il metodo di **riavvio** può essere utilizzato per riavviare un computer. Analogamente al metodo [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) , il metodo **reboot** richiede l'utente le cui credenziali di sicurezza vengono utilizzate dallo script per disporre del privilegio di arresto.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene richiamato il metodo reboot della classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .

> [!Note]  
> È necessario disporre del privilegio shutdown per richiamare correttamente il metodo Shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



Il codice Perl seguente richiama il metodo reboot della classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .

> [!Note]  
> È necessario disporre del privilegio shutdown per richiamare correttamente il metodo Shutdown.

 


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



Il codice VBScript seguente richiama il metodo reboot della classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) in un sistema remoto. Immettere \_ \_ il nome del sistema remoto con il nome del sistema remoto da riavviare.

> [!Note]  
> È necessario avere il privilegio RemoteShutdown per richiamare correttamente il metodo Reboot

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



che segue Perl richiama il metodo di riavvio della classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) in un sistema remoto. Immettere \_ \_ il nome del sistema remoto con il nome del sistema remoto da riavviare.

> [!Note]  
> È necessario disporre del privilegio RemoteShutdown per richiamare correttamente il metodo di riavvio.

 


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
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_OperatingSystem Win32**](win32-operatingsystem.md)
</dt> <dt>

[**CIM \_ OperatingSystem. Shutdown, metodo**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[Attività WMI: gestione desktop](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

