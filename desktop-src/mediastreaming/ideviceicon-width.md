---
title: Metodo IDeviceIcon Width
description: Recupera la larghezza dell'icona in pixel.
ms.assetid: 28ADA921-6808-43B8-966E-BA42B1B52931
keywords:
- Metodo Width API Streaming multimediale
- Metodo Width API Streaming multimediale, interfaccia IDeviceIcon
- Interfaccia IDeviceIcon API Streaming multimediale, metodo Width
topic_type:
- apiref
api_name:
- IDeviceIcon.Width
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc76fcd7915c350e04cbacfe756e424d31b0d27d5ced38b0ccf8664805fc9bb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473463"
---
# <a name="ideviceiconwidth-method"></a>Metodo IDeviceIcon::Width

Recupera la larghezza dell'icona in pixel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Width(
  [out] UINT32 *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore alla larghezza dell'icona in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

