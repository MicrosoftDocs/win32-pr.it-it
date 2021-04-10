---
description: GUID della partizione del Sottoscrittore.
ms.assetid: 0b2411d3-cdc1-492c-a54f-ca3d3bd8b953
title: 'Proprietà IEventSubscription3:: SubscriberPartitionID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberPartitionID
- IEventSubscription3.get_SubscriberPartitionID
- IEventSubscription3.put_SubscriberPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: b09c41ac1b3a90c3275daf7afa0cd90fe2bb905c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225778"
---
# <a name="ieventsubscription3subscriberpartitionid-property"></a>Proprietà IEventSubscription3:: SubscriberPartitionID

GUID della partizione del Sottoscrittore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_SubscriberPartitionID(
  [in]          BSTR bstrSubscriberPartitionID
);

HRESULT get_SubscriberPartitionID(
  [out, retval] BSTR *pbstrSubscriberPartitionID
);
```



## <a name="property-value"></a>Valore proprietà

Stringa contenente il GUID della partizione del Sottoscrittore.

## <a name="error-codes"></a>Codici di errore

Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSubscription3**](ieventsubscription3.md)
</dt> </dl>

 

 




