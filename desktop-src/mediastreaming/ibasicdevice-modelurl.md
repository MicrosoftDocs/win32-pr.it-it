---
title: Metodo IBasicDevice ModelUrl
description: Recupera l'URL del modello del dispositivo.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- Metodo ModelUrl API Di streaming multimediale
- Metodo ModelUrl API Streaming multimediale, interfaccia IBasicDevice
- Interfaccia IBasicDevice API Di streaming multimediale, metodo ModelUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7595af295b0d0bc565d79bf5450ee6c5c16b0da4f3baa4fcf636e4e5386920
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847651"
---
# <a name="ibasicdevicemodelurl-method"></a>Metodo IBasicDevice::ModelUrl

Recupera l'URL del modello del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'URL del modello del dispositivo.

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

 

 





