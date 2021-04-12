---
description: Un subset della funzionalità API WiFi nativa è supportato in Windows XP con Service Pack 2 (SP2) e Windows XP con Service Pack 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Supporto per le API WiFi native in Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346011"
---
# <a name="native-wifi-api-support-on-windows-xp"></a><span data-ttu-id="a42e3-103">Supporto per le API WiFi native in Windows XP</span><span class="sxs-lookup"><span data-stu-id="a42e3-103">Native Wifi API Support on Windows XP</span></span>

<span data-ttu-id="a42e3-104">Un subset della funzionalità API WiFi nativa è supportato in Windows XP con Service Pack 2 (SP2) e Windows XP con Service Pack 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="a42e3-104">A subset of the Native Wifi API functionality is supported on Windows XP with Service Pack 2 (SP2) and Windows XP with Service Pack 3 (SP3).</span></span> <span data-ttu-id="a42e3-105">Questa funzionalità è inclusa in Windows XP con SP3 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a42e3-105">This functionality is included in Windows XP with SP3 by default.</span></span> <span data-ttu-id="a42e3-106">In Windows XP con SP2 è possibile aggiungere questa funzionalità applicando un hotfix, noto come API LAN wireless per Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="a42e3-106">In Windows XP with SP2, this functionality can be added by applying a hotfix, which is known as Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="a42e3-107">Per ulteriori informazioni o per scaricare l'hotfix, vedere "gli sviluppatori non possono creare programmi client wireless che gestiscono profili e connessioni wireless tramite il servizio Wireless Zero Configuration in Microsoft Windows XP Service Pack 2 (SP2)" nella guida e supporto tecnico all'indirizzo [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .</span><span class="sxs-lookup"><span data-stu-id="a42e3-107">For more information or to download the hotfix, see "Developers cannot create wireless client programs that manage wireless profiles and connections over the Wireless Zero Configuration service in Microsoft Windows XP Service Pack 2 (SP2)" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997).</span></span>

<span data-ttu-id="a42e3-108">A causa delle differenze di architettura sottostanti in Windows XP, l'API WiFi nativa di presenta alcune limitazioni.</span><span class="sxs-lookup"><span data-stu-id="a42e3-108">Because of underlying architectural differences in Windows XP, the Native Wifi API on has some limitations.</span></span> <span data-ttu-id="a42e3-109">Di seguito è riportato un elenco di limitazioni:</span><span class="sxs-lookup"><span data-stu-id="a42e3-109">Here is a list of limitations:</span></span>

-   <span data-ttu-id="a42e3-110">Al massimo un SSID può essere associato a un profilo.</span><span class="sxs-lookup"><span data-stu-id="a42e3-110">At most one SSID can be associated with a profile.</span></span>
-   <span data-ttu-id="a42e3-111">Le reti dell'infrastruttura vengono sempre visualizzate prima delle reti ad hoc nell'elenco dei profili.</span><span class="sxs-lookup"><span data-stu-id="a42e3-111">Infrastructure networks always appear before ad hoc networks in the profile list.</span></span>
-   <span data-ttu-id="a42e3-112">I nomi dei profili derivano dall'SSID e non possono essere impostati dall'utente su una stringa arbitraria.</span><span class="sxs-lookup"><span data-stu-id="a42e3-112">Profile names are derived from the SSID, and cannot be set by the user to an arbitrary string.</span></span>
-   <span data-ttu-id="a42e3-113">I tipi PHY non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="a42e3-113">PHY types are not supported.</span></span>
-   <span data-ttu-id="a42e3-114">La memorizzazione nella cache Pairwise Master Key (PMK) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a42e3-114">Pairwise master key (PMK) caching is not supported.</span></span>
-   <span data-ttu-id="a42e3-115">Le funzioni di estensibilità del fornitore di hardware indipendente (IHV) non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="a42e3-115">Independent hardware vendor (IHV) extensibility functions are not supported.</span></span>
-   <span data-ttu-id="a42e3-116">Le autorizzazioni del profilo non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="a42e3-116">Profile permissions are not supported.</span></span>
-   <span data-ttu-id="a42e3-117">\_Sono disponibili solo la \_ connessione ACM per le notifiche \_ di WLAN \_ e le notifiche di notifica di rete WLAN \_ \_ ACM \_ disconnesse.</span><span class="sxs-lookup"><span data-stu-id="a42e3-117">Only the wlan\_notification\_acm\_connection\_complete and the wlan\_notification\_acm\_disconnected notifications are available.</span></span>
-   <span data-ttu-id="a42e3-118">Le impostazioni di configurazione globali 802.1 X e avvio EAPOL non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="a42e3-118">Global 802.1X and EAPOL configuration settings are not supported.</span></span>

<span data-ttu-id="a42e3-119">Le funzioni seguenti sono supportate da Windows XP con SP3 e dall'API LAN wireless per Windows XP con SP2:</span><span class="sxs-lookup"><span data-stu-id="a42e3-119">The following functions are supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>

-   [<span data-ttu-id="a42e3-120">**\_callback notifiche \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="a42e3-120">**WLAN\_NOTIFICATION\_CALLBACK**</span></span>](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [<span data-ttu-id="a42e3-121">**WlanAllocateMemory**</span><span class="sxs-lookup"><span data-stu-id="a42e3-121">**WlanAllocateMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [<span data-ttu-id="a42e3-122">**WlanCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="a42e3-122">**WlanCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [<span data-ttu-id="a42e3-123">**WlanConnect**</span><span class="sxs-lookup"><span data-stu-id="a42e3-123">**WlanConnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [<span data-ttu-id="a42e3-124">**WlanDeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="a42e3-124">**WlanDeleteProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [<span data-ttu-id="a42e3-125">**WlanDisconnect**</span><span class="sxs-lookup"><span data-stu-id="a42e3-125">**WlanDisconnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [<span data-ttu-id="a42e3-126">**WlanEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="a42e3-126">**WlanEnumInterfaces**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [<span data-ttu-id="a42e3-127">**WlanFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="a42e3-127">**WlanFreeMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [<span data-ttu-id="a42e3-128">**WlanGetAvailableNetworkList**</span><span class="sxs-lookup"><span data-stu-id="a42e3-128">**WlanGetAvailableNetworkList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [<span data-ttu-id="a42e3-129">**WlanGetProfile**</span><span class="sxs-lookup"><span data-stu-id="a42e3-129">**WlanGetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [<span data-ttu-id="a42e3-130">**WlanGetProfileList**</span><span class="sxs-lookup"><span data-stu-id="a42e3-130">**WlanGetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [<span data-ttu-id="a42e3-131">**WlanOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="a42e3-131">**WlanOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [<span data-ttu-id="a42e3-132">**WlanQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="a42e3-132">**WlanQueryInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [<span data-ttu-id="a42e3-133">**WlanReasonCodeToString**</span><span class="sxs-lookup"><span data-stu-id="a42e3-133">**WlanReasonCodeToString**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [<span data-ttu-id="a42e3-134">**WlanRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="a42e3-134">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [<span data-ttu-id="a42e3-135">**WlanScan**</span><span class="sxs-lookup"><span data-stu-id="a42e3-135">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [<span data-ttu-id="a42e3-136">**WlanSetInterface**</span><span class="sxs-lookup"><span data-stu-id="a42e3-136">**WlanSetInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [<span data-ttu-id="a42e3-137">**WlanSetProfile**</span><span class="sxs-lookup"><span data-stu-id="a42e3-137">**WlanSetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [<span data-ttu-id="a42e3-138">**WlanSetProfileEapXmlUserData**</span><span class="sxs-lookup"><span data-stu-id="a42e3-138">**WlanSetProfileEapXmlUserData**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [<span data-ttu-id="a42e3-139">**WlanSetProfileList**</span><span class="sxs-lookup"><span data-stu-id="a42e3-139">**WlanSetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [<span data-ttu-id="a42e3-140">**WlanSetProfilePosition**</span><span class="sxs-lookup"><span data-stu-id="a42e3-140">**WlanSetProfilePosition**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a><span data-ttu-id="a42e3-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a42e3-141">Related topics</span></span>

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[<span data-ttu-id="a42e3-142">Informazioni sul Wi-Fi nativo</span><span class="sxs-lookup"><span data-stu-id="a42e3-142">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 
