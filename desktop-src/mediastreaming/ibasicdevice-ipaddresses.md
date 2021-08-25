---
title: Metodo IBasicDevice IpAddresses
description: Restituisce un vettore di indirizzi IP.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- Metodo IpAddresses API Streaming multimediale
- Metodo IpAddresses API Streaming multimediale, interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale, metodo IpAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc997abb24c007e9e3e4d5c8028762daaca20e434ca4e3ab22fb278f567f998c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847681"
---
# <a name="ibasicdeviceipaddresses-method"></a>Metodo IBasicDevice::IpAddresses

Restituisce un vettore di indirizzi IP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve una raccolta enumerabile di puntatori agli indirizzi IP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





