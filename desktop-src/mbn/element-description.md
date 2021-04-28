---
description: Descrizione (Mobile Broadband) - Descrizione
MS-HAID: WWAN\_profile\_v4.element\_Description
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Descrizione (Mobile Broadband)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7adc4b26-1202-4f80-8b26-7879df687bb0
api_name:
- Description
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e72b2fca1df6ba76d933d289b5d73b717cb6af6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107019"
---
# <a name="description-mobile-broadband"></a><span data-ttu-id="09e0b-103">Descrizione (Mobile Broadband)</span><span class="sxs-lookup"><span data-stu-id="09e0b-103">Description (Mobile Broadband)</span></span>

<span data-ttu-id="09e0b-104">Descrizione del profilo.</span><span class="sxs-lookup"><span data-stu-id="09e0b-104">A description of the profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="09e0b-105">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="09e0b-105">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<Description>**

## <a name="syntax"></a><span data-ttu-id="09e0b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09e0b-106">Syntax</span></span>

``` syntax
<Description>

  nameType

</Description>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="09e0b-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="09e0b-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="09e0b-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="09e0b-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="09e0b-109">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="09e0b-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="09e0b-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="09e0b-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="09e0b-111">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="09e0b-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="09e0b-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="09e0b-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09e0b-113">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="09e0b-113">Parent Element</span></span></th>
<th><span data-ttu-id="09e0b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09e0b-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09e0b-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="09e0b-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="09e0b-116"><strong>L'elemento MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="09e0b-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="09e0b-117">Identifica un profilo Mobile Broadband con un set di opzioni più ricco rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="09e0b-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="09e0b-118">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un particolare set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="09e0b-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="09e0b-119">Usare <a href="element-profileconditionedon.md"><strong>l'elemento figlio ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono un profilo specifico il profilo attivo.</span><span class="sxs-lookup"><span data-stu-id="09e0b-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="09e0b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09e0b-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09e0b-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="09e0b-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



