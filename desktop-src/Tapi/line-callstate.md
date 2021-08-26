---
description: Il messaggio CALLSTATE TAPI LINE \_ viene inviato quando lo stato della chiamata specificata viene modificato.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: LINE_CALLSTATE messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d82dfb5f0d5e306085ecd2d7f29270d19c2c9c101e30ac547fe246b7e6fddb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012571"
---
# <a name="line_callstate-message"></a>LINE \_ CALLSTATE message

Il messaggio **\_ CALLSTATE TAPI LINE** viene inviato quando lo stato della chiamata specificata viene modificato. In genere, durante la durata di una chiamata vengono ricevuti diversi messaggi di questo tipo. Le applicazioni vengono notificate alle nuove chiamate in ingresso con questo messaggio. La nuova chiamata si trova nello *stato dell'offerta.* L'applicazione può [**usare lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) per recuperare informazioni più dettagliate sullo stato corrente della chiamata.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per la chiamata.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Nuovo stato della chiamata. Questo parametro deve essere una sola delle costanti [**LINECALLSTATE \_ seguenti.**](linecallstate--constants.md)



| dwParam1                                                                                                                                                                                             | Significato                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <dt>**LINECALLSTATE \_ BUSY**</dt> </dl>                         | *dwParam2* contiene informazioni dettagliate sulla modalità occupato. Questo parametro usa una delle [**costanti LINEBUSYMODE \_**](linebusymode--constants.md).<br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <dt>**LINECALLSTATE \_ CONNESSO**</dt> </dl>          | *dwParam2* contiene informazioni dettagliate sulla modalità connessa. Questo parametro usa una delle [**costanti LINECONNECTEDMODE \_**](lineconnectedmode--constants.md).<br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <dt>**LINECALLSTATE \_ DIALTONE**</dt> </dl>             | *dwParam2 contiene* informazioni dettagliate sulla modalità del tono di composizione. Questo parametro usa una delle [**costanti \_ LINEDIAGNOEMODE**](linedialtonemode--constants.md).<br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <dt>**OFFERTA \_ LINECALLSTATE**</dt> </dl>             | *dwParam2* contiene informazioni dettagliate sulla modalità connessa. Questo parametro usa una delle [**costanti \_ LINEOFFERINGMODE**](lineofferingmode--constants.md).<br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <dt>**LINECALLSTATE \_ SPECIALINFO**</dt> </dl>    | *dwParam2* contiene i dettagli sulla modalità informazioni speciali. Questo parametro usa una delle [**costanti LINESPECIALINFO \_**](linespecialinfo--constants.md).<br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <dt>**LINECALLSTATE \_ DISCONNESSO**</dt> </dl> | *dwParam2 contiene* informazioni dettagliate sulla modalità di disconnessione. Questo parametro usa una delle [**costanti LINEDISCONNECTMODE \_**](linedisconnectmode--constants.md).<br/>        |



 

</dd> <dt>

*dwParam2* 
</dt> <dd>

Informazioni dipendenti dallo stato di chiamata. Vedere *dwParam1*.

> [!Note]  
> Nei casi in cui è *appropriata una risposta ritardata,* usare LINEDISCONNECTMODE \_ TEMPFAILURE. Se è *appropriata una risposta in* elenco di blocco, usare LINEDISCONNECT \_ BLOCKED. Per altre informazioni, vedere [**Costanti LINEDISCONNECTMODE. \_**](linedisconnectmode--constants.md)

 

Se *dwParam1* è LINECALLSTATE \_ CONFERENCED, *dwParam2* contiene il parametro *hConfCall* della chiamata padre della conferenza di cui *l'oggetto hCall* è membro. Se la chiamata specificata in *dwParam2* non è stata considerata in precedenza dall'applicazione come una conferenza telefonica padre (*hConfCall*, l'applicazione deve eseguire questa operazione come risultato di questo messaggio. Se l'applicazione non dispone di un handle per la chiamata padre della conferenza (perché in precedenza ha chiamato [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) su tale handle) *dwParam2* è impostato su **NULL.**

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se zero, questo parametro indica che non è stata apportata alcuna modifica al privilegio dell'applicazione per la chiamata.

Se diverso da zero, specifica il privilegio dell'applicazione per la chiamata. Ciò si verifica nelle situazioni seguenti: (1) La prima volta che all'applicazione viene assegnato un handle a questa chiamata; (2) Quando l'applicazione è la destinazione di un handoff di chiamata (anche se l'applicazione era già un proprietario della chiamata). Questo parametro usa una delle costanti [**LINECALLPRIVILEGE \_ seguenti.**](linecallprivilege--constants.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato a qualsiasi applicazione che dispone di un handle per la chiamata. Il **messaggio LINE \_ CALLSTATE** invia inoltre una notifica alle applicazioni che monitorano le chiamate su una riga sull'esistenza e sullo stato delle chiamate in uscita stabilite da altre applicazioni o manualmente dall'utente(ad esempio, in un dispositivo telefonico collegato). Lo stato di chiamata di tali chiamate riflette lo stato effettivo della chiamata, che non *offre*. Esaminando lo stato della chiamata, l'applicazione può determinare se la chiamata è una chiamata in ingresso a cui è necessario rispondere o meno.

Un messaggio **LINE \_ CALLSTATE** con stato di chiamata sconosciuto può essere inviato a un'applicazione di monitoraggio come risultato di [**un'operazione lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**lineUnpark,**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) [**lineSetupTransfer,**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer) [**linePickup,**](/windows/desktop/api/Tapi/nf-tapi-linepickup) [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)o [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) richiesta da un'altra applicazione. Quando all'applicazione richiedente viene inviata una risposta [**LINE \_ REPLY**](line-reply.md) (operazione riuscita) per l'operazione richiesta, a tutte le applicazioni di monitoraggio nella riga viene inviato il messaggio **LINE \_ CALLSTATE** (sconosciuto). Poco dopo viene inviato un messaggio **LINE \_ CALLSTATE** che indica lo stato di chiamata "reale" della chiamata appena generata (usando le informazioni fornite dal provider di servizi) alle applicazioni richiedenti e di monitoraggio.

Un **messaggio LINE \_ CALLSTATE** (sconosciuto) viene inviato alle applicazioni di monitoraggio solo se [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) causa la risoluzione delle chiamate in una conferenza a tre.

Per la compatibilità con le versioni precedenti, le applicazioni meno recenti non prevedono alcun valore specifico in *dwParam2* di un messaggio LINECALLSTATE \_ CONFERENCED. TAPI passa quindi la chiamata *padre hConfCall* in *dwParam2* indipendentemente dalla versione API dell'applicazione che riceve il messaggio. Nel caso di una conferenza telefonica avviata dal provider di servizi, l'applicazione meno recente non è a conoscenza del fatto che la chiamata padre è diventata una conferenza telefonica, a meno che non si sia verificata un'analisi sconsciata di altre informazioni (ad esempio, [**chiamare lineGetConfRelatedCalls).**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)

Questo messaggio non può essere disabilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ REPLY**](line-reply.md)
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

 

 




