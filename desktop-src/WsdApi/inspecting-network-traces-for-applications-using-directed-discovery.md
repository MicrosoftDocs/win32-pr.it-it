---
description: Informazioni sull'ispezione delle tracce di rete tramite l'individuazione diretta. Un analizzatore di pacchetti di rete che visualizza pacchetti non elaborati può esaminare le richieste di scambio di metadati HTTP.
ms.assetid: 9b124117-06e7-4637-9863-0f9650861526
title: Analisi delle tracce di rete per le applicazioni tramite individuazione diretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d94ea3bc102c57c415be518883296e049490ca
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262123"
---
# <a name="inspecting-network-traces-for-applications-using-directed-discovery"></a><span data-ttu-id="84cae-104">Analisi delle tracce di rete per le applicazioni tramite individuazione diretta</span><span class="sxs-lookup"><span data-stu-id="84cae-104">Inspecting Network Traces for Applications Using Directed Discovery</span></span>

<span data-ttu-id="84cae-105">Qualsiasi analizzatore di pacchetti di rete in grado di visualizzare pacchetti non elaborati può essere usato per esaminare le richieste di scambio di metadati HTTP.</span><span class="sxs-lookup"><span data-stu-id="84cae-105">Any network packet analyzer that can display raw packets can be used to inspect HTTP metadata exchange requests.</span></span> <span data-ttu-id="84cae-106">Microsoft Network Monitor 3 (Netmon) è consigliato.</span><span class="sxs-lookup"><span data-stu-id="84cae-106">Microsoft Network Monitor 3 (Netmon) is recommended.</span></span> <span data-ttu-id="84cae-107">Per altre informazioni su Netmon, vedere [Download di Netmon e filtri DPWS di esempio.](downloading-netmon-and-sample-dpws-filters.md)</span><span class="sxs-lookup"><span data-stu-id="84cae-107">For more information about Netmon, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>

<span data-ttu-id="84cae-108">**Per esaminare le tracce di rete per l'individuazione diretta**</span><span class="sxs-lookup"><span data-stu-id="84cae-108">**To inspect network traces for directed discovery**</span></span>

1.  <span data-ttu-id="84cae-109">Configurare l'host e il client per l'esecuzione in rete, ovvero assicurarsi che l'host e il client funzionino in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="84cae-109">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="84cae-110">Installare l'analizzatore pacchetti (Netmon) nel client o nell'host.</span><span class="sxs-lookup"><span data-stu-id="84cae-110">Install the packet analyzer (Netmon) on either the client or the host.</span></span>
3.  <span data-ttu-id="84cae-111">Configurare l'analizzatore pacchetti per acquisire il traffico sulla scheda di rete che connette l'host e il client.</span><span class="sxs-lookup"><span data-stu-id="84cae-111">Configure the packet analyzer to capture traffic on the network adapter connecting the host and the client.</span></span>
4.  <span data-ttu-id="84cae-112">Riprodurre l'errore avviando l'host e il client o premendo F5 nel Esplora rete.</span><span class="sxs-lookup"><span data-stu-id="84cae-112">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
5.  <span data-ttu-id="84cae-113">Filtrare i risultati per isolare il traffico WS-Discovery scambio di metadati e dati.</span><span class="sxs-lookup"><span data-stu-id="84cae-113">Filter the results to isolate WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="84cae-114">Per visualizzare i filtri Netmon di esempio, vedere [Download dei filtri Netmon e DPWS di esempio](downloading-netmon-and-sample-dpws-filters.md).</span><span class="sxs-lookup"><span data-stu-id="84cae-114">To view sample Netmon filters, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="84cae-115">Questo passaggio è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84cae-115">This step is optional.</span></span>

     

6.  <span data-ttu-id="84cae-116">Verificare che i messaggi inviati tra client e host soddisfino i requisiti di traffico di base.</span><span class="sxs-lookup"><span data-stu-id="84cae-116">Verify that messages sent between client and host meet basic traffic requirements.</span></span>

## <a name="verifying-that-messages-meet-traffic-requirements"></a><span data-ttu-id="84cae-117">Verifica che i messaggi soddisfino i requisiti di traffico</span><span class="sxs-lookup"><span data-stu-id="84cae-117">Verifying that messages meet traffic requirements</span></span>

<span data-ttu-id="84cae-118">I client e gli host WSDAPI devono inviare messaggi conformi ai criteri seguenti.</span><span class="sxs-lookup"><span data-stu-id="84cae-118">WSDAPI clients and hosts must send messages that conform to the following criteria.</span></span> <span data-ttu-id="84cae-119">Per informazioni generali sui modelli di messaggio, vedere [Individuazione e modelli di messaggi di scambio di metadati](discovery-and-metadata-exchange-message-patterns.md).</span><span class="sxs-lookup"><span data-stu-id="84cae-119">For general information about message patterns, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).</span></span>

-   <span data-ttu-id="84cae-120">[I](probe-message.md) messaggi probe devono essere inviati tramite HTTP o HTTPS, in genere alla porta 5357 o 5358.</span><span class="sxs-lookup"><span data-stu-id="84cae-120">[Probe](probe-message.md) messages must be sent by HTTP or HTTPS, usually to port 5357 or 5358.</span></span>
-   <span data-ttu-id="84cae-121">**L'elemento Types** di un [messaggio Probe](probe-message.md) deve essere presente e non deve essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="84cae-121">The **Types** element of a [Probe](probe-message.md) message must be present and must not be empty.</span></span> <span data-ttu-id="84cae-122">Deve contenere i tipi a cui risponderà un host.</span><span class="sxs-lookup"><span data-stu-id="84cae-122">It must contain the types to which a host will respond.</span></span>
-   <span data-ttu-id="84cae-123">È necessario inviare un messaggio [ProbeMatches](probematches-message.md) alla porta HTTP o HTTPS da cui [è](probe-message.md) stato inviato il probe.</span><span class="sxs-lookup"><span data-stu-id="84cae-123">A [ProbeMatches](probematches-message.md) message must be sent to the HTTP or HTTPS port from which the [Probe](probe-message.md) was sent.</span></span>
-   <span data-ttu-id="84cae-124">**L'elemento RelatesTo** di [un messaggio ProbeMatches](probematches-message.md) deve essere presente e non deve essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="84cae-124">The **RelatesTo** element of a [ProbeMatches](probematches-message.md) message must be present and must not be empty.</span></span> <span data-ttu-id="84cae-125">Il valore deve corrispondere al valore **dell'elemento MessageId** del messaggio [Probe](probe-message.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="84cae-125">Its value must match the value of the **MessageId** element from the corresponding [Probe](probe-message.md) message.</span></span>
-   <span data-ttu-id="84cae-126">Se un **elemento XAddrs** è stato incluso nel [messaggio ProbeMatches,](probematches-message.md) gli indirizzi di trasporto forniti devono essere convalidati.</span><span class="sxs-lookup"><span data-stu-id="84cae-126">If an **XAddrs** element was included in the [ProbeMatches](probematches-message.md) message, the supplied transport addresses must be validated.</span></span> <span data-ttu-id="84cae-127">Per altre informazioni, vedere [Regole di convalida XAddr](xaddr-validation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="84cae-127">For more information, see [XAddr Validation Rules](xaddr-validation-rules.md).</span></span>
-   <span data-ttu-id="84cae-128">Un [messaggio ProbeMatches](probematches-message.md) deve essere inviato entro 4 secondi dal messaggio [Probe](probe-message.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="84cae-128">A [ProbeMatches](probematches-message.md) message must be sent within 4 seconds of the corresponding [Probe](probe-message.md) message.</span></span> <span data-ttu-id="84cae-129">Windows Firewall può eliminare un messaggio ProbeMatches inviato più di 4 secondi dopo un messaggio probe.</span><span class="sxs-lookup"><span data-stu-id="84cae-129">The Windows Firewall may drop a ProbeMatches message sent more than 4 seconds after a Probe message.</span></span>
-   <span data-ttu-id="84cae-130">Se nel messaggio [ProbeMatches](probematches-message.md) non è stato incluso alcun elemento **XAddrs** e il client o l'host invierà un messaggio HTTP ,ad esempio una richiesta get [metadata](get--metadata-exchange--http-request-and-message.md) exchange o un messaggio del servizio, il client o l'host deve inviare un messaggio [Resolve](resolve-message.md) tramite HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="84cae-130">If no **XAddrs** element was included in the [ProbeMatches](probematches-message.md) message, and the client or host will send an HTTP message (such as a [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange request or a service message), then the client or host must send a [Resolve](resolve-message.md) message by HTTP or HTTPS.</span></span> <span data-ttu-id="84cae-131">Questo messaggio viene in genere inviato alla porta 5357 o 5358.</span><span class="sxs-lookup"><span data-stu-id="84cae-131">This message is usually sent to port 5357 or 5358.</span></span>
-   <span data-ttu-id="84cae-132">Se viene [inviato un](resolve-message.md) messaggio Resolve, è necessario inviare un messaggio [ResolveMatches](resolvematches-message.md) alla porta HTTP o HTTPS da cui è stato inviato il messaggio Resolve.</span><span class="sxs-lookup"><span data-stu-id="84cae-132">If a [Resolve](resolve-message.md) message is sent, then a [ResolveMatches](resolvematches-message.md) message must be sent to the HTTP or HTTPS port from which the Resolve message was sent.</span></span>
-   <span data-ttu-id="84cae-133">Un [messaggio ResolveMatches](resolvematches-message.md) deve essere inviato entro 4 secondi dal messaggio [Resolve](resolve-message.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="84cae-133">A [ResolveMatches](resolvematches-message.md) message must be sent within 4 seconds of the corresponding [Resolve](resolve-message.md) message.</span></span> <span data-ttu-id="84cae-134">Windows Firewall può eliminare un messaggio ResolveMatchesmessage inviato più di 4 secondi dopo un messaggio di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="84cae-134">The Windows Firewall may drop a ResolveMatchesmessage sent more than 4 seconds after a Resolve message.</span></span>

<span data-ttu-id="84cae-135">Se i messaggi inviati dal programma non sono conformi a questi requisiti, la causa del problema è stata identificata correttamente e non sono necessari altri passaggi per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="84cae-135">If the messages sent by the program do not conform to these message requirements, the cause of the problem has been successfully identified and no further troubleshooting steps are necessary.</span></span> <span data-ttu-id="84cae-136">Riscrivere il programma in modo che generi messaggi conformi e rieseguire il programma.</span><span class="sxs-lookup"><span data-stu-id="84cae-136">Rewrite the program so that it generates conformant messages and retest the program.</span></span>

<span data-ttu-id="84cae-137">Se l'origine del problema non è ancora identificata, contattare il supporto tecnico Microsoft per assistenza.</span><span class="sxs-lookup"><span data-stu-id="84cae-137">If the source of the problem still cannot be identified, contact Microsoft support for assistance.</span></span> <span data-ttu-id="84cae-138">Prima di contattare il supporto tecnico, raccogliere i file di log appropriati per identificare la causa radice del problema.</span><span class="sxs-lookup"><span data-stu-id="84cae-138">Before contacting support, collect the appropriate log files to help identify the root cause of the problem.</span></span> <span data-ttu-id="84cae-139">Per altre informazioni, vedere [Abilitazione della traccia WSDAPI](enabling-wsdapi-tracing.md).</span><span class="sxs-lookup"><span data-stu-id="84cae-139">For more information, see [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84cae-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84cae-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84cae-141">Risoluzione dei problemi relativi alle applicazioni tramite individuazione diretta</span><span class="sxs-lookup"><span data-stu-id="84cae-141">Troubleshooting Applications Using Directed Discovery</span></span>](troubleshooting-applications-using-directed-discovery.md)
</dt> <dt>

[<span data-ttu-id="84cae-142">Procedure di diagnostica WSDAPI</span><span class="sxs-lookup"><span data-stu-id="84cae-142">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="84cae-143">Attività iniziali con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="84cae-143">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="84cae-144">Download di netmon e filtri DPWS di esempio</span><span class="sxs-lookup"><span data-stu-id="84cae-144">Downloading Netmon and Sample DPWS Filters</span></span>](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



