---
description: "Il metodo inattivo notifica al pin che il filtro non è più attivo. Questo metodo esegue l'override del Metodo CBasePin:: Inactive. Se il thread di streaming è attivo, questo metodo lo arresta e attende la chiusura del thread."
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Metodo CSourceStream. Inactive (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328170"
---
# <a name="csourcestreaminactive-method"></a>Metodo CSourceStream. Inactive

Il `Inactive` metodo notifica al pin che il filtro non è più attivo. Questo metodo esegue l'override del metodo [**CBasePin:: inactive**](cbasepin-inactive.md) . Se il thread di streaming è attivo, questo metodo lo arresta e attende la chiusura del thread.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




