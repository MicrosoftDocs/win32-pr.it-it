---
description: 'Metodo StartService della classe Win32_Service (provider WMI CIMWin32): tenta di inserire il servizio di riferimento nello stato di avvio.'
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: Metodo StartService della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a630b9d926ff5377312f1c67630a20816ab38b6c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086159"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Metodo StartService della classe Win32_Service (provider WMI CIMWin32)

Il **metodo StartService** tenta di inserire il servizio a cui si fa riferimento nello stato di avvio.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

La richiesta è stata accettata.

</dd> <dt>

**1**
</dt> <dd>

La richiesta non è supportata.

</dd> <dt>

**2**
</dt> <dd>

L'utente non dispone dell'accesso necessario.

</dd> <dt>

**3**
</dt> <dd>

Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.

</dd> <dt>

**4**
</dt> <dd>

Il codice di controllo richiesto non è valido o non è accettabile per il servizio.

</dd> <dt>

**5**
</dt> <dd>

Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** ) è uguale a 0, 1 o 2.

</dd> <dt>

**6**
</dt> <dd>

Il servizio non è stato avviato.

</dd> <dt>

**7**
</dt> <dd>

Il servizio non ha risposto in tempo utile alla richiesta di avvio.

</dd> <dt>

**8**
</dt> <dd>

Errore sconosciuto durante l'avvio del servizio.

</dd> <dt>

**9**
</dt> <dd>

Impossibile trovare il percorso della directory del file eseguibile del servizio.

</dd> <dt>

**10**
</dt> <dd>

Il servizio è già in esecuzione.

</dd> <dt>

**11**
</dt> <dd>

Il database a cui aggiungere il nuovo servizio è bloccato.

</dd> <dt>

**12**
</dt> <dd>

Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.

</dd> <dt>

**13**
</dt> <dd>

Impossibile trovare un servizio dipendente necessario.

</dd> <dt>

**14**
</dt> <dd>

Il servizio è stato disabilitato dal sistema.

</dd> <dt>

**15**
</dt> <dd>

Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.

</dd> <dt>

**16**
</dt> <dd>

Questo servizio viene rimosso dal sistema.

</dd> <dt>

**17**
</dt> <dd>

Il servizio non ha thread di esecuzione.

</dd> <dt>

**18**
</dt> <dd>

Il servizio ha dipendenze circolari all'avvio.

</dd> <dt>

**19**
</dt> <dd>

Un servizio è in esecuzione con lo stesso nome.

</dd> <dt>

**20**
</dt> <dd>

Il nome del servizio contiene caratteri non validi.

</dd> <dt>

**21**
</dt> <dd>

Al servizio sono stati passati parametri non validi.

</dd> <dt>

**22**
</dt> <dd>

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.

</dd> <dt>

**23**
</dt> <dd>

Il servizio esiste già nel database dei servizi disponibili dal sistema.

</dd> <dt>

**24**
</dt> <dd>

Il servizio è attualmente sospeso nel sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

Anche se potrebbe sembrare che non vi sia alcuna differenza pratica tra un servizio arrestato e un servizio in pausa, i due stati appaiono in modo diverso rispetto a Gestione controllo servizi. Un servizio arrestato è un servizio che non è in esecuzione e deve eseguire l'intera procedura di avvio del servizio. Un servizio sospeso, tuttavia, è ancora in esecuzione, ma ha avuto il suo funzionamento sospeso. Per questo problema, un servizio sospeso non deve eseguire l'intera procedura di avvio del servizio, ma richiede una procedura diversa per riprendere il funzionamento.

È necessario utilizzare il metodo appropriato per avviare un servizio arrestato o per riprendere un servizio sospeso. I [**metodi \_ startService**](win32-service.md) e [**ResumeService**](resumeservice-method-in-class-win32-service.md) del servizio Win32 devono essere usati nelle situazioni seguenti: 

-   Se un servizio è attualmente arrestato, è necessario usare il **metodo StartService** per riavviarlo. [**ResumeService**](resumeservice-method-in-class-win32-service.md) non può avviare un servizio attualmente arrestato.
-   Se un servizio è in pausa, è necessario usare [**ResumeService**](resumeservice-method-in-class-win32-service.md). Se si usa il **metodo StartService** in un servizio sospeso, viene visualizzato il messaggio "Il servizio è già in esecuzione". Tuttavia, il servizio rimane in pausa fino a quando non viene inviato il codice di controllo del servizio di ripresa.

Se si avvia un servizio arrestato che dipende da un altro servizio, vengono avviati entrambi i servizi. Quando un servizio viene avviato con questo metodo, i servizi dipendenti non vengono avviati automaticamente. È necessario usare la classe di associazione [**Win32 \_ DependentService**](win32-dependentservice.md) e la query [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) per individuare i dipendenti e avviarli separatamente.

## <a name="examples"></a>Esempio

L'esempio di PowerShell [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) abilita il Desktop remoto remoto.

L'esempio di PowerShell [Arresta, Avvia, Abilita](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) o Disabilita servizio avvia, arresta, abilita o disabilita un servizio.

L'esempio di codice VBSScript seguente illustra come avviare un servizio specifico da istanze del [**servizio Win32. \_**](win32-service.md)


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



Nell'esempio di codice Perl seguente viene illustrato come avviare un servizio specifico da istanze del [**servizio Win32. \_**](win32-service.md)


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if(!$@ && defined $ServiceSet)
{
 foreach my $service (in $ServiceSet)
 {
  my $Result = $service->StartService();
  if ($Result == 0) 
  {
   print "\nService started\n";
  }
  elsif ($Result == 10)
  {
   print "\nService already running\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



L'esempio di codice VBScript seguente, NetDDE, dipende dal servizio NetDDEDSDM. Lo script individua la classe da cui dipende NetDDE e lo avvia, che non avvia automaticamente NetDDE.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Stop NetDDE if it is running
Set objNetDDEService = objWMIService.Get("Win32_Service.Name='NetDDE'")
Return = objNetDDEService.StopService()

' NetDDE is in the dependent role to another service
Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " & "AssocClass=Win32_DependentService " & "Role=Dependent" )

' start the service on which NetDDE is dependent
For Each objService in colServiceList
    WScript.Echo "Starting " & objService.Name
    Return = objService.StartService()
    If Return = 0 Then
        WScript.Echo "Parent service " & objService.Name & " started successfully"
    Else
        WScript.Echo "Parent service " & objService.Name & " did not start. Return = " & Return
    End If
Next

' NetDDE is still stopped
Set objNetDDEService = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")
WScript.Echo "Dependent NetDDE service is " & objNetDDEService.State
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

[**Servizio \_ Win32**](win32-service.md)
</dt> <dt>

[Attività WMI: Servizi](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

