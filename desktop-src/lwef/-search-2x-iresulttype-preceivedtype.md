---
title: Proprietà IResultType PreceivedType (WdsSharedIDL. h)
description: Questa proprietà contiene la stringa utilizzata per identificare il tipo nell'indice.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà PreceivedType
- Proprietà PreceivedType caratteristiche dell'ambiente Windows legacy, interfaccia IResultType
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultType, proprietà PreceivedType
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873601"
---
# <a name="iresulttypepreceivedtype-property"></a>IResultType::P proprietà receivedType

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Questa proprietà contiene la stringa utilizzata per identificare il tipo nell'indice.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valore proprietà

Restituisce l'indirizzo della stringa identifyint il tipo nell'indice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





