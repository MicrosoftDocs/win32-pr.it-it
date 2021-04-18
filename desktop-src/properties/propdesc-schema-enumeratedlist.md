---
description: 'Specifica il modo in cui IPropertyDescription:: FormatForDisplay deve formattare il valore della proprietà come stringa.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312550"
---
# <a name="enumeratedlist"></a>enumeratedList

Specifica il modo in cui [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formattare il valore della proprietà come stringa. Influenza inoltre il modo in cui la proprietà può essere raggruppata o i valori da visualizzare nell'elenco se "editControl" è un listblox. Questa operazione è applicabile solo se <displayInfo displayType="Enumerated"> . Deve essere presente un solo elemento [enumeratedList]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [enumeratedList]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.

## <a name="syntax"></a>Sintassi


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                   | Elementi figlio                               |
|--------------------------------------------------|----------------------------------------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | [enum](./propdesc-schema-enum.md)           |
|                                                  | [enumRange](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a>Attributi



| Attributo          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| defaultText        | Pubblica. facoltativo. Specificare il testo predefinito da usare se viene assegnato un valore a [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) che non esegue il mapping a uno degli elementi enumerati nell'elenco. La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto a una stringa di visualizzazione. usare il riferimento, in modo che possa essere localizzato.                              |
| useValueForDefault | Pubblica. facoltativo. Se si imposta questa opzione su "true", [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) utilizzerà il valore così com'è, se il valore non viene mappato a uno degli elementi enumerati nell'elenco. Per **IPropertyDescription:: FormatForDisplay**, impostando questo valore su "true" si ha la precedenza sull'impostazione di "DefaultText". Il valore predefinito è "false". |



 

 

 
