---
description: Non supportato in Windows 7 e versioni successive. Specifica il controllo da usare nel generatore di query.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f05800fc026c61a4ea50098fb1d8f4deb98d971c9eecfed478d71bd3c01033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823561"
---
# <a name="querycontrol"></a>queryControl

Non supportato in Windows 7 e versioni successive. Specifica il controllo da usare nel generatore di query. Deve essere presente un solo [elemento queryControl]() per ogni [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [queryControl,]() le impostazioni dell'attributo predefinite vengono applicate alla descrizione della proprietà.

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
| [displayInfo](./propdesc-schema-displayinfo.md) | Nessuno           |



 

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
<td>Pubblica. facoltativo. Il valore predefinito &quot; è &quot; Default. I valori validi sono i seguenti. 
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
<td>Valore predefinito. Usa il controllo predefinito, in base <typeInfo type=&quot;&quot;> all'attributo . I tipi predefiniti sono elencati di seguito. Qualsiasi altro tipo comporta l'uso del &quot; controllo &quot; Text. 
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
<td>Stringa (multivalore)</td>
<td>MultiValueText</td>
</tr>
<tr class="odd">
<td>Numero o dimensioni</td>
<td>NumericText</td>
</tr>
<tr class="even">
<td>Number o Size (enum)</td>
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
<td>Usa il controllo calendario a discesa.</td>
</tr>
<tr class="even">
<td>CheckboxDropList</td>
<td>Usa il controllo elenco con caselle di controllo.</td>
</tr>
<tr class="odd">
<td>Elenco a discesa</td>
<td>Usa il controllo elenco a discesa.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Usa il controllo di modifica del testo multivalore.</td>
</tr>
<tr class="odd">
<td>NumericText</td>
<td>Usa il controllo di modifica del testo numerico.</td>
</tr>
<tr class="even">
<td>Classificazione</td>
<td>Usa il controllo classificazione a 5 stelle.</td>
</tr>
<tr class="odd">
<td>Testo</td>
<td>Usa il controllo di modifica del testo.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
