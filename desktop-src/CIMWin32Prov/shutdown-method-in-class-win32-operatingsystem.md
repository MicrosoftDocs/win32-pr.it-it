---
description: L'arresto&\# 8194; Il metodo della classe WMI Scarica i programmi e le dll fino a quando non è sicuro disattivare il computer.
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
ms.openlocfilehash: af80442087a0498849388f0da10946b08e282712
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483965"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a>Metodo Shutdown della classe Win32 \_ OperatingSystem

Il metodo **Shutdown** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) Scarica i programmi e le dll fino a quando non è sicuro disattivare il computer.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Shutdown();
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

Occasionalmente, i computer devono essere rimossi dalla rete, ad esempio per la manutenzione pianificata, perché il computer non funziona correttamente o per completare un processo di configurazione. Se, ad esempio, un server DHCP distribuisce indirizzi IP errati, potrebbe essere necessario arrestare il computer fino a quando non è possibile inviare un tecnico del servizio per risolvere il problema. Se si ritiene che si sia verificata una violazione della sicurezza, potrebbe essere necessario arrestare determinati server per assicurarsi che non sia possibile accedervi fino a quando il problema di sicurezza non è stato risolto. Per alcune operazioni di configurazione, ad esempio la modifica del nome di un computer, è necessario riavviare il computer prima che la modifica abbia effetto.

Questo metodo arresta immediatamente il computer, se possibile. Il sistema arresta tutti i processi in esecuzione, Scarica tutti i buffer di file sul disco e quindi spegne il sistema. Il processo chiamante deve avere il privilegio **se \_ Shutdown \_ Name** , come descritto nell'esempio seguente.


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



Per ulteriori informazioni sull'impostazione di un privilegio, vedere [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations) ed esecuzione di [operazioni con privilegi tramite VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript). Per altre opzioni di arresto, ad esempio una disconnessione o un arresto forzato, vedere il metodo [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) .

## <a name="examples"></a>Esempio

Il codice VBScript seguente arresta il computer locale.

> [!Note]  
> È necessario disporre del privilegio shutdown per richiamare correttamente il metodo Shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



Il codice Perl seguente arresta il computer locale.

> [!Note]  
> È necessario disporre del privilegio shutdown per richiamare correttamente il metodo Shutdown.

 


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



Il codice VBScript seguente arresta il computer remoto specificato. Immettere il *\_ \_ nome del sistema remoto* con il nome del sistema remoto da arrestare.

> [!Note]  
> Per richiamare correttamente il metodo **Shutdown** , è necessario avere il privilegio RemoteShutdown.

 


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
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_OperatingSystem Win32**](win32-operatingsystem.md)
</dt> <dt>

[Attività WMI: gestione desktop](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[Esecuzione di operazioni con privilegi tramite VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

