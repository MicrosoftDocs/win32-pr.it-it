---
title: IDeviceIcon (Metodo ContentType)
description: Recupera il tipo di contenuto dell'icona.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- API di streaming multimediale del Metodo ContentType
- API di streaming multimediale del Metodo ContentType, interfaccia IDeviceIcon
- API di streaming multimediale dell'interfaccia IDeviceIcon, Metodo ContentType
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872366"
---
# <a name="ideviceiconcontenttype-method"></a>Metodo IDeviceIcon:: ContentType

Recupera il tipo di contenuto dell'icona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve un puntatore al tipo di contenuto dell'icona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

