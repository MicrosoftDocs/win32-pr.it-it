---
title: Metodo IDeviceIcon Height
description: Recupera l'altezza dell'icona in pixel.
ms.assetid: 06E1B3AD-FF49-4BC9-AC67-E2E00954475F
keywords:
- Metodo Height API Streaming multimediale
- Metodo Height API Streaming multimediale, interfaccia IDeviceIcon
- Interfaccia IDeviceIcon API Streaming multimediale, metodo Height
topic_type:
- apiref
api_name:
- IDeviceIcon.Height
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d813c572b0fc9e562d40326d830c5ef3530857601811df78c3acd541314b402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060291"
---
# <a name="ideviceiconheight-method"></a>Metodo IDeviceIcon::Height

Recupera l'altezza dell'icona in pixel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Height(
  [out] UINT32 *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'altezza dell'icona in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

