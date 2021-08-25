---
description: Le costanti LINEAGENTSESSIONSTATE \_ descrivono vari stati della sessione dell'agente.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: LINEAGENTSESSIONSTATE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702c9820fb6c2157a386241b13ea0593c4156195bc74bcfa7655c76db171083d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682201"
---
# <a name="lineagentsessionstate_-constants"></a>Costanti LINEAGENTSESSIONSTATE \_

Le **costanti LINEAGENTSESSIONSTATE \_ descrivono** vari stati della sessione dell'agente.

<dl> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE \_ BUSYONCALL**
</dt> <dd> <dl> <dt>



L'agente è occupato nella gestione di una chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE \_ BUSYWRAPUP**
</dt> <dd> <dl> <dt>



L'agente è occupato nella gestione del wrapping della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ TERMINATO**
</dt> <dd> <dl> <dt>



La sessione dell'agente è terminata.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ NOTREADY**
</dt> <dd> <dl> <dt>



L'agente è connesso, ma occupato con un'attività diversa dalla gestione di una chiamata (ad esempio in caso di interruzione). Nessuna chiamata aggiuntiva deve essere instradata all'agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ READY**
</dt> <dd> <dl> <dt>



L'agente è pronto ad accettare chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE \_ RILASCIATO**
</dt> <dd> <dl> <dt>



La sessione dell'agente è stata rilasciata.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




