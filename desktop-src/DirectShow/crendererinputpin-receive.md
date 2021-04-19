---
description: "Il metodo Receive riceve il campione multimediale successivo nel flusso. Questo metodo esegue l'override del metodo CBaseInputPin:: Receive."
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: Metodo CRendererInputPin. Receive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333176"
---
# <a name="crendererinputpinreceive-method"></a>Metodo CRendererInputPin. Receive

Il `Receive` metodo riceve il campione multimediale successivo nel flusso. Questo metodo esegue l'override del metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) del filtro, che gestisce il rendering. Se il metodo ha esito negativo, il pin Invia un \_ evento ERRORABORT EC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




