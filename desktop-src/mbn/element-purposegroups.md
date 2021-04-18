---
description: PurposeGroups
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroups
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370cf6b0dc13848ca21a2a06e0b9806d753878c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306788"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span data-ttu-id="85813-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span><span class="sxs-lookup"><span data-stu-id="85813-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span></span>

<span data-ttu-id="85813-104">Elenco facoltativo di gruppi di profili, in cui ogni gruppo include i profili utilizzati per uno scopo comune.</span><span class="sxs-lookup"><span data-stu-id="85813-104">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span>

<span data-ttu-id="85813-105">Questo elemento è nuovo per la V4 dello schema.</span><span class="sxs-lookup"><span data-stu-id="85813-105">This element is new for v4 of the schema.</span></span>

<span data-ttu-id="85813-106">Un profilo può essere elencato in più gruppi.</span><span class="sxs-lookup"><span data-stu-id="85813-106">One profile can be listed in multiple groups.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="85813-107">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="85813-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a><span data-ttu-id="85813-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85813-108">Syntax</span></span>

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a><span data-ttu-id="85813-109">Chiave</span><span class="sxs-lookup"><span data-stu-id="85813-109">Key</span></span>

<span data-ttu-id="85813-110">`{}`   intervallo specifico di occorrenze</span><span class="sxs-lookup"><span data-stu-id="85813-110">`{}`   specific range of occurrences</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="85813-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="85813-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="85813-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="85813-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="85813-113">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="85813-113">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="85813-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="85813-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85813-115">Elemento figlio</span><span class="sxs-lookup"><span data-stu-id="85813-115">Child Element</span></span></th>
<th><span data-ttu-id="85813-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85813-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85813-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span><span class="sxs-lookup"><span data-stu-id="85813-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span></span></td>
<td><p><span data-ttu-id="85813-118">Rappresenta un profilo in un PurposeGroup di profili.</span><span class="sxs-lookup"><span data-stu-id="85813-118">Represents one profile in a PurposeGroup of profiles.</span></span></p>
<p><span data-ttu-id="85813-119">I profili sono specificati dal relativo valore <a href="simpletype-guidtype.md"><strong>guidType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85813-119">Profiles are specified by their <a href="simpletype-guidtype.md"><strong>guidType</strong></a> value.</span></span></p>
<p><span data-ttu-id="85813-120">Sono definiti quattro valori GUID, elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="85813-120">Four GUID values are defined, as listed in the following table.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="85813-121">Gruppo scopo</span><span class="sxs-lookup"><span data-stu-id="85813-121">Purpose group</span></span></th>
<th><span data-ttu-id="85813-122">GUID</span><span class="sxs-lookup"><span data-stu-id="85813-122">GUID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85813-123">Internet</span><span class="sxs-lookup"><span data-stu-id="85813-123">Internet</span></span></td>
<td><span data-ttu-id="85813-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span><span class="sxs-lookup"><span data-stu-id="85813-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85813-125">mms</span><span class="sxs-lookup"><span data-stu-id="85813-125">MMS</span></span></td>
<td><span data-ttu-id="85813-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span><span class="sxs-lookup"><span data-stu-id="85813-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85813-127">IMS</span><span class="sxs-lookup"><span data-stu-id="85813-127">IMS</span></span></td>
<td><span data-ttu-id="85813-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span><span class="sxs-lookup"><span data-stu-id="85813-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85813-129">SUPL</span><span class="sxs-lookup"><span data-stu-id="85813-129">SUPL</span></span></td>
<td><span data-ttu-id="85813-130">6D42669F-52A9-408E-9493-1071DCC437BD</span><span class="sxs-lookup"><span data-stu-id="85813-130">6D42669F-52A9-408E-9493-1071DCC437BD</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="85813-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="85813-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85813-132">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="85813-132">Parent Element</span></span></th>
<th><span data-ttu-id="85813-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85813-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85813-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="85813-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="85813-135">L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="85813-135">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="85813-136">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="85813-136">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="85813-137">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="85813-137">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="85813-138">Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="85813-138">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="85813-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85813-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85813-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="85813-140">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



