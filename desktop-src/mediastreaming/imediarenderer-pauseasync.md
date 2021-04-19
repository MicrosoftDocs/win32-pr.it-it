---
title: Metodo IMediaRenderer PauseAsync
description: Indica a ricevitore in modo asincrono di sospendere la riproduzione del contenuto corrente. | Metodo IMediaRenderer PauseAsync
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- API di streaming multimediale del metodo PauseAsync
- API di streaming multimediale del metodo PauseAsync, interfaccia IMediaRenderer
- API di streaming multimediale dell'interfaccia IMediaRenderer, metodo PauseAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8713fa4b2fe46a694024c2873cd50a0ec89ce898
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321898"
---
# <a name="imediarendererpauseasync-method"></a>IMediaRenderer::P metodo auseAsync

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

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





