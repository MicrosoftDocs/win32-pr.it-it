---
description: Contiene un criterio LAN wireless.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: Elemento WLANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ec26a3cab15014deabca4e9332c1fbef7a788b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130434"
---
# <a name="wlanpolicy-element"></a><span data-ttu-id="f53dd-103">Elemento WLANPolicy</span><span class="sxs-lookup"><span data-stu-id="f53dd-103">WLANPolicy Element</span></span>

<span data-ttu-id="f53dd-104">L'elemento **WLANPolicy** contiene un criterio LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="f53dd-104">The **WLANPolicy** element contains a wireless LAN policy.</span></span> <span data-ttu-id="f53dd-105">Questo elemento è l'elemento radice univoco per un profilo dei criteri wireless.</span><span class="sxs-lookup"><span data-stu-id="f53dd-105">This element is the unique root element for a wireless policy profile.</span></span>

<span data-ttu-id="f53dd-106">Lo spazio dei nomi di destinazione per l'elemento **WLANPolicy** è `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="f53dd-106">The target namespace for the **WLANPolicy** element is `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

``` syntax
<xs:element name="WLANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:element name="showDeniedNetwork"
                            type="boolean"
                         />
                        <xs:element name="allowEveryoneToCreateAllUserProfiles"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="f53dd-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f53dd-107">Child elements</span></span>



| <span data-ttu-id="f53dd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f53dd-108">Element</span></span>                                                                                                                    | <span data-ttu-id="f53dd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f53dd-109">Type</span></span>                                                                     | <span data-ttu-id="f53dd-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f53dd-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f53dd-111">**allowEveryoneToCreateAllUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="f53dd-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="f53dd-112">boolean</span><span class="sxs-lookup"><span data-stu-id="f53dd-112">boolean</span></span>                                                                  | <span data-ttu-id="f53dd-113">Specifica se un utente può creare un profilo per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="f53dd-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="f53dd-114">**Elenco serializzazione**</span><span class="sxs-lookup"><span data-stu-id="f53dd-114">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="f53dd-115">Elenco di reti LAN wireless a cui deve essere consentita la connessione di qualsiasi computer.</span><span class="sxs-lookup"><span data-stu-id="f53dd-115">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/>                                       |
| [<span data-ttu-id="f53dd-116">**blockList**</span><span class="sxs-lookup"><span data-stu-id="f53dd-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="f53dd-117">Elenco di reti LAN wireless a cui un computer non deve connettersi.</span><span class="sxs-lookup"><span data-stu-id="f53dd-117">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>                                                    |
| [<span data-ttu-id="f53dd-118">**denyAllESS**</span><span class="sxs-lookup"><span data-stu-id="f53dd-118">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | <span data-ttu-id="f53dd-119">boolean</span><span class="sxs-lookup"><span data-stu-id="f53dd-119">boolean</span></span>                                                                  | <span data-ttu-id="f53dd-120">Specifica se l'accesso a tutte le reti dell'infrastruttura è bloccato.</span><span class="sxs-lookup"><span data-stu-id="f53dd-120">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                                                           |
| [<span data-ttu-id="f53dd-121">**denyAllIBSS**</span><span class="sxs-lookup"><span data-stu-id="f53dd-121">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | <span data-ttu-id="f53dd-122">boolean</span><span class="sxs-lookup"><span data-stu-id="f53dd-122">boolean</span></span>                                                                  | <span data-ttu-id="f53dd-123">Specifica se l'accesso a tutte le reti ad hoc è bloccato.</span><span class="sxs-lookup"><span data-stu-id="f53dd-123">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                                                                   |
| [<span data-ttu-id="f53dd-124">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f53dd-124">**description**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [<span data-ttu-id="f53dd-125">**nameType**</span><span class="sxs-lookup"><span data-stu-id="f53dd-125">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="f53dd-126">Descrizione di un criterio LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="f53dd-126">The description of a wireless LAN policy.</span></span> <br/>                                                                                |
| [<span data-ttu-id="f53dd-127">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="f53dd-127">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="f53dd-128">boolean</span><span class="sxs-lookup"><span data-stu-id="f53dd-128">boolean</span></span>                                                                  | <span data-ttu-id="f53dd-129">Specifica se i computer utilizzano il servizio di configurazione automatica (AutoConfig) incorporato per gestire le connessioni wireless.</span><span class="sxs-lookup"><span data-stu-id="f53dd-129">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="f53dd-130">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="f53dd-130">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="f53dd-131">Contiene le impostazioni globali per il modulo di configurazione automatica (ACM).</span><span class="sxs-lookup"><span data-stu-id="f53dd-131">Contains the global settings for the Auto Configuration Module (ACM).</span></span> <br/>                                                    |
| [<span data-ttu-id="f53dd-132">**nome**</span><span class="sxs-lookup"><span data-stu-id="f53dd-132">**name**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [<span data-ttu-id="f53dd-133">**nameType**</span><span class="sxs-lookup"><span data-stu-id="f53dd-133">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="f53dd-134">Nome di un criterio LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="f53dd-134">The name of a wireless LAN policy.</span></span> <br/>                                                                                       |
| [<span data-ttu-id="f53dd-135">**network**</span><span class="sxs-lookup"><span data-stu-id="f53dd-135">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)                                                             | [<span data-ttu-id="f53dd-136">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="f53dd-136">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="f53dd-137">Rete consentita.</span><span class="sxs-lookup"><span data-stu-id="f53dd-137">An allowed network.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="f53dd-138">**network**</span><span class="sxs-lookup"><span data-stu-id="f53dd-138">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)                                                             | [<span data-ttu-id="f53dd-139">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="f53dd-139">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="f53dd-140">Rete bloccata.</span><span class="sxs-lookup"><span data-stu-id="f53dd-140">A blocked network.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="f53dd-141">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="f53dd-141">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | <span data-ttu-id="f53dd-142">Elenco di reti consentite e negate.</span><span class="sxs-lookup"><span data-stu-id="f53dd-142">The list of allowed and denied networks.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f53dd-143">**profileList**</span><span class="sxs-lookup"><span data-stu-id="f53dd-143">**profileList**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="f53dd-144">Contiene un elenco di profili da applicare a livello di dominio o di computer.</span><span class="sxs-lookup"><span data-stu-id="f53dd-144">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                |
| [<span data-ttu-id="f53dd-145">**showDeniedNetwork**</span><span class="sxs-lookup"><span data-stu-id="f53dd-145">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="f53dd-146">boolean</span><span class="sxs-lookup"><span data-stu-id="f53dd-146">boolean</span></span>                                                                  | <span data-ttu-id="f53dd-147">Specifica se le reti negate vengono visualizzate nella procedura guidata **Connetti a una rete** .</span><span class="sxs-lookup"><span data-stu-id="f53dd-147">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="remarks"></a><span data-ttu-id="f53dd-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="f53dd-148">Remarks</span></span>

<span data-ttu-id="f53dd-149">Per visualizzare l'elenco di elementi figlio in una struttura simile a un albero, [vedere \_ elementi dello schema dei criteri di rete WLAN](wlan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="f53dd-149">To view the list of child elements in a tree-like structure, see [WLAN\_policy Schema Elements](wlan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f53dd-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f53dd-150">Requirements</span></span>



| <span data-ttu-id="f53dd-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="f53dd-151">Requirement</span></span> | <span data-ttu-id="f53dd-152">Valore</span><span class="sxs-lookup"><span data-stu-id="f53dd-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f53dd-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f53dd-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f53dd-154">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f53dd-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f53dd-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f53dd-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f53dd-156">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f53dd-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




