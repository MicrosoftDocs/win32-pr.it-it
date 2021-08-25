---
description: Il metodo get \_ BitRate recupera una velocità in bit approssimativa per il video.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: CBaseControlVideo.get_BitRate metodo (Ctlutil.h)
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
ms.openlocfilehash: b33e3584bb0460b798101d8062c3647b983841c77653adcffd18580eade25c6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057271"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a>Metodo CBaseControlVideo.get \_ BitRate

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

Restituisce NOERROR in caso di esito positivo o E \_ OUTOFMEMORY se non è disponibile memoria sufficiente.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IBasicVideo::get \_ BitRate.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) Chiama la classe [**virtuale pura CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) per recuperare la [**struttura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




