---
description: Il metodo GetVideoFormat recupera un esempio video che rappresenta il formato video corrente.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Metodo CBaseControlVideo.GetVideoFormat (Ctlutil.h)
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
ms.openlocfilehash: e37a59b8d002a9c081de74c4974dca1f86d1c9d0a5f7f7b0caca11be6c026d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052771"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a>Metodo CBaseControlVideo.GetVideoFormat

Il `GetVideoFormat` metodo recupera un esempio video che rappresenta il formato video corrente.

## <a name="syntax"></a>Sintassi


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a una [**struttura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) che contiene il formato video corrente.

## <a name="remarks"></a>Commenti

Per restituire e controllare determinate informazioni tramite [**IBasicVideo,**](/windows/desktop/api/Control/nn-control-ibasicvideo)l'oggetto deve conoscere il formato video corrente. Ottiene queste informazioni chiamando questo metodo virtuale puro di cui le classi derivate devono eseguire l'override. Questa funzione membro viene chiamata dalle funzioni membro [**CBaseControlVideo**](cbasecontrolvideo.md) seguenti.

-   [**CBaseControlVideo::OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)
-   [**CBaseControlVideo::get \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)
-   [**CBaseControlVideo::get \_ BitRate**](cbasecontrolvideo-get-bitrate.md)
-   [**CBaseControlVideo::get \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)
-   [**CBaseControlVideo::get \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)
-   [**CBaseControlVideo::get \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)
-   [**CBaseControlVideo::GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)
-   [**CBaseControlVideo::GetVideoSize**](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




