---
title: MediaRenderer. StopAsync, metodo
description: Indica a ricevitore in modo asincrono di arrestare la riproduzione del contenuto corrente. | MediaRenderer. StopAsync, metodo
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- API di streaming multimediale del Metodo StopAsync
- API di streaming multimediale del Metodo StopAsync, interfaccia MediaRenderer
- API di streaming multimediale dell'interfaccia MediaRenderer, Metodo StopAsync
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 205c69a83572539974c1b8ad2cf45159c45335cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132262"
---
# <a name="mediarendererstopasync-method"></a>MediaRenderer. StopAsync, metodo

Indica a ricevitore in modo asincrono di arrestare la riproduzione del contenuto corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve un riferimento a un oggetto [**PlaybackOperation**](playbackoperation.md) usato per ottenere risultati dall'operazione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





