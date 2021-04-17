---
description: Il profilo dispositivo per gli host dei servizi Web (DPWS) e i client comunicano in rete utilizzando una serie di messaggi SOAP su UDP e HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Modelli di messaggi di individuazione e scambio di metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104234456"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a><span data-ttu-id="a88ab-103">Modelli di messaggi di individuazione e scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="a88ab-103">Discovery and Metadata Exchange Message Patterns</span></span>

<span data-ttu-id="a88ab-104">Il profilo dispositivo per gli host dei servizi Web (DPWS) e i client comunicano in rete utilizzando una serie di messaggi SOAP su UDP e HTTP.</span><span class="sxs-lookup"><span data-stu-id="a88ab-104">Device Profile for Web Services (DPWS) hosts and clients communicate over the network using a series of SOAP messages over UDP and HTTP.</span></span>

<span data-ttu-id="a88ab-105">Il diagramma seguente mostra una panoramica del traffico UDP e HTTP previsto tra un host e un client di DPWS.</span><span class="sxs-lookup"><span data-stu-id="a88ab-105">The following diagram shows an overview of the expected UDP and HTTP traffic between a DPWS host and client.</span></span>

![Diagramma che mostra il traffico UDP e HTTP tra un host DPWS e un client.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

<span data-ttu-id="a88ab-107">[Hello](hello-message.md), [bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md)e [Get](get--metadata-exchange--http-request-and-message.md) messages vengono generati senza richiesta di rete; questi messaggi vengono usati per annunciare lo stato del dispositivo o per emettere una richiesta di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a88ab-107">[Hello](hello-message.md), [Bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md), and [Get](get--metadata-exchange--http-request-and-message.md) messages are all generated without network solicitation; these messages are used to announce device state or to issue a search request.</span></span> <span data-ttu-id="a88ab-108">I messaggi [ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md)e [GetResponse](getresponse--metadata-exchange--message.md) vengono generati in risposta a probe, Resolve e Get messages.</span><span class="sxs-lookup"><span data-stu-id="a88ab-108">[ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md), and [GetResponse](getresponse--metadata-exchange--message.md) messages are generated in response to Probe, Resolve and Get messages.</span></span>

<span data-ttu-id="a88ab-109">I messaggi [Hello](hello-message.md), [bye](bye-message.md), [Resolve](resolve-message.md)e [ResolveMatches](resolvematches-message.md) vengono sempre eseguiti su UDP.</span><span class="sxs-lookup"><span data-stu-id="a88ab-109">[Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md), and [ResolveMatches](resolvematches-message.md) messages will always occur over UDP.</span></span> <span data-ttu-id="a88ab-110">Analogamente, i messaggi di metadati [Get](get--metadata-exchange--http-request-and-message.md) e [GetResponse](getresponse--metadata-exchange--message.md) vengono sempre eseguiti su http o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a88ab-110">Similarly, [Get](get--metadata-exchange--http-request-and-message.md) and [GetResponse](getresponse--metadata-exchange--message.md) metadata messages will always occur over HTTP or HTTPS.</span></span> <span data-ttu-id="a88ab-111">I messaggi [Probe](probe-message.md) e [ProbeMatches](probematches-message.md) vengono in genere trasmessi tramite UDP, ma avvengono tramite una connessione HTTP o HTTPS in uno scenario di individuazione diretta.</span><span class="sxs-lookup"><span data-stu-id="a88ab-111">[Probe](probe-message.md) and [ProbeMatches](probematches-message.md) messages are normally transmitted over UDP, but take place over an HTTP or HTTPS connection in a directed discovery scenario.</span></span> <span data-ttu-id="a88ab-112">Per ulteriori informazioni sui modelli di messaggi di individuazione diretta, vedere [risoluzione dei problemi relativi alle applicazioni mediante l'individuazione diretta](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="a88ab-112">For more information about directed discovery message patterns, see [Troubleshooting Applications Using Directed Discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="a88ab-113">Nell'elenco seguente viene illustrata la sequenza tipica dei messaggi in transito.</span><span class="sxs-lookup"><span data-stu-id="a88ab-113">The following list shows the typical sequence of messages on the wire.</span></span> <span data-ttu-id="a88ab-114">Non tutti i messaggi sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="a88ab-114">Not all messages are mandatory.</span></span>

1.  [<span data-ttu-id="a88ab-115">Ciao</span><span class="sxs-lookup"><span data-stu-id="a88ab-115">Hello</span></span>](hello-message.md)
2.  [<span data-ttu-id="a88ab-116">Probe</span><span class="sxs-lookup"><span data-stu-id="a88ab-116">Probe</span></span>](probe-message.md)
3.  [<span data-ttu-id="a88ab-117">ProbeMatches</span><span class="sxs-lookup"><span data-stu-id="a88ab-117">ProbeMatches</span></span>](probematches-message.md)
4.  [<span data-ttu-id="a88ab-118">Risolvi</span><span class="sxs-lookup"><span data-stu-id="a88ab-118">Resolve</span></span>](resolve-message.md)
5.  [<span data-ttu-id="a88ab-119">ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="a88ab-119">ResolveMatches</span></span>](resolvematches-message.md)
6.  <span data-ttu-id="a88ab-120">[Get](get--metadata-exchange--http-request-and-message.md) (richiesta di scambio di metadati)</span><span class="sxs-lookup"><span data-stu-id="a88ab-120">[Get](get--metadata-exchange--http-request-and-message.md) (metadata exchange request)</span></span>
7.  [<span data-ttu-id="a88ab-121">GetResponse</span><span class="sxs-lookup"><span data-stu-id="a88ab-121">GetResponse</span></span>](getresponse--metadata-exchange--message.md)
8.  [<span data-ttu-id="a88ab-122">Bye</span><span class="sxs-lookup"><span data-stu-id="a88ab-122">Bye</span></span>](bye-message.md)

## <a name="related-topics"></a><span data-ttu-id="a88ab-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a88ab-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a88ab-124">Informazioni sui servizi Web nei dispositivi</span><span class="sxs-lookup"><span data-stu-id="a88ab-124">About Web Services on Devices</span></span>](about-web-services-for-devices.md)
</dt> </dl>

 

 



