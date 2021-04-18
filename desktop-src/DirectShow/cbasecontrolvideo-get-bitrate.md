---
description: Il \_ metodo Get bitrate recupera una velocità in bit approssimativa per il video.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: Metodo CBaseControlVideo.get_BitRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327571"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a>CBaseControlVideo. Get \_ bitrate (metodo)

Il `get_BitRate` metodo recupera una velocità in bit approssimativa per il video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBitRate* 
</dt> <dd>

Puntatore alla velocità in bit, in bit al secondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR se ha esito positivo o E \_ OutOfMemory se non è disponibile memoria sufficiente.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ bitrate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) . Chiama il CBaseControlVideo virtuale pure [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) per recuperare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




