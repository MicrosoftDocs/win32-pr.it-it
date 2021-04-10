---
description: MmsConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb98506476558ed0e39df11bab4b9446de4fd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226055"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span data-ttu-id="3f69b-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f69b-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span></span>

<span data-ttu-id="3f69b-104">Informazioni di configurazione per il servizio messaggistica multimediale (MMS).</span><span class="sxs-lookup"><span data-stu-id="3f69b-104">Configuration information for Multimedia Messaging Service (MMS).</span></span>

<span data-ttu-id="3f69b-105">Oltre a impostare gli elementi di configurazione all'interno di questo elemento, un profilo MMS deve avere le impostazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3f69b-105">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span>

-   <span data-ttu-id="3f69b-106">L'elemento [**Name**](element-name.md) deve contenere un nome univoco a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="3f69b-106">Its [**Name**](element-name.md) element must contain a system-wide unique name.</span></span>
-   <span data-ttu-id="3f69b-107">Il relativo [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) deve essere impostato su **UserProvisioned**.</span><span class="sxs-lookup"><span data-stu-id="3f69b-107">Its [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) must be set to **UserProvisioned**.</span></span>
-   <span data-ttu-id="3f69b-108">Il [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) deve contenere il ICCID della SIM a cui è destinato questo profilo.</span><span class="sxs-lookup"><span data-stu-id="3f69b-108">Its [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) must contain the ICCID of the SIM that this profile is intended for.</span></span>
-   <span data-ttu-id="3f69b-109">Il relativo [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) deve essere impostato su **Manual**.</span><span class="sxs-lookup"><span data-stu-id="3f69b-109">Its [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) must be set to **Manual**.</span></span>
-   <span data-ttu-id="3f69b-110">Il [**PurposeGroupGuid**](element-purposegroupguid.md) deve contenere il GUID per il gruppo di scopi di MMS.</span><span class="sxs-lookup"><span data-stu-id="3f69b-110">Its [**PurposeGroupGuid**](element-purposegroupguid.md) must contain the GUID for MMS purpose group.</span></span>
-   <span data-ttu-id="3f69b-111">Il valore di [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) deve essere impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="3f69b-111">Its [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) must be set to **true**.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3f69b-112">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="3f69b-112">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<MmsConfiguration>**

## <a name="syntax"></a><span data-ttu-id="3f69b-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f69b-113">Syntax</span></span>

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
```

### <a name="key"></a><span data-ttu-id="3f69b-114">Chiave</span><span class="sxs-lookup"><span data-stu-id="3f69b-114">Key</span></span>

<span data-ttu-id="3f69b-115">`?`   facoltativo (zero o uno)</span><span class="sxs-lookup"><span data-stu-id="3f69b-115">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3f69b-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="3f69b-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3f69b-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="3f69b-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3f69b-118">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="3f69b-118">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3f69b-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3f69b-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f69b-120">Elemento figlio</span><span class="sxs-lookup"><span data-stu-id="3f69b-120">Child Element</span></span></th>
<th><span data-ttu-id="3f69b-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f69b-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3f69b-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span><span class="sxs-lookup"><span data-stu-id="3f69b-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span></span></td>
<td><p><span data-ttu-id="3f69b-123">Specifica la dimensione massima dei messaggi MMS, espressa in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="3f69b-123">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="3f69b-124">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3f69b-124">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f69b-125"><a href="element-mmscport.md">MmscPort</a></span><span class="sxs-lookup"><span data-stu-id="3f69b-125"><a href="element-mmscport.md">MmscPort</a></span></span></td>
<td><p><span data-ttu-id="3f69b-126">Specifica il numero di porta del server MMSC per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f69b-126">Specifies the port number of the MMSC server for the device.</span></span> <span data-ttu-id="3f69b-127">Specificare 0 per indicare che non è specificata alcuna porta specifica.</span><span class="sxs-lookup"><span data-stu-id="3f69b-127">Specify 0 to indicate that no specific port is specified.</span></span> <span data-ttu-id="3f69b-128">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3f69b-128">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f69b-129"><a href="element-mmscurl.md">MmscUrl</a></span><span class="sxs-lookup"><span data-stu-id="3f69b-129"><a href="element-mmscurl.md">MmscUrl</a></span></span></td>
<td><p><span data-ttu-id="3f69b-130">Specifica l'URL del server MMSC per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f69b-130">Specifies the URL of the MMSC server for the device.</span></span> <span data-ttu-id="3f69b-131">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3f69b-131">Optional.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3f69b-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3f69b-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f69b-133">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="3f69b-133">Parent Element</span></span></th>
<th><span data-ttu-id="3f69b-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f69b-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3f69b-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="3f69b-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="3f69b-136">L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="3f69b-136">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="3f69b-137">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="3f69b-137">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="3f69b-138">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="3f69b-138">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="3f69b-139">Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="3f69b-139">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="3f69b-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f69b-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f69b-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3f69b-141">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
