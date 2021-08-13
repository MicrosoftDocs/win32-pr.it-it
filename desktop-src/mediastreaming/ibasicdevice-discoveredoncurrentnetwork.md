---
title: Metodo IBasicDevice DiscoveredOnCurrentNetwork
description: Recupera un valore che indica se il dispositivo si trova nella rete corrente.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- Metodo DiscoveredOnCurrentNetwork API Streaming multimediale
- Metodo DiscoveredOnCurrentNetwork API Streaming multimediale, interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale, metodo DiscoveredOnCurrentNetwork
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 605962315e4eab2cdbd5beab264747d282d78ef7c6f44b3bbcbf2f249bac7548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473490"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a>Metodo IBasicDevice::D iscoveredOnCurrentNetwork

Recupera un valore che indica se il dispositivo si trova nella rete corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore a un valore booleano **true** se il dispositivo si trova nella rete corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





