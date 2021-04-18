---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f4593d1b55b4c95a2ec185fe5545ad7eb04141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306790"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span data-ttu-id="34566-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span><span class="sxs-lookup"><span data-stu-id="34566-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span></span>

<span data-ttu-id="34566-104">Profilo di configurazione modem DM.</span><span class="sxs-lookup"><span data-stu-id="34566-104">Modem DM configuration profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="34566-105">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="34566-105">Element hierarchy</span></span>

**<ModemDMConfigProfile>**

## <a name="syntax"></a><span data-ttu-id="34566-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34566-106">Syntax</span></span>

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a><span data-ttu-id="34566-107">Chiave</span><span class="sxs-lookup"><span data-stu-id="34566-107">Key</span></span>

<span data-ttu-id="34566-108">`?`   facoltativo (zero o uno)</span><span class="sxs-lookup"><span data-stu-id="34566-108">`?`   optional (zero or one)</span></span>

<span data-ttu-id="34566-109">`*`   facoltativo (zero o più)</span><span class="sxs-lookup"><span data-stu-id="34566-109">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="34566-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="34566-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="34566-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="34566-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="34566-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="34566-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="34566-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="34566-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34566-114">Elemento figlio</span><span class="sxs-lookup"><span data-stu-id="34566-114">Child Element</span></span></th>
<th><span data-ttu-id="34566-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34566-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34566-116"><a href="element-1-adminenable.md">AdminEnable</a></span><span class="sxs-lookup"><span data-stu-id="34566-116"><a href="element-1-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="34566-117">Specifica se il profilo è abilitato in amministrazione. Si tratta di un nuovo elemento per V4.</span><span class="sxs-lookup"><span data-stu-id="34566-117">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34566-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span><span class="sxs-lookup"><span data-stu-id="34566-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="34566-119">Specifica se il profilo è gestito dal roaming amministrativo.</span><span class="sxs-lookup"><span data-stu-id="34566-119">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="34566-120">Questo elemento è nuovo per V4.</span><span class="sxs-lookup"><span data-stu-id="34566-120">This element is new for v4.</span></span> <span data-ttu-id="34566-121">Il valore di questo elemento è un valore <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="34566-121">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="34566-122">Si tratta di un elemento facoltativo. Se non viene specificato alcun valore, <strong>AllRoamAllowed</strong> è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="34566-122">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34566-123"><a href="element-1-apnid.md">ApnID</a></span><span class="sxs-lookup"><span data-stu-id="34566-123"><a href="element-1-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="34566-124">ID APN associato a questo profilo. Questo elemento è una novità di V4 ed è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="34566-124">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34566-125"><a href="element-1-context.md">Contesto</a></span><span class="sxs-lookup"><span data-stu-id="34566-125"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="34566-126">Specifica i parametri necessari per stabilire una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="34566-126">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34566-127"><a href="element-1-name.md">Nome</a></span><span class="sxs-lookup"><span data-stu-id="34566-127"><a href="element-1-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="34566-128">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="34566-128">The name of the profile.</span></span> <span data-ttu-id="34566-129">Per ulteriori informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nome</strong></a> V1.</span><span class="sxs-lookup"><span data-stu-id="34566-129">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34566-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span><span class="sxs-lookup"><span data-stu-id="34566-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span></span></td>
<td><p><span data-ttu-id="34566-131">ID di connessione OEM per la configurazione del modem DM.</span><span class="sxs-lookup"><span data-stu-id="34566-131">The OEM connection ID for the modem DM configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34566-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></span><span class="sxs-lookup"><span data-stu-id="34566-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></span></span></td>
<td><p><span data-ttu-id="34566-133">Specifica il modo in cui è stato creato il profilo DM del modem.</span><span class="sxs-lookup"><span data-stu-id="34566-133">Specifies how this modem DM profile was created.</span></span></p>
<p><span data-ttu-id="34566-134">Questo valore viene usato per decidere se un utente può eliminare il profilo.</span><span class="sxs-lookup"><span data-stu-id="34566-134">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="34566-135">Gli utenti possono eliminare solo i profili <strong>UserProvisioned</strong> .</span><span class="sxs-lookup"><span data-stu-id="34566-135">Users can only delete <strong>UserProvisioned</strong> profiles.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34566-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span><span class="sxs-lookup"><span data-stu-id="34566-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="34566-137">Specifica che il profilo è attivo solo quando la condizione di roaming corrente è quella specificata.</span><span class="sxs-lookup"><span data-stu-id="34566-137">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="34566-138">In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="34566-138">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="34566-139">Il valore di questo elemento deve essere un valore <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valido.</span><span class="sxs-lookup"><span data-stu-id="34566-139">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34566-140"><a href="element-1-simiccid.md">SimIccID</a></span><span class="sxs-lookup"><span data-stu-id="34566-140"><a href="element-1-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="34566-141">Numero di identifcation SIM per i dispositivi GSM.</span><span class="sxs-lookup"><span data-stu-id="34566-141">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="34566-142">Per altri dettagli, vedere la documentazione per l'elemento V1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="34566-142">For more details , see the documentation for the v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="34566-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="34566-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="34566-144">Questo elemento (documento) più esterno potrebbe non essere contenuto da altri elementi.</span><span class="sxs-lookup"><span data-stu-id="34566-144">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="34566-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34566-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34566-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="34566-146">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



