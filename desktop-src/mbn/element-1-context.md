---
description: '\/Contesto ModemDMConfigProfile (v4)'
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Contesto (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 133f48d9c9a1c9dd9f0e04f59d5e35478caa9227
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388848"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span data-ttu-id="3b490-103"><span id="WWAN_profile_v4.element_1_Context"></span>\/Contesto ModemDMConfigProfile (v4)</span><span class="sxs-lookup"><span data-stu-id="3b490-103"><span id="WWAN_profile_v4.element_1_Context"></span>ModemDMConfigProfile\/Context (v4)</span></span>

<span data-ttu-id="3b490-104">Specifica i parametri necessari per stabilire una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="3b490-104">Specifies the parameters required to establish a data connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3b490-105">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="3b490-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a><span data-ttu-id="3b490-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b490-106">Syntax</span></span>

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a><span data-ttu-id="3b490-107">Chiave</span><span class="sxs-lookup"><span data-stu-id="3b490-107">Key</span></span>

<span data-ttu-id="3b490-108">`?`   facoltativo (zero o uno)</span><span class="sxs-lookup"><span data-stu-id="3b490-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3b490-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="3b490-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3b490-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="3b490-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3b490-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="3b490-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3b490-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3b490-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b490-113">Elemento figlio</span><span class="sxs-lookup"><span data-stu-id="3b490-113">Child Element</span></span></th>
<th><span data-ttu-id="3b490-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b490-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3b490-115"><a href="element-1-accessstring.md">AccessString</a></span><span class="sxs-lookup"><span data-stu-id="3b490-115"><a href="element-1-accessstring.md">AccessString</a></span></span></td>
<td><p><span data-ttu-id="3b490-116">Identifica l'APN o la stringa di connessione da utilizzare per stabilire una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="3b490-116">Identifies the APN or dial string to be used to establish a data connection.</span></span></p>
<p><span data-ttu-id="3b490-117">Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3b490-117">For more information, see the documentation for the v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b490-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span><span class="sxs-lookup"><span data-stu-id="3b490-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span></span></td>
<td><p><span data-ttu-id="3b490-119">>Specifica il protocollo di autenticazione da utilizzare per l'attivazione di un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="3b490-119">>Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span></p>
<p><span data-ttu-id="3b490-120">Si noti che in V4 è disponibile un nuovo valore di enumerazione per questo elemento.</span><span class="sxs-lookup"><span data-stu-id="3b490-120">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="3b490-121">La <strong>selezione di autoselezione</strong> indica che un protocollo di autenticazione deve essere prelevato da uno o più livelli inferiori.</span><span class="sxs-lookup"><span data-stu-id="3b490-121"><strong>AutoSelection</strong> means that an auth protocol is to be picked by lower layer(s).</span></span></p>
<p><span data-ttu-id="3b490-122">Per ulteriori informazioni, vedere la documentazione per l'elemento V1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3b490-122">For further information, see the documentation for the v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b490-123"><a href="element-1-compression.md">Compressione</a></span><span class="sxs-lookup"><span data-stu-id="3b490-123"><a href="element-1-compression.md">Compression</a></span></span></td>
<td><p><span data-ttu-id="3b490-124">Specifica se la compressione verrà utilizzata nel collegamento dati per l'intestazione e il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="3b490-124">Specifies whether compression will be used at the data link for header and data transfer.</span></span></p>
<p><span data-ttu-id="3b490-125">Per ulteriori informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> V1.</span><span class="sxs-lookup"><span data-stu-id="3b490-125">For more information, see the documentation for the v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b490-126"><a href="element-1-iptype.md">IPType</a></span><span class="sxs-lookup"><span data-stu-id="3b490-126"><a href="element-1-iptype.md">IPType</a></span></span></td>
<td><p><span data-ttu-id="3b490-127">Specifica il tipo di IP da utilizzare per la connessione dati.</span><span class="sxs-lookup"><span data-stu-id="3b490-127">Specifies the IP type to be used on this data connection.</span></span></p>
<p><span data-ttu-id="3b490-128">Questo elemento è nuovo in V4 dello schema.</span><span class="sxs-lookup"><span data-stu-id="3b490-128">This element is new in v4 of the schema.</span></span> <span data-ttu-id="3b490-129">L'elemento può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3b490-129">The element can have one of the following values.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3b490-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3b490-130">Value</span></span></th>
<th><span data-ttu-id="3b490-131">Significato</span><span class="sxs-lookup"><span data-stu-id="3b490-131">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3b490-132">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3b490-132">Default</span></span></td>
<td><span data-ttu-id="3b490-133">Il tipo di IP deve essere prelevato da uno o più livelli inferiori</span><span class="sxs-lookup"><span data-stu-id="3b490-133">IP type is to be picked by lower layer(s)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b490-134">IPv4</span><span class="sxs-lookup"><span data-stu-id="3b490-134">IPv4</span></span></td>
<td><span data-ttu-id="3b490-135">USA IPv4</span><span class="sxs-lookup"><span data-stu-id="3b490-135">Use IPv4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b490-136">IPv6</span><span class="sxs-lookup"><span data-stu-id="3b490-136">IPv6</span></span></td>
<td><span data-ttu-id="3b490-137">Utilizza IPv6</span><span class="sxs-lookup"><span data-stu-id="3b490-137">Use IPv6</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b490-138">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="3b490-138">IPv4v6</span></span></td>
<td><span data-ttu-id="3b490-139">Utilizzare IPv4 e/o IPv6 come disponibile.</span><span class="sxs-lookup"><span data-stu-id="3b490-139">Use IPv4 and/or IPv6, as available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b490-140">XLAT</span><span class="sxs-lookup"><span data-stu-id="3b490-140">XLAT</span></span></td>
<td><span data-ttu-id="3b490-141">Usare 464XLAT per eseguire il tunneling IPv4 su reti IPv6</span><span class="sxs-lookup"><span data-stu-id="3b490-141">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b490-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="3b490-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="3b490-143">Credenziali di accesso per una connessione.</span><span class="sxs-lookup"><span data-stu-id="3b490-143">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3b490-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3b490-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b490-145">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="3b490-145">Parent Element</span></span></th>
<th><span data-ttu-id="3b490-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b490-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3b490-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="3b490-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="3b490-148">L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="3b490-148">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="3b490-149">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="3b490-149">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="3b490-150">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="3b490-150">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="3b490-151">Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="3b490-151">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b490-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="3b490-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="3b490-153">Profilo di configurazione modem DM.</span><span class="sxs-lookup"><span data-stu-id="3b490-153">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="3b490-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b490-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b490-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3b490-155">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



