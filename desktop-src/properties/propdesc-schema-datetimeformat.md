---
description: 'Specifica il modo in cui IPropertyDescription:: FormatForDisplay deve formattare il valore della proprietà come stringa. Questa operazione è applicabile solo se <displayInfo displayType=&\#0034;DateTime&\#0034;> .'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226893"
---
# <a name="datetimeformat"></a>dateTimeFormat

Specifica il modo in cui [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formattare il valore della proprietà come stringa. Questa operazione è applicabile solo se <displayInfo displayType="DateTime"> . Deve essere presente un solo elemento [DateTimeFormat]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Se sono presenti più elementi, viene usato l'ultimo. Se non viene fornito alcun elemento [DateTimeFormat]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.

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
<td>formato</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot; Generale &quot; . I valori validi sono i seguenti. 
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
<td>Valore predefinito. Formatta il valore di data e ora usando <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>. Usare gli attributi <em>formatTimeAs</em> e <em>formatDateAs</em> per specificare la modalità di formattazione di data e ora. Richiede che il tipo di proprietà sia DateTime.</td>
</tr>
<tr class="even">
<td>Month</td>
<td>Formatta il valore come uno dei mesi dell'anno. Richiede che il tipo di proprietà sia Int32. Il valore deve essere archiviato come valore numerico con 1 che rappresenta il primo mese dell'anno.</td>
</tr>
<tr class="odd">
<td>YearMonth</td>
<td>Formatta il valore come &quot; anno mese &quot; . Richiede che il tipo di proprietà sia Int32. Il valore deve essere archiviato in modo che i due byte più elevati specifichino l'anno e i due byte più bassi specifichino il mese.</td>
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
<td>Pubblica. facoltativo. Il valore predefinito è &quot; ShortTime &quot; . Specifica il formato in cui visualizzare l'ora. Si applica quando <strong>formats &quot; = &quot; General</strong>. I valori validi sono i seguenti. 
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
<td>Valore predefinito. Mostra l'ora, ad esempio &quot; 7:48 PM &quot; .</td>
</tr>
<tr class="even">
<td>Lunga</td>
<td>Mostra l'ora, ad esempio &quot; 7:48:33 PM &quot; .</td>
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
<td>Pubblica. facoltativo. Il valore predefinito è &quot; shortdate &quot; . Specifica il formato in cui visualizzare la data. Si applica quando <strong>formats &quot; = &quot; General</strong>. I valori validi sono i seguenti. 
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
<td>Valore predefinito. Mostra la data, ad esempio &quot; 5/13/59 &quot; .</td>
</tr>
<tr class="even">
<td>LongDate</td>
<td>Mostra la data come &quot; mercoledì, 13 maggio 1959 &quot; .</td>
</tr>
<tr class="odd">
<td>HideDate</td>
<td>Non visualizzare la parte relativa alla data.</td>
</tr>
<tr class="even">
<td>RelativeShortDate</td>
<td>Mostra la data come &quot; shortdate &quot; , ma usa le descrizioni relative, ad esempio &quot; ieri &quot; , quando possibile.</td>
</tr>
<tr class="odd">
<td>RelativeLongDate</td>
<td>Mostra la data come &quot; LongDate &quot; , ma usa le descrizioni relative, ad esempio &quot; ieri &quot; , quando possibile.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
