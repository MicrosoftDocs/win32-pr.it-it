---
title: Tipo complesso TaskListType
description: Definisce un elenco di attività utilizzate per identificare i componenti di un'applicazione.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- Log eventi di tipo complesso TaskListType
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400198"
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
| [**attività**](eventmanifestschema-task-tasklisttype-element.md) | [**TaskType**](eventmanifestschema-tasktype-complextype.md) | Definisce un componente o un sottocomponente di un'applicazione.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





