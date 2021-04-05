---
title: Metodo IBasicDevice ModelNumber
description: Recupera il numero di modello del dispositivo.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- API di streaming multimediale del metodo ModelNumber
- API di streaming multimediale del metodo ModelNumber, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo ModelNumber
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8034e67e5f3c552f0af83678d75e33881f1318f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857334"
---
# <a name="ibasicdevicemodelnumber-method"></a>Metodo IBasicDevice:: ModelNumber

Recupera il numero di modello del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve un puntatore al numero di modello del dispositivo.

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

 

 





