---
description: Le \_ costanti LINETSPIOPTION descrivono l'ordine in cui i provider di servizi devono essere chiamati.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Costanti LINETSPIOPTION_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333540"
---
# <a name="linetspioption_-constants"></a>\_Costanti LINETSPIOPTION

Le **\_ costanti LINETSPIOPTION** descrivono l'ordine in cui i provider di servizi devono essere chiamati.

<dl> <dt>

<span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**\_NONREENTRANT LINETSPIOPTION**
</dt> <dd> <dl> <dt>



TAPI deve chiamare le funzioni in questo provider di servizi uno alla volta. deve attendere che ogni funzione restituisca (ma non per il completamento delle funzioni asincrone) prima di chiamare la stessa o un'altra funzione, nello stesso o in un altro thread, nello stesso o in un processore diverso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




