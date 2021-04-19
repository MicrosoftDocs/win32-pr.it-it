---
description: Il metodo EOS recapita una chiamata di fine flusso al pin di input.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Metodo COutputQueue. EOS (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330208"
---
# <a name="coutputqueueeos-method"></a>Metodo COutputQueue. EOS

Il `EOS` Metodo recapita una chiamata di fine flusso al pin di input.

## <a name="syntax"></a>Sintassi


```C++
void EOS();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se l'oggetto usa un thread, Accoda un \_ messaggio di controllo pacchetti EOS. Il thread recapita tutti gli esempi in sospeso e chiama il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input.

Se l'oggetto non utilizza un thread, viene chiamato il metodo [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) per recapitare eventuali esempi in sospeso. Chiama quindi **Ipin:: EndOfStream** sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




