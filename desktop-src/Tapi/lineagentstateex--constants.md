---
description: Le \_ costanti LINEAGENTSTATEEX descrivono lo stato di un agente in un indirizzo.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: Costanti LINEAGENTSTATEEX_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332913"
---
# <a name="lineagentstateex_-constants"></a>\_Costanti LINEAGENTSTATEEX

Le **\_ costanti LINEAGENTSTATEEX** descrivono lo stato di un agente in un indirizzo.

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**\_BUSYACD LINEAGENTSTATEEX**
</dt> <dd> <dl> <dt>



L'agente è occupato a gestire una chiamata instradata da una coda ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**\_BUSYINCOMING LINEAGENTSTATEEX**
</dt> <dd> <dl> <dt>



L'agente è occupato a gestire una chiamata in ingresso che non è stata trasferita all'agente da una coda ACD in cui è connesso l'agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**\_BUSYOUTGOING LINEAGENTSTATEEX**
</dt> <dd> <dl> <dt>



L'agente è occupato a gestire una chiamata in uscita, ad esempio una instradata da una coda di composizione predittiva.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NObattistrada**
</dt> <dd> <dl> <dt>



L'agente è connesso, ma è occupato da un'attività diversa da quella di una chiamata (ad esempio, in pausa). Nessuna chiamata aggiuntiva deve essere indirizzata all'agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ pronto**
</dt> <dd> <dl> <dt>



L'agente è pronto per accettare le chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ rilasciato**
</dt> <dd> <dl> <dt>



L'agente è stato rilasciato, probabilmente perché è stato disconnesso.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ sconosciuto**
</dt> <dd> <dl> <dt>



Lo stato dell'agente è attualmente sconosciuto, ma può diventare noto in un secondo momento. Questo può essere uno stato di transizione quando una linea o un indirizzo viene aperto per la prima volta.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




