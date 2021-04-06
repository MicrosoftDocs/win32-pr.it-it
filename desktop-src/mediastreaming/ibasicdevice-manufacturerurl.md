---
title: Metodo IBasicDevice ManufacturerUrl
description: Recupera l'URL del produttore del dispositivo.
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- API di streaming multimediale del metodo ManufacturerUrl
- API di streaming multimediale del metodo ManufacturerUrl, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo ManufacturerUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e41ca83c98507c65ead8d1faf2922ee84b45649
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045680"
---
# <a name="ibasicdevicemanufacturerurl-method"></a>Metodo IBasicDevice:: ManufacturerUrl

Recupera l'URL del produttore del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve un puntatore all'URL del produttore del dispositivo.

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

 

 





