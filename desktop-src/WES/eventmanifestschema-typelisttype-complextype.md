---
title: Tipo complesso TypeListType
description: Definisce i tipi utilizzati nel manifesto.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- Log eventi di tipo complesso TypeListType
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302157"
---
# <a name="typelisttype-complex-type"></a>Tipo complesso TypeListType

Definisce i tipi utilizzati nel manifesto.

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Tipo                                                                           | Descrizione                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**intipi**](eventmanifestschema-intypes-typelisttype-element.md)   | [**InputTypeListType**](eventmanifestschema-inputtypelisttype-complextype.md) | Definisce un elenco di tipi di dati di input.<br/>                                                              |
| [**xmltypes**](eventmanifestschema-xmltypes-typelisttype-element.md) | [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)     | Definisce un elenco di tipi di output utilizzati dal servizio per determinare come eseguire il rendering di un tipo di dati di input.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





