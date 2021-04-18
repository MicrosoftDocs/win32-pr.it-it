---
description: Il metodo DoBufferProcessingLoop genera dati multimediali e li recapita al pin di input downstream.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Metodo CSourceStream. DoBufferProcessingLoop (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329484"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a>CSourceStream. DoBufferProcessingLoop, metodo

Il `DoBufferProcessingLoop` metodo genera dati multimediali e li recapita al pin di input downstream.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Il thread ha ricevuto una richiesta di arresto.<br/>                              |
| <dl> <dt>**\_OK**</dt> </dl>    | Il flusso è terminato oppure il filtro downstream non accetta esempi.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo implementa il ciclo principale che elabora i dati e li recapita a valle. Ogni volta che viene attraversato il ciclo, il metodo recupera un esempio di supporto vuoto dall'allocatore. Passa l'esempio al metodo [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) . Il metodo **FillBuffer** , che deve essere implementato dalla classe derivata, genera dati multimediali e li inserisce nel buffer di esempio.

Il ciclo termina quando si verifica una delle condizioni seguenti:

-   Il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN di input rifiuta un campione.
-   Il metodo **FillBuffer** restituisce \_ false, che indica la fine del flusso o restituisce un codice di errore.
-   Il thread riceve una richiesta [**CSourceStream:: Stop**](csourcestream-stop.md) .

Il `DoBufferProcessingLoop` metodo gestisce la notifica di fine del flusso. Se si verifica un errore, viene inviato un evento [**EC \_ ERRORABORT**](ec-errorabort.md) al gestore del grafico dei filtri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




