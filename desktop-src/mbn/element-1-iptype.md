---
description: ModemDMConfigProfile \/ ... \/ IPType (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPType (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec57fbe0bbcb4c633ddb8485f048ce4230e0ca5
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388806"
---
# <a name="span-idwwan_profile_v4element_1_iptypespanmodemdmconfigprofileiptype-v4"></a><span data-ttu-id="305d4-103"><span id="WWAN_profile_v4.element_1_IPType"></span>ModemDMConfigProfile \/ ... \/ IPType (v4)</span><span class="sxs-lookup"><span data-stu-id="305d4-103"><span id="WWAN_profile_v4.element_1_IPType"></span>ModemDMConfigProfile\/...\/IPType (v4)</span></span>

<span data-ttu-id="305d4-104">Specifica il tipo di IP da utilizzare per la connessione dati.</span><span class="sxs-lookup"><span data-stu-id="305d4-104">Specifies the IP type to be used on this data connection.</span></span>

<span data-ttu-id="305d4-105">Questo elemento è nuovo in V4 dello schema.</span><span class="sxs-lookup"><span data-stu-id="305d4-105">This element is new in v4 of the schema.</span></span> <span data-ttu-id="305d4-106">L'elemento può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="305d4-106">The element can have one of the following values.</span></span>

| <span data-ttu-id="305d4-107">Valore</span><span class="sxs-lookup"><span data-stu-id="305d4-107">Value</span></span>   | <span data-ttu-id="305d4-108">Significato</span><span class="sxs-lookup"><span data-stu-id="305d4-108">Meaning</span></span>                                       |
|---------|-----------------------------------------------|
| <span data-ttu-id="305d4-109">Predefinito</span><span class="sxs-lookup"><span data-stu-id="305d4-109">Default</span></span> | <span data-ttu-id="305d4-110">Il tipo di IP deve essere prelevato da uno o più livelli inferiori</span><span class="sxs-lookup"><span data-stu-id="305d4-110">IP type is to be picked by lower layer(s)</span></span>     |
| <span data-ttu-id="305d4-111">IPv4</span><span class="sxs-lookup"><span data-stu-id="305d4-111">IPv4</span></span>    | <span data-ttu-id="305d4-112">USA IPv4</span><span class="sxs-lookup"><span data-stu-id="305d4-112">Use IPv4</span></span>                                      |
| <span data-ttu-id="305d4-113">IPv6</span><span class="sxs-lookup"><span data-stu-id="305d4-113">IPv6</span></span>    | <span data-ttu-id="305d4-114">Utilizza IPv6</span><span class="sxs-lookup"><span data-stu-id="305d4-114">Use IPv6</span></span>                                      |
| <span data-ttu-id="305d4-115">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="305d4-115">IPv4v6</span></span>  | <span data-ttu-id="305d4-116">Utilizzare IPv4 e/o IPv6 come disponibile.</span><span class="sxs-lookup"><span data-stu-id="305d4-116">Use IPv4 and/or IPv6, as available.</span></span>           |
| <span data-ttu-id="305d4-117">XLAT</span><span class="sxs-lookup"><span data-stu-id="305d4-117">XLAT</span></span>    | <span data-ttu-id="305d4-118">Usare 464XLAT per eseguire il tunneling IPv4 su reti IPv6</span><span class="sxs-lookup"><span data-stu-id="305d4-118">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span> |

 

## <a name="element-hierarchy"></a><span data-ttu-id="305d4-119">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="305d4-119">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a><span data-ttu-id="305d4-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="305d4-120">Syntax</span></span>

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="305d4-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="305d4-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="305d4-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="305d4-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="305d4-123">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="305d4-123">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="305d4-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="305d4-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="305d4-125">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="305d4-125">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="305d4-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="305d4-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="305d4-127">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="305d4-127">Parent Element</span></span></th>
<th><span data-ttu-id="305d4-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="305d4-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="305d4-129"><a href="element-1-context.md">Contesto</a></span><span class="sxs-lookup"><span data-stu-id="305d4-129"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="305d4-130">Specifica i parametri necessari per stabilire una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="305d4-130">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="305d4-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="305d4-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="305d4-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="305d4-132">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



