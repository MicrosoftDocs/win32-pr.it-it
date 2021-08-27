---
description: Flag che specifica se l'oggetto recapita i campioni in batch esatti.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: Membro COutputQueue::m_bBatchExact (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5859744c3670ccc789ae5d87a619b3b32c3731580d473ff8cc6d775348771f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087251"
---
# <a name="coutputqueuem_bbatchexact-member"></a>Membro COutputQueue::m \_ bBatchExact

Flag che specifica se l'oggetto recapita i campioni in batch esatti.

## <a name="syntax"></a>Sintassi


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>Osservazioni

Se il valore è **TRUE,** l'oggetto attende fino a quando non dispone di un batch completo di campioni di supporti prima di recapitarlo. In caso contrario, vengono recapitati gli esempi non appena arrivano. La [**variabile membro COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) definisce le dimensioni del batch.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




