---
description: AppSequence informazioni contenute in WS-Discovery messaggi di annuncio e risposta (Hello, ProbeMatches e ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Regole di convalida AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528591"
---
# <a name="appsequence-validation-rules"></a><span data-ttu-id="fd409-103">Regole di convalida AppSequence</span><span class="sxs-lookup"><span data-stu-id="fd409-103">AppSequence Validation Rules</span></span>

<span data-ttu-id="fd409-104">AppSequence informazioni contenute in WS-Discovery messaggi di annuncio e risposta ([Hello](hello-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md)).</span><span class="sxs-lookup"><span data-stu-id="fd409-104">AppSequence information contained in WS-Discovery announcement and response messages ([Hello](hello-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md)).</span></span> <span data-ttu-id="fd409-105">Queste informazioni vengono elaborate e convalidate da WSDAPI prima che questi messaggi vengano passati ai componenti sopra lo stack, ad esempio Network Explorer o un'applicazione che chiama WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="fd409-105">This information is processed and validated by WSDAPI before these messages are passed on to components above the stack (such as Network Explorer or an application calling into WSDAPI).</span></span>

<span data-ttu-id="fd409-106">Nel codice XML seguente viene illustrato un elemento AppSequence di esempio.</span><span class="sxs-lookup"><span data-stu-id="fd409-106">The following XML shows a sample AppSequence element.</span></span> <span data-ttu-id="fd409-107">Il prefisso WSD si riferisce allo spazio dei nomi `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="fd409-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

<span data-ttu-id="fd409-108">WSDAPI ignora i messaggi non aggiornati.</span><span class="sxs-lookup"><span data-stu-id="fd409-108">WSDAPI ignores stale messages.</span></span> <span data-ttu-id="fd409-109">Per ogni dispositivo (identificato in modo univoco dall'indirizzo endpoint nel corpo SOAP), WSDAPI ignora tutti i messaggi con un MessageNumber AppSequence inferiore rispetto all'ultimo messaggio visualizzato.</span><span class="sxs-lookup"><span data-stu-id="fd409-109">For each device (uniquely identified by the Endpoint Address in the SOAP Body), WSDAPI ignores any messages with an AppSequence MessageNumber lower than the last message seen.</span></span>

<span data-ttu-id="fd409-110">WSDAPI ignora gli annunci XAddr non aggiornati.</span><span class="sxs-lookup"><span data-stu-id="fd409-110">WSDAPI ignores stale XAddr announcements.</span></span> <span data-ttu-id="fd409-111">Se AppSequence InstanceId è inferiore rispetto all'ultimo InstanceId rilevato, WSDAPI ignora la XAddrs annunciata nel corpo SOAP.</span><span class="sxs-lookup"><span data-stu-id="fd409-111">If the AppSequence InstanceId is lower than the last InstanceId seen, WSDAPI ignores the XAddrs advertised in the SOAP body.</span></span> <span data-ttu-id="fd409-112">Se, inoltre, InstanceId è uguale al precedente, ma il valore di MetadataVersion è inferiore rispetto all'ultimo MetadataVersion, WSDAPI ignora il XAddrs.</span><span class="sxs-lookup"><span data-stu-id="fd409-112">Also, if the InstanceId is the same as previous but the MetadataVersion is lower than the last MetadataVersion, WSDAPI ignores the XAddrs.</span></span>

<span data-ttu-id="fd409-113">WSDAPI ignora i messaggi di WS-Discovery duplicati.</span><span class="sxs-lookup"><span data-stu-id="fd409-113">WSDAPI ignores duplicate WS-Discovery messages.</span></span> <span data-ttu-id="fd409-114">Se a WSDAPI vengono inviati due messaggi di WS-Discovery identici, verranno elaborati solo i primi messaggi ricevuti.</span><span class="sxs-lookup"><span data-stu-id="fd409-114">If two identical WS-Discovery messages are sent to WSDAPI, only the first received will be processed.</span></span> <span data-ttu-id="fd409-115">Questo è in genere rilevante solo per le applicazioni che effettuano chiamate direttamente nelle interfacce [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) o [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) .</span><span class="sxs-lookup"><span data-stu-id="fd409-115">This is typically only relevant for applications that call directly into the [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) or [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd409-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd409-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd409-117">Modelli di messaggi di individuazione e scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="fd409-117">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



