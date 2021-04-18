---
description: Le \_ costanti LINEAGENTSESSIONSTATE descrivono diversi Stati della sessione di Agent.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: Costanti LINEAGENTSESSIONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327784"
---
# <a name="lineagentsessionstate_-constants"></a>\_Costanti LINEAGENTSESSIONSTATE

Le **\_ costanti LINEAGENTSESSIONSTATE** descrivono diversi Stati della sessione di Agent.

<dl> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**\_BUSYONCALL LINEAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



L'agente è occupato a gestire una chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**\_BUSYWRAPUP LINEAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



L'agente occupa la gestione del completamento della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ terminato**
</dt> <dd> <dl> <dt>



La sessione dell'agente è terminata.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ NObattistrada**
</dt> <dd> <dl> <dt>



L'agente è connesso, ma è occupato da un'attività diversa da quella di una chiamata (ad esempio, in pausa). Nessuna chiamata aggiuntiva deve essere indirizzata all'agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ pronto**
</dt> <dd> <dl> <dt>



L'agente è pronto per accettare le chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE \_ rilasciato**
</dt> <dd> <dl> <dt>



La sessione dell'agente è stata rilasciata.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




