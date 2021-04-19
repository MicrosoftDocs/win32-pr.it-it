---
description: Il metodo PeekAllocator restituisce un puntatore all'allocatore del PIN. Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia.
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Metodo CTransInPlaceOutputPin. PeekAllocator (Transip. h)
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
ms.openlocfilehash: 805de37e2df2bf5a198107eea69d9107e799598c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326170"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a>CTransInPlaceOutputPin. PeekAllocator, metodo

Il `PeekAllocator` metodo restituisce un puntatore all'allocatore del PIN. Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia.

## <a name="syntax"></a>Sintassi


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la variabile membro [**CBaseOutputPin:: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




