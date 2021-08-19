---
description: Il metodo DoBufferProcessingLoop genera dati multimediali e lo recapita al pin di input downstream.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Metodo CSourceStream.DoBufferProcessingLoop (Source.h)
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
ms.openlocfilehash: d23df592abd125fd64362af89b6f81c5e9dcc20f0aa6cc998974a8fd2d4d87f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953740"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a>Metodo CSourceStream.DoBufferProcessingLoop

Il `DoBufferProcessingLoop` metodo genera i dati multimediali e lo recapita al pin di input downstream.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il thread ha ricevuto una richiesta di arresto.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Flusso terminato oppure il filtro downstream non accetta esempi.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo implementa il ciclo principale che elabora i dati e li recapita a valle. Ogni volta nel ciclo, il metodo recupera un campione multimediale vuoto dall'allocatore. Passa l'esempio al [**metodo CSourceStream::FillBuffer.**](csourcestream-fillbuffer.md) Il **metodo FillBuffer,** che la classe derivata deve implementare, genera dati multimediali e la inserisce nel buffer di esempio.

Il ciclo termina quando si verifica una delle condizioni seguenti:

-   Il metodo [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del pin di input rifiuta un esempio.
-   Il **metodo FillBuffer** restituisce S \_ FALSE, che indica la fine del flusso, o restituisce un codice di errore.
-   Il thread riceve una [**richiesta CSourceStream::Stop.**](csourcestream-stop.md)

Il `DoBufferProcessingLoop` metodo gestisce la notifica di fine flusso. Se si verifica un errore, invia un evento [**\_ EC ERRORABORT**](ec-errorabort.md) al gestore del grafico del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




