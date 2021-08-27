---
description: Moniker dei sottoscrittori.
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: Proprietà IEventSubscription2SubscriberMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: cdd783a4e3f8d29d3ffc4ae279602db71c3ee16247ad58c6f23aa10bb3ba5350
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070671"
---
# <a name="ieventsubscription2subscribermoniker-property"></a>Proprietà IEventSubscription2::SubscriberMoniker

Moniker del sottoscrittore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a>Valore proprietà

Stringa del moniker che specifica il sottoscrittore.

## <a name="error-codes"></a>Codici di errore

Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL e S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




