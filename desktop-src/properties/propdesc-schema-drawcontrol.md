---
description: Specifica il controllo da utilizzare quando si visualizza semplicemente la proprietà.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049788"
---
# <a name="drawcontrol"></a>drawControl

Specifica il controllo da utilizzare quando si visualizza semplicemente la proprietà. Deve essere presente un solo elemento [drawControl]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [drawControl]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.

Questo formato del controllo non consente la modifica delle proprietà.

## <a name="syntax"></a>Sintassi


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
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
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Predefinito</td>
<td>Valore predefinito. Usa il controllo predefinito, in base all' <typeInfo type=&quot;&quot;> attributo. Il tipo predefinito è &quot; String &quot; (multivalore) e il controllo predefinito è &quot; MultiValueText &quot; . Qualsiasi altro tipo comporta l'uso del &quot; &quot; controllo StaticText.</td>
</tr>
<tr class="even">
<td>MultiLineText</td>
<td>Usa il controllo testo a più righe.</td>
</tr>
<tr class="odd">
<td>MultiValueText</td>
<td>Usa il controllo di testo multivalore.</td>
</tr>
<tr class="even">
<td>PercentBar</td>
<td>Usa il controllo barra percentuale.</td>
</tr>
<tr class="odd">
<td>ProgressBar</td>
<td>Usa il controllo indicatore di stato.</td>
</tr>
<tr class="even">
<td>Classificazione</td>
<td>Usa il controllo della classificazione a 5 stelle.</td>
</tr>
<tr class="odd">
<td>StaticText</td>
<td>USA <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription:: FormatForDisplay</strong></a> per visualizzare il valore della proprietà.</td>
</tr>
<tr class="even">
<td>IconList</td>
<td><strong>Windows 7 e versioni successive.</strong> Enumerazione di icone.</td>
</tr>
<tr class="odd">
<td>BooleanCheckMark</td>
<td><strong>Windows 7 e versioni successive.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
