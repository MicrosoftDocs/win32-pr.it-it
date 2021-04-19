---
description: Il metodo OnDisplayChange Invia un \_ \_ evento di modifica della visualizzazione EC al gestore del grafico dei filtri.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Metodo CBaseRenderer. OnDisplayChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333354"
---
# <a name="cbaserendererondisplaychange-method"></a>CBaseRenderer. OnDisplayChange, metodo

Il `OnDisplayChange` metodo invia un evento di [**\_ \_ modifica della visualizzazione EC**](ec-display-changed.md) al gestore del grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'evento è stato pubblicato; in caso contrario, **false** .

## <a name="remarks"></a>Commenti

I renderer video devono chiamare questo metodo in risposta ai \_ messaggi WM DISPLAYCHANGE. Se il pin di input è connesso, il metodo invia un \_ \_ evento di modifica della visualizzazione EC al gestore del grafico dei filtri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




