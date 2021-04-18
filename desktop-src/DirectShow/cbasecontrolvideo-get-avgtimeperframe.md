---
description: Il \_ metodo Get AvgTimePerFrame Recupera il tempo medio per frame.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: Metodo CBaseControlVideo.get_AvgTimePerFrame (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327579"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a>Metodo CBaseControlVideo. Get \_ AvgTimePerFrame

Il `get_AvgTimePerFrame` metodo recupera il tempo medio per frame.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAvgTimePerFrame* 
</dt> <dd>

Puntatore al tempo medio per frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR se ha esito positivo o E \_ OutOfMemory se la memoria disponibile non è sufficiente.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) . Chiama la funzione membro [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtuale pure per recuperare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




