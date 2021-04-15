---
title: Proprietà IResultType PropertyCount (WdsSharedIDL. h)
description: Questa proprietà contiene il numero di proprietà esposte dal tipo.
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- Funzionalità dell'ambiente Windows legacy della Proprietà PropertyCount
- Proprietà PropertyCount caratteristiche dell'ambiente Windows legacy, interfaccia IResultType
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultType, Proprietà PropertyCount
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1804c0abd249d93470cb2570f5bd58c600e8d3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517391"
---
# <a name="iresulttypepropertycount-property"></a>IResultType::P proprietà ropertyCount

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Questa proprietà contiene il numero di proprietà esposte dal tipo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valore proprietà

Restituisce l'indirizzo del numero di proprietà esposte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





