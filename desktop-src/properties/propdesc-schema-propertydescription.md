---
description: Descrive una singola proprietà canonica univoca.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: proprietàDescrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1797880fbc9ce5bf56999c6fbd869b259f893f1391fbde6fca580da29dac3a61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011471"
---
# <a name="propertydescription"></a>proprietàDescrizione

Descrive una singola proprietà canonica univoca. Ogni proprietà di questo tipo che deve essere disponibile nel sistema deve avere un elemento [propertyDescription]() corrispondente.

## <a name="syntax-for-windows-7"></a>Sintassi per Windows 7


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a>Sintassi per Vista


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                           | Elementi figlio                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) | [searchInfo](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [labelInfo](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [Typeinfo](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [aliasInfo](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [displayInfo](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name      | Obbligatorio. Nome canonico della proprietà, univoco per il sistema. ad esempio `System.Rating` . Questa stringa è di tipo canonical-type ed è limitata a 64 caratteri. Il nome fa distinzione tra maiuscole e minuscole e deve usare la sintassi seguente: Publisher. Application.PropertyName. [**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) restituisce questo valore. |
| formatID  | Obbligatorio. Identificatore di formato della proprietà (FMTID). Il valore deve includere parentesi graffe di inclusione. ad esempio `{64440492-4C8B-11D1-8B70-080036B11A03}` . [**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) restituisce questo valore.                                                                                                                       |
| propID    | Obbligatorio. Identificatore della proprietà (PID); ad esempio `9` . [**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) restituisce questo valore. Questo valore deve essere maggiore o uguale a 2. I valori 0 e 1 sono riservati dal sistema.                                                                                                                  |



 

 

 
