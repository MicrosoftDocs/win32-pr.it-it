---
description: Il metodo EndOfStream notifica al filtro che il pin di input ha ricevuto una notifica di fine flusso.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Metodo CBaseRenderer.EndOfStream (Renbase.h)
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
ms.openlocfilehash: 9ff047865aa4f52dee6c03411cddb0c957327851f0f6ca1b7a03f0b6adaacfe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822732"
---
# <a name="cbaserendererendofstream-method"></a>Metodo CBaseRenderer.EndOfStream

Il `EndOfStream` metodo notifica al filtro che il pin di input ha ricevuto una notifica di fine flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il pin di input del filtro chiama questo metodo quando riceve una notifica di fine flusso.

Questo metodo imposta il flag [**\_ BEOS CBaseRenderer::m**](cbaserenderer-m-beos.md) su **TRUE** e chiama il metodo [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) per pianificare un [**evento EC \_ COMPLETE.**](ec-complete.md) Se il filtro è sospeso e in attesa di un esempio, questo metodo completa la transizione di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




