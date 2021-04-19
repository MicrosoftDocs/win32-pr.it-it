---
title: Metodo IBasicDevice Manufacturer
description: Recupera il nome del produttore del dispositivo.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- Metodo manufacturname API di streaming multimediale
- Manufacturname metodo API di streaming multimediale, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo Manufacturname
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 698b4b6c202ed157737b20296976a282c7f97ba3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299155"
---
# <a name="ibasicdevicemanufacturername-method"></a>Metodo IBasicDevice:: Manufacturname

Recupera il nome del produttore del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve un puntatore al nome del produttore del dispositivo.

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

 

 





