---
title: Tipo complesso TaskListType
description: Definisce un elenco di attività utilizzate per identificare i componenti di un'applicazione.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- EventLog di tipo complesso TaskListType
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d59457aaeeefeec4b490b4c399a2faafb4f62c22e67a600f741ccc16b3abcaad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750907"
---
# <a name="tasklisttype-complex-type"></a>Tipo complesso TaskListType

Definisce un elenco di attività utilizzate per identificare i componenti di un'applicazione.

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                       | Tipo                                                         | Descrizione                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**Attività**](eventmanifestschema-task-tasklisttype-element.md) | [**Tipo di attività**](eventmanifestschema-tasktype-complextype.md) | Definisce un componente o un sottocomponente di un'applicazione.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





