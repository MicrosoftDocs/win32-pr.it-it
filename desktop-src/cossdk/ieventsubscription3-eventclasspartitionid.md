---
description: GUID della partizione dell'oggetto della classe di evento.
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: 'Proprietà IEventSubscription3:: EventClassPartitionID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassPartitionID
- IEventSubscription3.get_EventClassPartitionID
- IEventSubscription3.put_EventClassPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: d41d3e2a170deffb73f1f533226421d88f150c01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524202"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a>Proprietà IEventSubscription3:: EventClassPartitionID

GUID della partizione dell'oggetto della classe di evento.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_EventClassPartitionID(
  [in]          BSTR bstrEventClassPartitionID
);

HRESULT get_EventClassPartitionID(
  [out, retval] BSTR *pbstrEventClassPartitionID
);
```



## <a name="property-value"></a>Valore proprietà

Stringa contenente il GUID della partizione della classe di evento.

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

 

 




