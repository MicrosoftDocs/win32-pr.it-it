---
title: GetStreamPropertiesOperation.Completed - proprietà
description: Ottiene o imposta un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da GetStreamPropertiesAsync.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- Proprietà Completata API Streaming multimediale
- Proprietà completata API Streaming multimediale, interfaccia GetStreamPropertiesOperation
- Interfaccia GetStreamPropertiesOperation API Streaming multimediale , proprietà Completed
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6fc6982866ed97f70467d13cb5e899d94a1459266ca0149d12400d154aad784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100665"
---
# <a name="getstreampropertiesoperationcompleted-property"></a>GetStreamPropertiesOperation.Completed - proprietà

Ottiene o imposta un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da [**GetStreamPropertiesAsync.**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a>Valore proprietà

Gestore eventi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)
</dt> </dl>

 

 