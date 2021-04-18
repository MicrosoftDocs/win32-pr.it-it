---
description: Specifica come configurare il motore di ricerca di Windows rispetto a una definizione di proprietà specificata.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310111"
---
# <a name="searchinfo"></a>searchInfo

Specifica come configurare il motore di ricerca di Windows rispetto a una definizione di proprietà specificata. Se non viene specificato alcun elemento [searchInfo]() , la proprietà non viene inclusa nel motore di ricerca di Windows. Questo elemento è stato modificato per Windows 7.

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
| [propertyDescription](./propdesc-schema-propertydescription.md) | nessuno           |



 

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>inInvertedIndex</td>
<td>Pubblica. facoltativo. Indica se il valore della proprietà deve essere archiviato nell'indice invertito. Ciò consente agli utenti finali di eseguire query full-text sui valori di questa proprietà. Il valore predefinito è &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>Pubblica. facoltativo. Indica se la proprietà deve essere archiviata anche nel database di ricerca di Windows come colonna, in modo che i fornitori di software indipendenti (ISV) possano creare query basate su predicato (ad esempio, &quot; Select * where &quot; System. title &quot; =' qqq ' &quot; ). Se l'autore dello schema desidera consentire agli utenti finali o agli sviluppatori di creare query basate su predicati sulle proprietà, è necessario impostare questa proprietà su &quot; true &quot; . Il valore predefinito è &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot;True&quot;. Se la proprietà è multivalore, questo attributo è sempre &quot; true &quot; .</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Pubblica. facoltativo. Per ottimizzare l'ordinamento e il raggruppamento, il motore di ricerca di Windows può creare indici secondari per le proprietà con la colonna = &quot; true &quot; . Questo attributo è utile solo quando inInvertedIndex è &quot; true &quot; in Windows Vista o quando la colonna è &quot; true &quot; in Windows 7. Se la proprietà tende a essere ordinata spesso dagli utenti, è necessario specificare questo attributo. Il valore predefinito in Windows Vista è &quot; NotIndexed &quot; . Il valore predefinito in Windows 7 è &quot; OnDemand &quot; . I valori seguenti sono validi.
<ul>
<li><strong>NotIndexed</strong>: mai compilare un indice di valore.</li>
<li><strong>Ondisk</strong>: compilare un indice valore per impostazione predefinita per questa proprietà.</li>
<li><strong>OnDiskAll</strong> (solo Windows 7 e versioni successive): compilare un indice valore per impostazione predefinita per questa proprietà e, se si tratta di una proprietà Vector, anche un indice valore per tutti i valori vettoriali concatenati.</li>
<li><strong>OnDiskVector</strong> (solo Windows 7 e versioni successive): compilare un indice valore per impostazione predefinita per i valori vettoriali concatenati.</li>
<li><strong>OnDemand</strong> (solo Windows 7 e versioni successive): solo gli indici del valore di compilazione per richiesta, ovvero solo la prima volta che vengono usati per una query.</li>
</ul></td>
</tr>
<tr class="odd">
<td>maxSize</td>
<td>Pubblica. facoltativo. Dimensione massima, in byte, consentita per una determinata proprietà archiviata nel database di ricerca di Windows. Il valore predefinito è:
<ul>
<li><strong>Windows Vista</strong>: 128 byte</li>
<li><strong>Windows 7 e versioni successive</strong>: 512 byte</li>
</ul>
Si noti che questa dimensione massima viene misurata in byte, non in caratteri. Il numero massimo di caratteri dipende dalla codifica.<br/></td>
</tr>
<tr class="even">
<td>tasti di scelta</td>
<td><strong>Windows 7 e versioni successive.</strong> Pubblica. facoltativo. Elenco di valori mnemonico che possono essere usati per fare riferimento alla proprietà nelle query di ricerca. L'elenco è delimitato dal carattere "|".</td>
</tr>
</tbody>
</table>



 

 

 
