---
description: Contenitore per uno o più elementi propertyDescription singoli.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310117"
---
# <a name="propertydescriptionlist"></a>propertyDescriptionList

Contenitore per uno o più elementi [PropertyDescription](./propdesc-schema-propertydescription.md) singoli. Un file di schema della descrizione della proprietà. propdesc deve contenere almeno un elemento [propertyDescriptionList]() .

## <a name="syntax"></a>Sintassi


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                        | Elementi figlio                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [schema](./propdesc-schema-entry.md) | [propertyDescription](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                               |
|-----------|---------------------------------------------------------------------------|
| publisher | Pubblica. Obbligatorio. Nome visualizzato del server di pubblicazione che fornisce lo schema. |
| product   | Pubblica. Obbligatorio. Nome visualizzato del prodotto che fornisce lo schema.   |



 

## <a name="remarks"></a>Commenti

Il [propertyDescriptionList]() non deve essere confuso con "elenchi di proprietà" e [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), che sono completamente distinti.

 

 
