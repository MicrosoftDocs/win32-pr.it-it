---
description: PurposeGroupGuid
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroupGuid
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroupGuid
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29ead67e44ac4735d17d97580b6bce5f187422994c9854bac19febf7a988bcbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358835"
---
# <a name="span-idwwan_profile_v4element_purposegroupguidspanpurposegroupguid"></a><span id="WWAN_profile_v4.element_PurposeGroupGuid"></span>PurposeGroupGuid

Rappresenta un profilo in un PurposeGroup di profili.

I profili vengono specificati dal relativo [**valore guidType.**](simpletype-guidtype.md)

Vengono definiti quattro valori GUID, come elencato nella tabella seguente.

| Gruppo di scopi | GUID                                 |
|---------------|--------------------------------------|
| Internet      | 3E5545D2-1137-4DC8-A198-33F1C657515F |
| mms           | 53E2C5D3-D13C-4068-AA38-9C48FF2E55A8 |
| IMS           | 474D66ED-0E4B-476B-A455-19BB1239ED13 |
| SUPL          | 6D42669F-52A9-408E-9493-1071DCC437BD |

 

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[<MBNProfileExt>](element-mbnprofileext.md)  
[<PurposeGroups>](element-purposegroups.md)  
**<PurposeGroupGuid>**

## <a name="syntax"></a>Sintassi

``` syntax
<PurposeGroupGuid>

  guidType

</PurposeGroupGuid>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento padre</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-purposegroups.md">PurposeGroups</a></td>
<td><p>Elenco facoltativo di gruppi di profili, in cui ogni gruppo include i profili usati per uno scopo comune.</p>
<p>Questo elemento è nuovo per la versione 4 dello schema.</p>
<p>Un profilo può essere elencato in più gruppi.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Spazio dei nomi</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



