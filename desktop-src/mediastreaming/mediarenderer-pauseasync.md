---
title: Metodo MediaRenderer.PauseAsync
description: Indica alla DMR di sospendere in modo asincrono la riproduzione del contenuto corrente. | Metodo MediaRenderer.PauseAsync
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- Metodo PauseAsync API Streaming multimediale
- Metodo PauseAsync API Streaming multimediale, interfaccia MediaRenderer
- Interfaccia MediaRenderer API Streaming multimediale, metodo PauseAsync
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5dcb4474f7a7843f2812cf64e0119912eca8ae320b29b9acb0131a65bbbffa19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060251"
---
# <a name="mediarendererpauseasync-method"></a>Metodo MediaRenderer.PauseAsync

Indica alla DMR di sospendere in modo asincrono la riproduzione del contenuto corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un riferimento a un oggetto [**PlaybackOperation**](playbackoperation.md) usato per ottenere i risultati dall'operazione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





