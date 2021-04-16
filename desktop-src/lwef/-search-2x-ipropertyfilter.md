---
title: Interfaccia IPropertyFilter (WdsSharedIDL. h)
description: Espone le proprietà utilizzate per filtrare la query.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilter
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilter, descritte
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
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518310"
---
# <a name="ipropertyfilter-interface"></a>Interfaccia IPropertyFilter

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Espone le proprietà utilizzate per filtrare la query.

## <a name="members"></a>Membri

L'interfaccia **IPropertyFilter** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPropertyFilter** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IPropertyFilter** ha queste proprietà.



| Proprietà                                                                                      | Tipo di accesso           | Descrizione                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [**IPropertyFilter:: IndexColumn**](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | Lettura/Scrittura<br/> | Nome della colonna indicizzata della proprietà in base a cui filtrare. <br/> |
| [**IPropertyFilter::LogicOperator**](-search-2x-ipropertyfilter-logicoperator.md)<br/> | Lettura/Scrittura<br/> | Operatore logico da usare quando si applica il filtro. <br/>       |
| [**IPropertyFilter::NestingDepth**](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | Lettura/Scrittura<br/> | Filtra la profondità all'interno di un set annidato di parentesi. <br/> |
| [**IPropertyFilter:: Text**](-search-2x-ipropertyfilter-text.md)<br/>                   | Lettura/Scrittura<br/> | Testo del filtro. <br/>                               |
| [**IPropertyFilter:: UID**](-search-2x-ipropertyfilter-uid.md)<br/>                     | Lettura/Scrittura<br/> | UID per la proprietà in base a cui filtrare. <br/>                 |



 

## <a name="remarks"></a>Commenti

Queste proprietà vengono utilizzate per filtrare la query.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

