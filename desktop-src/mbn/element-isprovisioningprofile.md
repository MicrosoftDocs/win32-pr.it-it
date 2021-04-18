---
description: IsProvisioningProfile
MS-HAID: WWAN\_profile\_v4.element\_IsProvisioningProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsProvisioningProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be857d96473fa81f0bf72580ced811de56eb2436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306794"
---
# <a name="span-idwwan_profile_v4element_isprovisioningprofilespanisprovisioningprofile"></a><span data-ttu-id="46748-103"><span id="WWAN_profile_v4.element_IsProvisioningProfile"></span>IsProvisioningProfile</span><span class="sxs-lookup"><span data-stu-id="46748-103"><span id="WWAN_profile_v4.element_IsProvisioningProfile"></span>IsProvisioningProfile</span></span>

<span data-ttu-id="46748-104">Specifica che il profilo deve essere usato solo per il provisioning. In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="46748-104">Specifies that this profile is to be used for provisioning only.Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="46748-105">Questo elemento è nuovo per V4.</span><span class="sxs-lookup"><span data-stu-id="46748-105">This element is new for v4.</span></span>

<span data-ttu-id="46748-106">Se **IsProvisioningProfile** è true, l' [**impostazione predefinita**](element-isdefault.md) deve essere false e [**ConnectionMode**](element-connectionmode.md) deve essere manuale.</span><span class="sxs-lookup"><span data-stu-id="46748-106">If **IsProvisioningProfile** is true, [**IsDefault**](element-isdefault.md) must be false, and [**ConnectionMode**](element-connectionmode.md) must be manual.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="46748-107">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="46748-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<IsProvisioningProfile>**

## <a name="syntax"></a><span data-ttu-id="46748-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46748-108">Syntax</span></span>

``` syntax
<IsProvisioningProfile>

  boolean

</IsProvisioningProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="46748-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="46748-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="46748-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="46748-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="46748-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="46748-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="46748-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="46748-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="46748-113">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="46748-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="46748-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="46748-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46748-115">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="46748-115">Parent Element</span></span></th>
<th><span data-ttu-id="46748-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46748-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46748-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="46748-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="46748-118">L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="46748-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="46748-119">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="46748-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="46748-120">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="46748-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="46748-121">Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="46748-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="46748-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46748-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46748-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="46748-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



