---
description: Il metodo get \_ VideoHeight recupera l'altezza del video nativo.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: CBaseControlVideo.get_VideoHeight metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a7ca4b87a9196a8b59ec00cdc0e458855fa1db4e1e8f7b5bfd233924475519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057081"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a>Metodo CBaseControlVideo.get \_ VideoHeight

Il `get_VideoHeight` metodo recupera l'altezza del video nativo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVideoHeight* 
</dt> <dd>

Puntatore all'altezza del video nativo, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR in caso di esito positivo o E \_ OUTOFMEMORY se la memoria disponibile non è sufficiente.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IBasicVideo::get \_ VideoHeight.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) Chiama la classe [**virtuale pura CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) per recuperare la [**struttura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




