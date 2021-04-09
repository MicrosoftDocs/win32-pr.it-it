---
description: Assegna il testo di enumerazione a un intervallo di valori. Ogni elemento enumRange specifica un valore minimo e si estende fino al valore minimo dell'elemento successivo o fino a quando non sono presenti altri elementi enumRange.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967111"
---
# <a name="enumrange"></a>enumRange

Assegna il testo di enumerazione a un intervallo di valori. Ogni elemento [enumRange]() specifica un valore minimo e si estende fino al valore minimo dell'elemento successivo o fino a quando non sono presenti altri elementi enumRange.

## <a name="syntax"></a>Sintassi

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                         | Elementi figlio |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | Nessuno           |



 

## <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| minValue  | Pubblica. Obbligatorio. Valore minimo nell'intervallo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| setValue  | Pubblica. facoltativo. Quando un utente seleziona questa enumerazione da un controllo Proprietà ListBox, questo valore discreto viene assegnato come valore della proprietà.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| text      | Pubblica. facoltativo. Testo utilizzato per visualizzare il valore enumerato. La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto a una stringa di visualizzazione. utilizzare la stringa di visualizzazione indiretta in modo che possa essere localizzata.                                                                                                                                                                                                                                                                                                                                                                                                   |
| tasti di scelta | **Windows 7 e versioni successive.** Pubblica. facoltativo. Elenco di valori mnemonico che possono essere usati per fare riferimento alla proprietà nelle query di ricerca. L'elenco è delimitato dal carattere " \| ".                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| name      | Obbligatorio. Nome di proprietà canonico, univoco per il sistema; ad esempio, System. rating. Questo attributo è limitato a 64 caratteri. Il nome fa distinzione tra maiuscole e minuscole e deve usare la sintassi seguente: Publisher. Application. PropertyName. I metodi seguenti restituiscono questo valore: [**IExplorerCommand:: GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2:: GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)e [**IPropertyUI:: GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)). |



 

 

 
