---
description: Il metodo OnWaitStart viene chiamato quando il filtro inizia ad attendere l'ora di presentazione di un esempio.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Metodo CBaseRenderer.OnWaitStart (Renbase.h)
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
ms.openlocfilehash: eaad14d0eec765a0ad12693c0a1eee67386bc9bb26344ee52c29224d129edf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822648"
---
# <a name="cbaserendereronwaitstart-method"></a>Metodo CBaseRenderer.OnWaitStart

Il `OnWaitStart` metodo viene chiamato quando il filtro inizia ad attendere l'ora di presentazione di un esempio.

## <a name="syntax"></a>Sintassi


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il [**metodo CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chiama questo metodo quando inizia ad attendere l'ora di presentazione di un esempio. Questo metodo non esegue alcun operazione nella classe di base, ma la classe derivata può eseguirne l'override.

Se si implementa il controllo di qualità, è possibile eseguire l'override di questo metodo insieme al metodo [**CBaseRenderer::OnWaitEnd.**](cbaserenderer-onwaitend.md) È possibile usare questi metodi per tenere traccia delle prestazioni del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




