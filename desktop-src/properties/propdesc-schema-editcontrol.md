---
description: Specifica il controllo da utilizzare durante la modifica della proprietà.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967584"
---
# <a name="editcontrol"></a>editControl

Specifica il controllo da utilizzare durante la modifica della proprietà. Deve essere presente un solo elemento [editControl]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [editControl]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.

Se <typeInfo isInnate="true"> , questo elemento viene ignorato perché non è possibile modificare una proprietà innata.

## <a name="syntax"></a>Sintassi


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
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
<th>Tipo</th>
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
<td>Datetime</td>
<td>Calendario</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Calendario</td>
<td>Usa il controllo Calendar.</td>
</tr>
<tr class="odd">
<td>CheckboxDropList</td>
<td>Usa il controllo elenco con le caselle di controllo.</td>
</tr>
<tr class="even">
<td>DropList</td>
<td>Usa il controllo elenco a discesa.</td>
</tr>
<tr class="odd">
<td>MultiLineText</td>
<td>Utilizza il controllo di modifica del testo su più righe.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Utilizza il controllo di modifica del testo multivalore.</td>
</tr>
<tr class="odd">
<td>Classificazione</td>
<td>Usa il controllo della classificazione a 5 stelle.</td>
</tr>
<tr class="even">
<td>Testo</td>
<td>Utilizza il controllo di modifica del testo.</td>
</tr>
<tr class="odd">
<td>IconList</td>
<td><strong>Windows 7 e versioni successive.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
