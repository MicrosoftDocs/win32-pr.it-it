---
description: Novità di Native WiFi
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Novità di Native WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309441"
---
# <a name="whats-new-in-native-wifi"></a><span data-ttu-id="f4b51-103">Novità di Native WiFi</span><span class="sxs-lookup"><span data-stu-id="f4b51-103">What's New in Native Wifi</span></span>

## <a name="windows-10-version-2004"></a><span data-ttu-id="f4b51-104">Windows 10, versione 2004</span><span class="sxs-lookup"><span data-stu-id="f4b51-104">Windows 10, version 2004</span></span>

<span data-ttu-id="f4b51-105">Vedere effettuare il [provisioning di un profilo di Wi-Fi tramite un sito Web](prov-wifi-profile-via-website.md).</span><span class="sxs-lookup"><span data-stu-id="f4b51-105">See [Provision a Wi-Fi profile via a website](prov-wifi-profile-via-website.md).</span></span>

## <a name="windows-10"></a><span data-ttu-id="f4b51-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f4b51-106">Windows 10</span></span>

<span data-ttu-id="f4b51-107">È stato aggiunto il supporto per Hotspot 2,0 allo [ \_ schema del profilo WLAN](wlan-profileschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="f4b51-107">Support for Hotspot 2.0 has been added to the [WLAN\_profile schema](wlan-profileschema-schema.md).</span></span> <span data-ttu-id="f4b51-108">Hotspot 2,0 consente la connessione automatica ai servizi Wi-Fi pubblici usando le credenziali esistenti e l'appartenenza alle reti del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="f4b51-108">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="f4b51-109">I provider di servizi specificano il modo in cui vengono stabilite le connessioni usando i nuovi elementi dello schema per descrivere le reti da usare e come eseguire l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f4b51-109">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span> <span data-ttu-id="f4b51-110">Per informazioni dettagliate, vedere la documentazione dell'elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f4b51-110">See the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element documentation for details.</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="f4b51-111">Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4b51-111">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="f4b51-112">Le funzionalità seguenti sono state aggiunte alle API native di Wi-Fi in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="f4b51-112">The following features have been added to the Native Wifi APIs on Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="f4b51-113">Una Wi-Fi funzionalità diretta basata sullo sviluppo di Wi-Fi specifiche tecniche peer-to-Peer v 1.1 da Wi-Fi Alliance (vedere le [specifiche pubblicate in Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="f4b51-113">A Wi-Fi Direct feature based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="f4b51-114">L'obiettivo della specifica tecnica peer-to-peer Wi-Fi è fornire una soluzione per Wi-Fi la connettività da dispositivo a dispositivo senza che sia necessario un punto di accesso wireless (AP wireless) per configurare la connessione o l'utilizzo del meccanismo di Wi-Fi ad hoc (IBSS) esistente.</span><span class="sxs-lookup"><span data-stu-id="f4b51-114">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism.</span></span>

<span data-ttu-id="f4b51-115">Le funzioni seguenti supportano la funzionalità Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="f4b51-115">The following functions support the Wi-Fi Direct feature.</span></span>

-   [<span data-ttu-id="f4b51-116">**\_ \_ callback completo della sessione di apertura della \_ direttiva GMA \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-116">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [<span data-ttu-id="f4b51-117">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="f4b51-117">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [<span data-ttu-id="f4b51-118">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="f4b51-118">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [<span data-ttu-id="f4b51-119">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="f4b51-119">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [<span data-ttu-id="f4b51-120">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="f4b51-120">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [<span data-ttu-id="f4b51-121">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="f4b51-121">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [<span data-ttu-id="f4b51-122">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="f4b51-122">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [<span data-ttu-id="f4b51-123">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="f4b51-123">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="f4b51-124">Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4b51-124">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="f4b51-125">Le funzionalità seguenti sono state aggiunte alle API native di Wi-Fi in Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f4b51-125">The following features have been added to the Native Wifi APIs on Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="f4b51-126">La rete wireless ospitata consente a una singola scheda di rete fisica di connettersi come client a un punto di accesso hardware (AP), mentre allo stesso tempo funge da AP software che consente ad altri dispositivi con supporto wireless di connettersi.</span><span class="sxs-lookup"><span data-stu-id="f4b51-126">The wireless Hosted Network allows a single physical wireless adapter to connect as a client to a hardware access point (AP), while at the same time acting as a software AP allowing other wireless-capable devices to connect to it.</span></span>

<span data-ttu-id="f4b51-127">Le funzioni seguenti supportano la funzionalità rete ospitata senza fili.</span><span class="sxs-lookup"><span data-stu-id="f4b51-127">The following functions support the wireless Hosted Network feature.</span></span>

-   [<span data-ttu-id="f4b51-128">**WlanHostedNetworkForceStart**</span><span class="sxs-lookup"><span data-stu-id="f4b51-128">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [<span data-ttu-id="f4b51-129">**WlanHostedNetworkForceStop**</span><span class="sxs-lookup"><span data-stu-id="f4b51-129">**WlanHostedNetworkForceStop**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [<span data-ttu-id="f4b51-130">**WlanHostedNetworkInitSettings**</span><span class="sxs-lookup"><span data-stu-id="f4b51-130">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [<span data-ttu-id="f4b51-131">**WlanHostedNetworkQueryProperty**</span><span class="sxs-lookup"><span data-stu-id="f4b51-131">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [<span data-ttu-id="f4b51-132">**WlanHostedNetworkQuerySecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="f4b51-132">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [<span data-ttu-id="f4b51-133">**WlanHostedNetworkQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="f4b51-133">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [<span data-ttu-id="f4b51-134">**WlanHostedNetworkRefreshSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="f4b51-134">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [<span data-ttu-id="f4b51-135">**WlanHostedNetworkSetProperty**</span><span class="sxs-lookup"><span data-stu-id="f4b51-135">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [<span data-ttu-id="f4b51-136">**WlanHostedNetworkSetSecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="f4b51-136">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [<span data-ttu-id="f4b51-137">**WlanHostedNetworkStartUsing**</span><span class="sxs-lookup"><span data-stu-id="f4b51-137">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [<span data-ttu-id="f4b51-138">**WlanHostedNetworkStopUsing**</span><span class="sxs-lookup"><span data-stu-id="f4b51-138">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [<span data-ttu-id="f4b51-139">**WlanRegisterVirtualStationNotification**</span><span class="sxs-lookup"><span data-stu-id="f4b51-139">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

<span data-ttu-id="f4b51-140">Le nuove strutture seguenti funzionano con la rete wireless ospitata.</span><span class="sxs-lookup"><span data-stu-id="f4b51-140">The following new structures that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="f4b51-141">**\_impostazioni di \_ connessione di rete ospitata da \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-141">**WLAN\_HOSTED\_NETWORK\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [<span data-ttu-id="f4b51-142">**\_ \_ \_ \_ \_ modifica stato peer di dati rete ospitata WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-142">**WLAN\_HOSTED\_NETWORK\_DATA\_PEER\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [<span data-ttu-id="f4b51-143">**\_ \_ stato peer di rete OSPITAta WLAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-143">**WLAN\_HOSTED\_NETWORK\_PEER\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [<span data-ttu-id="f4b51-144">**\_ \_ \_ stato radio rete ospitata WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-144">**WLAN\_HOSTED\_NETWORK\_RADIO\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [<span data-ttu-id="f4b51-145">**\_impostazioni di \_ sicurezza della rete ospitata da \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-145">**WLAN\_HOSTED\_NETWORK\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [<span data-ttu-id="f4b51-146">**\_ \_ \_ modifica dello stato della rete ospitata WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-146">**WLAN\_HOSTED\_NETWORK\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [<span data-ttu-id="f4b51-147">**\_stato rete ospitata WLAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-147">**WLAN\_HOSTED\_NETWORK\_STATUS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

<span data-ttu-id="f4b51-148">Le seguenti nuove enumerazioni che funzionano con la rete wireless ospitata.</span><span class="sxs-lookup"><span data-stu-id="f4b51-148">The following new enumerations that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="f4b51-149">**\_codice di \_ notifica della rete ospitata da \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-149">**WLAN\_HOSTED\_NETWORK\_NOTIFICATION\_CODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [<span data-ttu-id="f4b51-150">**\_ \_ codice operativo rete OSPITAta WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-150">**WLAN\_HOSTED\_NETWORK\_OPCODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [<span data-ttu-id="f4b51-151">**\_ \_ \_ \_ stato autenticazione peer rete ospitata WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-151">**WLAN\_HOSTED\_NETWORK\_PEER\_AUTH\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [<span data-ttu-id="f4b51-152">**\_motivo rete ospitata WLAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-152">**WLAN\_HOSTED\_NETWORK\_REASON**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [<span data-ttu-id="f4b51-153">**\_stato rete ospitata WLAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f4b51-153">**WLAN\_HOSTED\_NETWORK\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a><span data-ttu-id="f4b51-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4b51-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4b51-155">Informazioni sulla rete wireless ospitata</span><span class="sxs-lookup"><span data-stu-id="f4b51-155">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="f4b51-156">Uso della rete ospitata wireless e della condivisione della connessione Internet</span><span class="sxs-lookup"><span data-stu-id="f4b51-156">Using Wireless Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



