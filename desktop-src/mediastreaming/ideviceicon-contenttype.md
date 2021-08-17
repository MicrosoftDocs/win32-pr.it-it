---
title: Metodo ContentType IDeviceIcon
description: Recupera il tipo di contenuto dell'icona.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- Metodo ContentType API Streaming multimediale
- Metodo ContentType API Streaming multimediale, interfaccia IDeviceIcon
- Interfaccia IDeviceIcon API Streaming multimediale, metodo ContentType
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8fb9cb639381b60bb59965d12ce3f0545daf6d2725cde69d3dea3dee589f8f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461746"
---
# <a name="ideviceiconcontenttype-method"></a>Metodo IDeviceIcon::ContentType

Recupera il tipo di contenuto dell'icona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore al tipo di contenuto dell'icona.

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

 

