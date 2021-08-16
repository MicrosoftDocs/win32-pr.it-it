---
description: Valore booleano che indica se il filtro sta rilasciando frame. Se questo valore è TRUE, il filtro continua a eliminare i fotogrammi fino a raggiungere il fotogramma chiave successivo o fino a quando non riceve 30 fotogrammi delta in una riga senza fotogramma chiave.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: Membro CVideoTransformFilter::m_bSkipping (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f865bdc707b206a8528413a357a4e14bcfe88fff813e1f62a44d30e6f4843ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821916"
---
# <a name="cvideotransformfilterm_bskipping-member"></a>Membro CVideoTransformFilter::m \_ bSkipping

Valore booleano che indica se il filtro sta rilasciando frame. Se questo valore è **TRUE,** il filtro continua a eliminare i fotogrammi fino a raggiungere il fotogramma chiave successivo o fino a quando non riceve 30 fotogrammi delta in una riga senza fotogramma chiave.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




