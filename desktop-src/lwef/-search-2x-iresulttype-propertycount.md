---
title: Proprietà IResultType PropertyCount (WdsSharedIDL.h)
description: Questa proprietà contiene il numero di proprietà esposte dal tipo.
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- Proprietà PropertyCount Funzionalità dell'Windows legacy
- Proprietà PropertyCount Legacy Windows Environment Features , interfaccia IResultType
- Interfaccia IResultType Legacy Windows Environment Features , proprietà PropertyCount
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
ms.openlocfilehash: 6952f2efb6e0d14be22daf71e352747915b2ba05bf543d764ee9af5f496715ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014631"
---
# <a name="iresulttypepropertycount-property"></a>Proprietà IResultType::P ropertyCount

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Questa proprietà contiene il numero di proprietà esposte dal tipo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valore proprietà

restituisce l'indirizzo del numero di proprietà esposte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





