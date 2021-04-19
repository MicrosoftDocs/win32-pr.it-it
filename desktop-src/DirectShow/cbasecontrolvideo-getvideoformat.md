---
description: Il metodo GetVideoFormat recupera un esempio video che rappresenta il formato video corrente.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Metodo CBaseControlVideo. GetVideoFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332085"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a>CBaseControlVideo. GetVideoFormat, metodo

Il `GetVideoFormat` metodo recupera un esempio video che rappresenta il formato video corrente.

## <a name="syntax"></a>Sintassi


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) che contiene il formato video corrente.

## <a name="remarks"></a>Commenti

Per restituire e controllare determinate informazioni tramite [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), è necessario che l'oggetto conosca il formato video corrente. Ottiene queste informazioni chiamando il metodo virtuale pure che le classi derivate devono eseguire l'override. Questa funzione membro viene chiamata dalle funzioni membro [**CBaseControlVideo**](cbasecontrolvideo.md) seguenti.

-   [**CBaseControlVideo::OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)
-   [**CBaseControlVideo:: Get \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)
-   [**CBaseControlVideo:: Get \_ bitrate**](cbasecontrolvideo-get-bitrate.md)
-   [**CBaseControlVideo:: Get \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)
-   [**CBaseControlVideo:: Get \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)
-   [**CBaseControlVideo:: Get \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)
-   [**CBaseControlVideo::GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)
-   [**CBaseControlVideo::GetVideoSize**](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




