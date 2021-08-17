---
description: 'Metodo CTransformFilter.Pause: il metodo Pause sospende il filtro. Questo metodo implementa il metodo IMediaFilter::P ause.'
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: Metodo CTransformFilter.Pause (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 51584bc38c49345f6bb1d940aed24a052e9a4f9cd05fc2dc84246a6ba1168fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953500"
---
# <a name="ctransformfilterpause-method"></a>Metodo CTransformFilter.Pause

Il `Pause` metodo sospende il filtro. Questo metodo implementa il [**metodo IMediaFilter::P ause.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo StartStreaming.**](ctransformfilter-startstreaming.md) Il **metodo StartStreaming** non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




