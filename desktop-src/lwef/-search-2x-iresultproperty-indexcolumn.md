---
title: Proprietà IResultProperty IndexColumn (WdsSharedIDL. h)
description: Nome della colonna proprietà nell'indice.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- Funzionalità dell'ambiente Windows legacy della Proprietà IndexColumn
- Proprietà IndexColumn caratteristiche dell'ambiente Windows legacy, interfaccia IResultProperty
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultProperty, Proprietà IndexColumn
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
ms.openlocfilehash: 7a4749f9ba1200f1af8ba202056e48f0123e8402
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873605"
---
# <a name="iresultpropertyindexcolumn-property"></a>Proprietà IResultProperty:: IndexColumn

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Nome della colonna proprietà nell'indice.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Valore proprietà

Restituisce un puntatore al nome della colonna nell'indice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





