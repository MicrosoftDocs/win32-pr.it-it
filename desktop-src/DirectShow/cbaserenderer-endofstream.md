---
description: Il metodo EndOfStream notifica al filtro che il pin di input ha ricevuto una notifica di fine del flusso.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Metodo CBaseRenderer. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329384"
---
# <a name="cbaserendererendofstream-method"></a>CBaseRenderer. EndOfStream, metodo

Il `EndOfStream` metodo notifica al filtro che il pin di input ha ricevuto una notifica di fine del flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Il pin di input del filtro chiama questo metodo quando riceve una notifica di fine del flusso.

Questo metodo imposta il [**flag CBaseRenderer:: m \_ BEOS**](cbaserenderer-m-beos.md) su **true** e chiama il metodo [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) per pianificare un evento [**EC \_ complete**](ec-complete.md) . Se il filtro è sospeso e in attesa di un campione, questo metodo completa la transizione di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




