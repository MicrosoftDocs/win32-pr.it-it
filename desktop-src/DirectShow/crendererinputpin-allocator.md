---
description: Il metodo allocator recupera un puntatore all'allocatore di memoria.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: Metodo CRendererInputPin. allocator (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328819"
---
# <a name="crendererinputpinallocator-method"></a>Metodo CRendererInputPin. allocator

Il `Allocator` metodo recupera un puntatore all'allocatore di memoria.

## <a name="syntax"></a>Sintassi


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore o **null**.

## <a name="remarks"></a>Commenti

Questo metodo restituisce la variabile membro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) . Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia. Questo metodo è esclusivamente un metodo di funzione di accesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




