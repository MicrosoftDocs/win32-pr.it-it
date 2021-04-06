---
title: Metodo di descrizione IBasicDevice
description: Recupera una descrizione del dispositivo.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- Descrizione metodo API di streaming multimediale
- Descrizione metodo API di streaming multimediale, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo Description
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045614"
---
# <a name="ibasicdevicedescription-method"></a>IBasicDevice::D Metodo Descrizione

Recupera una descrizione del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve un puntatore alla descrizione del dispositivo.

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

 

 





