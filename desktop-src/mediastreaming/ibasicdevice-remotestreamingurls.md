---
title: Metodo IBasicDevice RemoteStreamingUrls
description: Restituisce un vettore di URL di streaming remoto.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- Metodo RemoteStreamingUrls API Streaming multimediale
- Metodo RemoteStreamingUrls API Streaming multimediale, interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale, metodo RemoteStreamingUrls
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90d98d908cb582c0c2885a9b24a0a525f1e719c82bdffe20e74597ca5fc262a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972330"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a>Metodo IBasicDevice::RemoteStreamingUrls

Restituisce un vettore di URL di streaming remoto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve una raccolta enumerabile di puntatori agli URL di streaming remoto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





