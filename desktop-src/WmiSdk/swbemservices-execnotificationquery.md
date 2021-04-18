---
description: Esegue una query per la ricezione di eventi. La chiamata restituisce immediatamente un risultato.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: Metodo SWbemServices.ExecNotificationQuery (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313164"
---
# <a name="swbemservicesexecnotificationquery-method"></a>Metodo cNotificationQuery SWbemServices.Exe

Il metodo **ExecNotificationQuery** dell'oggetto [**SWbemServices**](swbemservices.md) esegue una query per la ricezione di eventi. La chiamata restituisce immediatamente un risultato. L'utente può eseguire il polling dell'enumeratore restituito per gli eventi man mano che arrivano.

Il metodo viene chiamato in modalità semisincrono. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strQuery* 
</dt> <dd>

Obbligatorio. Stringa che contiene il testo della query correlata agli eventi. Questo parametro non può essere vuoto. Per ulteriori informazioni sulla creazione di stringhe di query WMI, vedere [esecuzione di query con WQL](querying-with-wql.md) e informazioni di riferimento su [WQL](wql-sql-for-wmi.md) .

</dd> <dt>

*strQueryLanguage* \[ opzionale\]
</dt> <dd>

Stringa che contiene il linguaggio di query da utilizzare. Se specificato, questo valore deve essere "WQL".

</dd> <dt>

*iFlags* \[ opzionale\]
</dt> <dd>

Si tratta di un numero intero che determina il comportamento della query. Il valore predefinito è **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**. Se si specifica questo parametro, questo parametro deve essere impostato sia su **wbemFlagReturnImmediately** che su **wbemFlagForwardOnly** oppure la chiamata ha esito negativo. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Causa la restituzione di un enumeratore di sola trasmissione. Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Causa la restituzione immediata della chiamata.

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ opzionale\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non si verificano errori, questo metodo restituisce un oggetto [**SWbemEventSource**](swbemeventsource.md) . È possibile chiamare il metodo [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) per recuperare gli eventi man mano che arrivano.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **ExecNotificationQuery** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non è autorizzato a visualizzare il set di risultati.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017)
</dt> <dd>

Sintassi di query non valida.

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018)
</dt> <dd>

Il linguaggio della query richiesta non è supportato.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

A differenza del metodo [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) , **ExecNotificationQuery** restituisce gli oggetti del tipo di evento generati da eventi futuri anziché da oggetti esistenti. Gli oggetti evento che **ExecNotificationQuery** le richieste possono essere intrinseci, ad esempio [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), o estrinseci, ad esempio eventi del provider del registro di sistema come gli eventi [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) o SNMP. Per ulteriori informazioni, vedere [determinazione del tipo di evento per la ricezione e la ricezione di notifiche degli](determining-the-type-of-event-to-receive.md) [eventi](receiving-event-notifications.md).

Esistono limiti al numero di parole chiave **and** e **or** che possono essere utilizzate nelle query WQL. Un numero elevato di parole chiave WQL utilizzate in una query complessa può causare la restituzione del codice di errore di **\_ \_ \_ violazione della quota E di WBEM** come valore **HRESULT** . Il limite di parole chiave WQL dipende dalla complessità della query.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente vengono monitorate le modifiche apportate ai volumi in un computer locale. Si noti che [**Win32 \_ VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) è un evento estrinseco definito da un provider e non da un evento intrinseco WMI definito. Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



Nell'esempio di codice VBScript riportato di seguito viene monitorata l'eliminazione del processo. Se si elimina un processo in Gestione attività o si chiude un'applicazione, lo script Visualizza un messaggio. Si noti che questo script esegue una query su un evento intrinseco definito da WMI- [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMSERVICES IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md)
</dt> <dt>

[**SWbemServices.ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[Ricezione di un evento WMI](receiving-a-wmi-event.md)
</dt> <dt>

[Esecuzione di query con WQL](querying-with-wql.md)
</dt> <dt>

[WQL (SQL per WMI)](wql-sql-for-wmi.md)
</dt> <dt>

[Determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

