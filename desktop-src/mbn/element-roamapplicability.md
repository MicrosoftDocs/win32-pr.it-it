---
description: MBNProfileExt \/ RoamApplicability (v4)
MS-HAID: WWAN\_profile\_v4.element\_RoamApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RoamApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29438df96a3a12bb791870b1cc0d59e84f77d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306787"
---
# <a name="span-idwwan_profile_v4element_roamapplicabilityspanmbnprofileextroamapplicability-v4"></a><span id="WWAN_profile_v4.element_RoamApplicability"></span>MBNProfileExt \/ RoamApplicability (v4)

Specifica che il profilo è attivo solo quando la condizione di roaming corrente è quella specificata. In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol). Il valore di questo elemento deve essere un valore [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) valido.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

## <a name="syntax"></a>Sintassi

``` syntax
<RoamApplicability>

  "NonPartnerOnly" | "PartnerOnly" | "HomeOnly" | "HomeAndPartner" | "PartnerAndNonpartner" | "AllRoaming"

</RoamApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuna.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuna.

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
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Profilo di configurazione modem DM.</p></td>
</tr>
<tr class="even">
<td><a href="element-profileconditionedon.md">ProfileConditionedOn</a></td>
<td><p>Specifica le condizioni che devono essere soddisfatte per l'applicazione di un profilo.</p>
<p>Questo elemento è nuovo per V4. Consente di specificare più profili che si applicano a condizioni diverse e che il profilo appropriato venga utilizzato automaticamente quando è applicabile. Questo elemento è facoltativo. Se non viene specificato, il profilo è sempre applicabile rispetto alle condizioni elencate.</p></td>
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

 

 



