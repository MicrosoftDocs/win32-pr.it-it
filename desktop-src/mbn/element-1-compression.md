---
description: ModemDMConfigProfile \/ ... \/ Compressione (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_Compression
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Compressione (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8dc3acd6-5997-47a5-bd30-899569b9aad9
api_name:
- Compression
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5796afb061bdc758bba020384501699fe3627e16
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388841"
---
# <a name="span-idwwan_profile_v4element_1_compressionspanmodemdmconfigprofilecompression-v4"></a><span data-ttu-id="1f829-103"><span id="WWAN_profile_v4.element_1_Compression"></span>ModemDMConfigProfile \/ ... \/ Compressione (v4)</span><span class="sxs-lookup"><span data-stu-id="1f829-103"><span id="WWAN_profile_v4.element_1_Compression"></span>ModemDMConfigProfile\/...\/Compression (v4)</span></span>

<span data-ttu-id="1f829-104">Specifica se la compressione verrà utilizzata nel collegamento dati per l'intestazione e il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="1f829-104">Specifies whether compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="1f829-105">Per ulteriori informazioni, vedere la documentazione relativa all'elemento [**Compression**](./schema-compression-contexttype-element.md) V1.</span><span class="sxs-lookup"><span data-stu-id="1f829-105">For more information, see the documentation for the v1 [**Compression**](./schema-compression-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="1f829-106">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="1f829-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

## <a name="syntax"></a><span data-ttu-id="1f829-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f829-107">Syntax</span></span>

``` syntax
<Compression>

  "DISABLE" | "ENABLE"

</Compression>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="1f829-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="1f829-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="1f829-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="1f829-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="1f829-110">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1f829-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="1f829-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1f829-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="1f829-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1f829-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="1f829-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="1f829-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f829-114">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1f829-114">Parent Element</span></span></th>
<th><span data-ttu-id="1f829-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f829-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f829-116"><a href="element-1-context.md">Contesto</a></span><span class="sxs-lookup"><span data-stu-id="1f829-116"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="1f829-117">Specifica i parametri necessari per stabilire una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="1f829-117">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="1f829-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f829-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f829-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1f829-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
