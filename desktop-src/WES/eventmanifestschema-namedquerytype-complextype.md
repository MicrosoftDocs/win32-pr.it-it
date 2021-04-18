---
title: Tipo complesso NamedQueryType
description: Non usato. Definisce un elenco di query denominate che eseguono una query sulla stringa del messaggio di evento per un valore ed eseguono un'azione specificata, se trovata. | Tipo complesso NamedQueryType
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- Log eventi di tipo complesso NamedQueryType
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321626"
---
# <a name="namedquerytype-complex-type"></a>Tipo complesso NamedQueryType

Non usato. Definisce un elenco di query denominate che eseguono una query sulla stringa del messaggio di evento per un valore ed eseguono un'azione specificata, se trovata.

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                       | Tipo                                                                             | Descrizione                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**patternMaps**](eventmanifestschema-patternmaps-namedquerytype-element.md) | [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) | Definisce un elenco di coppie di espressioni regolari utilizzate per modificare la stringa del messaggio.<br/> |



## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come utilizzare l'elemento [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) . Questo esempio accetta il contenuto della stringa del messaggio e lo inserisce nella stringa https://www .*MessageString*. com. Sostituisce quindi la stringa del messaggio con il risultato. Se, ad esempio, la stringa del messaggio contiene Microsoft, la query sostituirà la stringa di messaggio Microsoft con https://www.Microsoft.com .


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





