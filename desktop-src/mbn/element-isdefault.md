---
description: IsDefault
MS-HAID: WWAN\_profile\_v4.element\_IsDefault
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsDefault
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47dd13bba0a7ca44804c393f482e19e0173800a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129579"
---
# <a name="span-idwwan_profile_v4element_isdefaultspanisdefault"></a><span data-ttu-id="b9b4d-103"><span id="WWAN_profile_v4.element_IsDefault"></span>IsDefault</span><span class="sxs-lookup"><span data-stu-id="b9b4d-103"><span id="WWAN_profile_v4.element_IsDefault"></span>IsDefault</span></span>

<span data-ttu-id="b9b4d-104">Specifica se il profilo è il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="b9b4d-104">Specifies whether this profile is the default profile.</span></span>

<span data-ttu-id="b9b4d-105">Per informazioni più dettagliate su questo elemento, vedere la documentazione V1 per [**IsDefault**](./schema-isdefault-mbnprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="b9b4d-105">For more detail on this element, see the v1 documentation for [**IsDefault**](./schema-isdefault-mbnprofile-element.md).</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="b9b4d-106">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="b9b4d-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<IsDefault>**

## <a name="syntax"></a><span data-ttu-id="b9b4d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9b4d-107">Syntax</span></span>

``` syntax
<IsDefault>

  boolean

</IsDefault>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="b9b4d-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="b9b4d-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="b9b4d-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="b9b4d-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="b9b4d-110">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="b9b4d-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="b9b4d-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b9b4d-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="b9b4d-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="b9b4d-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="b9b4d-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b9b4d-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9b4d-114">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="b9b4d-114">Parent Element</span></span></th>
<th><span data-ttu-id="b9b4d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9b4d-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b9b4d-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="b9b4d-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="b9b4d-117">L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="b9b4d-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="b9b4d-118">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="b9b4d-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="b9b4d-119">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="b9b4d-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="b9b4d-120">Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="b9b4d-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="b9b4d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9b4d-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9b4d-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b9b4d-122">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
