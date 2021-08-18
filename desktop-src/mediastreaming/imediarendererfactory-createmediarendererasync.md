---
title: Metodo IMediaRendererFactory CreateMediaRendererAsync
description: Crea in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia IMediaRenderer usando il nome UDN (Unique Device Name) specificato.
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- Metodo CreateMediaRendererAsync API Streaming multimediale
- Metodo CreateMediaRendererAsync API Streaming multimediale, interfaccia IMediaRendererFactory
- Interfaccia IMediaRendererFactory API Streaming multimediale, metodo CreateMediaRendererAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e459324d96f031ab3433f0d8bfe8ba5de562d76c95f51affd7b72d130655fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735488"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a>Metodo IMediaRendererFactory::CreateMediaRendererAsync

Crea in modo asincrono una nuova istanza di un oggetto che implementa [**l'interfaccia IMediaRenderer**](imediarenderer.md) usando il nome UDN (Unique Device Name) specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*deviceIdentifier* \[ Pollici\]
</dt> <dd>

HSTRING contenente un UDN che identifica il dispositivo DLNA DMR per cui verrà creata un'istanza di [**IMediaRenderer.**](imediarenderer.md)

</dd> <dt>

*value* \[ out, retval\]
</dt> <dd>

Riceve un riferimento a un [**oggetto CreateMediaRendererOperation**](createmediarendereroperation.md) usato per ottenere risultati dall'operazione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

