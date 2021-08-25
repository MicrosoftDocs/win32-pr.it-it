---
description: Specifica il modo in cui IPropertyDescription::FormatForDisplay deve formattare il valore della proprietà booleanFormat come stringa.
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6ed13194fa18ba558c9c7fbac8fb7cd4317b67
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623717"
---
# <a name="booleanformat"></a>booleanFormat

Specifica il modo [**in cui IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formattare il valore della proprietà come stringa. Questo è applicabile solo se <displayInfo displayType="String"> . Deve essere presente un solo [elemento booleanFormat]() per ogni [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [booleanFormat,]() le impostazioni predefinite dell'attributo vengono applicate alla descrizione della proprietà.

## <a name="syntax"></a>Sintassi


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
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
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>formatAs</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è YesNo &quot; . I valori validi sono i seguenti. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>YesNo</td>
<td>Valore predefinito. Formatta il valore come &quot; Sì &quot; o &quot; &quot; No. Richiede che il tipo di proprietà sia booleano.</td>
</tr>
<tr class="even">
<td>Onoff</td>
<td>Formatta il valore come &quot; On &quot; o &quot; &quot; Off. Richiede che il tipo di proprietà sia booleano.</td>
</tr>
<tr class="odd">
<td>TrueFalse</td>
<td>Formatta il valore come &quot; True &quot; o &quot; &quot; False. Richiede che il tipo di proprietà sia booleano.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
