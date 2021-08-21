---
description: Specifica come configurare il motore di Windows di ricerca rispetto a una determinata definizione di proprietà.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbcfc901dfb4610210c4990c962b5251710e5653
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465628"
---
# <a name="searchinfo"></a>searchInfo

Specifica come configurare il motore di Windows di ricerca rispetto a una determinata definizione di proprietà. Se non viene specificato alcun elemento [searchInfo,]() la proprietà non viene inclusa nel motore Windows di ricerca. Questo elemento è stato modificato per Windows 7.

## <a name="syntax-for-windows-7"></a>Sintassi per Windows 7


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a>Sintassi per Windows Vista


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                   | Elementi figlio |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | Nessuno           |



 

## <a name="attributes"></a>Attributi




| Attributo | Descrizione | 
|-----------|-------------|
| inInvertedIndex | Pubblica. facoltativo. Indica se il valore della proprietà deve essere archiviato nell'indice invertito. Ciò consente agli utenti finali di eseguire query full-text sui valori di questa proprietà. Il valore predefinito è "false". | 
| isColumn | Pubblica. facoltativo. Indica se la proprietà deve essere archiviata anche nel database di ricerca di Windows come colonna, in modo che i fornitori di software indipendenti (ISV) possano creare query basate su predicato, ad esempio "Select * Where "System.Title"='qqq'"). Se l'autore dello schema vuole consentire agli utenti finali (o agli sviluppatori) di creare query basate su predicato sulle proprietà, deve essere impostato su "true". Il valore predefinito è "false". | 
| isColumnSparse | Pubblica. facoltativo. Il valore predefinito è "true". Se la proprietà è multivalore, questo attributo è sempre "true". | 
| columnIndexType | Pubblica. facoltativo. Per ottimizzare l'ordinamento e il raggruppamento, Windows motore di ricerca può creare indici secondari per le proprietà con isColumn="true". Questo attributo è utile solo quando inInvertedIndex è "true" in Windows Vista o quando isColumn è "true" in Windows 7. Se la proprietà tende a essere ordinata frequentemente in base agli utenti, questo attributo deve essere specificato. Il valore predefinito in Windows Vista è "NotIndexed". Il valore predefinito in Windows 7 è "OnDemand". I valori seguenti sono validi.<ul><li><strong>NotIndexed:</strong>non compilare mai un indice dei valori.</li><li><strong>OnDisk:</strong>consente di compilare un indice dei valori per impostazione predefinita per questa proprietà.</li><li><strong>OnDiskAll</strong> (solo Windows 7 e versioni successive): creare un indice dei valori per impostazione predefinita per questa proprietà e, se si tratta di una proprietà vettore, anche un indice dei valori per tutti i valori di vettore concatenati.</li><li><strong>OnDiskVector</strong> (solo Windows 7 e versioni successive): creare un indice dei valori per impostazione predefinita per i valori del vettore concatenato.</li><li><strong>OnDemand</strong> (solo Windows 7 e versioni successive): compila solo gli indici dei valori su richiesta, ovvero solo la prima volta che vengono usati per una query.</li></ul> | 
| Maxsize | Pubblica. facoltativo. Dimensioni massime, in byte, consentite per una determinata proprietà archiviata nel database Windows di ricerca. Il valore predefinito è:<ul><li><strong>Windows Vista:</strong>128 byte</li><li><strong>Windows 7 e versioni successive</strong>: 512 byte</li></ul>Si noti che questa dimensione massima viene misurata in byte, non in caratteri. Il numero massimo di caratteri dipende dalla codifica.<br /> | 
| tasti di scelta | <strong>Windows 7 e versioni successive.</strong> Pubblica. facoltativo. Elenco di valori mnemoici che possono essere usati per fare riferimento alla proprietà nelle query di ricerca. L'elenco è delimitato da '|' carattere. | 




 

 

 
