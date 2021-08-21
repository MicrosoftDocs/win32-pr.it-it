---
description: Il metodo EOS recapita una chiamata di fine flusso al pin di input.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Metodo COutputQueue.EOS (Outputq.h)
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
ms.openlocfilehash: 3effb06498ae65cad8eefd9a3144cab140926006cd38acee45c553c4295b0a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537141"
---
# <a name="coutputqueueeos-method"></a>Metodo COutputQueue.EOS

Il `EOS` metodo recapita una chiamata di fine flusso al pin di input.

## <a name="syntax"></a>Sintassi


```C++
void EOS();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se l'oggetto usa un thread, accoda un messaggio di controllo \_ PACKET EOS. Il thread recapita eventuali esempi in sospeso e chiama il [**metodo IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input.

Se l'oggetto non usa un thread, chiama il metodo [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) per recapitare eventuali esempi in sospeso. Chiama quindi **IPin::EndOfStream** sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




