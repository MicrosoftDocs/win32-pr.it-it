---
description: ConnectionMode
MS-HAID: WWAN\_profile\_v4.element\_ConnectionMode
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ConnectionMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b356780908f8fb6ce6d41e41d2db78e823d6e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966667"
---
# <a name="span-idwwan_profile_v4element_connectionmodespanconnectionmode"></a><span data-ttu-id="f980c-103"><span id="WWAN_profile_v4.element_ConnectionMode"></span>ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="f980c-103"><span id="WWAN_profile_v4.element_ConnectionMode"></span>ConnectionMode</span></span>

<span data-ttu-id="f980c-104">Specifica l'impostazione di connessione automatica da usare per un dispositivo mobile broadband.</span><span class="sxs-lookup"><span data-stu-id="f980c-104">Specifies the auto connection setting to be used for a Mobile Broadband device.</span></span>

<span data-ttu-id="f980c-105">Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f980c-105">For more information, see the documentation for the v1 [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="f980c-106">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="f980c-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ConnectionMode>**

## <a name="syntax"></a><span data-ttu-id="f980c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f980c-107">Syntax</span></span>

``` syntax
<ConnectionMode>

  "manual" | "auto" | "auto-home"

</ConnectionMode>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="f980c-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="f980c-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="f980c-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="f980c-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="f980c-110">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="f980c-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="f980c-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f980c-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="f980c-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="f980c-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="f980c-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f980c-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f980c-114">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="f980c-114">Parent Element</span></span></th>
<th><span data-ttu-id="f980c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f980c-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f980c-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="f980c-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="f980c-117">L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="f980c-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="f980c-118">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="f980c-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="f980c-119">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="f980c-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="f980c-120">Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="f980c-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="f980c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f980c-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f980c-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f980c-122">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
