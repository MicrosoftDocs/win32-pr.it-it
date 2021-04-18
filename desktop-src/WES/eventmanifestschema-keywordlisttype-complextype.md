---
title: Tipo complesso KeywordListType
description: Definisce un elenco di parole chiave che categorizzano gli eventi. | Tipo complesso KeywordListType
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- Log eventi di tipo complesso KeywordListType
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321530"
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
| [**parola chiave**](eventmanifestschema-keyword-keywordlisttype-element.md) | [**KeywordType**](eventmanifestschema-keywordtype-complextype.md) | Definisce una parola chiave che identifica una categoria di eventi. È possibile specificare un massimo di 48 parole chiave.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





