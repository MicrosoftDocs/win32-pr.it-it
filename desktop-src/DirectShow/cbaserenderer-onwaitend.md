---
description: Il metodo OnWaitEnd viene chiamato quando il filtro viene eseguito in attesa dell'ora di presentazione di un campione.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Metodo CBaseRenderer. OnWaitEnd (Renbase. h)
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
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333346"
---
# <a name="cbaserendereronwaitend-method"></a>CBaseRenderer. OnWaitEnd, metodo

Il `OnWaitEnd` metodo viene chiamato quando il filtro viene eseguito in attesa dell'ora di presentazione di un campione.

## <a name="syntax"></a>Sintassi


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chiama questo metodo quando ha terminato l'attesa dell'ora di presentazione di un campione. Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.

Se si implementa il controllo della qualità, è possibile eseguire l'override di questo metodo insieme al metodo [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) . È possibile utilizzare questi metodi per tenere traccia delle prestazioni del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




