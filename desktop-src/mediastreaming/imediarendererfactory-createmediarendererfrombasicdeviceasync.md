---
title: Metodo IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync
description: Crea in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia IMediaRenderer usando l'interfaccia IBasicDevice specificata.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- Metodo CreateMediaRendererFromBasicDeviceAsync API Streaming multimediale
- Metodo CreateMediaRendererFromBasicDeviceAsync API Streaming multimediale , interfaccia IMediaRendererFactory
- Interfaccia IMediaRendererFactory API Streaming multimediale, metodo CreateMediaRendererFromBasicDeviceAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b9ee80a4f681bb57d62f84d35cf3a254e38982a10f642a35e35187f6af9e48e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092291"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a>Metodo IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync

Crea in modo asincrono una nuova istanza di un oggetto che implementa [**l'interfaccia IMediaRenderer**](imediarenderer.md) usando l'interfaccia [**IBasicDevice**](ibasicdevice.md) specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*basicDevice* \[ Pollici\]
</dt> <dd>

Puntatore a [**un'interfaccia IBasicDevice**](ibasicdevice.md) che rappresenta il dispositivo per cui verrà creata un'istanza di [**IMediaRenderer.**](imediarenderer.md)

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

 

