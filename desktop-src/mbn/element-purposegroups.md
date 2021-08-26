---
description: PurposeGroups
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroups
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3b158938e1a41f6ab8d3f1df0cae6a2166bc21c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630937"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups

Elenco facoltativo di gruppi di profili, in cui ogni gruppo include i profili usati per uno scopo comune.

Questo elemento è nuovo per la versione 4 dello schema.

Un profilo può essere elencato in più gruppi.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a>Sintassi

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a>Chiave

`{}`   intervallo specifico di occorrenze

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Elemento figlio</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-purposegroupguid.md">PurposeGroupGuid</a></td>
<td><p>Rappresenta un profilo in un PurposeGroup di profili.</p>
<p>I profili vengono specificati dal relativo <a href="simpletype-guidtype.md"><strong>valore guidType.</strong></a></p>
<p>Vengono definiti quattro valori GUID, come elencato nella tabella seguente.</p>
<table>
<thead>
<tr class="header">
<th>Gruppo di scopi</th>
<th>GUID</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Internet</td>
<td>3E5545D2-1137-4DC8-A198-33F1C657515F</td>
</tr>
<tr class="even">
<td>mms</td>
<td>53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</td>
</tr>
<tr class="odd">
<td>IMS</td>
<td>474D66ED-0E4B-476B-A455-19BB1239ED13</td>
</tr>
<tr class="even">
<td>SUPL</td>
<td>6D42669F-52A9-408E-9493-1071DCC437BD</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Elemento padre</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p><strong>L'elemento MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente. Identifica un profilo Mobile Broadband con un set più ricco di opzioni rispetto all'elemento MBNProfile.</p>
<p>In un profilo possono essere presenti più elementi MbnProfileExt che descrivono le impostazioni del profilo per un determinato set di condizioni operative. Usare <a href="element-profileconditionedon.md"><strong>l'elemento figlio ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono un profilo specifico il profilo attivo.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Spazio dei nomi</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



