---
description: Le costanti LINEAGENTSTATEEX \_ descrivono lo stato di un agente in un indirizzo.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: LINEAGENTSTATEEX_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f46c00b337a9106165616fe2eaf86bd2b2634b0c113369558953203313d59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140094"
---
# <a name="lineagentstateex_-constants"></a>Costanti LINEAGENTSTATEEX \_

Le **costanti LINEAGENTSTATEEX \_ descrivono** lo stato di un agente in un indirizzo.

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**
</dt> <dd> <dl> <dt>



L'agente è occupato a gestire una chiamata indirizzata da una coda ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



L'agente è occupato a gestire una chiamata in ingresso che non è stata trasferita all'agente da una coda ACD in cui l'agente è connesso.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**
</dt> <dd> <dl> <dt>



L'agente è occupato a gestire una chiamata in uscita, ad esempio una instradata da una coda di composizione predittiva.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NOTREADY**
</dt> <dd> <dl> <dt>



L'agente è connesso, ma occupato con un'attività diversa dall'esecuzione di una chiamata (ad esempio in caso di interruzione). Nessuna chiamata aggiuntiva deve essere instradata all'agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ READY**
</dt> <dd> <dl> <dt>



L'agente è pronto ad accettare le chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ RILASCIATO**
</dt> <dd> <dl> <dt>



L'agente è stato rilasciato, probabilmente perché si è disconnesso.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Lo stato dell'agente è attualmente sconosciuto, ma potrebbe diventare noto in un secondo momento. Può trattarsi di uno stato di transizione quando una riga o un indirizzo viene aperto per la prima volta.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




