---
title: Metodo IBasicDevice ModelUrl
description: Recupera l'URL del modello del dispositivo.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- API di streaming multimediale del metodo ModelUrl
- API di streaming multimediale del metodo ModelUrl, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo ModelUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f616d1a122f5fe6025c80742df61eb86d41514a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333895"
---
# <a name="ibasicdevicemodelurl-method"></a>Metodo IBasicDevice:: ModelUrl

Recupera l'URL del modello del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve un puntatore all'URL del modello del dispositivo.

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

 

 





