---
description: Flag che specifica se l'oggetto recapita esempi in batch esatti.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Membro COutputQueue:: m_bBatchExact (Outputq. h)'
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
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330856"
---
# <a name="coutputqueuem_bbatchexact-member"></a>Membro bBatchExact di COutputQueue:: m \_

Flag che specifica se l'oggetto recapita esempi in batch esatti.

## <a name="syntax"></a>Sintassi


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>Osservazioni

Se il valore è **true**, l'oggetto attende fino a quando non dispone di un batch completo di esempi di supporti prima di recapito. In caso contrario, recapita gli esempi Man mano che arrivano. La variabile membro [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) definisce le dimensioni del batch.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




