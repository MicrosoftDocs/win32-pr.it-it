---
description: Criteri di filtro che governano la sottoscrizione.
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: 'Proprietà IEventSubscription2:: FilterCriteria'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1443a89433cff91a298e8c390fce8f1f64b99f1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127407"
---
# <a name="ieventsubscription2filtercriteria-property"></a>Proprietà IEventSubscription2:: FilterCriteria

Criteri di filtro che governano la sottoscrizione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a>Valore proprietà

Criteri di filtro o CLSID per una classe che implementa [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).

## <a name="error-codes"></a>Codici di errore

Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




