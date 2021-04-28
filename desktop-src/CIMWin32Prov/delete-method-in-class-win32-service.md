---
description: Metodo Delete della classe Win32_Service (provider WMI CIMWin32) - Eliminazione&\# 8194; Il metodo della classe WMI elimina un servizio esistente.
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4031184e23e99fc54237ed0b0b4196fe6c075c5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089579"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Metodo Delete della classe Win32_Service (provider WMI CIMWin32)

Il **metodo** [Elimina classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) elimina un servizio esistente.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

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

L'utente non aveva l'accesso necessario.

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

Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**State)** è uguale a 0, 1 o 2.

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

Il servizio presenta dipendenze circolari all'avvio.

</dd> <dt>

**19**
</dt> <dd>

Un servizio viene eseguito con lo stesso nome.

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

Quando l'organizzazione cambia, è possibile decidere di rimuovere determinati servizi da determinati computer. I servizi all'interno e di terze parti possono essere rimossi tramite WMI, mentre i servizi del sistema operativo possono essere rimossi usando Sysocmgr.exe.

Quando si prepara la rimozione dei servizi, tenere presenti le informazioni seguenti:

-   I servizi devono essere arrestati prima di rimuoverli. Se il servizio è in esecuzione quando si esegue il comando delete, il servizio viene contrassegnato per l'eliminazione, ma continua a essere eseguito fino all'arresto e alla chiusura di tutti gli handle aperti.

    Se il servizio non viene mai arrestato, tale servizio non verrà mai eliminato.

-   La rimozione di un servizio non rimuove il file eseguibile del servizio.

    La rimozione di un servizio tramite WMI elimina le voci del Registro di sistema correlate in HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ \\ CurrentControlSet Services. Di conseguenza, il servizio non è più installato e non è disponibile tramite lo snap-in Servizi. TUTTAVIA, WMI non elimina il file eseguibile, pertanto è possibile reinstallare facilmente il servizio. Per eliminare il file eseguibile, è necessario recuperare il nome del percorso e quindi eliminare il file.

-   La rimozione di un servizio windows 2000 di base (ad esempio DHCP) tramite WMI elimina le voci del Registro di sistema per tale servizio, ma non rimuove il collegamento dal menu Strumenti di amministrazione o rimuove il servizio dall'Aggiunta guidata componenti di Windows. Ciò può confondere chiunque stia tentando di determinare come è stato configurato il computer.

    Ad esempio, se si rimuove il servizio DHCP tramite uno script WMI, il servizio DHCP non è più elencato nello snap-in Servizi. Tuttavia, un collegamento non funzionante alla console DHCP rimane nel menu Strumenti di amministrazione e, se si avvia la Creazione guidata componenti di Windows, indica che il servizio DHCP è installato.

    Per questo problema, è consigliabile usare sempre Sysocmgr.exe per rimuovere i servizi di Windows 2000 a livello di codice.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene descritto come eliminare un servizio.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



L'esempio di codice Perl seguente descrive come eliminare un servizio.


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
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

[**Servizio \_ Win32**](win32-service.md)
</dt> <dt>

[Attività WMI: Servizi](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

