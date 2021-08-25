---
title: Metodo IBasicDevice ManufacturerName
description: Recupera il nome del produttore del dispositivo.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- Metodo ManufacturerName API Streaming multimediale
- Metodo ManufacturerName API Streaming multimediale, interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale, metodo ManufacturerName
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 453e11fc547998b6dc3e39017684c30cacd205c0c17b21846925d4de472f43a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011831"
---
# <a name="ibasicdevicemanufacturername-method"></a>Metodo IBasicDevice::ManufacturerName

Recupera il nome del produttore del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore al nome del produttore del dispositivo.

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

 

 





