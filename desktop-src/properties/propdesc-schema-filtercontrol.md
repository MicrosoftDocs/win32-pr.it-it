---
description: Specifica il controllo da utilizzare nel menu del filtro di intestazione.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c0de28eaa349b9a999ba39c1bad47aa01d43d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310124"
---
# <a name="filtercontrol"></a>filterControl

Specifica il controllo da utilizzare nel menu del filtro di intestazione. Deve essere presente un solo elemento [filterControl]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [filterControl]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.

## <a name="syntax"></a>Sintassi


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
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
<td>Valore predefinito. Usa il controllo predefinito, in base all' <typeInfo type=&quot;&quot;> attributo. Il tipo predefinito è &quot; DateTime &quot; e il controllo predefinito è &quot; Calendar &quot; . Qualsiasi altro tipo non produce alcun controllo filtro speciale.</td>
</tr>
<tr class="even">
<td>Calendario</td>
<td>Usa il controllo Calendar.</td>
</tr>
<tr class="odd">
<td>Classificazione</td>
<td>Usa il controllo della classificazione a 5 stelle.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
