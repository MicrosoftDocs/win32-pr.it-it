---
title: Tipo complesso QueryListType
description: Definisce un elenco di query che possono contenere un set di selettori ed eliminati utilizzati per includere eventi in o escludere eventi dal set di risultati.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- Log eventi di tipo complesso QueryListType
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301548"
---
# <a name="querylisttype-complex-type"></a>Tipo complesso QueryListType

Definisce un elenco di query che possono contenere un set di selettori ed eliminati utilizzati per includere eventi in o escludere eventi dal set di risultati.

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                  | Tipo                                                   | Descrizione                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**Query**](queryschema-query-querylisttype-element.md) | [**QueryType**](queryschema-querytype-complextype.md) | Definisce un set di selettori ed eliminati utilizzati per includere eventi in o escludere eventi dal set di risultati.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





