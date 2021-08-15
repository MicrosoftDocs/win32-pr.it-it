---
title: Proprietà IPropertyFilterCollection AddItem (WdsSharedIDL.h)
description: Aggiunge un nuovo filtro alla raccolta.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- Proprietà AddItem Funzionalità dell'Windows legacy
- Proprietà AddItem Legacy Windows Environment Features , interfaccia IPropertyFilterCollection
- Interfaccia IPropertyFilterCollection Legacy Windows Environment Features , proprietà AddItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeafec95549fefa244dff6ff44ad9110150ae1b410e38b423a0a31f09cf54194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755448"
---
# <a name="ipropertyfiltercollectionadditem-property"></a>Proprietà IPropertyFilterCollection::AddItem

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Aggiunge un nuovo filtro alla raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Valore proprietà

restituisce un puntatore all'indirizzo per il nuovo filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





