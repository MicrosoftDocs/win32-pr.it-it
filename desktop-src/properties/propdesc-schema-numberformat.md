---
description: Specifica il modo in cui IPropertyDescription::FormatForDisplay deve formattare il valore della proprietà come stringa. Questa opzione è applicabile solo se <displayInfo displayType=&\#0034;Number&\#0034;> .
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: numberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6601e6647d8fa1ac8b8cb262d47192810583c93f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622687"
---
# <a name="numberformat"></a>numberFormat

Specifica il modo in [**cui IPropertyDescription::FormatForDisplay deve**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) formattare il valore della proprietà come stringa. Questa opzione è applicabile solo se <displayInfo displayType="Number"> . Deve essere presente un solo [elemento numberFormat]() per ogni [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se sono presenti più elementi, viene usato l'ultimo. Se non [viene specificato alcun elemento numberFormat,]() le impostazioni predefinite dell'attributo vengono applicate alla descrizione della proprietà.

## <a name="syntax"></a>Sintassi


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
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
<td>Pubblica. facoltativo. Il valore predefinito è &quot; &quot; Generale. Specifica il formato di visualizzazione. I valori validi sono i seguenti. 
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
<td>Valore predefinito. Visualizza il valore come numero non formattato.</td>
</tr>
<tr class="even">
<td>Percentuale</td>
<td>Formatta il valore come percentuale. Richiede che la proprietà sia UInt32.</td>
</tr>
<tr class="odd">
<td>ByteSize</td>
<td>Formatta il valore come byte, &quot; &quot; &quot; KB, MB &quot; o GB in base alle &quot; &quot; esigenze. Richiede che la proprietà sia UInt64.</td>
</tr>
<tr class="even">
<td>KBSize</td>
<td>Formatta il valore come &quot; &quot; KB, indipendentemente dal valore. Richiede che la proprietà sia UInt64.</td>
</tr>
<tr class="odd">
<td>SampleSize</td>
<td>Formatta il valore come numero di bit. Richiede che la proprietà sia UInt32.</td>
</tr>
<tr class="even">
<td>Velocità in bit</td>
<td>Formatta il valore in &quot; &quot; Kbps. Richiede che la proprietà sia UInt32. Il valore deve essere archiviato in &quot; unità bit al &quot; secondo.</td>
</tr>
<tr class="odd">
<td>SampleRate</td>
<td>Formatta il valore in &quot; &quot; KHz. Richiede che la proprietà sia UInt32. Il valore deve essere archiviato in &quot; unità &quot; Hertz.</td>
</tr>
<tr class="even">
<td>FrameRate</td>
<td>Formatta il valore in fotogrammi al secondo. Richiede che la proprietà sia UInt32. Il valore deve essere archiviato in &quot; unità kilo-frames-al &quot; secondo.</td>
</tr>
<tr class="odd">
<td>Pixel</td>
<td>Formatta il valore in unità di pixel. Richiede che la proprietà sia UInt32.</td>
</tr>
<tr class="even">
<td>DPI</td>
<td>Formatta il valore in punti per pollice. Richiede che la proprietà sia UInt32.</td>
</tr>
<tr class="odd">
<td>Durata</td>
<td>Formatta il valore come durata. Usare <formatDurationAs> per specificare il formato della durata. Richiede che la proprietà sia UInt64.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatDurationAs</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è hh:mm:ss &quot; . Si applica solo se <em>formatAs= &quot; Duration &quot; </em>. Richiede che la proprietà sia UInt64. I valori validi sono i seguenti. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>hh:mm</td>
<td>Formatta il valore in ore e minuti.</td>
</tr>
<tr class="even">
<td>hh:mm:ss</td>
<td>Valore predefinito. Formatta il valore in ore, minuti e secondi.</td>
</tr>
<tr class="odd">
<td>hh:mm:ss.fff</td>
<td>Formatta il valore in ore, minuti, secondi e millisecondi.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
