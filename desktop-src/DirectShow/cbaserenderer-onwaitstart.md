---
description: Il metodo OnWaitStart viene chiamato quando il filtro inizia ad attendere l'ora di presentazione di un campione.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Metodo CBaseRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333345"
---
# <a name="cbaserendereronwaitstart-method"></a>CBaseRenderer. OnWaitStart, metodo

Il `OnWaitStart` metodo viene chiamato quando il filtro inizia ad attendere l'ora di presentazione di un campione.

## <a name="syntax"></a>Sintassi


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chiama questo metodo quando inizia ad attendere l'ora di presentazione di un campione. Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.

Se si implementa il controllo della qualità, è possibile eseguire l'override di questo metodo insieme al metodo [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) . È possibile utilizzare questi metodi per tenere traccia delle prestazioni del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




