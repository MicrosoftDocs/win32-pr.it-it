---
description: Elenca le procedure di diagnostica da utilizzare per la risoluzione dei problemi relativi ai client di individuazione funzioni.
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Risoluzione dei problemi relativi ai client di individuazione delle funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753666"
---
# <a name="troubleshooting-function-discovery-clients"></a><span data-ttu-id="415cc-103">Risoluzione dei problemi relativi ai client di individuazione delle funzioni</span><span class="sxs-lookup"><span data-stu-id="415cc-103">Troubleshooting Function Discovery Clients</span></span>

<span data-ttu-id="415cc-104">Client di individuazione funzioni:</span><span class="sxs-lookup"><span data-stu-id="415cc-104">Function Discovery clients:</span></span>

-   <span data-ttu-id="415cc-105">Usare sempre WS-Discovery UDP per l'individuazione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="415cc-105">Always use UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="415cc-106">Avviare sempre le connessioni HTTP o HTTPS per lo scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="415cc-106">Always initiate HTTP or HTTPS connections for metadata exchange</span></span>
-   <span data-ttu-id="415cc-107">USA a volte l'individuazione diretta</span><span class="sxs-lookup"><span data-stu-id="415cc-107">Sometimes use directed discovery</span></span>
-   <span data-ttu-id="415cc-108">USA a volte un canale sicuro (HTTPS) per lo scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="415cc-108">Sometimes use a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="415cc-109">Nell'elenco seguente viene illustrata la sequenza tipica dei messaggi inviati e ricevuti dai client di individuazione funzioni.</span><span class="sxs-lookup"><span data-stu-id="415cc-109">The following list shows the typical sequence of messages sent and received by Function Discovery clients.</span></span> <span data-ttu-id="415cc-110">Non tutti i messaggi sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="415cc-110">Not all messages are mandatory.</span></span>

1.  <span data-ttu-id="415cc-111">Il client invia un messaggio [Probe](probe-message.md) per individuare i dispositivi e i servizi.</span><span class="sxs-lookup"><span data-stu-id="415cc-111">The client sends a [Probe](probe-message.md) message to discover devices and services.</span></span> <span data-ttu-id="415cc-112">Se il client utilizza l'individuazione diretta, il messaggio viene inviato tramite HTTP o HTTPS. in caso contrario, il messaggio viene inviato dal multicast UDP alla porta 3702.</span><span class="sxs-lookup"><span data-stu-id="415cc-112">If the client is using directed discovery then this message is sent over HTTP or HTTPS; otherwise, the message is sent by UDP multicast to port 3702.</span></span>
2.  <span data-ttu-id="415cc-113">Il client riceve i messaggi [ProbeMatches](probematches-message.md) da dispositivi o servizi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="415cc-113">The client receives [ProbeMatches](probematches-message.md) messages from matching devices or services.</span></span> <span data-ttu-id="415cc-114">I messaggi di individuazione indirizzati vengono inviati tramite HTTP o HTTPS. in caso contrario, questi messaggi vengono inviati dall'unicast UDP e provengono dalla porta 3702.</span><span class="sxs-lookup"><span data-stu-id="415cc-114">Directed discovery messages are sent over HTTP or HTTPS; otherwise, these messages are sent by UDP unicast and originate from port 3702.</span></span>
3.  <span data-ttu-id="415cc-115">Se non è stato incluso alcun XAddrs nel messaggio ProbeMatches, il client invierà un messaggio di [risoluzione](resolve-message.md) tramite multicast UDP alla porta 3702.</span><span class="sxs-lookup"><span data-stu-id="415cc-115">If no XAddrs were included in the ProbeMatches message, then the client will send a [Resolve](resolve-message.md) message by UDP multicast to port 3702.</span></span>
4.  <span data-ttu-id="415cc-116">Se è stato inviato un messaggio di [risoluzione](resolve-message.md) , il client riceve un messaggio [ResolveMatches](resolvematches-message.md) dai servizi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="415cc-116">If a [Resolve](resolve-message.md) message was sent, then the client receives a [ResolveMatches](resolvematches-message.md) message from matching services.</span></span> <span data-ttu-id="415cc-117">Questo messaggio viene inviato dall'unicast UDP dalla porta 3702 alla porta in cui ha avuto origine il messaggio di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="415cc-117">This message is sent by UDP unicast from port 3702 to the port where the Resolve message originated.</span></span>
5.  <span data-ttu-id="415cc-118">Il client invia un messaggio [Get](get--metadata-exchange--http-request-and-message.md) per richiedere i metadati dal dispositivo o dal servizio.</span><span class="sxs-lookup"><span data-stu-id="415cc-118">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to request metadata from the device or service.</span></span> <span data-ttu-id="415cc-119">Questo messaggio viene inviato da HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="415cc-119">This message is sent by HTTP or HTTPS.</span></span>
6.  <span data-ttu-id="415cc-120">Il client riceve un messaggio [GetResponse](getresponse--metadata-exchange--message.md) con i metadati del dispositivo o del servizio.</span><span class="sxs-lookup"><span data-stu-id="415cc-120">The client receives a [GetResponse](getresponse--metadata-exchange--message.md) message with the device or service metadata.</span></span> <span data-ttu-id="415cc-121">Questo messaggio viene inviato da HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="415cc-121">This message is sent by HTTP or HTTPS.</span></span>

<span data-ttu-id="415cc-122">Le seguenti procedure di diagnostica devono essere utilizzate (in ordine) per facilitare l'identificazione dei problemi relativi a un client di individuazione delle funzioni.</span><span class="sxs-lookup"><span data-stu-id="415cc-122">The following diagnostic procedures should be used (in order) to help identify problems with a Function Discovery client.</span></span>

<span data-ttu-id="415cc-123">**Per risolvere i problemi relativi a un client di individuazione funzioni**</span><span class="sxs-lookup"><span data-stu-id="415cc-123">**To troubleshoot a Function Discovery client**</span></span>

1.  <span data-ttu-id="415cc-124">Se si usa l'individuazione diretta, [risolvere i problemi di individuazione diretta](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="415cc-124">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="415cc-125">[Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="415cc-125">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="415cc-126">[Utilizzare un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="415cc-126">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="415cc-127">[Usare il client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="415cc-127">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="415cc-128">[Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="415cc-128">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="415cc-129">[Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="415cc-129">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="415cc-130">[Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="415cc-130">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="415cc-131">[Esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="415cc-131">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="415cc-132">Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in [Abilitazione della traccia di WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="415cc-132">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="415cc-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="415cc-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="415cc-134">Introduzione con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="415cc-134">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



