---
description: Specifica le informazioni di visualizzazione di una proprietà.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0bbc3cf0f17d24672e30a110d95341c1cb902d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622087"
---
# <a name="displayinfo"></a>displayInfo

Specifica le informazioni di visualizzazione di una proprietà. Deve essere presente un solo [elemento displayInfo]() per ogni [propertyDescription.](./propdesc-schema-propertydescription.md)

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [displayInfo,]() alla descrizione della proprietà vengono applicate le impostazioni predefinite dell'attributo.

## <a name="syntax"></a>Sintassi


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="FileName"/>
                                <xs:enumeration value="FilePath"/>
                                <xs:enumeration value="Hyperlink"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
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
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="value" type="xs:string" use="required"/>
                                <xs:attribute name="text" type="xs:string" use="required"/>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
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
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
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
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                   | Elementi figlio                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [proprietàDescrizione](./propdesc-schema-propertydescription.md) | [Stringformat](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [booleanFormat](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [numberFormat](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [Datetimeformat](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [enumeratedList](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [DrawControl](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [editControl](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [filterControl](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | [queryControl](./propdesc-schema-querycontrol.md) (Windows Vista. Non supportato in Windows 7 e versioni successive. |



 

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
<td>defaultColumnWidth</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è 20 &quot; .</td>
</tr>
<tr class="even">
<td>displayType</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è &quot; String. Specifica il tipo della stringa di visualizzazione. Una volta impostati qui, i <strong>valori PROPDESC_DISPLAYTYPE</strong> vengono recuperati da <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription::GetDisplayType</strong></a>. Di seguito sono riportati i tipi validi. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Stringa</td>
<td>Valore predefinito. Il valore viene visualizzato come stringa. Usare &quot; stringFormat &quot; per formattare. Il metodo restituisce PDDT_STRING.</td>
</tr>
<tr class="even">
<td>Numero</td>
<td>Impostazione predefinita per le proprietà numeriche. Il valore viene visualizzato come numero. Usare &quot; numberFormat &quot; per formattare. Il metodo restituisce PDDT_NUMBER.</td>
</tr>
<tr class="odd">
<td>Boolean</td>
<td>Valore predefinito se <typeInfo type=&quot;Boolean&quot;> . Il valore viene visualizzato come valore booleano. Usare &quot; booleanFormat &quot; per formattare. Il metodo restituisce PDDT_BOOLEAN.</td>
</tr>
<tr class="even">
<td>Datetime</td>
<td>Valore predefinito se <typeInfo type=&quot;DateTime&quot;> . Il valore viene visualizzato come data o ora. Usare &quot; dateTimeFormat &quot; per formattare. Il metodo restituisce PDDT_DATETIME.</td>
</tr>
<tr class="odd">
<td>Enumerazione</td>
<td>Il valore viene visualizzato come mapping di stringhe di visualizzazione fornito &quot; dall'elemento &quot; enumeratedList. Il metodo restituisce PDDT_ENUMERATED.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>allineamento</td>
<td>facoltativo. Il valore predefinito &quot; è &quot; Left. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sinistra</td>
<td>Valore predefinito. Allinea a sinistra.</td>
</tr>
<tr class="even">
<td>Center</td>
<td>Allinea al centro.</td>
</tr>
<tr class="odd">
<td>Destra</td>
<td>Allinea a destra.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>relativeDescriptionType</td>
<td>facoltativo. Il valore predefinito &quot; è &quot; Generale. Specifica come devono essere descritti due valori di questa proprietà quando vengono confrontati tra loro. In caso di equivalenza, &quot; viene &quot; sempre usato Same. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription::GetRelativeDescription</strong></a> e <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription::GetRelativeDescriptionType</strong></a> usano questo valore per determinare i nomi visualizzati della descrizione relativa da usare. 
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
<td>Valore predefinito. Usa &quot; diversi &quot;  /  &quot; . &quot;  /  &quot; &quot;</td>
</tr>
<tr class="even">
<td>Data</td>
<td>Valore predefinito se <typeInfo type=&quot;DateTime&quot;> . Usa earlier Same Later oppure usa la versione più recente di o &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; prima &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; della stessa &quot; versione &quot;  /  &quot; &quot;  /  &quot; &quot; successiva.</td>
</tr>
<tr class="odd">
<td>Dimensione</td>
<td>Usa &quot; più piccoli con le stesse dimensioni &quot;  /  &quot; &quot;  /  &quot; maggiori&quot;</td>
</tr>
<tr class="even">
<td>Conteggio</td>
<td>Usa &quot; più piccoli con le stesse dimensioni &quot;  /  &quot; &quot;  /  &quot; maggiori&quot;</td>
</tr>
<tr class="odd">
<td>Revisione</td>
<td>Usa &quot; in &quot;  /  &quot; precedenza lo stesso &quot;  /  &quot; in un secondo momento&quot;</td>
</tr>
<tr class="even">
<td>Length</td>
<td>Usa &quot; più breve e più a &quot;  /  &quot; &quot;  /  &quot; lungo&quot;</td>
</tr>
<tr class="odd">
<td>Durata</td>
<td>Usa &quot; più breve e più a &quot;  /  &quot; &quot;  /  &quot; lungo&quot;</td>
</tr>
<tr class="even">
<td>speed</td>
<td>Usa &quot; più lentamente lo stesso più &quot;  /  &quot; &quot;  /  &quot; velocemente&quot;</td>
</tr>
<tr class="odd">
<td>Tariffa</td>
<td>Usa &quot; più lentamente lo stesso più &quot;  /  &quot; &quot;  /  &quot; velocemente&quot;</td>
</tr>
<tr class="even">
<td>Classificazione</td>
<td>Usa &quot; più in basso lo stesso valore più &quot;  /  &quot; &quot;  /  &quot; alto&quot;</td>
</tr>
<tr class="odd">
<td>Priorità</td>
<td>Usa &quot; più in basso lo stesso valore più &quot;  /  &quot; &quot;  /  &quot; alto&quot;</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>defaultSortDirection</td>
<td>Specifica la direzione di ordinamento. Il valore predefinito &quot; è &quot; Crescente. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Crescente</td>
<td>Ordina in ordine crescente.</td>
</tr>
<tr class="even">
<td>Decrescente</td>
<td>Ordina in senso decrescente.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
