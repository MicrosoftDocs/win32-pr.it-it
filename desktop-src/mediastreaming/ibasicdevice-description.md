---
title: Metodo IBasicDevice Description
description: Recupera una descrizione del dispositivo.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- Metodo di descrizione API Streaming multimediale
- Metodo description API Streaming multimediale, interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale, metodo Description
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cfaf3ba8ca9c74d094aa8cdc15f4c190d6e5141fb11ff255b6e7682b667846d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972350"
---
# <a name="ibasicdevicedescription-method"></a>Metodo IBasicDevice::D escription

Recupera una descrizione del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore alla descrizione del dispositivo.

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

 

 





