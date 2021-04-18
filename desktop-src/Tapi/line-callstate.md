---
description: Il messaggio della linea TAPI \_ CALLSTATE viene inviato quando lo stato della chiamata specificata viene modificato.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: Messaggio di LINE_CALLSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327500"
---
# <a name="line_callstate-message"></a>\_Messaggio linea CALLSTATE

Il messaggio della **linea TAPI \_ CALLSTATE** viene inviato quando lo stato della chiamata specificata viene modificato. In genere, molti di questi messaggi vengono ricevuti durante la durata di una chiamata. Le applicazioni ricevono notifiche relative a nuove chiamate in ingresso con questo messaggio. la nuova chiamata è nello stato dell' *offerta* . L'applicazione può utilizzare [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) per recuperare informazioni più dettagliate sullo stato corrente della chiamata.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle della chiamata.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Nuovo stato della chiamata. Questo parametro deve essere una sola delle seguenti [**\_ costanti LINECALLSTATE**](linecallstate--constants.md).



| dwParam1                                                                                                                                                                                             | Significato                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <dt>**LINECALLSTATE \_ occupato**</dt> </dl>                         | *dwParam2* contiene informazioni dettagliate sulla modalità di occupato. Questo parametro usa una delle [**\_ costanti LINEBUSYMODE**](linebusymode--constants.md).<br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <dt>**LINECALLSTATE \_ connesso**</dt> </dl>          | *dwParam2* contiene informazioni dettagliate sulla modalità connessa. Questo parametro usa una delle [**\_ costanti LINECONNECTEDMODE**](lineconnectedmode--constants.md).<br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <dt>**LINECALLSTATE \_ DIaltone**</dt> </dl>             | *dwParam2* contiene informazioni dettagliate sulla modalità di composizione del segnale. Questo parametro usa una delle [**\_ costanti LINEDIALTONEMODE**](linedialtonemode--constants.md).<br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <dt>**\_offerta LINECALLSTATE**</dt> </dl>             | *dwParam2* contiene informazioni dettagliate sulla modalità connessa. Questo parametro usa una delle [**\_ costanti LINEOFFERINGMODE**](lineofferingmode--constants.md).<br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <dt>**\_SPECIALINFO LINECALLSTATE**</dt> </dl>    | *dwParam2* contiene i dettagli sulla modalità di informazione speciale. Questo parametro usa una delle [**\_ costanti LINESPECIALINFO**](linespecialinfo--constants.md).<br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <dt>**LINECALLSTATE \_ disconnesso**</dt> </dl> | *dwParam2* contiene informazioni dettagliate sulla modalità di disconnessione. Questo parametro usa una delle [**\_ costanti LINEDISCONNECTMODE**](linedisconnectmode--constants.md).<br/>        |



 

</dd> <dt>

*dwParam2* 
</dt> <dd>

Informazioni dipendenti dallo stato della chiamata. Vedere *dwParam1*.

> [!Note]  
> Nei casi in cui è appropriata una risposta *ritardata* , usare LINEDISCONNECTMODE \_ TEMPFAILURE. Quando una risposta *Blocklisting* è appropriata, usare LINEDISCONNECT \_ bloccato. Per ulteriori informazioni, vedere [**\_ costanti LINEDISCONNECTMODE**](linedisconnectmode--constants.md).

 

Se *dwParam1* è LINECALLSTATE \_ conferenced, *DwParam2* contiene il parametro *hConfCall* della chiamata padre della conferenza di cui l'oggetto *hCall* è membro. Se la chiamata specificata in *dwParam2* non è stata precedentemente considerata come chiamata di conferenza padre da parte dell'applicazione (*hConfCall*, l'applicazione deve eseguire questa operazione in seguito a questo messaggio. Se l'applicazione non dispone di un handle per la chiamata padre della conferenza (perché in precedenza è stato chiamato [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) su tale handle) *dwParam2* è impostato su **null**.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se è zero, questo parametro indica che non sono state apportate modifiche al privilegio dell'applicazione per la chiamata.

Se diverso da zero, specifica il privilegio dell'applicazione per la chiamata. Questo problema si verifica nelle situazioni seguenti: (1) la prima volta che all'applicazione viene assegnato un handle per la chiamata; (2) quando l'applicazione è la destinazione di una chiamata uniforme (anche se l'applicazione è già un proprietario della chiamata). Questo parametro usa una delle [**\_ costanti LINECALLPRIVILEGE**](linecallprivilege--constants.md)seguenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato a qualsiasi applicazione che dispone di un handle per la chiamata. Il messaggio di **riga \_ CALLSTATE** notifica anche alle applicazioni che monitorano le chiamate su una riga sull'esistenza e sullo stato delle chiamate in uscita stabilite da altre applicazioni o manualmente dall'utente (ad esempio, in un dispositivo telefonico collegato). Lo stato di chiamata di tali chiamate riflette lo stato effettivo della chiamata, che non *offre*. Esaminando lo stato della chiamata, l'applicazione è in grado di determinare se la chiamata è una chiamata in ingresso a cui è necessario rispondere o meno.

Un **messaggio \_ CALLSTATE di riga** con uno stato di chiamata sconosciuto può essere inviato a un'applicazione di monitoraggio come risultato di un [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), lineUnpark [**, lineSetupTransfer, linePickup**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer) [**,**](/windows/desktop/api/Tapi/nf-tapi-linepickup) [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)o [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) completato che è stato richiesto da un'altra applicazione. [](/windows/desktop/api/Tapi/nf-tapi-lineunpark) Nel momento in cui l'applicazione richiedente riceve una risposta di [**riga \_**](line-reply.md) (operazione riuscita) per l'operazione richiesta, tutte le applicazioni di monitoraggio sulla riga riceveranno il messaggio di **riga \_ CALLSTATE** (sconosciuto). Un messaggio di **riga \_ CALLSTATE** che indica lo stato di chiamata "reale" della chiamata appena generata viene inviato (usando le informazioni fornite dal provider di servizi) per le applicazioni che eseguono la richiesta e il monitoraggio subito dopo.

Un messaggio di **riga \_ CALLSTATE** (sconosciuto) viene inviato al monitoraggio delle applicazioni solo se [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) causa la risoluzione delle chiamate in una conferenza a tre vie.

Per compatibilità con le versioni precedenti, le applicazioni meno recenti non sono in attesa di un valore specifico in *dwParam2* di un \_ messaggio di conferenza LINECALLSTATE. TAPI passa quindi la chiamata padre *hConfCall* in *dwParam2* indipendentemente dalla versione API dell'applicazione che riceve il messaggio. Nel caso di una chiamata di conferenza iniziata dal provider di servizi, l'applicazione precedente non è consapevole che la chiamata padre è diventata una chiamata di conferenza a meno che non si verifichino spontaneamente altre informazioni (ad esempio, chiamare [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).

Questo messaggio non può essere disabilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_risposta riga**](line-reply.md)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




