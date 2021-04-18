---
title: MediaRenderer. PauseAsync, metodo
description: Indica a ricevitore in modo asincrono di sospendere la riproduzione del contenuto corrente. | MediaRenderer. PauseAsync, metodo
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- API di streaming multimediale del metodo PauseAsync
- API di streaming multimediale del metodo PauseAsync, interfaccia MediaRenderer
- API di streaming multimediale dell'interfaccia MediaRenderer, metodo PauseAsync
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321935"
---
# <a name="mediarendererpauseasync-method"></a>MediaRenderer. PauseAsync, metodo

Indica a ricevitore in modo asincrono di sospendere la riproduzione del contenuto corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PauseAsync(
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

 

 





