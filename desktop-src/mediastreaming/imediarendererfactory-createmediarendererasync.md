---
title: Metodo IMediaRendererFactory CreateMediaRendererAsync
description: Crea in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia IMediaRenderer usando il nome univoco del dispositivo (UDN) specificato.
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- API di streaming multimediale del metodo CreateMediaRendererAsync
- API di streaming multimediale del metodo CreateMediaRendererAsync, interfaccia IMediaRendererFactory
- API di streaming multimediale dell'interfaccia IMediaRendererFactory, metodo CreateMediaRendererAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725882"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a>Metodo IMediaRendererFactory:: CreateMediaRendererAsync

Crea in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia [**IMediaRenderer**](imediarenderer.md) usando il nome univoco del dispositivo (UDN) specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DeviceIdentifier* \[ in\]
</dt> <dd>

Un HSTRING contenente un UDN che identifica il dispositivo ricevitore DLNA per cui verrà creata un'istanza di [**IMediaRenderer**](imediarenderer.md) .

</dd> <dt>

*valore* \[ di out, retval\]
</dt> <dd>

Riceve un riferimento a un oggetto [**CreateMediaRendererOperation**](createmediarendereroperation.md) usato per ottenere risultati dall'operazione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

