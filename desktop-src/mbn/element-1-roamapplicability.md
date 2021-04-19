---
description: ModemDMConfigProfile \/ RoamApplicability (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_RoamApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RoamApplicability (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d78618598b758d4c2654f0f2911637e638aacf
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388797"
---
# <a name="span-idwwan_profile_v4element_1_roamapplicabilityspanmodemdmconfigprofileroamapplicability-v4"></a><span data-ttu-id="6e04a-103"><span id="WWAN_profile_v4.element_1_RoamApplicability"></span>ModemDMConfigProfile \/ RoamApplicability (v4)</span><span class="sxs-lookup"><span data-stu-id="6e04a-103"><span id="WWAN_profile_v4.element_1_RoamApplicability"></span>ModemDMConfigProfile\/RoamApplicability (v4)</span></span>

<span data-ttu-id="6e04a-104">Specifica che il profilo è attivo solo quando la condizione di roaming corrente è quella specificata.</span><span class="sxs-lookup"><span data-stu-id="6e04a-104">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="6e04a-105">In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="6e04a-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="6e04a-106">Il valore di questo elemento deve essere un valore [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) valido.</span><span class="sxs-lookup"><span data-stu-id="6e04a-106">The value of this element must be a valid [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="6e04a-107">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="6e04a-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

## <a name="syntax"></a><span data-ttu-id="6e04a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e04a-108">Syntax</span></span>

``` syntax
<RoamApplicability>

  "NonPartnerOnly" | "PartnerOnly" | "HomeOnly" | "HomeAndPartner" | "PartnerAndNonpartner" | "AllRoaming"

</RoamApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="6e04a-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="6e04a-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="6e04a-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="6e04a-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="6e04a-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="6e04a-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="6e04a-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="6e04a-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="6e04a-113">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="6e04a-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="6e04a-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="6e04a-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e04a-115">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="6e04a-115">Parent Element</span></span></th>
<th><span data-ttu-id="6e04a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e04a-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6e04a-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="6e04a-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="6e04a-118">Profilo di configurazione modem DM.</span><span class="sxs-lookup"><span data-stu-id="6e04a-118">Modem DM configuration profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e04a-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="6e04a-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="6e04a-120">Specifica le condizioni che devono essere soddisfatte per l'applicazione di un profilo.</span><span class="sxs-lookup"><span data-stu-id="6e04a-120">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="6e04a-121">Questo elemento è nuovo per V4.</span><span class="sxs-lookup"><span data-stu-id="6e04a-121">This element is new for v4.</span></span> <span data-ttu-id="6e04a-122">Consente di specificare più profili che si applicano a condizioni diverse e che il profilo appropriato venga utilizzato automaticamente quando è applicabile.</span><span class="sxs-lookup"><span data-stu-id="6e04a-122">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="6e04a-123">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6e04a-123">This element is optional.</span></span> <span data-ttu-id="6e04a-124">Se non viene specificato, il profilo è sempre applicabile rispetto alle condizioni elencate.</span><span class="sxs-lookup"><span data-stu-id="6e04a-124">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="6e04a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e04a-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e04a-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e04a-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



