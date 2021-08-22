---
description: Il metodo OnWaitEnd viene chiamato quando il filtro viene eseguito in attesa dell'ora di presentazione di un esempio.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Metodo CBaseRenderer.OnWaitEnd (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451f475f8830e1b6e2c51f3e0fc571f86f520030fe8ec3dad6acf3d9d5e5c6fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537441"
---
# <a name="cbaserendereronwaitend-method"></a>Metodo CBaseRenderer.OnWaitEnd

Il `OnWaitEnd` metodo viene chiamato quando il filtro viene eseguito in attesa dell'ora di presentazione di un esempio.

## <a name="syntax"></a>Sintassi


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il [**metodo CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chiama questo metodo al termine dell'attesa dell'ora di presentazione di un esempio. Questo metodo non esegue alcun operazione nella classe di base, ma la classe derivata può eseguirne l'override.

Se si implementa il controllo di qualità, è possibile eseguire l'override di questo metodo insieme al metodo [**CBaseRenderer::OnWaitStart.**](cbaserenderer-onwaitstart.md) È possibile usare questi metodi per tenere traccia delle prestazioni del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




