---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343781"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span data-ttu-id="85b11-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span><span class="sxs-lookup"><span data-stu-id="85b11-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span></span>

<span data-ttu-id="85b11-104">L'elemento **MBNProfileExt** è un'estensione dell'elemento MBNProfile precedente.</span><span class="sxs-lookup"><span data-stu-id="85b11-104">The **MBNProfileExt** element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="85b11-105">Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="85b11-105">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span>

<span data-ttu-id="85b11-106">In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative.</span><span class="sxs-lookup"><span data-stu-id="85b11-106">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="85b11-107">Usare l'elemento figlio [**ProfileConditionedOn**](element-profileconditionedon.md) di **MBNProfileExt** per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="85b11-107">Use the [**ProfileConditionedOn**](element-profileconditionedon.md) child element of **MBNProfileExt** to specify which operating conditions make a particular profile the active profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="85b11-108">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="85b11-108">Element hierarchy</span></span>

**<MBNProfileExt>**

## <a name="syntax"></a><span data-ttu-id="85b11-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85b11-109">Syntax</span></span>

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a><span data-ttu-id="85b11-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="85b11-110">Key</span></span>

<span data-ttu-id="85b11-111">`?`   facoltativo (zero o uno)</span><span class="sxs-lookup"><span data-stu-id="85b11-111">`?`   optional (zero or one)</span></span>

<span data-ttu-id="85b11-112">`*`   facoltativo (zero o più)</span><span class="sxs-lookup"><span data-stu-id="85b11-112">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="85b11-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="85b11-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="85b11-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="85b11-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="85b11-115">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="85b11-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="85b11-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="85b11-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85b11-117">Elemento figlio</span><span class="sxs-lookup"><span data-stu-id="85b11-117">Child Element</span></span></th>
<th><span data-ttu-id="85b11-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85b11-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85b11-119"><a href="element-adminenable.md">AdminEnable</a></span><span class="sxs-lookup"><span data-stu-id="85b11-119"><a href="element-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="85b11-120">Specifica se il profilo è abilitato in amministrazione. Si tratta di un nuovo elemento per V4.</span><span class="sxs-lookup"><span data-stu-id="85b11-120">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b11-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span><span class="sxs-lookup"><span data-stu-id="85b11-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="85b11-122">Specifica se il profilo è gestito dal roaming amministrativo.</span><span class="sxs-lookup"><span data-stu-id="85b11-122">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="85b11-123">Questo elemento è nuovo per V4.</span><span class="sxs-lookup"><span data-stu-id="85b11-123">This element is new for v4.</span></span> <span data-ttu-id="85b11-124">Il valore di questo elemento è un valore <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b11-124">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="85b11-125">Si tratta di un elemento facoltativo. Se non viene specificato alcun valore, <strong>AllRoamAllowed</strong> è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="85b11-125">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b11-126"><a href="element-apnid.md">ApnID</a></span><span class="sxs-lookup"><span data-stu-id="85b11-126"><a href="element-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="85b11-127">ID APN associato a questo profilo. Questo elemento è una novità di V4 ed è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="85b11-127">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b11-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span><span class="sxs-lookup"><span data-stu-id="85b11-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span></span></td>
<td><p><span data-ttu-id="85b11-129">Specifica se il dispositivo mobile broadband si connetterà automaticamente a una rete.</span><span class="sxs-lookup"><span data-stu-id="85b11-129">Specifies whether the Mobile Broadband device will automatically connect to a network.</span></span></p>
<p><span data-ttu-id="85b11-130">Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b11-130">For more information, see the documentation for the v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b11-131"><a href="element-connectionmode.md">ConnectionMode</a></span><span class="sxs-lookup"><span data-stu-id="85b11-131"><a href="element-connectionmode.md">ConnectionMode</a></span></span></td>
<td><p><span data-ttu-id="85b11-132">Specifica l'impostazione di connessione automatica da usare per un dispositivo mobile broadband.</span><span class="sxs-lookup"><span data-stu-id="85b11-132">Specifies the auto connection setting to be used for a Mobile Broadband device.</span></span></p>
<p><span data-ttu-id="85b11-133">Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b11-133">For more information, see the documentation for the v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b11-134"><a href="element-context.md">Contesto</a></span><span class="sxs-lookup"><span data-stu-id="85b11-134"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="85b11-135">Specifica i parametri necessari per stabilire una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="85b11-135">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b11-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span><span class="sxs-lookup"><span data-stu-id="85b11-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span></span></td>
<td><p><span data-ttu-id="85b11-137">Specifica un elenco di provider di rete preferiti durante il roaming.</span><span class="sxs-lookup"><span data-stu-id="85b11-137">Specifies a list of preferred network providers when roaming.</span></span></p>
<p><span data-ttu-id="85b11-138">Per informazioni dettagliate, vedere la documentazione per l'elemento V1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b11-138">For details, see the documentation for the v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b11-139"><a href="element-description.md">Descrizione</a></span><span class="sxs-lookup"><span data-stu-id="85b11-139"><a href="element-description.md">Description</a></span></span></td>
<td><p><span data-ttu-id="85b11-140">Descrizione del profilo.</span><span class="sxs-lookup"><span data-stu-id="85b11-140">A description of the profile.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b11-141"><a href="element-homeprovidername.md">HomeProviderName</a></span><span class="sxs-lookup"><span data-stu-id="85b11-141"><a href="element-homeprovidername.md">HomeProviderName</a></span></span></td>
<td><p><span data-ttu-id="85b11-142">Nome del provider Home per la SIM/dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="85b11-142">The name of the home provider for the given SIM/Device.</span></span> <span data-ttu-id="85b11-143">Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b11-143">For more information, see the documentation for the v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b11-144"><a href="element-iconfilepath.md">ICONFilePath</a></span><span class="sxs-lookup"><span data-stu-id="85b11-144"><a href="element-iconfilepath.md">ICONFilePath</a></span></span></td>
<td><p><span data-ttu-id="85b11-145">Percorso del file di icona per la connessione.</span><span class="sxs-lookup"><span data-stu-id="85b11-145">The path to the icon file for the connection.</span></span> <span data-ttu-id="85b11-146">L'interfaccia utente di connessione al sistema operativo Visualizza l'icona quando viene eseguita una connessione utilizzando questo profilo.</span><span class="sxs-lookup"><span data-stu-id="85b11-146">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span></p>
<p><span data-ttu-id="85b11-147">Per ulteriori informazioni sull'utilizzo di questo elemento, vedere la documentazione V1 relativa a <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="85b11-147">For more details on using this element, see the v1 documentation for <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b11-148"><a href="element-isdefault.md">IsDefault</a></span><span class="sxs-lookup"><span data-stu-id="85b11-148"><a href="element-isdefault.md">IsDefault</a></span></span></td>
<td><p><span data-ttu-id="85b11-149">Specifica se il profilo è il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="85b11-149">Specifies whether this profile is the default profile.</span></span></p>
<p><span data-ttu-id="85b11-150">Per informazioni più dettagliate su questo elemento, vedere la documentazione V1 per <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="85b11-150">For more detail on this element, see the v1 documentation for <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b11-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span><span class="sxs-lookup"><span data-stu-id="85b11-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span></span></td>
<td><p><span data-ttu-id="85b11-152">Specifica che il profilo è esclusivo per gli altri profili degli stessi set di profili. Questo elemento è nuovo per V4.</span><span class="sxs-lookup"><span data-stu-id="85b11-152">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b11-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span><span class="sxs-lookup"><span data-stu-id="85b11-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span></span></td>
<td><p><span data-ttu-id="85b11-154">Specifica che questo profilo è un profilo di contesto PDP aggiuntivo di lunga durata. Se il valore di questo elemento è <strong>true</strong>, anche <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve essere impostato su <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b11-154">Specifies that this profile is a long-standing additional PDP context profile.If the value of this element is <strong>true</strong>, then <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must also be set to <strong>true</strong>.</span></span> <span data-ttu-id="85b11-155">Si tratta di un nuovo elemento per V4.</span><span class="sxs-lookup"><span data-stu-id="85b11-155">This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b11-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span><span class="sxs-lookup"><span data-stu-id="85b11-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span></span></td>
<td><p><span data-ttu-id="85b11-157">Specifica che il profilo deve essere usato solo per il provisioning. In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="85b11-157">Specifies that this profile is to be used for provisioning only.Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="85b11-158">Questo elemento è nuovo per V4.</span><span class="sxs-lookup"><span data-stu-id="85b11-158">This element is new for v4.</span></span></p>
<p><span data-ttu-id="85b11-159">Se <strong>IsProvisioningProfile</strong> è true, l' <a href="element-isdefault.md"><strong>impostazione predefinita</strong></a> deve essere false e <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> deve essere manuale.</span><span class="sxs-lookup"><span data-stu-id="85b11-159">If <strong>IsProvisioningProfile</strong> is true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> must be false, and <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> must be manual.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b11-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="85b11-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="85b11-161">Informazioni di configurazione per il servizio messaggistica multimediale (MMS).</span><span class="sxs-lookup"><span data-stu-id="85b11-161">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="85b11-162">Oltre a impostare gli elementi di configurazione all'interno di questo elemento, un profilo MMS deve avere le impostazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="85b11-162">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="85b11-163">L'elemento <a href="element-name.md"><strong>Name</strong></a> deve contenere un nome univoco a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="85b11-163">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="85b11-164">Il relativo <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> deve essere impostato su <strong>UserProvisioned</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b11-164">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="85b11-165">Il <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> deve contenere il ICCID della SIM a cui è destinato questo profilo.</span><span class="sxs-lookup"><span data-stu-id="85b11-165">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="85b11-166">Il relativo <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> deve essere impostato su <strong>Manual</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b11-166">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="85b11-167">Il <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> deve contenere il GUID per il gruppo di scopi di MMS.</span><span class="sxs-lookup"><span data-stu-id="85b11-167">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="85b11-168">Il valore di <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve essere impostato su <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b11-168">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b11-169"><a href="element-name.md">Nome</a></span><span class="sxs-lookup"><span data-stu-id="85b11-169"><a href="element-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="85b11-170">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="85b11-170">The name of the profile.</span></span> <span data-ttu-id="85b11-171">Per ulteriori informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nome</strong></a> V1.</span><span class="sxs-lookup"><span data-stu-id="85b11-171">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b11-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="85b11-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="85b11-173">Specifica le condizioni che devono essere soddisfatte per l'applicazione di un profilo.</span><span class="sxs-lookup"><span data-stu-id="85b11-173">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="85b11-174">Questo elemento è nuovo per V4.</span><span class="sxs-lookup"><span data-stu-id="85b11-174">This element is new for v4.</span></span> <span data-ttu-id="85b11-175">Consente di specificare più profili che si applicano a condizioni diverse e che il profilo appropriato venga utilizzato automaticamente quando è applicabile.</span><span class="sxs-lookup"><span data-stu-id="85b11-175">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="85b11-176">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="85b11-176">This element is optional.</span></span> <span data-ttu-id="85b11-177">Se non viene specificato, il profilo è sempre applicabile rispetto alle condizioni elencate.</span><span class="sxs-lookup"><span data-stu-id="85b11-177">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b11-178"><a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a></span><span class="sxs-lookup"><span data-stu-id="85b11-178"><a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a></span></span></td>
<td><p><span data-ttu-id="85b11-179">Specifica l'autore del profilo.</span><span class="sxs-lookup"><span data-stu-id="85b11-179">Specifies the creator of the profile.</span></span></p>
<p><span data-ttu-id="85b11-180">Per ulteriori informazioni su questo elemento, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b11-180">For more information about this element, see the documentation for the v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b11-181"><a href="element-purposegroups.md">PurposeGroups</a></span><span class="sxs-lookup"><span data-stu-id="85b11-181"><a href="element-purposegroups.md">PurposeGroups</a></span></span></td>
<td><p><span data-ttu-id="85b11-182">Elenco facoltativo di gruppi di profili, in cui ogni gruppo include i profili utilizzati per uno scopo comune.</span><span class="sxs-lookup"><span data-stu-id="85b11-182">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span></p>
<p><span data-ttu-id="85b11-183">Questo elemento è nuovo per la V4 dello schema.</span><span class="sxs-lookup"><span data-stu-id="85b11-183">This element is new for v4 of the schema.</span></span></p>
<p><span data-ttu-id="85b11-184">Un profilo può essere elencato in più gruppi.</span><span class="sxs-lookup"><span data-stu-id="85b11-184">One profile can be listed in multiple groups.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b11-185"><a href="element-simiccid.md">SimIccID</a></span><span class="sxs-lookup"><span data-stu-id="85b11-185"><a href="element-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="85b11-186">Numero di identifcation SIM per i dispositivi GSM.</span><span class="sxs-lookup"><span data-stu-id="85b11-186">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="85b11-187">Per altri dettagli, vedere la documentazione per l'elemento V1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b11-187">For more details , see the documentation for the v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b11-188"><a href="element-subscriberid.md">SubscriberID</a></span><span class="sxs-lookup"><span data-stu-id="85b11-188"><a href="element-subscriberid.md">SubscriberID</a></span></span></td>
<td><p><span data-ttu-id="85b11-189">Identifica l'identificatore univoco del profilo.</span><span class="sxs-lookup"><span data-stu-id="85b11-189">Identifies the unique identifier of the profile.</span></span></p>
<p><span data-ttu-id="85b11-190">Per una rete GSM questo deve contenere IMSI (International Mobile Subscriber Identity) della SIM e per i dispositivi CDMA deve contenere il numero minimo di identificazione mobile del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85b11-190">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span></p>
<p><span data-ttu-id="85b11-191">Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b11-191">For more information, see the documentation for the v1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="85b11-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="85b11-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="85b11-193">Questo elemento (documento) più esterno potrebbe non essere contenuto da altri elementi.</span><span class="sxs-lookup"><span data-stu-id="85b11-193">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="85b11-194">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85b11-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85b11-195">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="85b11-195">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
