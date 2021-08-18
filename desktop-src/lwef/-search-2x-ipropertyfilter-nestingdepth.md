---
title: Proprietà IPropertyFilter NestingDepth (WdsSharedIDL.h)
description: Filtra la profondità all'interno di un set annidato di parentesi.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- Proprietà NestingDepth Funzionalità Windows dell'ambiente legacy
- Proprietà NestingDepth Legacy Windows Environment Features , interfaccia IPropertyFilter
- Interfaccia IPropertyFilter Legacy Windows Environment Features , proprietà NestingDepth
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2499d7a3d5505f4cb428cbc8831ec0ea4e0a71843693f5a8ba1250995071df32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481209"
---
# <a name="ipropertyfilternestingdepth-property"></a>Proprietà IPropertyFilter::NestingDepth

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Filtra la profondità all'interno di un set annidato di parentesi.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a>Valore proprietà

Imposta il numero che indica la profondità delle parentesi annidate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





