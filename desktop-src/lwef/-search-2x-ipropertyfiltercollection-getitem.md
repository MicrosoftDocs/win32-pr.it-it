---
title: Proprietà GetItem di IPropertyFilterCollection (WdsSharedIDL. h)
description: Restituisce un filtro specifico all'interno della raccolta.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- Proprietà GetItem funzionalità dell'ambiente Windows legacy
- Proprietà GetItem funzionalità dell'ambiente Windows legacy, interfaccia IPropertyFilterCollection
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection, proprietà GetItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964069"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a>Proprietà IPropertyFilterCollection:: GetItem

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Restituisce un filtro specifico all'interno della raccolta.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Valore proprietà

Imposta l'indirizzo del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





