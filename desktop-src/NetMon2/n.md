---
description: Glossario dei termini Network Monitor che iniziano con la lettera N.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: N (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54404640b13bff3b098b9d223e656e8f1905c055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883662"
---
# <a name="n-network-monitor"></a><span data-ttu-id="3e7c5-103">N (Network Monitor)</span><span class="sxs-lookup"><span data-stu-id="3e7c5-103">N (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="3e7c5-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span><span class="sxs-lookup"><span data-stu-id="3e7c5-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span></span>
</dt> <dd>

<span data-ttu-id="3e7c5-105">Vedere Specifica dell'interfaccia del driver di rete.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-105">See network driver interface specification.</span></span>

</dd> <dt>

<span data-ttu-id="3e7c5-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**specifiche di Network Driver Interface (NDIS)**</span><span class="sxs-lookup"><span data-stu-id="3e7c5-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**network driver interface specification (NDIS)**</span></span>
</dt> <dd>

<span data-ttu-id="3e7c5-107">Specifica per l'interfaccia tra i driver di dispositivo e una rete.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-107">The specification for the interface between device drivers and a network.</span></span> <span data-ttu-id="3e7c5-108">Tutti i trasporti chiamano l'interfaccia NDIS per accedere alle schede di interfaccia di rete e utilizzarle.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-108">All transports call the NDIS interface to access and work with network interface cards.</span></span>

</dd> <dt>

<span data-ttu-id="3e7c5-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Agente di Network Monitor**</span><span class="sxs-lookup"><span data-stu-id="3e7c5-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Network Monitor agent**</span></span>
</dt> <dd>

<span data-ttu-id="3e7c5-110">Componente Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-110">A Network Monitor component.</span></span> <span data-ttu-id="3e7c5-111">L'agente consente a un computer remoto di acquisire i dati dalla rete.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-111">The agent enables a remote computer to capture data from the network.</span></span> <span data-ttu-id="3e7c5-112">Quando un'installazione di Network Monitor si connette in remoto all'agente di Network Monitor e avvia un'acquisizione, le statistiche dall'acquisizione vengono trasferite attraverso la rete al computer di gestione.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-112">When a Network Monitor installation connects remotely to the Network Monitor agent and initiates a capture, statistics from the capture are transferred over the network to the managing computer.</span></span> <span data-ttu-id="3e7c5-113">Il trasferimento procede a intervalli specificati quando viene steffettuata la connessione.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-113">The transfer proceeds at intervals specified when the connection is made.</span></span>

</dd> <dt>

<span data-ttu-id="3e7c5-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**provider di pacchetti di rete (NPP)**</span><span class="sxs-lookup"><span data-stu-id="3e7c5-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**network packet provider (NPP)**</span></span>
</dt> <dd>

<span data-ttu-id="3e7c5-115">Il componente Network Monitor che raccoglie il traffico di rete nei frame, quindi passa i frame a un'applicazione Expert e NPP.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-115">The Network Monitor component that collects network traffic in frames, and then passes the frames to an expert, and NPP application.</span></span> <span data-ttu-id="3e7c5-116">Un NPP usa il driver di sistema Network Monitor (Nmnt.sys) per ottenere i frame raccolti dalla rete e offre diverse interfacce COM che passano i frame a un'applicazione Expert, monitor e Network Packet Provider (NPP) in cui possono essere visualizzati e analizzati.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-116">An NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network, and provides several COM interfaces that pass the frames to an expert, monitor, and network packet provider (NPP) application where they can be displayed and analyzed.</span></span>

</dd> <dt>

<span data-ttu-id="3e7c5-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span><span class="sxs-lookup"><span data-stu-id="3e7c5-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span></span>
</dt> <dd>

<span data-ttu-id="3e7c5-118">Vedere provider di pacchetti di rete.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-118">See network packet provider.</span></span>

</dd> <dt>

<span data-ttu-id="3e7c5-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**Applicazione NPP**</span><span class="sxs-lookup"><span data-stu-id="3e7c5-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**NPP application**</span></span>
</dt> <dd>

<span data-ttu-id="3e7c5-120">Applicazione che ignora sia l'interfaccia utente di Network Monitor che lo strumento di controllo del monitoraggio e si connette direttamente al provider di pacchetti di rete (NPP).</span><span class="sxs-lookup"><span data-stu-id="3e7c5-120">An application that bypasses both the Network Monitor UI and Monitor Control Tool, and connects directly to the network packet provider (NPP).</span></span> <span data-ttu-id="3e7c5-121">Un'applicazione NPP può connettersi al componente NPP con una delle cinque interfacce COM di NPP.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-121">An NPP application can connect to the NPP component with any of the five NPP COM interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="3e7c5-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**Ricerca NPP**</span><span class="sxs-lookup"><span data-stu-id="3e7c5-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**NPP Finder**</span></span>
</dt> <dd>

<span data-ttu-id="3e7c5-123">Componente Network Monitor che comunica con centrali.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-123">The Network Monitor component that communicates with NPPs.</span></span>

</dd> </dl>

 

 



