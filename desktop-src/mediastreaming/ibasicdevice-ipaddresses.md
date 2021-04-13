---
title: IBasicDevice (metodo IpAddresses)
description: Restituisce un vettore di indirizzi IP.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- API di streaming multimediale del metodo IpAddresses
- API di streaming multimediale del metodo IpAddresses, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo IpAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397626"
---
# <a name="ibasicdeviceipaddresses-method"></a>Metodo IBasicDevice:: IpAddresses

Restituisce un vettore di indirizzi IP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve una raccolta enumerabile di puntatori a indirizzi IP.

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

 

 





