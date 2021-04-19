---
description: Il metodo Run segnala al thread di streaming di essere eseguito.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Metodo CSourceStream. Run (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332321"
---
# <a name="csourcestreamrun-method"></a>Metodo CSourceStream. Run

Il `Run` metodo segnala al thread di streaming di essere eseguito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Run();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o e \_ imprevisto.

## <a name="remarks"></a>Commenti

Nella classe di base, questo metodo ha lo stesso effetto della richiesta [**CSourceStream::P ause**](csourcestream-pause.md) e non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




