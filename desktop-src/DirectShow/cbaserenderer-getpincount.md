---
description: Il metodo GetPinCount Recupera il numero di pin.
ms.assetid: 518de15d-2ecf-425e-b4cd-14aaaf938417
title: Metodo CBaseRenderer. GetPinCount (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71b3703389019e2217a595884ac983e90835cdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325518"
---
# <a name="cbaserenderergetpincount-method"></a>CBaseRenderer. GetPinCount, metodo

Il `GetPinCount` metodo recupera il numero di pin.

## <a name="syntax"></a>Sintassi


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 1.

## <a name="remarks"></a>Commenti

Questo metodo implementa il metodo [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md) , che è virtuale puro nella classe **CBaseFilter** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




