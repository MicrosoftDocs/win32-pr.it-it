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
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span data-ttu-id="55dc9-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span><span class="sxs-lookup"><span data-stu-id="55dc9-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span></span>

<span data-ttu-id="55dc9-104">Specifica le condizioni che devono essere soddisfatte per l'applicazione di un profilo.</span><span class="sxs-lookup"><span data-stu-id="55dc9-104">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span>

<span data-ttu-id="55dc9-105">Questo elemento è nuovo per V4.</span><span class="sxs-lookup"><span data-stu-id="55dc9-105">This element is new for v4.</span></span> <span data-ttu-id="55dc9-106">Consente di specificare più profili che si applicano a condizioni diverse e che il profilo appropriato venga utilizzato automaticamente quando è applicabile.</span><span class="sxs-lookup"><span data-stu-id="55dc9-106">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="55dc9-107">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="55dc9-107">This element is optional.</span></span> <span data-ttu-id="55dc9-108">Se non viene specificato, il profilo è sempre applicabile rispetto alle condizioni elencate.</span><span class="sxs-lookup"><span data-stu-id="55dc9-108">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="55dc9-109">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="55dc9-109">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a><span data-ttu-id="55dc9-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55dc9-110">Syntax</span></span>

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

### <a name="key"></a><span data-ttu-id="55dc9-111">Chiave</span><span class="sxs-lookup"><span data-stu-id="55dc9-111">Key</span></span>

<span data-ttu-id="55dc9-112">`?`   facoltativo (zero o uno)</span><span class="sxs-lookup"><span data-stu-id="55dc9-112">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="55dc9-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="55dc9-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="55dc9-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="55dc9-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="55dc9-115">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="55dc9-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="55dc9-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="55dc9-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55dc9-117">Elemento figlio</span><span class="sxs-lookup"><span data-stu-id="55dc9-117">Child Element</span></span></th>
<th><span data-ttu-id="55dc9-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55dc9-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55dc9-119"><a href="element-cellularclass.md">CellularClass</a></span><span class="sxs-lookup"><span data-stu-id="55dc9-119"><a href="element-cellularclass.md">CellularClass</a></span></span></td>
<td><p><span data-ttu-id="55dc9-120">Specifica che il profilo è attivo solo quando la classe cellulare corrente è quella specificata.</span><span class="sxs-lookup"><span data-stu-id="55dc9-120">Specifies that this profile is active only when the current cellular class is the one specified.</span></span> <span data-ttu-id="55dc9-121">In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="55dc9-121">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55dc9-122"><a href="element-imsi.md">IMSI</a></span><span class="sxs-lookup"><span data-stu-id="55dc9-122"><a href="element-imsi.md">IMSI</a></span></span></td>
<td><p><span data-ttu-id="55dc9-123">Specifica che il profilo è attivo solo quando il IMSI corrente usato in ICCID è quello specificato.</span><span class="sxs-lookup"><span data-stu-id="55dc9-123">Specifies that this profile is active only when the current IMSI being used in the ICCID is the one specified.</span></span> <span data-ttu-id="55dc9-124">In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="55dc9-124">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55dc9-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span><span class="sxs-lookup"><span data-stu-id="55dc9-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span></span></td>
<td><p><span data-ttu-id="55dc9-126">Specifica che il profilo è attivo solo quando è connesso a una rete IWLAN.</span><span class="sxs-lookup"><span data-stu-id="55dc9-126">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="55dc9-127">In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="55dc9-127">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="55dc9-128">Il valore di questo elemento deve essere un valore <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> valido.</span><span class="sxs-lookup"><span data-stu-id="55dc9-128">The value of this element must be a valid <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55dc9-129"><a href="element-ratapplicability.md">RATApplicability</a></span><span class="sxs-lookup"><span data-stu-id="55dc9-129"><a href="element-ratapplicability.md">RATApplicability</a></span></span></td>
<td><p><span data-ttu-id="55dc9-130">Specifica che il profilo è attivo solo quando il tipo di ratto è quello specificato.</span><span class="sxs-lookup"><span data-stu-id="55dc9-130">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="55dc9-131">In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="55dc9-131">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55dc9-132"><a href="element-roamapplicability.md">RoamApplicability</a></span><span class="sxs-lookup"><span data-stu-id="55dc9-132"><a href="element-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="55dc9-133">Specifica che il profilo è attivo solo quando la condizione di roaming corrente è quella specificata.</span><span class="sxs-lookup"><span data-stu-id="55dc9-133">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="55dc9-134">In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="55dc9-134">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="55dc9-135">Il valore di questo elemento deve essere un valore <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valido.</span><span class="sxs-lookup"><span data-stu-id="55dc9-135">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="55dc9-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="55dc9-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55dc9-137">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="55dc9-137">Parent Element</span></span></th>
<th><span data-ttu-id="55dc9-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55dc9-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55dc9-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="55dc9-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="55dc9-140">L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="55dc9-140">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="55dc9-141">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="55dc9-141">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="55dc9-142">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="55dc9-142">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="55dc9-143">Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="55dc9-143">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="55dc9-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55dc9-144">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55dc9-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="55dc9-145">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



