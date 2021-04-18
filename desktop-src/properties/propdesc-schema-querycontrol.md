---
description: Non supportato in Windows 7 e versioni successive. Specifica il controllo da utilizzare nel generatore di query.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448b47038f82afb9f860209bfe89eb9e6eecb890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310115"
---
# <a name="querycontrol"></a>queryControl

Non supportato in Windows 7 e versioni successive. Specifica il controllo da utilizzare nel generatore di query. Deve essere presente un solo elemento [queryControl]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [queryControl]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.

## <a name="syntax"></a>Sintassi


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                   | Elementi figlio |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | nessuno           |



 

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
<td>controllo</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot; default &quot; . I valori validi sono i seguenti. 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Predefinito</td>
<td>Valore predefinito. Usa il controllo predefinito, in base all' <typeInfo type=&quot;&quot;> attributo. I tipi predefiniti sono elencati di seguito. Qualsiasi altro tipo comporta l'utilizzo del &quot; controllo di testo &quot; . 
<table>
<thead>
<tr class="header">
<th>ConditionType</th>
<th>Control</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>string</td>
<td>Testo</td>
</tr>
<tr class="even">
<td>String (multivalore)</td>
<td>MultiValueText</td>
</tr>
<tr class="odd">
<td>Numero o dimensioni</td>
<td>NumericText</td>
</tr>
<tr class="even">
<td>Numero o dimensione (enumerazione)</td>
<td>Elenco</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Calendario</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Boolean</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Usa il controllo booleano.</td>
</tr>
<tr class="odd">
<td>Calendario</td>
<td>Usa il controllo del calendario a discesa.</td>
</tr>
<tr class="even">
<td>CheckboxDropList</td>
<td>Usa il controllo elenco con le caselle di controllo.</td>
</tr>
<tr class="odd">
<td>DropList</td>
<td>Usa il controllo elenco a discesa.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Utilizza il controllo di modifica del testo multivalore.</td>
</tr>
<tr class="odd">
<td>NumericText</td>
<td>Utilizza il controllo di modifica del testo numerico.</td>
</tr>
<tr class="even">
<td>Classificazione</td>
<td>Usa il controllo della classificazione a 5 stelle.</td>
</tr>
<tr class="odd">
<td>Testo</td>
<td>Utilizza il controllo di modifica del testo.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
