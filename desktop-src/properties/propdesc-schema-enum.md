---
description: Usato per assegnare testo enumerato a valori discreti.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1336a690fe7ac1e19a8606912a4f7d538d3842ab6a490d17b89f90f64bbfbc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970980"
---
# <a name="enum"></a>enum

Usato per assegnare testo enumerato a valori discreti. Un numero qualsiasi di questi elementi può esistere in [un oggetto enumeratedList](./propdesc-schema-enumeratedlist.md). A livello di codice, sono rappresentati come oggetti IPropertyEnumType, il cui metodo [**IPropertyEnumType::GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) restituisce PET \_ DISCRETEVALUE.

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
| text      | Pubblica. Obbligatorio. Testo utilizzato per visualizzare il valore enumerato. La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto alla stringa di visualizzazione. usare la stringa di visualizzazione indiretta in modo che possa essere localizzata. |
| tasti di scelta | **Windows 7 e versioni successive.** Pubblica. facoltativo. Elenco di valori mnemoici che possono essere usati per fare riferimento alla proprietà nelle query di ricerca. L'elenco è delimitato dal carattere ' \| '.                                     |



 

 

 
