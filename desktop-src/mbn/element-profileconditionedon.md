---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129027"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn

Specifica le condizioni che devono essere soddisfatte per l'applicazione di un profilo.

Questo elemento è nuovo per V4. Consente di specificare più profili che si applicano a condizioni diverse e che il profilo appropriato venga utilizzato automaticamente quando è applicabile. Questo elemento è facoltativo. Se non viene specificato, il profilo è sempre applicabile rispetto alle condizioni elencate.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a>Sintassi

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a>Chiave

`?`   facoltativo (zero o uno)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuna.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento figlio</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-cellularclass.md">CellularClass</a></td>
<td><p>Specifica che il profilo è attivo solo quando la classe cellulare corrente è quella specificata. In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</p></td>
</tr>
<tr class="even">
<td><a href="element-imsi.md">IMSI</a></td>
<td><p>Specifica che il profilo è attivo solo quando il IMSI corrente usato in ICCID è quello specificato. In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</p></td>
</tr>
<tr class="odd">
<td><a href="element-iwlanapplicability.md">IwlanApplicability</a></td>
<td><p>Specifica che il profilo è attivo solo quando è connesso a una rete IWLAN. In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol). Il valore di questo elemento deve essere un valore <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> valido.</p></td>
</tr>
<tr class="even">
<td><a href="element-ratapplicability.md">RATApplicability</a></td>
<td><p>Specifica che il profilo è attivo solo quando il tipo di ratto è quello specificato. In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</p></td>
</tr>
<tr class="odd">
<td><a href="element-roamapplicability.md">RoamApplicability</a></td>
<td><p>Specifica che il profilo è attivo solo quando la condizione di roaming corrente è quella specificata. In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol). Il valore di questo elemento deve essere un valore <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valido.</p></td>
</tr>
</tbody>
</table>

 

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
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente. Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</p>
<p>In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative. Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</p></td>
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

 

 



