---
description: Il metodo OnStartStreaming viene chiamato quando il filtro inizia il flusso.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Metodo CBaseRenderer. OnStartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66433795b0674e1d2d5b7a7de5b1dcd1b50eb424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327954"
---
# <a name="cbaserendereronstartstreaming-method"></a>CBaseRenderer. OnStartStreaming, metodo

Il `OnStartStreaming` metodo viene chiamato quando il filtro inizia il flusso.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Il metodo [**CBaseRenderer:: StartStreaming**](cbaserenderer-startstreaming.md) chiama questo metodo. Non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




