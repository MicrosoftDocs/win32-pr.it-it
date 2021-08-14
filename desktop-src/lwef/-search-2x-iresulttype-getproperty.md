---
title: Proprietà GetProperty IResultType (WdsSharedIDL.h)
description: Questa proprietà contiene informazioni sulla proprietà specificate.
ms.assetid: 04c810f2-c781-4384-93ae-1060466e2bc4
keywords:
- Proprietà GetProperty Funzionalità dell'Windows legacy
- Proprietà GetProperty Legacy Windows Environment Features , interfaccia IResultType
- Interfaccia IResultType Legacy Windows Environment Features , proprietà GetProperty
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
ms.openlocfilehash: f35a0f2bce8fb4e098a2452b6d5575fa9843283562f7f1d051b588d9a0c8cd05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481105"
---
# <a name="iresulttypegetproperty-property"></a>Proprietà IResultType::GetProperty

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Questa proprietà contiene informazioni sulla proprietà specificate.

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

Imposta l'indirizzo delle informazioni sulla proprietà specificate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





