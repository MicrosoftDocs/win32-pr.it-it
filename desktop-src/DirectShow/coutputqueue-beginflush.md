---
description: Il Metodo BeginFlush avvia un'operazione di svuotamento.
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Metodo COutputQueue. BeginFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 462c3027e38bd94f061eb927c0d52576e29c997b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330214"
---
# <a name="coutputqueuebeginflush-method"></a>COutputQueue. BeginFlush, metodo

Il `BeginFlush` metodo inizia un'operazione di svuotamento.

## <a name="syntax"></a>Sintassi


```C++
void BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo imposta la variabile membro [**COutputQueue:: m \_ BFlushing**](coutputqueue-m-bflushing.md) su **true**. Se l'oggetto utilizza un thread, il thread chiama il metodo [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) per liberare tutti gli esempi in sospeso. In caso contrario, l'oggetto chiama **FreeSamples** durante il metodo [**COutputQueue:: EndFlush**](coutputqueue-endflush.md) . Questo metodo imposta anche la variabile membro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) su S \_ false, che fa sì che l'oggetto elimini tutti i nuovi esempi.

L'oggetto passa la notifica di scaricamento downstream chiamando il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




