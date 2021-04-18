---
description: Utilizzato per assegnare il testo enumerato a valori discreti.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312551"
---
# <a name="enum"></a>enum

Utilizzato per assegnare il testo enumerato a valori discreti. In [enumeratedList](./propdesc-schema-enumeratedlist.md)è possibile che esista un numero qualsiasi di questi elementi. A livello di codice, questi sono rappresentati come oggetti IPropertyEnumType, il cui metodo [**IPropertyEnumType:: GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) restituisce PET \_ DISCRETEVALUE.

## <a name="syntax"></a>Sintassi


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                         | Elementi figlio |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | Nessuno           |



 

## <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore     | Pubblica. Obbligatorio. Valore discreto (stringa o numero) a cui assegnare il testo enumerato.                                                                                                                           |
| text      | Pubblica. Obbligatorio. Testo utilizzato per visualizzare il valore enumerato. La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto a una stringa di visualizzazione. utilizzare la stringa di visualizzazione indiretta in modo che possa essere localizzata. |
| tasti di scelta | **Windows 7 e versioni successive.** Pubblica. facoltativo. Elenco di valori mnemonico che possono essere usati per fare riferimento alla proprietà nelle query di ricerca. L'elenco è delimitato dal carattere " \| ".                                     |



 

 

 
