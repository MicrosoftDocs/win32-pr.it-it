---
title: Tipo complesso PatternMapListType
description: Non usato. Definisce un elenco di coppie di espressioni regolari usate per modificare la stringa del messaggio.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- EventLog di tipo complesso PatternMapListType
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbf96f7033f353662578e477fb8e35e0bfcda6db390f6492e29840e5e1faa5cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136204"
---
# <a name="patternmaplisttype-complex-type"></a>Tipo complesso PatternMapListType

Non usato. Definisce un elenco di coppie di espressioni regolari usate per modificare la stringa del messaggio.

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                         | Tipo                                                                     | Descrizione                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**patternMap**](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md) | Definisce un mapping tra due espressioni regolari. Un'espressione viene usata per trovare una stringa corrispondente nella stringa di messaggio e l'altra viene usata per modificare la stringa prima che il servizio la inserisca nuovamente nella stringa del messaggio. Viene usato il primo mapping dei criteri corrispondente e non vengono tentati altri modelli.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





