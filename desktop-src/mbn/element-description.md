---
description: Descrizione
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
ms.openlocfilehash: f8a4cbb21b12176771d3ab9091aef0540d8a7c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484844"
---
# <a name="description-mobile-broadband"></a><span data-ttu-id="65e44-103">Descrizione (Mobile Broadband)</span><span class="sxs-lookup"><span data-stu-id="65e44-103">Description (Mobile Broadband)</span></span>

<span data-ttu-id="65e44-104">Descrizione del profilo.</span><span class="sxs-lookup"><span data-stu-id="65e44-104">A description of the profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="65e44-105">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="65e44-105">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<Description>**

## <a name="syntax"></a><span data-ttu-id="65e44-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65e44-106">Syntax</span></span>

``` syntax
<Description>

  nameType

</Description>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="65e44-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="65e44-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="65e44-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="65e44-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="65e44-109">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="65e44-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="65e44-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="65e44-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="65e44-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="65e44-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="65e44-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="65e44-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65e44-113">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="65e44-113">Parent Element</span></span></th>
<th><span data-ttu-id="65e44-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65e44-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65e44-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="65e44-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="65e44-116">L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="65e44-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="65e44-117">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="65e44-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="65e44-118">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="65e44-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="65e44-119">Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="65e44-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="65e44-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65e44-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65e44-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="65e44-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



