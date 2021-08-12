---
description: Il metodo OnRenderEnd esegue l'arrotondamento per i casi in cui il tempo di rendering varia a causa di interruzioni.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Metodo CBaseVideoRenderer.OnRenderEnd (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24d622ec62b27ae2e85eb9bef37516c82acbb17e03bef9a51b161edacd0b95c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658689"
---
# <a name="cbasevideorendereronrenderend-method"></a>Metodo CBaseVideoRenderer.OnRenderEnd

Il `OnRenderEnd` metodo esegue l'arrotondamento per i casi in cui il tempo di rendering varia a causa di interruzioni.

## <a name="syntax"></a>Sintassi


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'esempio multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro deve essere chiamata subito dopo il disegno di un'immagine.

Questa funzione membro esegue l'override [**di CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




