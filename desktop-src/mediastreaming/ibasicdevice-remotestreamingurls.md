---
title: Metodo IBasicDevice RemoteStreamingUrls
description: Restituisce un vettore di URL di streaming remoto.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- API di streaming multimediale del metodo RemoteStreamingUrls
- API di streaming multimediale del metodo RemoteStreamingUrls, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo RemoteStreamingUrls
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdc4bd363096e7b808a51cfbddb764daabe03a55
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397603"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a>Metodo IBasicDevice:: RemoteStreamingUrls

Restituisce un vettore di URL di streaming remoto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve una raccolta enumerabile di puntatori agli URL di streaming remoto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





