---
title: Proprietà GetProperty IResultType (WdsSharedIDL. h)
description: Questa proprietà contiene informazioni sulle proprietà specificate.
ms.assetid: 04c810f2-c781-4384-93ae-1060466e2bc4
keywords:
- Funzionalità di proprietà dell'ambiente Windows legacy della proprietà GetProperty
- Proprietà GetProperty ambiente Windows legacy, interfaccia IResultType
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultType, proprietà GetProperty
topic_type:
- apiref
api_name:
- IResultType.GetProperty
- IResultType.get_GetProperty
- IResultType.put_GetProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd62517e7db9fdc15841c443ba9010903ddea697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873602"
---
# <a name="iresulttypegetproperty-property"></a>Proprietà IResultType:: GetProperty

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Questa proprietà contiene informazioni sulle proprietà specificate.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GetProperty(
  [in]          VARIANT        index
);

HRESULT get_GetProperty(
  [out, retval] ISrsultPropery **prop
);
```



## <a name="property-value"></a>Valore proprietà

Imposta l'indirizzo delle informazioni sulle proprietà specificate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





