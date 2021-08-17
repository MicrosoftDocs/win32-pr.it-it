---
title: Interfaccia IPropertyFilter (WdsSharedIDL.h)
description: Espone le proprietà utilizzate per filtrare la query.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Interfaccia IPropertyFilter Funzionalità dell'Windows legacy
- Interfaccia IPropertyFilter Legacy Windows Environment Features , descritta
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5bc406661492702e4a012cab58a2e0a3e08507aeaa13d10b010f14ce31e6fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481095"
---
# <a name="ipropertyfilter-interface"></a>Interfaccia IPropertyFilter

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Espone le proprietà utilizzate per filtrare la query.

## <a name="members"></a>Membri

**L'interfaccia IPropertyFilter** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPropertyFilter** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IPropertyFilter** ha queste proprietà.



| Proprietà                                                                                      | Tipo di accesso           | Descrizione                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [**IPropertyFilter::IndexColumn**](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | Lettura/Scrittura<br/> | Nome della colonna indicizzata della proprietà in base a cui filtrare. <br/> |
| [**IPropertyFilter::LogicOperator**](-search-2x-ipropertyfilter-logicoperator.md)<br/> | Lettura/Scrittura<br/> | Operatore logico da usare quando si applica il filtro. <br/>       |
| [**IPropertyFilter::NestingDepth**](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | Lettura/Scrittura<br/> | Filtra la profondità all'interno di un set annidato di parentesi. <br/> |
| [**IPropertyFilter::Text**](-search-2x-ipropertyfilter-text.md)<br/>                   | Lettura/Scrittura<br/> | Testo del filtro. <br/>                               |
| [**IPropertyFilter::UID**](-search-2x-ipropertyfilter-uid.md)<br/>                     | Lettura/Scrittura<br/> | UID per la proprietà in base a cui filtrare. <br/>                 |



 

## <a name="remarks"></a>Commenti

Queste proprietà vengono usate per filtrare la query.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

