---
title: Tipo complesso QueryListType
description: Definisce un elenco di query che possono contenere un set di selettori ed eliminatori utilizzati per includere o escludere eventi dal set di risultati.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- EventLog di tipo complesso QueryListType
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1692427538dcd500cd4190839ffcc148c7358e0aee7f5a27b4906192a0810b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904161"
---
# <a name="querylisttype-complex-type"></a>Tipo complesso QueryListType

Definisce un elenco di query che possono contenere un set di selettori ed eliminatori utilizzati per includere o escludere eventi dal set di risultati.

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
| [**Query**](queryschema-query-querylisttype-element.md) | [**Tipo di query**](queryschema-querytype-complextype.md) | Definisce un set di selettori ed eliminatori utilizzati per includere o escludere eventi dal set di risultati.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





