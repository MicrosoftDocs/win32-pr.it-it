---
description: Se è stata raggiunta la fine del flusso, il metodo SendEndOfStream pianifica un \_ evento di completamento EC per il gestore del grafico dei filtri.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Metodo CBaseRenderer. SendEndOfStream (Renbase. h)
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
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326428"
---
# <a name="cbaserenderersendendofstream-method"></a>CBaseRenderer. SendEndOfStream, metodo

Se è stata raggiunta la fine del flusso, il `SendEndOfStream` metodo pianifica un \_ evento di completamento EC per il gestore del grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Il gestore del grafico del filtro non accetta le notifiche degli eventi.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

Il filtro potrebbe ricevere una notifica di fine flusso prima dell'ora di arresto dell'esempio corrente. In tal caso, il filtro deve attendere prima di inviare una notifica di [**\_ completamento della EC**](ec-complete.md) al gestore del grafo dei filtri.

Di conseguenza:

-   Se il filtro ha ricevuto una notifica di fine del flusso (EOS) iniziale, questo metodo pianifica un evento del timer. Quando l'evento timer viene attivato, il filtro Invia l' \_ evento di completamento EC.
-   Se il filtro ha ricevuto una notifica EOS che non era anticipata, questo metodo invia \_ immediatamente l'evento di completamento EC.
-   Se il filtro non dispone di alcuna notifica EOS in sospeso, il metodo restituisce senza eseguire alcuna operazione.

Il metodo di callback del timer è [**CBaseRenderer:: TimerCallback**](cbaserenderer-timercallback.md). Per recapitare l' \_ evento EC completo, il filtro chiama il metodo [**CBaseRenderer:: NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




