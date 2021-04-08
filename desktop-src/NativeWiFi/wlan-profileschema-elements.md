---
description: Lo \_ schema del profilo WLAN definisce gli elementi seguenti.
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: Elementi dello schema WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752306"
---
# <a name="wlan_profile-schema-elements"></a><span data-ttu-id="7dafa-103">\_Elementi dello schema del profilo WLAN</span><span class="sxs-lookup"><span data-stu-id="7dafa-103">WLAN\_profile Schema Elements</span></span>

<span data-ttu-id="7dafa-104">Lo \_ schema del profilo WLAN definisce gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7dafa-104">The WLAN\_profile schema defines the following elements.</span></span> <span data-ttu-id="7dafa-105">La maggior parte degli elementi si trova nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/profile/v1` , ad eccezione di [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), che si trova nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="7dafa-105">Most elements are in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`, except for [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), which is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v2`.</span></span>

<span data-ttu-id="7dafa-106">Nell'elenco seguente vengono illustrati gli elementi definiti nell'ordine in cui gli elementi vengono visualizzati in un profilo.</span><span class="sxs-lookup"><span data-stu-id="7dafa-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="7dafa-107">Viene applicato l'ordinamento degli elementi.</span><span class="sxs-lookup"><span data-stu-id="7dafa-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="7dafa-108">Non tutti gli elementi sono in tutti i profili, perché alcuni elementi sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="7dafa-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="7dafa-109">Questo elenco non Mostra tutti i possibili elementi che possono essere visualizzati in un profilo wireless, in quanto è possibile aggiungere elementi in **xs: qualsiasi** punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="7dafa-109">This list does not show all possible elements that can appear in a wireless profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="7dafa-110">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="7dafa-110">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
    -   [<span data-ttu-id="7dafa-111">**nome (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-111">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)
    -   [<span data-ttu-id="7dafa-112">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-112">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [<span data-ttu-id="7dafa-113">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-113">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [<span data-ttu-id="7dafa-114">**esadecimale (SSID)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-114">**hex (SSID)**</span></span>](wlan-profileschema-hex-ssid-element.md)
            -   [<span data-ttu-id="7dafa-115">**nome (SSID)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-115">**name (SSID)**</span></span>](wlan-profileschema-name-ssid-element.md)
        -   [<span data-ttu-id="7dafa-116">**non broadcast (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-116">**nonBroadcast (SSIDConfig)**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [<span data-ttu-id="7dafa-117">**Hotspot2 (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-117">**Hotspot2 (WLANProfile)**</span></span>](wlan-profileschema-hotspot2-element.md)
        -   [<span data-ttu-id="7dafa-118">**NomeDominio (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-118">**DomainName (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-domainname-element.md)
        -   [<span data-ttu-id="7dafa-119">**NAIRealm (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-119">**NAIRealm (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [<span data-ttu-id="7dafa-120">**Network3GPP (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-120">**Network3GPP (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [<span data-ttu-id="7dafa-121">**RoamingConsortium (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-121">**RoamingConsortium (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [<span data-ttu-id="7dafa-122">**connectionType (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-122">**connectionType (WLANProfile)**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [<span data-ttu-id="7dafa-123">**connectionMode (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-123">**connectionMode (WLANProfile)**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [<span data-ttu-id="7dafa-124">**autoswitch (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-124">**autoSwitch (WLANProfile)**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [<span data-ttu-id="7dafa-125">**CSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
        -   [<span data-ttu-id="7dafa-126">**connettività (MSM)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-126">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
            -   [<span data-ttu-id="7dafa-127">**phyType (connettività)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-127">**phyType (connectivity)**</span></span>](wlan-profileschema-phytype-connectivity-element.md)
        -   [<span data-ttu-id="7dafa-128">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-128">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
            -   [<span data-ttu-id="7dafa-129">**authEncryption (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-129">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
                -   [<span data-ttu-id="7dafa-130">**autenticazione (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-130">**authentication (authEncryption)**</span></span>](wlan-profileschema-authentication-authencryption-element.md)
                -   [<span data-ttu-id="7dafa-131">**crittografia (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-131">**encryption (authEncryption)**</span></span>](wlan-profileschema-encryption-authencryption-element.md)
                -   [<span data-ttu-id="7dafa-132">**useOneX (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-132">**useOneX (authEncryption)**</span></span>](wlan-profileschema-useonex-authencryption-element.md)
                -   [<span data-ttu-id="7dafa-133">**FIPSMode (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-133">**FIPSMode (authEncryption)**</span></span>](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [<span data-ttu-id="7dafa-134">**sharedKey (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-134">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
                -   [<span data-ttu-id="7dafa-135">**Tipo di sharedKey**</span><span class="sxs-lookup"><span data-stu-id="7dafa-135">**keyType (sharedKey)**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)
                -   [<span data-ttu-id="7dafa-136">**protetto (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-136">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)
                -   [<span data-ttu-id="7dafa-137">**Material (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-137">**keyMaterial (sharedKey)**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [<span data-ttu-id="7dafa-138">**Indice di indicizzazione (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-138">**keyIndex (security)**</span></span>](wlan-profileschema-keyindex-security-element.md)
            -   [<span data-ttu-id="7dafa-139">**PMKCacheMode (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-139">**PMKCacheMode (security)**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)
            -   [<span data-ttu-id="7dafa-140">**PMKCacheTTL (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-140">**PMKCacheTTL (security)**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)
            -   [<span data-ttu-id="7dafa-141">**PMKCacheSize (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-141">**PMKCacheSize (security)**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)
            -   [<span data-ttu-id="7dafa-142">**preAuthMode (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-142">**preAuthMode (security)**</span></span>](wlan-profileschema-preauthmode-security-element.md)
            -   [<span data-ttu-id="7dafa-143">**preAuthThrottle (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-143">**preAuthThrottle (security)**</span></span>](wlan-profileschema-preauththrottle-security-element.md)
    -   [<span data-ttu-id="7dafa-144">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-144">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [<span data-ttu-id="7dafa-145">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-145">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
            -   [<span data-ttu-id="7dafa-146">**OUI (OUIHeader)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-146">**OUI (OUIHeader)**</span></span>](wlan-profileschema-oui-ouiheader-element.md)
            -   [<span data-ttu-id="7dafa-147">**tipo (OUIHeader)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-147">**type (OUIHeader)**</span></span>](wlan-profileschema-type-ouiheader-element.md)
        -   [<span data-ttu-id="7dafa-148">**connettività (IHV)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-148">**connectivity (IHV)**</span></span>](wlan-profileschema-connectivity-ihv-element.md)
        -   [<span data-ttu-id="7dafa-149">**sicurezza (IHV)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-149">**security (IHV)**</span></span>](wlan-profileschema-security-ihv-element.md)
        -   [<span data-ttu-id="7dafa-150">**useMSOneX (IHV)**</span><span class="sxs-lookup"><span data-stu-id="7dafa-150">**useMSOneX (IHV)**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)

 

 



