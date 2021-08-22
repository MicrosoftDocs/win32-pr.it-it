---
description: "Metodo CTransInPlaceOutputPin.PeekAllocator: il metodo PeekAllocator restituisce un puntatore all'allocatore del pin. Il metodo non incrementa il conteggio dei riferimenti sull'interfaccia."
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Metodo CTransInPlaceOutputPin.PeekAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b8833780411ae126dcda20c579fc5f6a681362da3707ee68879b06800b7b032
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654769"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a>Metodo CTransInPlaceOutputPin.PeekAllocator

Il `PeekAllocator` metodo restituisce un puntatore all'allocatore del pin. Il metodo non incrementa il conteggio dei riferimenti sull'interfaccia.

## <a name="syntax"></a>Sintassi


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la [**variabile membro \_ PAllocator CBaseOutputPin::m.**](cbaseoutputpin-m-pallocator.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




