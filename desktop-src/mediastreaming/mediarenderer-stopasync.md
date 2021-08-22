---
title: Metodo MediaRenderer.StopAsync
description: Indica alla dmr in modo asincrono di interrompere la riproduzione del contenuto corrente. | Metodo MediaRenderer.StopAsync
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- Api Streaming multimediale del metodo StopAsync
- Metodo StopAsync API Streaming multimediale, interfaccia MediaRenderer
- Interfaccia MediaRenderer API Streaming multimediale, metodo StopAsync
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c13e69952261643f2ac74df1e3978fb10e846488ee2c4794ee3ecac17251469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972140"
---
# <a name="mediarendererstopasync-method"></a>Metodo MediaRenderer.StopAsync

Indica alla dmr in modo asincrono di interrompere la riproduzione del contenuto corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT StopAsync(
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

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





