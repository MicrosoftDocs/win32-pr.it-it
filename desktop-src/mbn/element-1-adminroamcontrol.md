---
description: ModemDMConfigProfile \/ AdminRoamControl (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_AdminRoamControl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AdminRoamControl (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92ba97fd2657b28d1c845598825aae648124d36
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388869"
---
# <a name="span-idwwan_profile_v4element_1_adminroamcontrolspanmodemdmconfigprofileadminroamcontrol-v4"></a><span data-ttu-id="d103f-103"><span id="WWAN_profile_v4.element_1_AdminRoamControl"></span>ModemDMConfigProfile \/ AdminRoamControl (v4)</span><span class="sxs-lookup"><span data-stu-id="d103f-103"><span id="WWAN_profile_v4.element_1_AdminRoamControl"></span>ModemDMConfigProfile\/AdminRoamControl (v4)</span></span>

<span data-ttu-id="d103f-104">Specifica se il profilo è gestito dal roaming amministrativo.</span><span class="sxs-lookup"><span data-stu-id="d103f-104">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="d103f-105">Questo elemento è nuovo per V4.</span><span class="sxs-lookup"><span data-stu-id="d103f-105">This element is new for v4.</span></span> <span data-ttu-id="d103f-106">Il valore di questo elemento è un valore [**roamControlType**](simpletype-roamcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="d103f-106">The value of this element is a [**roamControlType**](simpletype-roamcontroltype.md) value.</span></span> <span data-ttu-id="d103f-107">Si tratta di un elemento facoltativo. Se non viene specificato alcun valore, **AllRoamAllowed** è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d103f-107">This is an optional element; if no value is specified, then **AllRoamAllowed** is the default.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="d103f-108">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="d103f-108">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<AdminRoamControl\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<AdminRoamControl\>**

## <a name="syntax"></a><span data-ttu-id="d103f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d103f-109">Syntax</span></span>

``` syntax
<AdminRoamControl>

  "AllRoamAllowed" | "PartnerRoamAllowed" | "NoRoamAllowed"

</AdminRoamControl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="d103f-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="d103f-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="d103f-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="d103f-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="d103f-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="d103f-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="d103f-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d103f-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="d103f-114">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="d103f-114">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="d103f-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d103f-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d103f-116">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="d103f-116">Parent Element</span></span></th>
<th><span data-ttu-id="d103f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d103f-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d103f-118"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="d103f-118"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="d103f-119">L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="d103f-119">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="d103f-120">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="d103f-120">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="d103f-121">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="d103f-121">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="d103f-122">Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="d103f-122">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d103f-123"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="d103f-123"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="d103f-124">Profilo di configurazione modem DM.</span><span class="sxs-lookup"><span data-stu-id="d103f-124">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="d103f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d103f-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d103f-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d103f-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



