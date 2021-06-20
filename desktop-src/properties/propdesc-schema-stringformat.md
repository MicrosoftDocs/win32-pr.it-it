---
description: Specifica il modo in cui IPropertyDescription::FormatForDisplay deve formattare il valore della proprietà stringFormat come stringa.
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730355507b78d99eba02e82666427dd29425c942
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408354"
---
# <a name="stringformat"></a>stringFormat

Specifica il modo [**in cui IPropertyDescription::FormatForDisplay deve**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) formattare il valore della proprietà come stringa. Questa opzione è applicabile solo se <displayInfo displayType="String"> . Deve essere presente un solo [elemento stringFormat]() per ogni [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se sono presenti più elementi, viene usato l'ultimo. Se non viene [specificato alcun elemento stringFormat,]() le impostazioni dell'attributo predefinite vengono applicate alla descrizione della proprietà.

## <a name="syntax"></a>Sintassi


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
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
<td>Pubblica. facoltativo. Il valore predefinito è &quot; &quot; Generale. I valori validi sono i seguenti. 
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
<td>Valore predefinito. Restituisce il valore come stringa non formattata.</td>
</tr>
<tr class="even">
<td>FileName</td>
<td>Formatta il valore come nome file. Nasconde l'estensione in base alle impostazioni utente. Richiede che il tipo di proprietà sia String.</td>
</tr>
<tr class="odd">
<td>FilePath</td>
<td>Formatta il valore come percorso di file. Nasconde l'estensione in base alle impostazioni utente. Richiede che il tipo di proprietà sia String.</td>
</tr>
<tr class="even">
<td>Hyperlink</td>
<td>Formatta il valore come collegamento ipertestuale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
