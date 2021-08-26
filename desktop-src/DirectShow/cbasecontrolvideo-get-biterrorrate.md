---
description: Il metodo get \_ BitErrorRate recupera una frequenza di errore in bit approssimativa per il video.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: CBaseControlVideo.get_BitErrorRate metodo (Ctlutil.h)
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
ms.openlocfilehash: 2602d203ca5a418dcc889d26932cd28be78d984390e71cff996e6fd3938030a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057291"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a>Metodo CBaseControlVideo.get \_ BitErrorRate

Il `get_BitErrorRate` metodo recupera una frequenza di errore in bit approssimativa per il video.

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

Puntatore alla frequenza di errore in bit (un errore per circa questo numero di bit).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR in caso di esito positivo o E \_ OUTOFMEMORY se la memoria disponibile non è sufficiente.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IBasicVideo::get \_ BitErrorRate.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) Chiama il metodo [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtuale puro per recuperare la [**struttura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




