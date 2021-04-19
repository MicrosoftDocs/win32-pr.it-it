---
description: Le \_ costanti del flag di bit LINEADDRESSSTATE descrivono diversi elementi di stato dell'indirizzo.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: Costanti LINEADDRESSSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332916"
---
# <a name="lineaddressstate_-constants"></a>\_Costanti LINEADDRESSSTATE

Le costanti del flag di bit **LINEADDRESSSTATE \_** descrivono diversi elementi di stato dell'indirizzo.

<dl> <dt>

<span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**\_CAPSCHANGE LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



Indica che, a causa delle modifiche di configurazione apportate dall'utente o altre circostanze, uno o più membri della struttura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) per l'indirizzo sono stati modificati. Per leggere la struttura aggiornata, l'applicazione deve usare [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) . Se un provider di servizi invia un messaggio di [**riga \_ ADDRESSSTATE**](line-addressstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni che hanno negoziato la versione di TAPI 1,4 o versioni successive. le applicazioni che trattano una versione precedente dell'API riceveranno i messaggi di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) specificando LINEDEVSTATE \_ reinit, richiedendo di arrestare e reinizializzare la connessione a TAPI per ottenere le informazioni aggiornate.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**\_DEVSPECIFIC LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



L'elemento specifico del dispositivo dello stato dell'indirizzo è stato modificato.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE \_ in futuro**
</dt> <dd> <dl> <dt>



Lo stato di avanzamento dell'indirizzo è stato modificato, incluso probabilmente il numero di anelli per determinare una condizione di nessuna risposta. L'applicazione deve controllare lo stato dell'indirizzo per determinare i dettagli relativi allo stato di avanzamento corrente dell'indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**\_INUSEMANY LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



L'indirizzo monitorato o con bridging è stato modificato in modo da essere utilizzato da una stazione per essere utilizzato da più di una stazione.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**\_INUSEONE LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



L'indirizzo è stato modificato da inattivo o utilizzato da molte stazioni con Bridge per essere utilizzato da una sola stazione.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**\_INUSEZERO LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



L'indirizzo è stato modificato in inattivo (non è utilizzato da alcuna stazione).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**\_NUMCALLS LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



Il numero di chiamate sull'indirizzo è stato modificato. Questo è il risultato di eventi quali una nuova chiamata in ingresso, una chiamata in uscita sull'indirizzo o una chiamata che modifica lo stato di attesa. Questo flag copre le modifiche apportate ai membri **dwNumActiveCalls**, **dwNumOnHoldCalls** e **dwNumOnHoldPendingCalls** nella struttura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) . L'applicazione deve controllare tutti e tre i membri quando riceve un messaggio di [**riga \_ ADDRESSSTATE**](line-addressstate.md) (numCalls).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ altro**
</dt> <dd> <dl> <dt>



Gli elementi di stato Address diversi da quelli elencati di seguito sono stati modificati. L'applicazione deve controllare lo stato dell'indirizzo corrente per determinare quali elementi sono stati modificati.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**\_terminali LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



Le impostazioni del terminale per l'indirizzo sono state modificate.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Un'applicazione riceve una notifica sulle modifiche apportate a questi elementi di stato nel messaggio di [**riga \_ ADDRESSSTATE**](line-addressstate.md) . Le funzionalità del dispositivo dell'indirizzo indicano quali modifiche allo stato dell'indirizzo possono essere segnalate per questo indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**LINEA \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




