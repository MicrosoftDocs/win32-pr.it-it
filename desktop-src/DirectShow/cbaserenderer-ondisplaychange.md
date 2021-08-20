---
description: Il metodo OnDisplayChange invia un evento EC \_ DISPLAY CHANGED al gestore del grafico dei \_ filtri.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Metodo CBaseRenderer.OnDisplayChange (Renbase.h)
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
ms.openlocfilehash: 3f7fc5d733d90ab88f1114558947b6e72958c1d8b18d507ce612c1865fc400e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016879"
---
# <a name="cbaserendererondisplaychange-method"></a>Metodo CBaseRenderer.OnDisplayChange

Il `OnDisplayChange` metodo invia un evento EC DISPLAY [**\_ \_ CHANGED**](ec-display-changed.md) al gestore del grafico del filtro.

## <a name="syntax"></a>Sintassi


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'evento è stato pubblicato oppure FALSE in **caso** contrario.

## <a name="remarks"></a>Commenti

I renderer video devono chiamare questo metodo in risposta ai messaggi \_ WM DISPLAYCHANGE. Se il pin di input è connesso, il metodo invia un evento EC \_ DISPLAY CHANGED al gestore del grafico del \_ filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




