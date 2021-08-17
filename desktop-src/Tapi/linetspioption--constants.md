---
description: Le costanti LINETSPIOPTION descrivono i provider di servizi degli \_ ordini da chiamare.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: LINETSPIOPTION_ costanti (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5d4a57edd80a83ab442313706fd40a2fbd79f545a0b3e9485e5d8c88b8c2f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404857"
---
# <a name="linetspioption_-constants"></a>Costanti LINETSPIOPTION \_

Le **costanti LINETSPIOPTION \_ descrivono** i provider di servizi degli ordini da chiamare.

<dl> <dt>

<span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**
</dt> <dd> <dl> <dt>



TAPI deve chiamare le funzioni in questo provider di servizi una alla volta. deve attendere da ogni funzione di restituire (ma non per il completamento delle funzioni asincrone) prima di chiamare la stessa funzione o un'altra funzione, nello stesso thread o in un thread diverso, nello stesso processore o in un processore diverso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



 

 




