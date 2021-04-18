---
description: Se l'host e il client generici possono vedersi reciprocamente nella rete, ma l'host e il client effettivi non possono, è probabile che il problema si trovi nei messaggi inviati tra gli endpoint sulla rete.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Uso del client di debug WSD per verificare il traffico multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f03e06baefc40bad843a5193b2cec604383251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312671"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a><span data-ttu-id="d94a8-103">Uso del client di debug WSD per verificare il traffico multicast</span><span class="sxs-lookup"><span data-stu-id="d94a8-103">Using WSD Debug Client to Verify Multicast Traffic</span></span>

<span data-ttu-id="d94a8-104">Se l'host e il client generici possono vedersi reciprocamente nella rete, ma l'host e il client effettivi non possono, è probabile che il problema si trovi nei messaggi inviati tra gli endpoint sulla rete.</span><span class="sxs-lookup"><span data-stu-id="d94a8-104">If the generic host and client can see each other on the network but the actual host and client cannot, it is likely that the problem is in the messages sent between the endpoints over the network.</span></span> <span data-ttu-id="d94a8-105">Per ulteriori informazioni sull'host e sul client generico, vedere [utilizzo di un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="d94a8-105">For more information about the generic host and client, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span> <span data-ttu-id="d94a8-106">Poiché le tracce di rete complete possono essere difficili da raccogliere, filtrare e leggere, lo strumento client di debug WSD può essere utilizzato per stampare i lati multicast dei messaggi WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="d94a8-106">Because full network traces can be difficult to collect, filter, and read, the WSD Debug Client tool can be used to print the multicast sides of WS-Discovery messages.</span></span>

<span data-ttu-id="d94a8-107">Il client di debug WSD in modalità multicast può ispezionare solo la metà dei messaggi, poiché il client non è in grado di stampare messaggi unicast.</span><span class="sxs-lookup"><span data-stu-id="d94a8-107">The WSD Debug Client in multicast mode can only inspect half of the messages, since the client cannot print unicast messages.</span></span> <span data-ttu-id="d94a8-108">Se il traffico unicast è di interesse, passare direttamente al [controllo delle tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="d94a8-108">If unicast traffic is of interest, skip directly to [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="d94a8-109">Questa procedura mostra un metodo che consente di visualizzare tutto il traffico multicast sulla rete.</span><span class="sxs-lookup"><span data-stu-id="d94a8-109">This procedure shows a method that will display all multicast traffic on the network.</span></span> <span data-ttu-id="d94a8-110">Per visualizzare solo il traffico multicast da e verso il dispositivo, vedere la sezione [Filtering WSD debug client results](#filtering-wsd-debug-client-results) riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="d94a8-110">To display only multicast traffic to and from the device, see the [Filtering WSD Debug Client Results](#filtering-wsd-debug-client-results) section below.</span></span>

<span data-ttu-id="d94a8-111">**Per usare il client di debug WSD per verificare il traffico multicast**</span><span class="sxs-lookup"><span data-stu-id="d94a8-111">**To use the WSD Debug Client to verify multicast traffic**</span></span>

1.  <span data-ttu-id="d94a8-112">Configurare l'host e il client in modo che vengano eseguiti attraverso la rete (ovvero, assicurarsi che l'host e il client operino in computer diversi).</span><span class="sxs-lookup"><span data-stu-id="d94a8-112">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="d94a8-113">Aprire un prompt dei comandi ed eseguire il comando seguente: **WSDDebug \_client.exe/Mode multicast**</span><span class="sxs-lookup"><span data-stu-id="d94a8-113">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
3.  <span data-ttu-id="d94a8-114">Riprodurre l'errore avviando l'host e il client o premendo F5 in Network Explorer.</span><span class="sxs-lookup"><span data-stu-id="d94a8-114">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
4.  <span data-ttu-id="d94a8-115">Verificare che i messaggi siano multicast.</span><span class="sxs-lookup"><span data-stu-id="d94a8-115">Verify that messages are being multicast.</span></span>

<span data-ttu-id="d94a8-116">Se i messaggi richiesti vengono visualizzati nell'output del client di debug WSD, l'errore dell'applicazione potrebbe trovarsi nel contenuto del messaggio multicast o nell'esistenza o nel contenuto dei messaggi di risposta unicast corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="d94a8-116">If the required messages are displayed in the WSD Debug Client output, then the application failure may be in the multicast message content, or in the existence or content of the corresponding unicast response messages.</span></span> <span data-ttu-id="d94a8-117">Continuare la risoluzione dei problemi seguendo le istruzioni riportate in [ispezione delle tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="d94a8-117">Continue troubleshooting by following the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="d94a8-118">Se i messaggi richiesti vengono visualizzati nell'output del client di debug WSD, è probabile che l'origine del problema dell'applicazione sia stata identificata.</span><span class="sxs-lookup"><span data-stu-id="d94a8-118">If the required messages are displayed in the WSD Debug Client output, then it is likely that the source of the application problem has been identified.</span></span> <span data-ttu-id="d94a8-119">È probabile che il traffico multicast non venga trasmesso sulla rete.</span><span class="sxs-lookup"><span data-stu-id="d94a8-119">It is likely that the multicast traffic is not being transmitted on the network.</span></span> <span data-ttu-id="d94a8-120">Questo errore può verificarsi quando l'applicazione non enumera correttamente gli adapter multicast.</span><span class="sxs-lookup"><span data-stu-id="d94a8-120">This failure can happen when the application does not enumerate multicast adapters correctly.</span></span> <span data-ttu-id="d94a8-121">Le applicazioni devono inviare in modo esplicito il traffico multicast su tutte le interfacce di rete. in caso contrario, è possibile che i pacchetti non vengano generati per l'interfaccia di loopback o per altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="d94a8-121">Applications must explicitly send multicast traffic over all network interfaces; otherwise, packets may not be generated for the loopback interface or for other interfaces.</span></span> <span data-ttu-id="d94a8-122">Per verificare che i pacchetti non siano visualizzati sulla rete, seguire le istruzioni riportate in [ispezione delle tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) e cercare le evidenze dei messaggi multicast mancanti.</span><span class="sxs-lookup"><span data-stu-id="d94a8-122">To verify that the packets are not appearing on the network, follow the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and look for evidence of missing multicast messages.</span></span>

## <a name="verifying-that-messages-are-being-multicast"></a><span data-ttu-id="d94a8-123">Verifica del multicast dei messaggi</span><span class="sxs-lookup"><span data-stu-id="d94a8-123">Verifying that messages are being multicast</span></span>

<span data-ttu-id="d94a8-124">Verificare sempre che i messaggi [Probe](probe-message.md) siano in multicast.</span><span class="sxs-lookup"><span data-stu-id="d94a8-124">Always verify that [Probe](probe-message.md) messages are being multicast.</span></span> <span data-ttu-id="d94a8-125">Facoltativamente, verificare che i messaggi [Hello](hello-message.md) e [Resolve](resolve-message.md) siano in multicast.</span><span class="sxs-lookup"><span data-stu-id="d94a8-125">Optionally, verify that [Hello](hello-message.md) and [Resolve](resolve-message.md) messages are being multicast.</span></span> <span data-ttu-id="d94a8-126">Si noti che non tutte le applicazioni utilizzano i messaggi di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="d94a8-126">Note that not all applications use Resolve messages.</span></span> <span data-ttu-id="d94a8-127">Per ulteriori informazioni sui modelli di messaggio utilizzati da client e host, vedere [modelli di messaggio di scambio di metadati e individuazione](discovery-and-metadata-exchange-message-patterns.md) e [Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="d94a8-127">For more information about message patterns used by clients and hosts, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md) and [Getting Started with WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).</span></span>

<span data-ttu-id="d94a8-128">I messaggi devono essere attivati per poter essere inviati come descritto nel passaggio 3 precedente.</span><span class="sxs-lookup"><span data-stu-id="d94a8-128">Messages must be triggered in order to be sent as described in step 3 above.</span></span> <span data-ttu-id="d94a8-129">Il client di debug WSD Visualizza il messaggio SOAP non elaborato come output.</span><span class="sxs-lookup"><span data-stu-id="d94a8-129">The WSD Debug Client displays the raw SOAP message as output.</span></span> <span data-ttu-id="d94a8-130">Poiché tutti i messaggi stampati dal client di debug WSD in modalità multicast vengono ricevuti su un socket multicast, l'indirizzo di destinazione del messaggio non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="d94a8-130">Because all messages printed by WSD Debug Client in multicast mode are received over a multicast socket, the message destination address is not displayed.</span></span>

<span data-ttu-id="d94a8-131">L'output del client di debug WSD di esempio seguente mostra un messaggio Probe.</span><span class="sxs-lookup"><span data-stu-id="d94a8-131">The following sample WSD Debug Client output shows a Probe message.</span></span> <span data-ttu-id="d94a8-132">L'elemento <wsa: Action> identifica il messaggio come messaggio Probe.</span><span class="sxs-lookup"><span data-stu-id="d94a8-132">The <wsa:Action> element identifies the message as a Probe message.</span></span> <span data-ttu-id="d94a8-133">Esaminare il campo <wsa: Action> per verificare che il messaggio ricevuto sia un messaggio Probe.</span><span class="sxs-lookup"><span data-stu-id="d94a8-133">Inspect the <wsa:Action> field to verify that the received message was a Probe message.</span></span>

``` syntax
UDP message at 05/08/07 10:06:55 from soap.udp://[127.0.0.1:49334]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe</wsa:Action>
<wsa:MessageID>urn:uuid:256ad815-1576-4e59-8efc-4c1e0f15fdd2</wsa:MessageID></so
ap:Header><soap:Body><wsd:Probe><wsd:Types>wsdp:Device</wsd:Types></wsd:Probe></
soap:Body></soap:Envelope>
```

<span data-ttu-id="d94a8-134">L'output del client di debug WSD di esempio seguente mostra un messaggio Hello.</span><span class="sxs-lookup"><span data-stu-id="d94a8-134">The following sample WSD Debug Client output shows a Hello message.</span></span> <span data-ttu-id="d94a8-135">L'elemento <wsa: Action> identifica il messaggio come messaggio Hello.</span><span class="sxs-lookup"><span data-stu-id="d94a8-135">The <wsa:Action> element identifies the message as a Hello message.</span></span>

``` syntax
UDP message at 05/08/07 10:10:49 from soap.udp://[[::1]:49343]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello</wsa:Action>
<wsa:MessageID>urn:uuid:8999e29a-b056-4345-9e13-f42dbedab28a</wsa:MessageID><wsd
:AppSequence InstanceId="1" SequenceId="urn:uuid:abb0a2a1-6efc-4242-b8e7-c02484a
6eea2" MessageNumber="1"></wsd:AppSequence></soap:Header><soap:Body><wsd:Hello><
wsa:EndpointReference><wsa:Address>urn:uuid:02a76d74-82d0-43e6-ab09-16f54ab81ac6
</wsa:Address></wsa:EndpointReference><wsd:Types>wsdp:Device</wsd:Types><wsd:Met
adataVersion>1</wsd:MetadataVersion></wsd:Hello></soap:Body></soap:Envelope>
```

## <a name="filtering-wsd-debug-client-results"></a><span data-ttu-id="d94a8-136">Filtro dei risultati del client di debug WSD</span><span class="sxs-lookup"><span data-stu-id="d94a8-136">Filtering WSD Debug Client Results</span></span>

<span data-ttu-id="d94a8-137">Il filtro dei risultati del client di debug WSD può aiutare a identificare il traffico degli eventi imprevisti che interessa il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d94a8-137">Filtering the WSD Debug Client results can help identify incident traffic involving the device.</span></span> <span data-ttu-id="d94a8-138">Il filtro è necessario solo per le reti rumorose.</span><span class="sxs-lookup"><span data-stu-id="d94a8-138">Filtering is only necessary on noisy networks.</span></span>

<span data-ttu-id="d94a8-139">Esistono due modi per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="d94a8-139">There are two ways to filter results.</span></span> <span data-ttu-id="d94a8-140">Gli indirizzi IP da filtrare possono essere identificati in modo esplicito all'avvio del client di debug WSD.</span><span class="sxs-lookup"><span data-stu-id="d94a8-140">The IP addresses to filter can be explicitly identified when starting the WSD Debug Client.</span></span> <span data-ttu-id="d94a8-141">In alternativa, è possibile specificare gli indirizzi IP dopo l'avvio del client.</span><span class="sxs-lookup"><span data-stu-id="d94a8-141">Alternatively, the IP addresses can be specified after the client has started.</span></span> <span data-ttu-id="d94a8-142">In questa sezione vengono descritti entrambi i metodi.</span><span class="sxs-lookup"><span data-stu-id="d94a8-142">This section describes both methods.</span></span>

<span data-ttu-id="d94a8-143">**Per specificare gli indirizzi IP da filtrare all'avvio del client di debug WSD**</span><span class="sxs-lookup"><span data-stu-id="d94a8-143">**To specify IP addresses to filter when starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="d94a8-144">Configurare l'host e il client in modo che vengano eseguiti attraverso la rete (ovvero, assicurarsi che l'host e il client operino in computer diversi).</span><span class="sxs-lookup"><span data-stu-id="d94a8-144">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="d94a8-145">Raccogliere gli indirizzi IP del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d94a8-145">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="d94a8-146">Se il dispositivo dispone di più indirizzi (ad esempio, dispone di indirizzi IPv4 e IPv6) tutti gli indirizzi devono essere raccolti.</span><span class="sxs-lookup"><span data-stu-id="d94a8-146">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="d94a8-147">Aprire un prompt dei comandi ed eseguire il comando seguente: \**WSDDebug \_client.exe/Mode multicast/IP Add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="d94a8-147">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast /ip add** *<device IP>*</span></span>

<span data-ttu-id="d94a8-148">*<device IP>* è un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="d94a8-148">*<device IP>* is an IP address.</span></span> <span data-ttu-id="d94a8-149">Nell'elenco seguente vengono illustrati alcuni formati di esempio per questo indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="d94a8-149">The following list shows some sample formats for this IP address.</span></span>

-   <span data-ttu-id="d94a8-150">192.168.0.1</span><span class="sxs-lookup"><span data-stu-id="d94a8-150">192.168.0.1</span></span>
-   <span data-ttu-id="d94a8-151">:: 1</span><span class="sxs-lookup"><span data-stu-id="d94a8-151">::1</span></span>
-   <span data-ttu-id="d94a8-152">mydevice.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d94a8-152">mydevice.contoso.com</span></span>

<span data-ttu-id="d94a8-153">Il client di debug WSD risolve automaticamente i nomi host specificati al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="d94a8-153">The WSD Debug Client automatically resolves hostnames supplied at the command prompt.</span></span>

<span data-ttu-id="d94a8-154">**Per filtrare i risultati dopo l'avvio del client di debug WSD**</span><span class="sxs-lookup"><span data-stu-id="d94a8-154">**To filter results after starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="d94a8-155">Configurare l'host e il client in modo che vengano eseguiti attraverso la rete (ovvero, assicurarsi che l'host e il client operino in computer diversi).</span><span class="sxs-lookup"><span data-stu-id="d94a8-155">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="d94a8-156">Raccogliere gli indirizzi IP del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d94a8-156">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="d94a8-157">Se il dispositivo dispone di più indirizzi (ad esempio, dispone di indirizzi IPv4 e IPv6) tutti gli indirizzi devono essere raccolti.</span><span class="sxs-lookup"><span data-stu-id="d94a8-157">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="d94a8-158">Aprire un prompt dei comandi ed eseguire il comando seguente: **WSDDebug \_client.exe/Mode multicast**</span><span class="sxs-lookup"><span data-stu-id="d94a8-158">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
4.  <span data-ttu-id="d94a8-159">Al prompt dei comandi del client di debug WSD eseguire il comando seguente: \**IP Add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="d94a8-159">At the WSD Debug Client command prompt, run the following command: **ip add** *<device IP>*</span></span>
5.  <span data-ttu-id="d94a8-160">Ripetere il passaggio 4 fino a quando non sono stati aggiunti tutti gli indirizzi IP del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d94a8-160">Repeat step 4 until all device IP addresses have been added.</span></span>

<span data-ttu-id="d94a8-161">Nella procedura seguente si presuppone che il client di debug WSD sia stato avviato e che il filtro in base all'indirizzo IP sia in corso.</span><span class="sxs-lookup"><span data-stu-id="d94a8-161">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="d94a8-162">**Per verificare che gli indirizzi IP corretti vengano filtrati**</span><span class="sxs-lookup"><span data-stu-id="d94a8-162">**To verify that the correct IP addresses are being filtered**</span></span>

-   <span data-ttu-id="d94a8-163">Al prompt dei comandi del client di debug WSD eseguire il comando seguente: **IP Print**</span><span class="sxs-lookup"><span data-stu-id="d94a8-163">At the WSD Debug Client command prompt, run the following command: **ip print**</span></span>

    <span data-ttu-id="d94a8-164">Viene visualizzato l'elenco degli indirizzi IP da filtrare.</span><span class="sxs-lookup"><span data-stu-id="d94a8-164">The list of IP addresses being filtered appears.</span></span>

<span data-ttu-id="d94a8-165">Nella procedura seguente si presuppone che il client di debug WSD sia stato avviato e che il filtro in base all'indirizzo IP sia in corso.</span><span class="sxs-lookup"><span data-stu-id="d94a8-165">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="d94a8-166">**Per disabilitare il filtro**</span><span class="sxs-lookup"><span data-stu-id="d94a8-166">**To disable filtering**</span></span>

-   <span data-ttu-id="d94a8-167">Al prompt dei comandi del client di debug WSD eseguire il comando seguente: **IP Clear**</span><span class="sxs-lookup"><span data-stu-id="d94a8-167">At the WSD Debug Client command prompt, run the following command: **ip clear**</span></span>

    <span data-ttu-id="d94a8-168">Tutto il traffico multicast verrà ora visualizzato nell'output di debug.</span><span class="sxs-lookup"><span data-stu-id="d94a8-168">All multicast traffic will now be shown in the debug output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d94a8-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d94a8-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d94a8-170">Procedure di diagnostica WSDAPI</span><span class="sxs-lookup"><span data-stu-id="d94a8-170">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="d94a8-171">Introduzione con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="d94a8-171">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



