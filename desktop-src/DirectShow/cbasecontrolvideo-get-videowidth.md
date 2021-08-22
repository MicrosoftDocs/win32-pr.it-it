---
description: Il metodo get \_ VideoWidth recupera la larghezza del video nativo.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: CBaseControlVideo.get_VideoWidth metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268316dd9b7f37894f60ed45878c7de9bbc8d379301daa7bbefedcadd0b8e77f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661378"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a>Metodo CBaseControlVideo.get \_ VideoWidth

Il `get_VideoWidth` metodo recupera la larghezza del video nativo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVideoWidth* 
</dt> <dd>

Puntatore alla larghezza del video nativo, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR se ha esito positivo oppure E \_ OUTOFMEMORY se la memoria disponibile non è sufficiente.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IBasicVideo::get \_ VideoWidth.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) Chiama la classe [**virtuale pura CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) per recuperare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




