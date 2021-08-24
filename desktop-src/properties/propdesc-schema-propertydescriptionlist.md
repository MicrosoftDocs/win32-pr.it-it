---
description: Contenitore per uno o più singoli elementi propertyDescription.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f22e5e8e2c90b1a9f9587117f684ebfb89c55ee702749248cb0a886d5ba8266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341841"
---
# <a name="propertydescriptionlist"></a>propertyDescriptionList

Contenitore per uno o più singoli [elementi propertyDescription.](./propdesc-schema-propertydescription.md) Un file di schema di descrizione della proprietà con estensione propdesc deve contenere almeno un [elemento propertyDescriptionList.]()

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
| [schema](./propdesc-schema-entry.md) | [proprietàDescrizione](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                               |
|-----------|---------------------------------------------------------------------------|
| publisher | Pubblica. Obbligatorio. Nome visualizzato del server di pubblicazione che fornisce lo schema. |
| product   | Pubblica. Obbligatorio. Nome visualizzato del prodotto che fornisce lo schema.   |



 

## <a name="remarks"></a>Commenti

[PropertyDescriptionList non]() deve essere confuso con gli "elenchi di proprietà" e [**IPropertyDescriptionList,**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)che sono completamente separati.

 

 
