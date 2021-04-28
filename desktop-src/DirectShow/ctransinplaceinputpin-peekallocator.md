---
description: "Metodo CTransInPlaceInputPin.PeekAllocator: il metodo PeekAllocator restituisce un puntatore all'allocatore del pin. Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia ."
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Metodo CTransInPlaceInputPin.PeekAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7a5f7cb0fbe754890b1d7930bb54c6fca47afa5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084669"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a>Metodo CTransInPlaceInputPin.PeekAllocator

Il `PeekAllocator` metodo restituisce un puntatore all'allocatore del pin. Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia .

## <a name="syntax"></a>Sintassi


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la [**variabile membro CBaseInputPin::m \_ pAllocator.**](cbaseinputpin-m-pallocator.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




