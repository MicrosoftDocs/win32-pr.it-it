---
description: Il \_ metodo Get FramesDroppedInRenderer Recupera il numero di frame eliminati dal renderer.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: Metodo CBaseVideoRenderer.get_FramesDroppedInRenderer (Renbase. h)
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
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326417"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a>Metodo CBaseVideoRenderer. Get \_ FramesDroppedInRenderer

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

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IQualProp:: Get \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) . Questo è il modo in cui la pagina delle proprietà recupera i dati dall'utilità di pianificazione. I frame possono anche essere eliminati a Monte senza che vengano visualizzati anche dal renderer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




