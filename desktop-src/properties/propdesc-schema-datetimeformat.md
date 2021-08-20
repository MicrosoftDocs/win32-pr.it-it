---
description: Specifica il modo in cui IPropertyDescription::FormatForDisplay deve formattare il valore della proprietà come stringa. Questo è applicabile solo se <displayInfo displayType=&\#0034;DateTime&\#0034;> .
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: Datetimeformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a0719a5aca399af56a66d0181d6e4b175a520f789de9b5158ba0af5d8efab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056096"
---
# <a name="datetimeformat"></a>Datetimeformat

Specifica il modo [**in cui IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formattare il valore della proprietà come stringa. Questo è applicabile solo se <displayInfo displayType="DateTime"> . Deve essere presente un solo [elemento dateTimeFormat]() per ogni [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se sono presenti più elementi, viene usato l'ultimo. Se non [viene specificato alcun elemento dateTimeFormat,]() le impostazioni predefinite dell'attributo vengono applicate alla descrizione della proprietà.

## <a name="syntax"></a>Sintassi


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
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
<td>formatAs</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è &quot; Generale. I valori validi sono i seguenti. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Generale</td>
<td>Valore predefinito. Formatta il valore di data e ora <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>usando SHFormatDateTime.</strong></a> Usare gli <em>attributi formatTimeAs</em> e <em>formatDateAs</em> per specificare come vengono formattate l'ora e la data. Richiede che il tipo di proprietà sia DateTime.</td>
</tr>
<tr class="even">
<td>Month</td>
<td>Formatta il valore come uno dei mesi dell'anno. Richiede che il tipo di proprietà sia Int32. Il valore deve essere archiviato come valore numerico con 1 che rappresenta il primo mese dell'anno.</td>
</tr>
<tr class="odd">
<td>YearMonth</td>
<td>Formatta il valore come &quot; Year - &quot; Month. Richiede che il tipo di proprietà sia Int32. Il valore deve essere archiviato in modo che i due byte più alti specificano l'anno e i due byte inferiori specificano il mese.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>Formatta il valore come stringa semplice.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatTimeAs</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è &quot; ShortTime. Specifica il formato in cui visualizzare l'ora. Si applica <strong>quando formatAs= &quot; General &quot; </strong>. I valori validi sono i seguenti. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortTime</td>
<td>Valore predefinito. Visualizzare l'ora, &quot; ad esempio 19:48. &quot;</td>
</tr>
<tr class="even">
<td>LongTime</td>
<td>Visualizzare l'ora, &quot; ad esempio 19:48:33. &quot;</td>
</tr>
<tr class="odd">
<td>HideTime</td>
<td>Non visualizzare la parte relativa all'ora della data.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>formatDateAs</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è &quot; ShortDate. Specifica il formato in cui visualizzare la data. Si applica <strong>quando formatAs= &quot; General &quot; </strong>. I valori validi sono i seguenti. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortDate</td>
<td>Valore predefinito. Visualizzare la data, ad &quot; esempio 13/5/59. &quot;</td>
</tr>
<tr class="even">
<td>LongDate</td>
<td>Visualizzare la data, ad &quot; esempio mercoledì, 13 maggio 1959. &quot;</td>
</tr>
<tr class="odd">
<td>HideDate</td>
<td>Non visualizzare la parte relativa alla data.</td>
</tr>
<tr class="even">
<td>RelativeShortDate</td>
<td>Visualizzare la data come &quot; ShortDate &quot; , ma usare descrizioni relative, ad esempio &quot; il giorno &quot; prima, quando possibile.</td>
</tr>
<tr class="odd">
<td>RelativeLongDate</td>
<td>Visualizzare la data, ad &quot; esempio LongDate &quot; , ma usare descrizioni relative, ad esempio &quot; il giorno &quot; prima, quando possibile.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
