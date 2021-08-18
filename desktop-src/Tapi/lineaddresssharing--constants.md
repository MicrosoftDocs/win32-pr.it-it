---
description: Le costanti del flag di bit LINEADDRESSSHARING descrivono vari modi in cui un \_ indirizzo può essere condiviso tra le righe.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: LINEADDRESSSHARING_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fe92c92efd75a4f6e731944c487acff2ffd70e173dd04b03244ec9d55e8aba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003129"
---
# <a name="lineaddresssharing_-constants"></a>Costanti \_ LINEADDRESSSHARING

Le costanti del flag di bit **LINEADDRESSSHARING \_** descrivono vari modi in cui un indirizzo può essere condiviso tra le righe.

<dl> <dt>

<span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ PRIVATE**
</dt> <dd> <dl> <dt>



L'indirizzo è privato per la riga dell'utente. non viene assegnato ad altre stazioni.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**
</dt> <dd> <dl> <dt>



L'indirizzo viene con bridge a una o più stazioni. La prima riga per attivare una chiamata sulla riga avrà accesso esclusivo all'indirizzo e alle chiamate che possono esistere su di essa. Altre righe non saranno in grado di usare l'indirizzo con bridge mentre è in uso.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**
</dt> <dd> <dl> <dt>



L'indirizzo è con bridge con una o più altre stazioni. La prima riga per attivare una chiamata sulla riga avrà accesso esclusivo solo alla chiamata corrispondente. Altre applicazioni che usano l'indirizzo avranno un aspetto di chiamata nuovo e separato.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**
</dt> <dd> <dl> <dt>



L'indirizzo è con bridge con una o più altre righe. Tutte le parti con bridge possono condividere le chiamate sull'indirizzo, che quindi funziona come conferenza.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ MONITORATO**
</dt> <dd> <dl> <dt>



Si tratta di un indirizzo il cui stato di inattività/occupato viene reso disponibile per questa riga.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Il modo in cui un indirizzo viene condiviso su più righe può influire sul comportamento di tale indirizzo. [**LINE \_ I messaggi CALLSTATE**](line-callstate.md) [**e LINE \_ ADDRESSSTATE**](line-addressstate.md) vengono inviati all'applicazione in risposta alle attività delle stazioni di bridging. È tramite questi messaggi che un'applicazione può tenere traccia dello stato dell'indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**LINE \_ CALLSTATE**](line-callstate.md)
</dt> </dl>

 

 




