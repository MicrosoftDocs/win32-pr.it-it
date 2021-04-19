---
description: Viene illustrato l'utilizzo delle funzioni di gestione di rete wireless di base.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Esempio di API WiFi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311689"
---
# <a name="native-wifi-api-sample"></a><span data-ttu-id="16a13-103">Esempio di API WiFi nativa</span><span class="sxs-lookup"><span data-stu-id="16a13-103">Native Wifi API Sample</span></span>

<span data-ttu-id="16a13-104">Con Microsoft Windows Software Development Kit (SDK) è incluso un esempio di API Wi-Fi nativo che illustra l'uso delle funzioni di gestione di rete wireless di base.</span><span class="sxs-lookup"><span data-stu-id="16a13-104">A Native Wifi API sample that demonstrates the use of basic wireless network management functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="16a13-105">La versione più recente del Windows SDK è disponibile nell' [area download](https://developer.microsoft.com/windows/downloads).</span><span class="sxs-lookup"><span data-stu-id="16a13-105">The latest version of the Windows SDK is available from the [Download Center](https://developer.microsoft.com/windows/downloads).</span></span>

<span data-ttu-id="16a13-106">Per impostazione predefinita, il codice sorgente di esempio di WiFi nativo viene installato nella directory seguente:</span><span class="sxs-lookup"><span data-stu-id="16a13-106">By default, the Native Wifi sample source code is installed in the following directory:</span></span>

<span data-ttu-id="16a13-107">**C: \\ programmi \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="16a13-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="16a13-108">L'esempio di API WiFi nativa si trova nella cartella seguente:</span><span class="sxs-lookup"><span data-stu-id="16a13-108">The Native Wifi API sample is located under the following folder:</span></span>

<span data-ttu-id="16a13-109">**AutoConfig**</span><span class="sxs-lookup"><span data-stu-id="16a13-109">**autoconfig**</span></span>

<span data-ttu-id="16a13-110">Questo esempio può essere compilato ed eseguito in Windows Vista e versioni successive, Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="16a13-110">The Native Wifi sample can be compiled and run on Windows Vista and later, Windows XP with Service Pack 3 (SP3), and Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="16a13-111">Alcune funzionalità dell'esempio non sono supportate in Windows XP con SP3 e nell'API LAN wireless per Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="16a13-111">Some features of the sample are not supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="16a13-112">Per un elenco delle funzioni supportate da Windows XP con SP3 e dall'API LAN wireless per Windows XP con SP2, vedere [supporto per le API WiFi native in Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span><span class="sxs-lookup"><span data-stu-id="16a13-112">For a list of functions supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, see [Native Wifi API Support on Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span></span>

<span data-ttu-id="16a13-113">Nell'esempio di connessione Wi-Fi nativa viene illustrato come eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="16a13-113">The Native Wifi sample demonstrates how to perform the following tasks:</span></span>

-   <span data-ttu-id="16a13-114">Enumerare le interfacce wireless.</span><span class="sxs-lookup"><span data-stu-id="16a13-114">Enumerate wireless interfaces.</span></span> <span data-ttu-id="16a13-115">Vedere [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span><span class="sxs-lookup"><span data-stu-id="16a13-115">See [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span></span>
-   <span data-ttu-id="16a13-116">Ottenere le funzionalità di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="16a13-116">Get the capabilities of an interface.</span></span> <span data-ttu-id="16a13-117">Vedere [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span><span class="sxs-lookup"><span data-stu-id="16a13-117">See [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span></span>

    <span data-ttu-id="16a13-118">\* \* Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2: \* \* questa funzionalità non è supportata.</span><span class="sxs-lookup"><span data-stu-id="16a13-118">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* This feature is not supported.</span></span>

-   <span data-ttu-id="16a13-119">Eseguire una query su un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="16a13-119">Query an interface.</span></span> <span data-ttu-id="16a13-120">Vedere [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span><span class="sxs-lookup"><span data-stu-id="16a13-120">See [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span></span>
-   <span data-ttu-id="16a13-121">Impostare i parametri per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="16a13-121">Set parameters for a network interface.</span></span> <span data-ttu-id="16a13-122">Vedere [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span><span class="sxs-lookup"><span data-stu-id="16a13-122">See [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span></span> <span data-ttu-id="16a13-123">Questa funzione può essere utilizzata per attivare e disattivare la radio wireless (e quindi abilitare o disabilitare la connettività di rete wireless).</span><span class="sxs-lookup"><span data-stu-id="16a13-123">This function can be used to turn the wireless radio on and off (and therefore enable or disable wireless network connectivity).</span></span>
-   <span data-ttu-id="16a13-124">Ricercare le reti wireless disponibili.</span><span class="sxs-lookup"><span data-stu-id="16a13-124">Scan for available wireless networks.</span></span> <span data-ttu-id="16a13-125">Vedere [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span><span class="sxs-lookup"><span data-stu-id="16a13-125">See [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span></span>
-   <span data-ttu-id="16a13-126">Ottiene l'elenco delle reti wireless disponibili o visibili.</span><span class="sxs-lookup"><span data-stu-id="16a13-126">Get the list of available or visible wireless networks.</span></span> <span data-ttu-id="16a13-127">Vedere [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span><span class="sxs-lookup"><span data-stu-id="16a13-127">See [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span></span>
-   <span data-ttu-id="16a13-128">Ottenere, salvare o eliminare un profilo.</span><span class="sxs-lookup"><span data-stu-id="16a13-128">Get, save, or delete a profile.</span></span> <span data-ttu-id="16a13-129">Vedere [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)e [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span><span class="sxs-lookup"><span data-stu-id="16a13-129">See [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), and [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span></span>
-   <span data-ttu-id="16a13-130">Connettersi o disconnettersi da una rete wireless.</span><span class="sxs-lookup"><span data-stu-id="16a13-130">Connect to or disconnect from a wireless network.</span></span> <span data-ttu-id="16a13-131">Vedere [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) e [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span><span class="sxs-lookup"><span data-stu-id="16a13-131">See [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) and [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span></span>

## <a name="related-topics"></a><span data-ttu-id="16a13-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16a13-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16a13-133">Uso del WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="16a13-133">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="16a13-134">Forum su Windows Vista Wireless SDK</span><span class="sxs-lookup"><span data-stu-id="16a13-134">Windows Vista Wireless SDK Forum</span></span>](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

<span data-ttu-id="16a13-135">[Risoluzione dei problemi relativi alle connessioni wireless di Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="16a13-135">[Troubleshooting Windows Vista 802.11 Wireless Connections](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span></span>
</dt> </dl>

 

 
