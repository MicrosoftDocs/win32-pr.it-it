---
description: Il metodo Receive riceve l'esempio multimediale successivo nel flusso.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Metodo CBaseRenderer.Receive (Renbase.h)
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
ms.openlocfilehash: fe440b7ac0c7b05c2d3cf9d7ca2019a788e272b7aca6acd6a747738a255ca39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131441"
---
# <a name="cbaserendererreceive-method"></a>Metodo CBaseRenderer.Receive

Il `Receive` metodo riceve l'esempio multimediale successivo nel flusso.

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

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Il pin di input chiama questo metodo quando riceve un campione dal filtro upstream.

Se il filtro è in esecuzione, questo metodo esegue la procedura seguente:

1.  Pianifica l'esempio per il rendering ([**CBaseRenderer::P repareReceive**](cbaserenderer-preparereceive.md)).
2.  Attende l'ora pianificata ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).
3.  Esegue il rendering dell'esempio ([**CBaseRenderer::Render**](cbaserenderer-render.md)).
4.  Rilascia l'esempio ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).

Se il filtro viene sospeso, il metodo esegue la procedura seguente:

1.  Notifica alla classe derivata che è disponibile un esempio ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).
2.  Attende l'ora pianificata.
3.  Esegue il rendering dell'esempio.
4.  Rilascia l'esempio.

Durante la sospensione, il metodo attende nel passaggio 2 finché il filtro non passa a uno stato in esecuzione. A questo punto, il filtro pianifica l'esempio.

Nella classe di base il **metodo OnReceiveFirstSample** non esegue alcuna operazione. La classe derivata può eseguirne l'override. Ad esempio, quando un renderer video viene sospeso, il primo esempio viene visualizzato come immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




