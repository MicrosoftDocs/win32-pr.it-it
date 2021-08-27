---
description: APPLICAZIONEApplicazione
MS-HAID: WWAN\_profile\_v4.element\_RATApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: APPLICAZIONEApplicazione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdeb94362480b00a4d1a3d0d6a7dedc49d4cf9f7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467568"
---
# <a name="span-idwwan_profile_v4element_ratapplicabilityspanratapplicability"></a><span id="WWAN_profile_v4.element_RATApplicability"></span>APPLICAZIONEApplicazione

Specifica che questo profilo è attivo solo quando il tipo PIÙ BASSO è quello specificato. In caso contrario, il profilo non è applicabile e non può essere usato per attivare un contesto PDP (Packet Data Protocol).

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<RATApplicability>**

## <a name="syntax"></a>Sintassi

``` syntax
<RATApplicability>

  "LTE_eHRPD" | "3GPP_LEGACY"

</RATApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre


| Elemento padre | Descrizione | 
|----------------|-------------|
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Specifica le condizioni che devono essere soddisfatte perché un profilo sia applicabile.</p><p>Questo elemento è una novità per v4. Consente di specificare più profili che si applicano in condizioni diverse e di usare automaticamente il profilo appropriato quando è applicabile. Questo elemento è facoltativo. Se non viene specificato, il profilo è sempre applicabile in relazione alle condizioni elencate.</p> | 


 

## <a name="requirements"></a>Requisiti


| | | <p>Spazio dei nomi</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



