---
description: Specifica il controllo da usare nel menu del filtro dell'intestazione.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac7424cf281c08f1d8de87686e95a38be3f4f3a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627547"
---
# <a name="filtercontrol"></a>filterControl

Specifica il controllo da usare nel menu del filtro dell'intestazione. Deve essere presente un solo [elemento filterControl]() per ogni [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [filterControl,]() le impostazioni predefinite dell'attributo vengono applicate alla descrizione della proprietà.

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
<td>controllo</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è &quot; Default. I valori validi sono i seguenti. 
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
<td>Valore predefinito. Usa il controllo predefinito, in base <typeInfo type=&quot;&quot;> all'attributo . Il tipo predefinito è &quot; DateTime &quot; e il controllo predefinito è &quot; &quot; Calendar. Qualsiasi altro tipo non comporta alcun controllo filtro speciale.</td>
</tr>
<tr class="even">
<td>Calendario</td>
<td>Usa il controllo calendario.</td>
</tr>
<tr class="odd">
<td>Classificazione</td>
<td>Usa il controllo classificazione a 5 stelle.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
