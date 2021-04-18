---
description: Le \_ costanti del flag di bit LINEADDRESSSHARING descrivono i vari modi in cui un indirizzo può essere condiviso tra le linee.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: Costanti LINEADDRESSSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328417"
---
# <a name="lineaddresssharing_-constants"></a>\_Costanti LINEADDRESSSHARING

Le costanti del flag di bit **LINEADDRESSSHARING \_** descrivono i vari modi in cui un indirizzo può essere condiviso tra le linee.

<dl> <dt>

<span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ privato**
</dt> <dd> <dl> <dt>



L'indirizzo è privato per la riga dell'utente; non viene assegnato ad altre stazioni.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**\_BRIDGEDEXCL LINEADDRESSSHARING**
</dt> <dd> <dl> <dt>



L'indirizzo viene colmato a una o più stazioni. La prima riga per attivare una chiamata sulla riga avrà accesso esclusivo all'indirizzo e alle chiamate che possono esistere. Altre righe non saranno in grado di usare l'indirizzo con Bridge mentre è in uso.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**\_BRIDGEDNEW LINEADDRESSSHARING**
</dt> <dd> <dl> <dt>



L'indirizzo viene colmato con una o più stazioni. La prima riga per attivare una chiamata sulla riga avrà accesso esclusivo solo alla chiamata corrispondente. Altre applicazioni che usano l'indirizzo genereranno un aspetto di chiamata nuovo e separato.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**\_BRIDGEDSHARED LINEADDRESSSHARING**
</dt> <dd> <dl> <dt>



L'indirizzo viene colmato con una o più righe. Tutte le parti con bridging possono condividere chiamate sull'indirizzo, che quindi funge da conferenza.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ monitorato**
</dt> <dd> <dl> <dt>



Si tratta di un indirizzo il cui stato di inattività è reso disponibile a questa riga.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Il modo in cui un indirizzo viene condiviso tra le righe può influire sul comportamento di tale indirizzo. [**Riga \_ di**](line-callstate.md) I messaggi CALLSTATE e [**line \_ ADDRESSSTATE**](line-addressstate.md) vengono inviati all'applicazione in risposta alle attività da parte delle stazioni di bridging. Attraverso questi messaggi, un'applicazione può tenere traccia dello stato dell'indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**LINEA \_ CALLSTATE**](line-callstate.md)
</dt> </dl>

 

 




