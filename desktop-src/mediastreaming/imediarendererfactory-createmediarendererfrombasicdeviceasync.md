---
title: Metodo IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync
description: Crea in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia IMediaRenderer utilizzando l'interfaccia IBasicDevice specificata.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- API di streaming multimediale del metodo CreateMediaRendererFromBasicDeviceAsync
- API di streaming multimediale del metodo CreateMediaRendererFromBasicDeviceAsync, interfaccia IMediaRendererFactory
- API di streaming multimediale dell'interfaccia IMediaRendererFactory, metodo CreateMediaRendererFromBasicDeviceAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046645"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a>Metodo IMediaRendererFactory:: CreateMediaRendererFromBasicDeviceAsync

Crea in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia [**IMediaRenderer**](imediarenderer.md) utilizzando l'interfaccia [**IBasicDevice**](ibasicdevice.md) specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*basicDevice* \[ in\]
</dt> <dd>

Puntatore a un'interfaccia [**IBasicDevice**](ibasicdevice.md) che rappresenta il dispositivo per cui verrà creata un'istanza di [**IMediaRenderer**](imediarenderer.md) .

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

 

