---
title: Metodo IBasicDevice PresentationUrl
description: Recupera l'URL di presentazione del dispositivo.
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- Metodo PresentationUrl API Streaming multimediale
- Metodo PresentationUrl API Streaming multimediale, interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale, metodo PresentationUrl
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d5908b80e7b413ca646279a751e12ec7d9c7e6e98ae7ecff3ad1f1d9e60bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235938"
---
# <a name="ibasicdevicepresentationurl-method"></a>Metodo IBasicDevice::P resentationUrl

Recupera l'URL di presentazione del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'URL di presentazione del dispositivo.

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

 

 





