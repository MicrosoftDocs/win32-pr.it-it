---
title: Tipo complesso KeywordListType
description: Definisce un elenco di parole chiave che categorizzano gli eventi. | Tipo complesso KeywordListType
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- EventLog di tipo complesso KeywordListType
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: da027136deed48a97b2ea9384bc37a1a45d00650d90b8fd855ea8226e58583aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343647"
---
# <a name="keywordlisttype-complex-type"></a>Tipo complesso KeywordListType

Definisce un elenco di parole chiave che categorizzano gli eventi.

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                | Tipo                                                               | Descrizione                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Parola chiave**](eventmanifestschema-keyword-keywordlisttype-element.md) | [**Tipo di parola chiave**](eventmanifestschema-keywordtype-complextype.md) | Definisce una parola chiave che identifica una categoria di eventi. È possibile specificare un massimo di 48 parole chiave.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





