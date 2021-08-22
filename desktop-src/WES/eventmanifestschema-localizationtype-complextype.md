---
title: Tipo complesso LocalizationType
description: Definisce un gruppo di risorse localizzate a cui si fa riferimento nel manifesto. | Tipo complesso LocalizationType
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- EventLog di tipo complesso LocalizationType
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a596ff981944943c193fb158f14aa04eafb0b0b3d4df660d2034c5b5d281be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055949"
---
# <a name="localizationtype-complex-type"></a>Tipo complesso LocalizationType

Definisce un gruppo di risorse localizzate a cui si fa riferimento nel manifesto.

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                         | Tipo                                                                       | Descrizione                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Risorse**](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | Definisce un gruppo di tabelle di stringhe che contengono le stringhe localizzate a cui si fa riferimento nel manifesto.<br/> |
| [**Stringtable**](eventmanifestschema-stringtable-localizationtype-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto.<br/>                             |



## <a name="attributes"></a>Attributi



| Nome            | Tipo   | Descrizione                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture         | string | Nome della lingua che identifica le impostazioni cultura delle stringhe localizzate nella tabella delle stringhe. Ad esempio, "en-US" per l'inglese (Stati Uniti).<br/> |
| fallbackCulture | string | Non usato.<br/>                                                                                                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





