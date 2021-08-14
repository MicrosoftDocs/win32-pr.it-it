---
description: Il metodo get FramesDrawn recupera la variabile membro \_ m cFramesDrawn, fornendo il numero di fotogrammi disegnati \_ dall'avvio del flusso.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: CBaseVideoRenderer.get_FramesDrawn metodo (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65a7c698d129a3606f6ba75f856289ca2b4e15c438d3890eb0a97e4a198ee808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822584"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a>Metodo CBaseVideoRenderer.get \_ FramesDrawn

Il `get_FramesDrawn` metodo recupera la variabile membro m **\_ cFramesDrawn,** fornendo il numero di fotogrammi disegnati dall'avvio del flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcFramesDrawn* 
</dt> <dd>

Puntatore al numero di frame disegnati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IQualProp::get \_ FramesDrawn.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




