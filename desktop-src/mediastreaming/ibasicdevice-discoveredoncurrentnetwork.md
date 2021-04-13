---
title: Metodo IBasicDevice DiscoveredOnCurrentNetwork
description: Recupera un valore che indica se il dispositivo si trova nella rete corrente.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- API di streaming multimediale del metodo DiscoveredOnCurrentNetwork
- API di streaming multimediale del metodo DiscoveredOnCurrentNetwork, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo DiscoveredOnCurrentNetwork
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397458"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a>IBasicDevice::D Metodo iscoveredOnCurrentNetwork

Recupera un valore che indica se il dispositivo si trova nella rete corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve un puntatore a un valore booleano che è **true** se il dispositivo si trova nella rete corrente.

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

 

 





