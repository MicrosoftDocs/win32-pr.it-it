---
description: Tenta di collocare il servizio a cui si fa riferimento nello stato resumed.
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: Metodo ResumeService della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ed4141b02d6e08bd4b106d2c1f72ce3fe0620fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878314"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Metodo ResumeService della classe Win32_Service (provider WMI CIMWin32)

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tenta di collocare il servizio a cui si fa riferimento nello stato resumed.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ResumeService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

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

Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.

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

Impossibile trovare il percorso di directory del file eseguibile del servizio.

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

Questo servizio verrà rimosso dal sistema.

</dd> <dt>

**17**
</dt> <dd>

Il servizio non dispone di un thread di esecuzione.

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

Sono stati passati parametri non validi al servizio.

</dd> <dt>

**22**
</dt> <dd>

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.

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

Sebbene sia possibile che non esistano differenze pratiche tra un servizio interrotto e un servizio sospeso, i due stati vengono visualizzati in modo diverso rispetto a SCM. Un servizio interrotto è un servizio che non è in esecuzione e che deve seguire l'intera procedura di avvio del servizio. Un servizio sospeso, tuttavia, è ancora in esecuzione, ma il suo funzionamento è stato sospeso. Per questo motivo, non è necessario che un servizio sospeso attraversi l'intera procedura di avvio del servizio, ma è necessaria una procedura diversa per riprendere il funzionamento.

È necessario utilizzare il metodo appropriato per avviare un servizio che è stato interrotto o per riprendere un servizio che è stato sospeso. I metodi del [**\_ servizio Win32**](win32-service.md) [**StartService**](startservice-method-in-class-win32-service.md) e **ResumeService** devono essere utilizzati nelle situazioni seguenti:

-   Se un servizio è attualmente arrestato, è necessario usare il metodo [**StartService**](startservice-method-in-class-win32-service.md) per riavviarlo; **ResumeService** non è in grado di avviare un servizio attualmente arrestato.
-   Se un servizio viene sospeso, è necessario utilizzare **ResumeService**. Se si usa il metodo [**StartService**](startservice-method-in-class-win32-service.md) in un servizio in pausa, viene visualizzato il messaggio "il servizio è già in esecuzione". Tuttavia, il servizio rimane sospeso fino a quando non viene inviato il codice di controllo del servizio di ripresa.

## <a name="examples"></a>Esempio

L'esempio [Resume avvio automatico dei servizi che sono in pausa](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript riavvia tutti i servizi di avvio automatico sospesi.

Nell'esempio di codice VBScript seguente viene descritto come riprendere un servizio sospeso dalle istanze del [**\_ servizio Win32**](win32-service.md).

> [!Note]  
> Il servizio deve supportare la sospensione ed essere già in esecuzione.

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



Nell'esempio di codice Perl seguente viene descritto come riprendere un servizio sospeso dalle istanze del [**\_ servizio Win32**](win32-service.md).

> [!Note]  
> Il servizio deve supportare la sospensione ed essere già in esecuzione.

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
    }
   }
  }
  else
  {
   print "\nService does not support pause\n";
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
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Servizio Win32**](win32-service.md)
</dt> <dt>

[Attività WMI: Servizi](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

