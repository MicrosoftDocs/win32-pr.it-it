---
description: Il metodo get \_ FramesDroppedInRenderer recupera il numero di frame eliminati dal renderer.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: CBaseVideoRenderer.get_FramesDroppedInRenderer metodo (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21bd2e9c2f9edb50ca3800c95b59ba19fd91674d5ef343cf35842380ce617978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016759"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a>Metodo CBaseVideoRenderer.get \_ FramesDroppedInRenderer

Il `get_FramesDroppedInRenderer` metodo recupera il numero di frame eliminati dal renderer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcFramesDropped* 
</dt> <dd>

Puntatore al numero di frame eliminati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IQualProp::get \_ FramesDroppedInRenderer.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) In questo modo la pagina delle proprietà recupera i dati dall'utilità di pianificazione. I frame possono anche essere rilasciati a monte senza che il renderer li veda.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




