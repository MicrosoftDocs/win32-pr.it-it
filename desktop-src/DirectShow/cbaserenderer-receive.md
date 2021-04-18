---
description: Il metodo Receive riceve il campione multimediale successivo nel flusso.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Metodo CBaseRenderer. Receive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333894"
---
# <a name="cbaserendererreceive-method"></a>Metodo CBaseRenderer. Receive

Il `Receive` metodo riceve il campione multimediale successivo nel flusso.

## <a name="syntax"></a>Sintassi


```C++
virtual Receive(
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

Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.

## <a name="remarks"></a>Commenti

Il pin di input chiama questo metodo quando riceve un esempio dal filtro upstream.

Se il filtro è in esecuzione, questo metodo esegue i passaggi seguenti:

1.  Pianifica l'esempio per il rendering ([**CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md)).
2.  Attende l'ora pianificata ([**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).
3.  Esegue il rendering dell'esempio ([**CBaseRenderer:: Render**](cbaserenderer-render.md)).
4.  Rilascia l'esempio ([**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md)).

Se il filtro è sospeso, il metodo esegue i passaggi seguenti:

1.  Notifica alla classe derivata che è disponibile un esempio ([**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).
2.  Attende l'ora pianificata.
3.  Esegue il rendering dell'esempio.
4.  Rilascia l'esempio.

Durante la pausa, il metodo attende nel passaggio 2 fino a quando il filtro passa a uno stato di esecuzione. A questo punto, il filtro pianifica l'esempio.

Nella classe di base, il metodo **OnReceiveFirstSample** non esegue alcuna operazione. La classe derivata può eseguire l'override. Ad esempio, quando un renderer video viene sospeso, viene visualizzato il primo campione come immagine ancora.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




