---
description: Un set di strumenti di debug basato su Web Services on Devices API (WSDAPI) è disponibile nel Windows SDK e Windows Driver Kit (WDK).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Strumenti di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131823"
---
# <a name="debugging-tools"></a><span data-ttu-id="dd222-103">Strumenti di debug</span><span class="sxs-lookup"><span data-stu-id="dd222-103">Debugging Tools</span></span>

<span data-ttu-id="dd222-104">Un set di strumenti di debug basato su Web Services on Devices API (WSDAPI) è disponibile nel Windows SDK e Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="dd222-104">A debugging toolset built on Web Services on Devices API (WSDAPI) is available in the Windows SDK and the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="dd222-105">Questi strumenti possono essere usati per testare le funzionalità delle applicazioni personalizzate scritte in WSDAPI o per i dispositivi e i client scritti usando altri profili di dispositivo per gli stack di servizi Web (DPWS).</span><span class="sxs-lookup"><span data-stu-id="dd222-105">These tools can be used to test the functionality of custom applications written on WSDAPI, or devices and clients written using other Device Profile for Web Services (DPWS) stacks.</span></span>

<span data-ttu-id="dd222-106">\_ \_ Per esaminare le caratteristiche dei client o degli host di DPWS, è possibile usare gli strumenti WSD debug host (wsddebughost.exe) e WSD debug client (wsddebugclient.exe).</span><span class="sxs-lookup"><span data-stu-id="dd222-106">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools can be used to inspect the characteristics of DPWS clients or hosts.</span></span> <span data-ttu-id="dd222-107">Possono anche essere usati per risolvere i problemi di connettività o configurazione.</span><span class="sxs-lookup"><span data-stu-id="dd222-107">They can also be used to troubleshoot connectivity or configuration problems.</span></span> <span data-ttu-id="dd222-108">Per ulteriori informazioni, vedere la [Guida alla risoluzione dei problemi di WSDAPI](wsdapi-troubleshooting-guide.md).</span><span class="sxs-lookup"><span data-stu-id="dd222-108">For more information, see [WSDAPI Troubleshooting Guide](wsdapi-troubleshooting-guide.md).</span></span> <span data-ttu-id="dd222-109">Questi strumenti sono disponibili solo nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="dd222-109">These tools are only available in the SDK.</span></span> <span data-ttu-id="dd222-110">Gli strumenti SDK si trovano nella seguente directory: <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="dd222-110">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="dd222-111">Lo [strumento WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) può essere utilizzato per testare l'interoperabilità a livello SOAP o di trasporto, ovvero garantire che i messaggi siano ben formati.</span><span class="sxs-lookup"><span data-stu-id="dd222-111">The [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) can be used to test SOAP-level or transport-level interoperability (that is, ensuring messages are well-formed).</span></span> <span data-ttu-id="dd222-112">Questo strumento è disponibile solo in WDK.</span><span class="sxs-lookup"><span data-stu-id="dd222-112">This tool is only available in the WDK.</span></span>

## <a name="the-wsd-debug-client"></a><span data-ttu-id="dd222-113">Client di debug WSD</span><span class="sxs-lookup"><span data-stu-id="dd222-113">The WSD Debug Client</span></span>

<span data-ttu-id="dd222-114">Il client di debug WSD (wsddebug \_client.exe) fornisce una console interattiva che può essere usata per inviare e ricevere messaggi di WS-Discovery e per ottenere i metadati.</span><span class="sxs-lookup"><span data-stu-id="dd222-114">The WSD Debug Client (wsddebug\_client.exe) provides an interactive console that can be used to send and receive WS-Discovery messages, and to obtain metadata.</span></span> <span data-ttu-id="dd222-115">Può inoltre essere utilizzato per generare e utilizzare messaggi multicast non elaborati.</span><span class="sxs-lookup"><span data-stu-id="dd222-115">It can also be used to generate and consume raw multicast messages.</span></span>

<span data-ttu-id="dd222-116">Il client di debug WSD funziona in una delle tre modalità seguenti: multicast, individuazione e metadati.</span><span class="sxs-lookup"><span data-stu-id="dd222-116">The WSD Debug Client operates in one of three modes: multicast, discovery, and metadata.</span></span>



| <span data-ttu-id="dd222-117">Mode</span><span class="sxs-lookup"><span data-stu-id="dd222-117">Mode</span></span>      | <span data-ttu-id="dd222-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd222-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd222-119">Multicast</span><span class="sxs-lookup"><span data-stu-id="dd222-119">Multicast</span></span> | <span data-ttu-id="dd222-120">In modalità multicast il client di debug WSD Invia e riceve messaggi multicast non formattati sulla porta UDP 3702, come definito in WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="dd222-120">In Multicast mode, the WSD Debug Client sends and receives unformatted multicast messages on UDP port 3702, as defined in WS-Discovery.</span></span> <span data-ttu-id="dd222-121">L'utente può salvare questi messaggi SOAP in un file di testo e può modificare e ritrasmettere i messaggi con il client di debug WSD.</span><span class="sxs-lookup"><span data-stu-id="dd222-121">The user may save these SOAP messages in a text file, and may modify and rebroadcast the messages with the WSD Debug Client.</span></span>                                                                                                                                 |
| <span data-ttu-id="dd222-122">Individuazione</span><span class="sxs-lookup"><span data-stu-id="dd222-122">Discovery</span></span> | <span data-ttu-id="dd222-123">In modalità di individuazione, il client di debug WSD Invia e riceve messaggi formattati WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="dd222-123">In Discovery mode, the WSD Debug Client sends and receives formatted WS-Discovery messages.</span></span> <span data-ttu-id="dd222-124">Può visualizzare i messaggi [Hello](hello-message.md), [bye](bye-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md) ricevuti.</span><span class="sxs-lookup"><span data-stu-id="dd222-124">It can display received [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md) messages.</span></span> <span data-ttu-id="dd222-125">Può inviare messaggi [Probe](probe-message.md) su UDP o http e [risolvere](resolve-message.md) i messaggi tramite UDP.</span><span class="sxs-lookup"><span data-stu-id="dd222-125">It can send [Probe](probe-message.md) messages over UDP or HTTP, and [Resolve](resolve-message.md) messages over UDP.</span></span> |
| <span data-ttu-id="dd222-126">Metadati</span><span class="sxs-lookup"><span data-stu-id="dd222-126">Metadata</span></span>  | <span data-ttu-id="dd222-127">Oltre a implementare tutte le funzionalità della modalità di individuazione, la modalità dei metadati tenta anche di recuperare i metadati dai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="dd222-127">In addition to implementing all of the features of Discovery mode, Metadata mode also attempts to retrieve metadata from devices.</span></span>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="dd222-128">Per ulteriori informazioni, vedere [utilizzo di un host e di un client generico per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md), [utilizzo di un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md)e [utilizzo del client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="dd222-128">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md), [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md), and [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

## <a name="the-wsd-debug-host"></a><span data-ttu-id="dd222-129">Host di debug WSD</span><span class="sxs-lookup"><span data-stu-id="dd222-129">The WSD Debug Host</span></span>

<span data-ttu-id="dd222-130">L'host di debug WSD (wsddebug \_host.exe) fornisce una console interattiva utilizzata per annunciare l'host, rispondere alle richieste dei client e stampare le informazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="dd222-130">The WSD Debug Host (wsddebug\_host.exe) provides an interactive console used to announce the host, respond to client requests, and print diagnostic information.</span></span>

<span data-ttu-id="dd222-131">L'host di debug WSD funziona in una delle due modalità seguenti: individuazione e metadati.</span><span class="sxs-lookup"><span data-stu-id="dd222-131">The WSD Debug Host operates in one of two modes: discovery and metadata.</span></span>



| <span data-ttu-id="dd222-132">Mode</span><span class="sxs-lookup"><span data-stu-id="dd222-132">Mode</span></span>      | <span data-ttu-id="dd222-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd222-133">Description</span></span>                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd222-134">Individuazione</span><span class="sxs-lookup"><span data-stu-id="dd222-134">Discovery</span></span> | <span data-ttu-id="dd222-135">In modalità di individuazione, l'host di debug WSD stampa i messaggi formattati WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="dd222-135">In Discovery mode, the WSD Debug Host prints formatted WS-Discovery messages.</span></span> <span data-ttu-id="dd222-136">Invia anche messaggi [Hello](hello-message.md) e [bye](bye-message.md) e risponde automaticamente al [Probe](probe-message.md) e alla [risoluzione](resolve-message.md) dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="dd222-136">It also sends [Hello](hello-message.md) and [Bye](bye-message.md) messages, and automatically responds to [Probe](probe-message.md) and [Resolve](resolve-message.md) messages.</span></span> |
| <span data-ttu-id="dd222-137">Metadati</span><span class="sxs-lookup"><span data-stu-id="dd222-137">Metadata</span></span>  | <span data-ttu-id="dd222-138">Oltre a implementare tutte le funzionalità della modalità di individuazione, la modalità metadati annuncia un servizio metadati e consente ai client di connettersi ed eseguire lo scambio di metadati.</span><span class="sxs-lookup"><span data-stu-id="dd222-138">In addition to implementing all of the features of Discovery mode, Metadata mode advertises a metadata service and allows clients to connect and perform metadata exchange.</span></span>                                                                                       |



 

<span data-ttu-id="dd222-139">Per ulteriori informazioni, vedere [utilizzo di un host e di un client generico per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md) e [utilizzo di un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="dd222-139">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) and [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd222-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dd222-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd222-141">Sviluppo di applicazioni WSD in Windows</span><span class="sxs-lookup"><span data-stu-id="dd222-141">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="dd222-142">Strumenti di sviluppo WSDAPI</span><span class="sxs-lookup"><span data-stu-id="dd222-142">WSDAPI Development Tools</span></span>](wsdapi-development-tools.md)
</dt> <dt>

[<span data-ttu-id="dd222-143">Guida alla risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="dd222-143">WSDAPI Troubleshooting Guide</span></span>](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



