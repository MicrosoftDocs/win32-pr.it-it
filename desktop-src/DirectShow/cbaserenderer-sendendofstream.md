---
description: Se è stata raggiunta la fine del flusso, il metodo SendEndOfStream pianifica un evento EC \_ COMPLETE per il gestore del grafico del filtro.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Metodo CBaseRenderer.SendEndOfStream (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 344783d8e8aac755d157f125b02827c9f362ca96271dccb84134f451b31d1bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954820"
---
# <a name="cbaserenderersendendofstream-method"></a>Metodo CBaseRenderer.SendEndOfStream

Se è stata raggiunta la fine del flusso, il `SendEndOfStream` metodo pianifica un evento EC COMPLETE per il gestore del grafico dei \_ filtri.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili sono quelli riportati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il gestore del grafico del filtro non accetta notifiche degli eventi.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

Il filtro potrebbe ricevere una notifica di fine flusso prima dell'ora di arresto dell'esempio corrente. In tal caso, il filtro deve attendere prima di pubblicare una [**notifica EC \_ COMPLETE**](ec-complete.md) al gestore del grafo del filtro.

Di conseguenza:

-   Se il filtro ha ricevuto una notifica di fine flusso anticipata (EOS), questo metodo pianifica un evento timer. Quando l'evento timer viene attivato, il filtro invia l'evento EC \_ COMPLETE.
-   Se il filtro ha ricevuto una notifica EOS non anticipata, questo metodo invia immediatamente l'evento EC \_ COMPLETE.
-   Se il filtro non ha alcuna notifica EOS in sospeso, il metodo restituisce senza eseguire alcuna operazione.

Il metodo di callback del timer [**è CBaseRenderer::TimerCallback.**](cbaserenderer-timercallback.md) Per recapitare \_ l'evento EC COMPLETE, il filtro chiama il [**metodo CBaseRenderer::NotifyEndOfStream.**](cbaserenderer-notifyendofstream.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




