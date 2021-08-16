---
title: Metodo IBasicDevice Type
description: Recupera un valore di enumerazione che indica il tipo di dispositivo del dispositivo DLNA.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- Metodo di tipo API Streaming multimediale
- Metodo type API Streaming multimediale, interfaccia IBasicDevice
- Metodo Type dell'interfaccia IBasicDevice dell'API Streaming multimediale
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 433b255615a3fb57d59589b09a4a8b3e0f4cec5c02115bc737041d1fd94a197f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100625"
---
# <a name="ibasicdevicetype-method"></a>Metodo IBasicDevice::Type

Recupera un valore di enumerazione che indica il tipo di dispositivo del dispositivo DLNA.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore a un [**valore DeviceTypes.**](devicetypes.md)

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

 

 





