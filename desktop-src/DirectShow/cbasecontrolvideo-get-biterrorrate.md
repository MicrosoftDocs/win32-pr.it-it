---
description: Il \_ metodo Get BitErrorRate recupera una frequenza degli errori di bit approssimativa per il video.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: Metodo CBaseControlVideo.get_BitErrorRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327578"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a>Metodo CBaseControlVideo. Get \_ BitErrorRate

Il `get_BitErrorRate` metodo recupera una frequenza degli errori di bit approssimativa per il video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBitErrorRate* 
</dt> <dd>

Puntatore alla frequenza degli errori di bit (un errore per approssimativamente questo numero di bit).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR se ha esito positivo o E \_ OutOfMemory se la memoria disponibile non è sufficiente.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) . Chiama il metodo [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtuale pure per recuperare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




