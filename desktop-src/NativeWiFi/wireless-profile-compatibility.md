---
description: A causa delle differenze di architettura sottostanti nel sistema operativo, Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2) supportano solo un subset degli elementi descritti nello \_ schema del profilo WLAN e il materiale di riferimento dello schema Onex.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilità del profilo wireless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529239"
---
# <a name="wireless-profile-compatibility"></a><span data-ttu-id="1602e-103">Compatibilità del profilo wireless</span><span class="sxs-lookup"><span data-stu-id="1602e-103">Wireless Profile Compatibility</span></span>

<span data-ttu-id="1602e-104">A causa delle differenze di architettura sottostanti nel sistema operativo, Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2) supportano solo un subset degli elementi descritti [nello \_ schema del profilo WLAN](wlan-profileschema-schema.md) e il materiale di riferimento [dello schema Onex](onexschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="1602e-104">Because of underlying architectural differences in the operating system, Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) support only a subset of the elements described in the [WLAN\_profile Schema](wlan-profileschema-schema.md) and [OneX Schema](onexschema-schema.md) reference material.</span></span>

<span data-ttu-id="1602e-105">Tutti i profili conformi ai requisiti di Windows XP con SP3 e dell'API LAN wireless per Windows XP con SP2 possono essere utilizzati anche in Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1602e-105">All profiles that conform to Windows XP with SP3 and Wireless LAN API for Windows XP with SP2 requirements can also be used on Windows Vista and Windows Server 2008.</span></span>

## <a name="wlan_profile-support"></a><span data-ttu-id="1602e-106">\_Supporto del profilo WLAN</span><span class="sxs-lookup"><span data-stu-id="1602e-106">WLAN\_profile Support</span></span>

<span data-ttu-id="1602e-107">Gli elementi del \_ profilo WLAN seguenti non sono supportati in Windows XP con SP3 o l'API LAN wireless per Windows XP con SP2:</span><span class="sxs-lookup"><span data-stu-id="1602e-107">The following WLAN\_profile elements are not supported in Windows XP with SP3 or Wireless LAN API for Windows XP with SP2:</span></span>

-   <span data-ttu-id="1602e-108">connettività (IHV)</span><span class="sxs-lookup"><span data-stu-id="1602e-108">connectivity (IHV)</span></span>
-   <span data-ttu-id="1602e-109">IHV (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="1602e-109">IHV (WLANProfile)</span></span>
-   <span data-ttu-id="1602e-110">OUI (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="1602e-110">OUI (OUIHeader)</span></span>
-   <span data-ttu-id="1602e-111">phyType (connettività)</span><span class="sxs-lookup"><span data-stu-id="1602e-111">phyType (connectivity)</span></span>
-   <span data-ttu-id="1602e-112">PMKCacheMode (sicurezza)</span><span class="sxs-lookup"><span data-stu-id="1602e-112">PMKCacheMode (security)</span></span>
-   <span data-ttu-id="1602e-113">PMKCacheSize (sicurezza)</span><span class="sxs-lookup"><span data-stu-id="1602e-113">PMKCacheSize (security)</span></span>
-   <span data-ttu-id="1602e-114">PMKCacheTTL (sicurezza)</span><span class="sxs-lookup"><span data-stu-id="1602e-114">PMKCacheTTL (security)</span></span>
-   <span data-ttu-id="1602e-115">preAuthMode (sicurezza)</span><span class="sxs-lookup"><span data-stu-id="1602e-115">preAuthMode (security)</span></span>
-   <span data-ttu-id="1602e-116">preAuthThrottle (sicurezza)</span><span class="sxs-lookup"><span data-stu-id="1602e-116">preAuthThrottle (security)</span></span>
-   <span data-ttu-id="1602e-117">sicurezza (IHV)</span><span class="sxs-lookup"><span data-stu-id="1602e-117">security (IHV)</span></span>
-   <span data-ttu-id="1602e-118">tipo (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="1602e-118">type (OUIHeader)</span></span>
-   <span data-ttu-id="1602e-119">useMSOneX (IHV)</span><span class="sxs-lookup"><span data-stu-id="1602e-119">useMSOneX (IHV)</span></span>

<span data-ttu-id="1602e-120">La tabella seguente mostra \_ gli elementi del profilo WLAN con valori vincolati per Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:</span><span class="sxs-lookup"><span data-stu-id="1602e-120">The following table shows WLAN\_profile elements with constrained values for Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>



| <span data-ttu-id="1602e-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="1602e-121">Element</span></span>                                                                               | <span data-ttu-id="1602e-122">Vincolo</span><span class="sxs-lookup"><span data-stu-id="1602e-122">Constraint</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1602e-123">**nome (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="1602e-123">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)             | <span data-ttu-id="1602e-124">L'elemento Name viene ignorato quando il profilo viene salvato nell'archivio profili.</span><span class="sxs-lookup"><span data-stu-id="1602e-124">The name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="1602e-125">Il nome del profilo viene derivato automaticamente dall'SSID della rete.</span><span class="sxs-lookup"><span data-stu-id="1602e-125">The name of the profile is derived automatically from the SSID of the network.</span></span> <span data-ttu-id="1602e-126">Per i profili di rete dell'infrastruttura, il nome del profilo è il SSID della rete.</span><span class="sxs-lookup"><span data-stu-id="1602e-126">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="1602e-127">Per i profili di rete ad hoc, il nome del profilo è il SSID della rete ad hoc seguita da `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="1602e-127">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> |
| [<span data-ttu-id="1602e-128">**protetto (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="1602e-128">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)       | <span data-ttu-id="1602e-129">Il valore di deve essere FALSE.</span><span class="sxs-lookup"><span data-stu-id="1602e-129">Must have a value of FALSE.</span></span>                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="1602e-130">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="1602e-130">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md) | <span data-ttu-id="1602e-131">Limitato a un elemento [**SSID figlio (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1602e-131">Restricted to one child [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a><span data-ttu-id="1602e-132">Supporto di OneX</span><span class="sxs-lookup"><span data-stu-id="1602e-132">OneX Support</span></span>

<span data-ttu-id="1602e-133">Solo l'elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) è supportato in Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="1602e-133">Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="1602e-134">Gli altri elementi OneX, se presenti in un profilo, verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="1602e-134">Other OneX elements, if present in a profile, will be ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1602e-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1602e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1602e-136">Informazioni sull'API WiFi nativa</span><span class="sxs-lookup"><span data-stu-id="1602e-136">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="1602e-137">Supporto per le API WiFi native in Windows XP</span><span class="sxs-lookup"><span data-stu-id="1602e-137">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



