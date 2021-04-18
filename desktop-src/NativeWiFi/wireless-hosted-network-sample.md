---
description: Viene illustrato l'utilizzo di funzioni di rete ospitate senza fili.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Esempio di rete wireless ospitata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307724"
---
# <a name="wireless-hosted-network-sample"></a><span data-ttu-id="5d027-103">Esempio di rete wireless ospitata</span><span class="sxs-lookup"><span data-stu-id="5d027-103">Wireless Hosted Network Sample</span></span>

<span data-ttu-id="5d027-104">Un esempio di rete wireless ospitata che illustra l'utilizzo delle funzioni di rete ospitata senza fili è incluso in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="5d027-104">A wireless Hosted Network sample that demonstrates the use of wireless Hosted Network functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5d027-105">La versione più recente del Windows SDK è disponibile nell' [area download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span><span class="sxs-lookup"><span data-stu-id="5d027-105">The latest version of the Windows SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span>

<span data-ttu-id="5d027-106">Per impostazione predefinita, il codice sorgente di esempio di rete wireless ospitata è installato nella directory seguente:</span><span class="sxs-lookup"><span data-stu-id="5d027-106">By default, the wireless Hosted Network sample source code is installed in the following directory:</span></span>

<span data-ttu-id="5d027-107">**C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ NetDs \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="5d027-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="5d027-108">L'esempio wireless Hosted Network si trova nella cartella seguente:</span><span class="sxs-lookup"><span data-stu-id="5d027-108">The wireless Hosted Network sample is located under the following folder:</span></span>

<span data-ttu-id="5d027-109">**WirelessHostedNetwork**</span><span class="sxs-lookup"><span data-stu-id="5d027-109">**WirelessHostedNetwork**</span></span>

<span data-ttu-id="5d027-110">È possibile compilare l'esempio wireless Hosted Network nell'Windows SDK per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5d027-110">The Wireless Hosted Network sample can be compiled on the Windows SDK for Windows 7.</span></span> <span data-ttu-id="5d027-111">L'esempio wireless Hosted Network può essere eseguito in Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato.</span><span class="sxs-lookup"><span data-stu-id="5d027-111">The Wireless Hosted Network sample can be run on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span>

<span data-ttu-id="5d027-112">In Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato, il sistema operativo installa un dispositivo virtuale se nel computer è presente una scheda di rete ospitata che supporta la connessione wireless.</span><span class="sxs-lookup"><span data-stu-id="5d027-112">On Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine.</span></span> <span data-ttu-id="5d027-113">Questo dispositivo virtuale viene normalmente visualizzato nella "cartella connessioni di rete" come "connessione di rete wireless 2" con il nome del dispositivo "Microsoft Virtual WiFi Miniport Adapter" Se il computer dispone di una singola scheda di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="5d027-113">This virtual device normally shows up in the "Network Connections Folder" as "Wireless Network Connection 2" with a Device Name of "Microsoft Virtual WiFi Miniport adapter" if the computer has a single wireless network adapter.</span></span> <span data-ttu-id="5d027-114">Questo dispositivo virtuale viene usato esclusivamente per eseguire le connessioni del punto di accesso software (SoftAP).</span><span class="sxs-lookup"><span data-stu-id="5d027-114">This virtual device is used exclusively for performing software access point (SoftAP) connections.</span></span> <span data-ttu-id="5d027-115">La durata del dispositivo virtuale è legata alla scheda wireless fisica.</span><span class="sxs-lookup"><span data-stu-id="5d027-115">The lifetime of this virtual device is tied to the physical wireless adapter.</span></span> <span data-ttu-id="5d027-116">Se la scheda fisica wireless è disabilitata, verrà rimosso anche questo dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="5d027-116">If the physical wireless adapter is disabled, this virtual device will be removed as well.</span></span>

<span data-ttu-id="5d027-117">Le funzioni di rete ospitata senza fili vengono utilizzate per avviare e arrestare la rete ospitata senza fili, configurare o modificare le impostazioni oppure eseguire una query per ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="5d027-117">The wireless Hosted Network functions are used to start and stop the wireless Hosted Network, configure or change settings, or query for information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d027-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d027-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d027-119">Informazioni sulla rete wireless ospitata</span><span class="sxs-lookup"><span data-stu-id="5d027-119">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="5d027-120">Uso della condivisione connessione Internet e della rete ospitata</span><span class="sxs-lookup"><span data-stu-id="5d027-120">Using Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[<span data-ttu-id="5d027-121">**WlanHostedNetworkForceStart**</span><span class="sxs-lookup"><span data-stu-id="5d027-121">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[<span data-ttu-id="5d027-122">**WlanHostedNetworkInitSettings**</span><span class="sxs-lookup"><span data-stu-id="5d027-122">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[<span data-ttu-id="5d027-123">**WlanHostedNetworkQueryProperty**</span><span class="sxs-lookup"><span data-stu-id="5d027-123">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[<span data-ttu-id="5d027-124">**WlanHostedNetworkQuerySecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="5d027-124">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[<span data-ttu-id="5d027-125">**WlanHostedNetworkQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="5d027-125">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[<span data-ttu-id="5d027-126">**WlanHostedNetworkRefreshSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="5d027-126">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[<span data-ttu-id="5d027-127">**WlanHostedNetworkSetProperty**</span><span class="sxs-lookup"><span data-stu-id="5d027-127">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[<span data-ttu-id="5d027-128">**WlanHostedNetworkSetSecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="5d027-128">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[<span data-ttu-id="5d027-129">**WlanHostedNetworkStartUsing**</span><span class="sxs-lookup"><span data-stu-id="5d027-129">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[<span data-ttu-id="5d027-130">**WlanHostedNetworkStopUsing**</span><span class="sxs-lookup"><span data-stu-id="5d027-130">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[<span data-ttu-id="5d027-131">**WlanRegisterVirtualStationNotification**</span><span class="sxs-lookup"><span data-stu-id="5d027-131">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



