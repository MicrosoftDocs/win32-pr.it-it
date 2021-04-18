---
description: Il metodo ThrottleWait inserisce un periodo di attesa dopo ciascun frame.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: Metodo CBaseVideoRenderer. ThrottleWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7408cfb011fa0fbbb223b6757ddb10ff9cbd357b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325344"
---
# <a name="cbasevideorendererthrottlewait-method"></a>CBaseVideoRenderer. ThrottleWait, metodo

Il `ThrottleWait` metodo inserisce un periodo di attesa dopo ciascun frame.

## <a name="syntax"></a>Sintassi


```C++
void ThrottleWait();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro attende un periodo di tempo ottenuto dal membro dati **m \_ trThrottle** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




