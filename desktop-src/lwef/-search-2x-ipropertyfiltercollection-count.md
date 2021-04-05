---
title: Proprietà Count IPropertyFilterCollection (WdsSharedIDL. h)
description: Numero di filtri nella raccolta.
ms.assetid: 9d656f06-eb1d-4cc6-9096-252f0fc65ae2
keywords:
- Proprietà Count funzionalità dell'ambiente Windows legacy
- Proprietà Count funzionalità dell'ambiente Windows legacy, interfaccia IPropertyFilterCollection
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection, proprietà Count
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.Count
- IPropertyFilterCollection.get_Count
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258a2ca8089cecb8e2e15fbe7e9e92ce1ed3468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741047"
---
# <a name="ipropertyfiltercollectioncount-property"></a>Proprietà IPropertyFilterCollection:: count

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Numero di filtri nella raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valore proprietà

Restituisce un puntatore al numero di filtri nella raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





