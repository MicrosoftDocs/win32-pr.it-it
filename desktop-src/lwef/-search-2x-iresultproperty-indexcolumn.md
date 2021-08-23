---
title: Proprietà IndexColumn IResultProperty (WdsSharedIDL.h)
description: Nome della colonna Properties nell'indice.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- Proprietà IndexColumn Funzionalità dell'Windows legacy
- Proprietà IndexColumn Legacy Windows funzionalità dell'ambiente, interfaccia IResultProperty
- Interfaccia IResultProperty Legacy Windows Environment Features , proprietà IndexColumn
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a78d91b9e823dbf8d3c7a2273247706f9ae2bb04c6f64d08f5555eb875023c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754774"
---
# <a name="iresultpropertyindexcolumn-property"></a>Proprietà IResultProperty::IndexColumn

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Nome della colonna Properties nell'indice.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Valore proprietà

restituisce un puntatore al nome della colonna nell'indice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





