---
description: Specifica il controllo da utilizzare quando si modifica la proprietà .
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdb47a3866c156ff10dba8eed4584f814793b863e8f615ae5e1a10b8d687ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118055991"
---
# <a name="editcontrol"></a>editControl

Specifica il controllo da utilizzare quando si modifica la proprietà . Deve essere presente un solo [elemento editControl]() per ogni [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [editControl,]() alla descrizione della proprietà vengono applicate le impostazioni predefinite dell'attributo.

Se , questo elemento viene ignorato perché non è possibile modificare una <typeInfo isInnate="true"> proprietà innata.

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
<td>Stringa (multivalore)</td>
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
<td>Usa il controllo calendario.</td>
</tr>
<tr class="odd">
<td>CheckboxDropList</td>
<td>Usa il controllo elenco con caselle di controllo.</td>
</tr>
<tr class="even">
<td>Elenco a discesa</td>
<td>Usa il controllo elenco a discesa.</td>
</tr>
<tr class="odd">
<td>MultiLineText</td>
<td>Usa il controllo di modifica del testo su più righe.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Usa il controllo di modifica del testo multivalore.</td>
</tr>
<tr class="odd">
<td>Classificazione</td>
<td>Usa il controllo classificazione a 5 stelle.</td>
</tr>
<tr class="even">
<td>Testo</td>
<td>Usa il controllo di modifica del testo.</td>
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



 

 

 
