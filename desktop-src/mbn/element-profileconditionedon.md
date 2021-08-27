---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44257377400ec8877b07b6aa29766552b72e28e6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882894"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn

Specifica le condizioni che devono essere soddisfatte perché un profilo sia applicabile.

Questo elemento è nuovo per la versione 4. Consente di specificare più profili che si applicano in condizioni diverse e di usare automaticamente il profilo appropriato quando è applicabile. Questo elemento è facoltativo. Se non viene specificato, il profilo è sempre applicabile rispetto alle condizioni elencate.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;ProfileConditionedOn&gt;**

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

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio


| Elemento figlio | Descrizione | 
|---------------|-------------|
| <a href="element-cellularclass.md">CellularClass</a> | <p>Specifica che questo profilo è attivo solo quando la classe cellulare corrente è quella specificata. In caso contrario, il profilo non è applicabile e non può essere usato per attivare un contesto PDP (Packet Data Protocol).</p> | 
| <a href="element-imsi.md">IMSI</a> | <p>Specifica che questo profilo è attivo solo quando l'IMSI corrente usato nell'ICCID è quello specificato. In caso contrario, il profilo non è applicabile e non può essere usato per attivare un contesto PDP (Packet Data Protocol).</p> | 
| <a href="element-iwlanapplicability.md">IwlanApplicability</a> | <p>Specifica che questo profilo è attivo solo quando è connesso a una rete IWLAN. In caso contrario, il profilo non è applicabile e non può essere usato per attivare un contesto PDP (Packet Data Protocol). Il valore di questo elemento deve essere un valore <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> valido.</p> | 
| <a href="element-ratapplicability.md">APPLICAZIONE DI BASEApplicità</a> | <p>Specifica che questo profilo è attivo solo quando il tipo RAT è quello specificato. In caso contrario, il profilo non è applicabile e non può essere usato per attivare un contesto PDP (Packet Data Protocol).</p> | 
| <a href="element-roamapplicability.md">RoamApplicability</a> | <p>Specifica che questo profilo è attivo solo quando la condizione di roaming corrente è quella specificata. In caso contrario, il profilo non è applicabile e non può essere usato per attivare un contesto PDP (Packet Data Protocol). Il valore di questo elemento deve essere un valore <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valido.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre


| Elemento padre | Descrizione | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p><strong>L'elemento MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente. Identifica un profilo Mobile Broadband con un set più ricco di opzioni rispetto all'elemento MBNProfile.</p><p>In un profilo possono essere presenti più elementi MbnProfileExt che descrivono le impostazioni del profilo per un determinato set di condizioni operative. Usare <a href="element-profileconditionedon.md"><strong>l'elemento figlio ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono un profilo specifico il profilo attivo.</p> | 


 

## <a name="requirements"></a>Requisiti


| | | <p>Spazio dei nomi</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



