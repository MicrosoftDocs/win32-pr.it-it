---
title: Metodo IBasicDevice FriendlyName
description: Recupera il nome descrittivo del dispositivo.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- Metodo FriendlyName API Streaming multimediale
- Metodo FriendlyName API Streaming multimediale, interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale, metodo FriendlyName
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35084fafb92b3716208aa6062f065cc4e25a45d2d1a412083076b9e355d2ce43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735611"
---
# <a name="ibasicdevicefriendlyname-method"></a>Metodo IBasicDevice::FriendlyName

Recupera il nome descrittivo del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore al nome descrittivo del dispositivo.

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

 

 





