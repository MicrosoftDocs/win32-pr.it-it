---
description: Il metodo GetVideoSize recupera la larghezza e l'altezza del video nativo.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Metodo CBaseControlVideo.GetVideoSize (Ctlutil.h)
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
ms.openlocfilehash: b49f58901ac362b5a03d069485ec4dbf74e22d4549dc628f26baa5c2bfa85234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056941"
---
# <a name="cbasecontrolvideogetvideosize-method"></a>Metodo CBaseControlVideo.GetVideoSize

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

Restituisce un **valore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




