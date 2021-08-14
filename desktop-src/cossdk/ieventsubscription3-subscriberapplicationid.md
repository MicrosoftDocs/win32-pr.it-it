---
description: GUID dell'applicazione del sottoscrittore.
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: Proprietà IEventSubscription3::SubscriberApplicationID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 723a64b4e34c58b49f0ffa0851af836a536ff86ea23ee1b966a8ec243267950c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306369"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a>Proprietà IEventSubscription3::SubscriberApplicationID

GUID dell'applicazione del sottoscrittore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a>Valore proprietà

Stringa contenente il GUID dell'applicazione sottoscrittore.

## <a name="error-codes"></a>Codici di errore

Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL e S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSubscription3**](ieventsubscription3.md)
</dt> </dl>

 

 




