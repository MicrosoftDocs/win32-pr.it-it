---
description: Le \_ costanti LINEAGENTSTATE descrivono lo stato di un agente in un indirizzo.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: Costanti LINEAGENTSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332914"
---
# <a name="lineagentstate_-constants"></a>\_Costanti LINEAGENTSTATE

Le **\_ costanti LINEAGENTSTATE** descrivono lo stato di un agente in un indirizzo.

<dl> <dt>

<span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**\_BUSYACD LINEAGENTSTATE**
</dt> <dd> <dl> <dt>



L'agente è occupato a gestire una chiamata instradata da una coda ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**\_BUSYINCOMING LINEAGENTSTATE**
</dt> <dd> <dl> <dt>



L'agente è occupato a gestire una chiamata in ingresso che non è stata trasferita all'agente da una coda ACD in cui è connesso l'agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**\_BUSYOTHER LINEAGENTSTATE**
</dt> <dd> <dl> <dt>



L'agente occupa la gestione di un altro tipo di chiamata, ad esempio una chiamata personale in uscita non trasferita all'agente da un dialer predittivo. Questo valore può essere utilizzato anche quando l'agente è noto come occupato in una chiamata, ma il tipo di chiamata è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**\_BUSYOUTBOUND LINEAGENTSTATE**
</dt> <dd> <dl> <dt>



L'agente è occupato a gestire una chiamata in uscita, ad esempio una instradata da una coda di composizione predittiva.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**\_LOGGEDOFF LINEAGENTSTATE**
</dt> <dd> <dl> <dt>



Nessun agente è connesso all'indirizzo.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ NObattistrada**
</dt> <dd> <dl> <dt>



L'agente è connesso, ma è occupato da un'attività diversa da quella di una chiamata (ad esempio, in pausa). Nessuna chiamata aggiuntiva deve essere indirizzata all'agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ pronto**
</dt> <dd> <dl> <dt>



L'agente è pronto per accettare le chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE non \_ disponibile**
</dt> <dd> <dl> <dt>



Lo stato dell'agente è sconosciuto e non verrà mai reso noto. In [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)questa condizione può essere rappresentata anche dal membro **dwAgentState** impostato su 0.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ sconosciuto**
</dt> <dd> <dl> <dt>



Lo stato dell'agente è attualmente sconosciuto, ma può diventare noto in un secondo momento. Questo può essere uno stato di transizione quando una linea o un indirizzo viene aperto per la prima volta.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**\_WORKINGAFTERCALL LINEAGENTSTATE**
</dt> <dd> <dl> <dt>



L'agente ha completato la chiamata precedente, ma è ancora occupato con il lavoro correlato alla chiamata. L'agente non deve ricevere chiamate aggiuntive.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I 16 bit superiori di questo set di costanti sono riservati per le estensioni specifiche del dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




