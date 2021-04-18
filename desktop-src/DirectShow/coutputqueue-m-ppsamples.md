---
description: 'Matrice di campioni di dimensioni COutputQueue:: m \_ lBatchSize.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Membro COutputQueue:: m_ppSamples (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329523"
---
# <a name="coutputqueuem_ppsamples-member"></a>Membro ppSamples di COutputQueue:: m \_

Matrice di campioni di dimensioni [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).

## <a name="syntax"></a>Sintassi


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>Osservazioni

Il thread di lavoro estrae gli esempi dalla coda e li inserisce in questa matrice. Passa la matrice al metodo [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) . Se l'oggetto non utilizza un thread di lavoro, l'oggetto inserisce esempi direttamente in questa matrice. La variabile membro dell' [**\_ elenco COutputQueue:: m**](coutputqueue-m-list.md) include la coda.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




