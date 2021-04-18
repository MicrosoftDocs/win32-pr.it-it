---
description: CellularClass
MS-HAID: WWAN\_profile\_v4.element\_CellularClass
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CellularClass
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1953d07176262aba35f54cc80c9b712002cd857
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306804"
---
# <a name="span-idwwan_profile_v4element_cellularclassspancellularclass"></a><span data-ttu-id="76943-103"><span id="WWAN_profile_v4.element_CellularClass"></span>CellularClass</span><span class="sxs-lookup"><span data-stu-id="76943-103"><span id="WWAN_profile_v4.element_CellularClass"></span>CellularClass</span></span>

<span data-ttu-id="76943-104">Specifica che il profilo è attivo solo quando la classe cellulare corrente è quella specificata.</span><span class="sxs-lookup"><span data-stu-id="76943-104">Specifies that this profile is active only when the current cellular class is the one specified.</span></span> <span data-ttu-id="76943-105">In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="76943-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="76943-106">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="76943-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<CellularClass>**

## <a name="syntax"></a><span data-ttu-id="76943-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76943-107">Syntax</span></span>

``` syntax
<CellularClass>

  "3GPP" | "3GPP2"

</CellularClass>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="76943-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="76943-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="76943-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="76943-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="76943-110">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="76943-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="76943-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="76943-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="76943-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="76943-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="76943-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="76943-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76943-114">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="76943-114">Parent Element</span></span></th>
<th><span data-ttu-id="76943-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76943-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76943-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="76943-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="76943-117">Specifica le condizioni che devono essere soddisfatte per l'applicazione di un profilo.</span><span class="sxs-lookup"><span data-stu-id="76943-117">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="76943-118">Questo elemento è nuovo per V4.</span><span class="sxs-lookup"><span data-stu-id="76943-118">This element is new for v4.</span></span> <span data-ttu-id="76943-119">Consente di specificare più profili che si applicano a condizioni diverse e che il profilo appropriato venga utilizzato automaticamente quando è applicabile.</span><span class="sxs-lookup"><span data-stu-id="76943-119">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="76943-120">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="76943-120">This element is optional.</span></span> <span data-ttu-id="76943-121">Se non viene specificato, il profilo è sempre applicabile rispetto alle condizioni elencate.</span><span class="sxs-lookup"><span data-stu-id="76943-121">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="76943-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76943-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76943-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="76943-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



