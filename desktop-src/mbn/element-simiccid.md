---
description: MBNProfileExt \/ SimIccID (v4)
MS-HAID: WWAN\_profile\_v4.element\_SimIccID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SimIccID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b7c679683d98e1a4039c90f1dfb37d4ff765e3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988634"
---
# <a name="span-idwwan_profile_v4element_simiccidspanmbnprofileextsimiccid-v4"></a><span id="WWAN_profile_v4.element_SimIccID"></span>MBNProfileExt \/ SimIccID (v4)

Numero di identificazione SIM per i dispositivi GSM. Per altre informazioni, vedere la documentazione per l'elemento [**SimIccID**](./schema-simiccid-mbnprofile-element.md) v1.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<SimIccID\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<SimIccID\>**

## <a name="syntax"></a>Sintassi

``` syntax
<SimIccID>

  simIccIDType

</SimIccID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre


| Elemento padre | Descrizione | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p><strong>L'elemento MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente. Identifica un profilo Mobile Broadband con un set più ricco di opzioni rispetto all'elemento MBNProfile.</p><p>In un profilo possono essere presenti più elementi MbnProfileExt che descrivono le impostazioni del profilo per un determinato set di condizioni operative. Usare <a href="element-profileconditionedon.md"><strong>l'elemento figlio ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono un profilo specifico il profilo attivo.</p> | 
| <a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a> | <p>Profilo di configurazione dm modem.</p> | 


 

## <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p>Spazio dei nomi</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
