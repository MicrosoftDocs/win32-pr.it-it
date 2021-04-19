---
description: Il metodo GetVideoSize recupera la larghezza e l'altezza del video nativo.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Metodo CBaseControlVideo. GetVideoSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b1df6fe781f036043728050354519dfa6e28d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332082"
---
# <a name="cbasecontrolvideogetvideosize-method"></a>CBaseControlVideo. GetVideoSize, metodo

Il `GetVideoSize` metodo recupera la larghezza e l'altezza del video nativo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWidth* 
</dt> <dd>

Puntatore alla larghezza del video.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntatore all'altezza del video.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




