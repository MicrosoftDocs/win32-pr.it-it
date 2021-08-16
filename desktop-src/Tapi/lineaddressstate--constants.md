---
description: Le costanti del flag di bit LINEADDRESSSTATE \_ descrivono vari elementi di stato degli indirizzi.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: LINEADDRESSSTATE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddf746d98328df51497374b990eb23f3885516ee1374d9cfdafb8799d016fb74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761853"
---
# <a name="lineaddressstate_-constants"></a>Costanti \_ LINEADDRESSSTATE

Le costanti del flag di bit **LINEADDRESSSTATE \_** descrivono vari elementi di stato degli indirizzi.

<dl> <dt>

<span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica che, a causa di modifiche di configurazione apportate dall'utente o in altre circostanze, uno o più membri nella struttura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) per l'indirizzo sono stati modificati. L'applicazione deve usare [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) per leggere la struttura aggiornata. Se un provider di servizi invia un messaggio [**LINE \_ ADDRESSSTATE**](line-addressstate.md) contenente questo valore a TAPI, TAPI lo passerà alle applicazioni che hanno negoziato TAPI versione 1.4 o successiva. Le applicazioni che negoziano una versione precedente dell'API riceveranno messaggi [**\_ LINEDEVSTATE**](line-linedevstate.md) che specificano LINEDEVSTATE REINIT, che richiedono l'arresto e la reinizializzazione della connessione a TAPI per ottenere le informazioni \_ aggiornate.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



L'elemento specifico del dispositivo dello stato dell'indirizzo è stato modificato.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE \_ FORWARD**
</dt> <dd> <dl> <dt>



Lo stato di inoltro dell'indirizzo è stato modificato, incluso il numero di anelli per determinare una condizione di nessuna risposta. L'applicazione deve controllare lo stato dell'indirizzo per determinare i dettagli sullo stato di inoltro corrente dell'indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**
</dt> <dd> <dl> <dt>



L'indirizzo monitorato o bridged è stato modificato da in uso da una stazione a in uso da più di una stazione.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**
</dt> <dd> <dl> <dt>



L'indirizzo è cambiato da inattivo o in uso da molte stazioni con bridge ad essere in uso da una sola stazione.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**
</dt> <dd> <dl> <dt>



L'indirizzo è stato modificato in inattivo (non è in uso da nessuna stazioni).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



Il numero di chiamate sull'indirizzo è stato modificato. Questo è il risultato di eventi come una nuova chiamata in ingresso, una chiamata in uscita sull'indirizzo o una chiamata che ne modifica lo stato di blocco. Questo flag illustra le modifiche apportate ai membri **dwNumActiveCalls**, **dwNumOnHoldCalls** **e dwNumOnHoldPendingCalls nella** struttura [**LINEADDRESSSTATUS.**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) L'applicazione deve controllare tutti e tre questi membri quando riceve un messaggio [**LINE \_ ADDRESSSTATE**](line-addressstate.md) (numCalls).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ OTHER**
</dt> <dd> <dl> <dt>



Gli elementi di stato degli indirizzi diversi da quelli elencati di seguito sono stati modificati. L'applicazione deve controllare lo stato dell'indirizzo corrente per determinare quali elementi sono stati modificati.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**\_TERMINALI LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



Le impostazioni del terminale per l'indirizzo sono state modificate.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Un'applicazione viene notificata in caso di modifiche a questi elementi di stato nel [**messaggio LINE \_ ADDRESSSTATE.**](line-addressstate.md) Le funzionalità del dispositivo dell'indirizzo indicano quali modifiche dello stato dell'indirizzo possono essere segnalate per questo indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




