---
description: Arresto del&\# 8194; Il metodo della classe WMI scarica programmi e DLL finché non è sicuro spegnere il computer.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Metodo Shutdown della classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 068551ee013634bde9a42584764c36f255bf322bedb97e6ebb3a5075c113e742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800841"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a>Metodo Shutdown della classe OperatingSystem Win32 \_

Il **metodo della** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) Shutdown scarica programmi e DLL fino a quando non è sicuro spegnere il computer.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Shutdown();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per i codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Altro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

I computer talvolta devono essere rimossi dalla rete, ad esempio per la manutenzione pianificata, perché il computer non funziona correttamente o per completare un processo di configurazione. Ad esempio, se un server DHCP sta inviare indirizzi IP erro, potrebbe essere necessario arrestare il computer fino a quando non sarà possibile inviare un tecnico del servizio per risolvere il problema. Se si sospetta che si sia verificata una violazione della sicurezza, potrebbe essere necessario arrestare alcuni server per assicurarsi che non sia possibile accedervi fino a quando il problema di sicurezza non è stato risolto. Alcune operazioni di configurazione, ad esempio la modifica del nome di un computer, richiedono il riavvio del computer prima che la modifica venga attivata.

Questo metodo arresta immediatamente il computer, se possibile. Il sistema arresta tutti i processi in esecuzione, scarica tutti i buffer di file sul disco e quindi arresta il sistema. Il processo chiamante deve avere **il edizione Standard \_ SHUTDOWN \_ NAME,** come descritto nell'esempio seguente.


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



Per altre informazioni sull'impostazione di un privilegio, vedere [Esecuzione di operazioni con](/windows/desktop/WmiSdk/executing-privileged-operations) privilegi ed Esecuzione di operazioni con privilegi tramite [VBScript.](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript) Per altre opzioni di arresto, ad esempio una disconnessione o un arresto forzato, vedi il [**metodo Win32Shutdown.**](win32shutdown-method-in-class-win32-operatingsystem.md)

## <a name="examples"></a>Esempio

Il codice VBScript seguente arresta il computer locale.

> [!Note]  
> Per richiamare correttamente il metodo Shutdown, è necessario disporre del privilegio Shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



Il codice Perl seguente arresta il computer locale.

> [!Note]  
> Per richiamare correttamente il metodo Shutdown, è necessario disporre del privilegio Shutdown.

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
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



Il codice VBScript seguente arresta il computer remoto specificato. Compilare *REMOTE SYSTEM NAME \_ \_ con* il nome del sistema remoto da arrestare.

> [!Note]  
> Per richiamare correttamente il metodo **Shutdown,** è necessario disporre del privilegio RemoteShutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
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

[Attività WMI: Gestione desktop](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[Esecuzione di operazioni con privilegi tramite VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

