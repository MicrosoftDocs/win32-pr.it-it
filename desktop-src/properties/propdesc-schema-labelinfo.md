---
description: Specifica la modalità di visualizzazione delle etichette della proprietà.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310121"
---
# <a name="labelinfo"></a>labelInfo

Specifica la modalità di visualizzazione delle etichette della proprietà. Deve essere presente un solo elemento [labelInfo]() per ogni elemento [PropertyDescription](./propdesc-schema-propertydescription.md) .

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [labelInfo]() , l'etichetta della proprietà non viene visualizzata; Tuttavia, si tratta in genere di un difetto.

## <a name="syntax"></a>Sintassi


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                   | Elementi figlio |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | nessuno           |



 

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
<td>label</td>
<td>Pubblica. facoltativo. Etichetta visualizzata nell'interfaccia utente (ad esempio, l'etichetta della colonna dettagli o il riquadro di anteprima). La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto a una stringa di visualizzazione. Utilizzare la stringa di visualizzazione indiretta perché può essere localizzata. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription:: GetDisplayName</strong></a> restituisce il nome visualizzato risolto.</td>
</tr>
<tr class="even">
<td>sortDescription</td>
<td>facoltativo. Specifica le stringhe offerte come opzioni di ordinamento. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription:: GetSortDescription</strong></a> restituisce questa descrizione di ordinamento. I valori seguenti forniscono le stringhe dell'interfaccia utente corrispondenti.
<ul>
<li>Generale: ordinamento in corso di ordinamento &quot; &quot;  /  &quot; in corso&quot;</li>
<li>AToZ: &quot; a all'inizio &quot;  /  &quot; Z all'inizio&quot;</li>
<li>LowestHighest: &quot; più basso nella parte superiore &quot;  /  &quot; più in alto nella parte superiore&quot;</li>
<li>OldestNewest: il &quot; più recente all'inizio più &quot;  /  &quot; recente all'inizio&quot;</li>
<li>SmallestLargest: più &quot; piccolo nella parte superiore &quot;  /  &quot; più grande all'inizio&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>invitationText</td>
<td>facoltativo. Testo della stringa della Guida visualizzato come istruzioni per l'utente per il controllo o la descrizione comando (ad esempio, &quot; immettere il nome dell'autore &quot; ). La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto a una stringa di visualizzazione. Utilizzare la stringa di visualizzazione indiretta perché può essere localizzata. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription:: GetEditInvitation</strong></a> restituisce il testo dell'invito risolto.</td>
</tr>
<tr class="even">
<td>hideLabel</td>
<td>facoltativo. Il valore predefinito è &quot;false&quot;. Indica se l'etichetta è nascosta.</td>
</tr>
</tbody>
</table>



 

 

 
