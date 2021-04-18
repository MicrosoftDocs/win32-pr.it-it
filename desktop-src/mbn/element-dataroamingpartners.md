---
description: DataRoamingPartners
MS-HAID: WWAN\_profile\_v4.element\_DataRoamingPartners
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DataRoamingPartners
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c29edf9c-4e70-4b8f-8c71-0ec8a9fad60d
api_name:
- DataRoamingPartners
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6df58bc0765b5254645c45270f8145f5d10d422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306801"
---
# <a name="span-idwwan_profile_v4element_dataroamingpartnersspandataroamingpartners"></a><span data-ttu-id="19f84-103"><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners</span><span class="sxs-lookup"><span data-stu-id="19f84-103"><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners</span></span>

<span data-ttu-id="19f84-104">Specifica un elenco di provider di rete preferiti durante il roaming.</span><span class="sxs-lookup"><span data-stu-id="19f84-104">Specifies a list of preferred network providers when roaming.</span></span>

<span data-ttu-id="19f84-105">Per informazioni dettagliate, vedere la documentazione per l'elemento V1 [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="19f84-105">For details, see the documentation for the v1 [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="19f84-106">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="19f84-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<DataRoamingPartners>**

## <a name="syntax"></a><span data-ttu-id="19f84-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19f84-107">Syntax</span></span>

``` syntax
<DataRoamingPartners>

  <!-- Child elements -->
  Provider+

</DataRoamingPartners>
```

### <a name="key"></a><span data-ttu-id="19f84-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="19f84-108">Key</span></span>

<span data-ttu-id="19f84-109">`+`   obbligatorio (uno o più)</span><span class="sxs-lookup"><span data-stu-id="19f84-109">`+`   required (one or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="19f84-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="19f84-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="19f84-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="19f84-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="19f84-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="19f84-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="19f84-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="19f84-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19f84-114">Elemento figlio</span><span class="sxs-lookup"><span data-stu-id="19f84-114">Child Element</span></span></th>
<th><span data-ttu-id="19f84-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19f84-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19f84-116"><a href="element-provider.md">Provider</a></span><span class="sxs-lookup"><span data-stu-id="19f84-116"><a href="element-provider.md">Provider</a></span></span></td>
<td><p><span data-ttu-id="19f84-117">Specifica un provider di rete preferito in un elenco di provider da usare durante il roaming.</span><span class="sxs-lookup"><span data-stu-id="19f84-117">Specifies one preferred network provider in a list of providers to be used when roaming.</span></span></p>
<p><span data-ttu-id="19f84-118">Il valore di questo elemento è un'istanza del tipo complesso V1 <a href="../mbn/schema-providertype-complextype.md"><strong>ProviderType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="19f84-118">The value of this element is an instance of the v1 <a href="../mbn/schema-providertype-complextype.md"><strong>providerType</strong></a> complex type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="19f84-119"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="19f84-119"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19f84-120">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="19f84-120">Parent Element</span></span></th>
<th><span data-ttu-id="19f84-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19f84-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19f84-122"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="19f84-122"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="19f84-123">L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="19f84-123">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="19f84-124">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="19f84-124">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="19f84-125">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="19f84-125">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="19f84-126">Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="19f84-126">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="19f84-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19f84-127">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19f84-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="19f84-128">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
