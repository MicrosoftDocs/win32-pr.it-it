---
description: Elenca le procedure di diagnostica da usare per la risoluzione dei problemi di Network Explorer.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Risoluzione dei problemi di Esplora reti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966671"
---
# <a name="troubleshooting-the-network-explorer"></a><span data-ttu-id="40a53-103">Risoluzione dei problemi di Esplora reti</span><span class="sxs-lookup"><span data-stu-id="40a53-103">Troubleshooting the Network Explorer</span></span>

<span data-ttu-id="40a53-104">Esplora reti:</span><span class="sxs-lookup"><span data-stu-id="40a53-104">The Network Explorer:</span></span>

-   <span data-ttu-id="40a53-105">Usa sempre WS-Discovery UDP per l'individuazione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="40a53-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="40a53-106">Avvia sempre una connessione HTTP o HTTPS per lo scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="40a53-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="40a53-107">USA a volte un canale sicuro (HTTPS) per lo scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="40a53-107">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="40a53-108">Per identificare i problemi con Esplora reti, è necessario usare le procedure di diagnostica seguenti (in ordine).</span><span class="sxs-lookup"><span data-stu-id="40a53-108">The following diagnostic procedures should be used (in order) to help identify problems with the Network Explorer.</span></span>

<span data-ttu-id="40a53-109">**Per risolvere i problemi di Esplora reti**</span><span class="sxs-lookup"><span data-stu-id="40a53-109">**To troubleshoot the Network Explorer**</span></span>

1.  <span data-ttu-id="40a53-110">[Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="40a53-110">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="40a53-111">[Utilizzare un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="40a53-111">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
3.  <span data-ttu-id="40a53-112">[Usare il client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="40a53-112">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
4.  <span data-ttu-id="40a53-113">[Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="40a53-113">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
5.  <span data-ttu-id="40a53-114">[Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="40a53-114">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
6.  <span data-ttu-id="40a53-115">[Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="40a53-115">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
7.  <span data-ttu-id="40a53-116">[Esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="40a53-116">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="40a53-117">Esplora reti usa l' [individuazione funzione](/previous-versions/windows/desktop/fundisc/fd-portal) per enumerare i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="40a53-117">The Network Explorer uses [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) to enumerate network devices.</span></span> <span data-ttu-id="40a53-118">Per ulteriori informazioni sulla risoluzione dei problemi, vedere [risoluzione dei problemi relativi ai client di individuazione funzioni](troubleshooting-function-discovery-clients.md).</span><span class="sxs-lookup"><span data-stu-id="40a53-118">For more troubleshooting information, see [Troubleshooting Function Discovery Clients](troubleshooting-function-discovery-clients.md).</span></span>

<span data-ttu-id="40a53-119">Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in [Abilitazione della traccia di WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="40a53-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40a53-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40a53-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40a53-121">Introduzione con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="40a53-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="40a53-122">Risoluzione dei problemi relativi ai client di individuazione delle funzioni</span><span class="sxs-lookup"><span data-stu-id="40a53-122">Troubleshooting Function Discovery Clients</span></span>](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
