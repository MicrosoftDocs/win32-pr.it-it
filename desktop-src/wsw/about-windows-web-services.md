---
title: Informazioni sui servizi Web Windows
description: L'API dei servizi Web Windows è un'API a più livelli e può essere illustrata come indicato di seguito.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104566429"
---
# <a name="about-windows-web-services"></a><span data-ttu-id="c8881-103">Informazioni sui servizi Web Windows</span><span class="sxs-lookup"><span data-stu-id="c8881-103">About Windows Web Services</span></span>

<span data-ttu-id="c8881-104">L'API dei servizi Web Windows è un'API a più livelli e può essere illustrata come indicato di seguito</span><span class="sxs-lookup"><span data-stu-id="c8881-104">The Windows Web Services API is a layered API and it may be pictured as follows</span></span>

![Diagramma che mostra i livelli e le aree multilivello dell'API dei servizi Web Windows.](images/apistack.png)

<span data-ttu-id="c8881-106">WWSAPI è un'API a più livelli.</span><span class="sxs-lookup"><span data-stu-id="c8881-106">The WWSAPI is a layered API.</span></span> <span data-ttu-id="c8881-107">Si prevede che la maggior parte degli sviluppatori sia destinata al modello del servizio, ovvero un modello di programmazione basato su metodo.</span><span class="sxs-lookup"><span data-stu-id="c8881-107">We expect most developers to target the Service Model, which is a method-based programming model.</span></span> <span data-ttu-id="c8881-108">Nel modello del servizio, l'host del servizio fornisce il modello di programmazione lato server, mentre il proxy del servizio fornisce il modello di programmazione lato client.</span><span class="sxs-lookup"><span data-stu-id="c8881-108">In the Service Model, the Service Host provides the server side programming model, while Service Proxy provides the client side programming model.</span></span>

<span data-ttu-id="c8881-109">Ogni livello espone un set di API e tipi che possono essere usati con le API di tale livello.</span><span class="sxs-lookup"><span data-stu-id="c8881-109">Every layer exposes a set of APIs and types that can be used with APIs of that layer.</span></span>

## <a name="service-model"></a><span data-ttu-id="c8881-110">Modello del servizio</span><span class="sxs-lookup"><span data-stu-id="c8881-110">Service Model</span></span>

<span data-ttu-id="c8881-111">Il livello di livello superiore denominato [modello di servizio](service-model-layer-overview.md) fornisce un modello di programmazione basato sul metodo ed è il modello più semplice da usare.</span><span class="sxs-lookup"><span data-stu-id="c8881-111">The top level layer called the [Service Model](service-model-layer-overview.md) provides a method-based programming model and it is the easiest model to use.</span></span> <span data-ttu-id="c8881-112">Nel modello del servizio, l' [host del servizio](service-host.md) fornisce il modello di programmazione lato server, mentre il [proxy del servizio](service-proxy.md) fornisce il modello di programmazione lato client.</span><span class="sxs-lookup"><span data-stu-id="c8881-112">In the Service Model, the [Service Host](service-host.md) provides the server side programming model, while the [Service Proxy](service-proxy.md) provides the client side programming model.</span></span> <span data-ttu-id="c8881-113">Il [contesto](context.md) viene utilizzato all'interno del modello del servizio per passare uno stato pertinente disponibile all'operazione del servizio e/o al callback quando viene richiamato.</span><span class="sxs-lookup"><span data-stu-id="c8881-113">[Context](context.md) is used within the Service Model to pass in a relevant state available to the service operation and/or the callback when it is invoked.</span></span> <span data-ttu-id="c8881-114">Il [contratto di servizio](contract.md) e viene usato per specificare un contratto di servizio in un endpoint esposto nel servizio.</span><span class="sxs-lookup"><span data-stu-id="c8881-114">And [Service Contract](contract.md) is used to specify a service contract on an endpoint exposed on the service.</span></span> <span data-ttu-id="c8881-115">I componenti e le operazioni seguenti fanno parte del livello di servizio:</span><span class="sxs-lookup"><span data-stu-id="c8881-115">The following components and operations are part of the Service Layer:</span></span>

-   [<span data-ttu-id="c8881-116">Host del servizio</span><span class="sxs-lookup"><span data-stu-id="c8881-116">Service Host</span></span>](service-host.md)
-   [<span data-ttu-id="c8881-117">Proxy servizio</span><span class="sxs-lookup"><span data-stu-id="c8881-117">Service Proxy</span></span>](service-proxy.md)
-   [<span data-ttu-id="c8881-118">Contesto</span><span class="sxs-lookup"><span data-stu-id="c8881-118">Context</span></span>](context.md)
-   [<span data-ttu-id="c8881-119">Contratto</span><span class="sxs-lookup"><span data-stu-id="c8881-119">Contract</span></span>](contract.md)
-   [<span data-ttu-id="c8881-120">Metadati del servizio</span><span class="sxs-lookup"><span data-stu-id="c8881-120">Service Metadata</span></span>](service-metadata.md)

## <a name="channel-layer"></a><span data-ttu-id="c8881-121">Livello del canale</span><span class="sxs-lookup"><span data-stu-id="c8881-121">Channel Layer</span></span>

<span data-ttu-id="c8881-122">Il modello di servizio si basa su un livello del canale, che offre la massima flessibilità, ma è più difficile da usare.</span><span class="sxs-lookup"><span data-stu-id="c8881-122">The Service Model is built upon a Channel Layer, which provides full flexibility but is more difficult to use.</span></span> <span data-ttu-id="c8881-123">I componenti e le operazioni seguenti fanno parte del livello del canale:</span><span class="sxs-lookup"><span data-stu-id="c8881-123">The following components and operations are part of the Channel Layer:</span></span>

-   [<span data-ttu-id="c8881-124">Messaggio</span><span class="sxs-lookup"><span data-stu-id="c8881-124">Message</span></span>](message.md)
-   [<span data-ttu-id="c8881-125">Channel</span><span class="sxs-lookup"><span data-stu-id="c8881-125">Channel</span></span>](channel.md)
-   [<span data-ttu-id="c8881-126">Listener</span><span class="sxs-lookup"><span data-stu-id="c8881-126">Listener</span></span>](listener.md)
-   [<span data-ttu-id="c8881-127">Errori</span><span class="sxs-lookup"><span data-stu-id="c8881-127">Faults</span></span>](faults.md)
-   [<span data-ttu-id="c8881-128">Url</span><span class="sxs-lookup"><span data-stu-id="c8881-128">Url</span></span>](url.md)
-   [<span data-ttu-id="c8881-129">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="c8881-129">Security</span></span>](security-overview.md)
-   [<span data-ttu-id="c8881-130">Importazione di metadati</span><span class="sxs-lookup"><span data-stu-id="c8881-130">Metadata Import</span></span>](metadata-import.md)

## <a name="xml-layer"></a><span data-ttu-id="c8881-131">Livello XML</span><span class="sxs-lookup"><span data-stu-id="c8881-131">XML Layer</span></span>

<span data-ttu-id="c8881-132">Il livello del canale si basa a sua volta su un Framework XML leggero, che include la deserializzazione dei tipi di dati C.</span><span class="sxs-lookup"><span data-stu-id="c8881-132">The Channel Layer is in turn built upon a lightweight XML framework, which includes deserialization of C data types.</span></span> <span data-ttu-id="c8881-133">I componenti e le operazioni seguenti fanno parte del livello XML:</span><span class="sxs-lookup"><span data-stu-id="c8881-133">The following components and operations are part of the XML Layer:</span></span>

-   [<span data-ttu-id="c8881-134">Writer XML</span><span class="sxs-lookup"><span data-stu-id="c8881-134">XML Writer</span></span>](xml-writer.md)
-   [<span data-ttu-id="c8881-135">Lettore XML</span><span class="sxs-lookup"><span data-stu-id="c8881-135">XML Reader</span></span>](xml-reader.md)
-   [<span data-ttu-id="c8881-136">Buffer XML</span><span class="sxs-lookup"><span data-stu-id="c8881-136">XML Buffer</span></span>](xml-buffer.md)
-   [<span data-ttu-id="c8881-137">Serializzazione</span><span class="sxs-lookup"><span data-stu-id="c8881-137">Serialization</span></span>](serialization.md)
-   [<span data-ttu-id="c8881-138">Supporto del linguaggio XML</span><span class="sxs-lookup"><span data-stu-id="c8881-138">XML Language Support</span></span>](xml-language-support.md)

## <a name="common-to-all-layers"></a><span data-ttu-id="c8881-139">Comune a tutti i livelli</span><span class="sxs-lookup"><span data-stu-id="c8881-139">Common to all layers</span></span>

<span data-ttu-id="c8881-140">Di seguito sono riportati gli argomenti che si applicano a uno dei tre livelli:</span><span class="sxs-lookup"><span data-stu-id="c8881-140">The following are topics that apply to any of the three layers:</span></span>

-   [<span data-ttu-id="c8881-141">Errori</span><span class="sxs-lookup"><span data-stu-id="c8881-141">Errors</span></span>](errors.md)
-   [<span data-ttu-id="c8881-142">Modello asincrono</span><span class="sxs-lookup"><span data-stu-id="c8881-142">Asynchronous Model</span></span>](asynchronous-model.md)
-   [<span data-ttu-id="c8881-143">Thread safety</span><span class="sxs-lookup"><span data-stu-id="c8881-143">Thread Safety</span></span>](thread-safety.md)
-   [<span data-ttu-id="c8881-144">Traccia</span><span class="sxs-lookup"><span data-stu-id="c8881-144">Tracing</span></span>](tracing.md)
-   [<span data-ttu-id="c8881-145">Annullamento</span><span class="sxs-lookup"><span data-stu-id="c8881-145">Cancellation</span></span>](cancellation.md)
-   [<span data-ttu-id="c8881-146">Utilità</span><span class="sxs-lookup"><span data-stu-id="c8881-146">Utilities</span></span>](utilities.md)
-   [<span data-ttu-id="c8881-147">Debug</span><span class="sxs-lookup"><span data-stu-id="c8881-147">Debugging</span></span>](debugging.md)
-   [<span data-ttu-id="c8881-148">Strumento compilatore wsutil</span><span class="sxs-lookup"><span data-stu-id="c8881-148">Wsutil Compiler tool</span></span>](wsutil-compiler-tool.md)
-   [<span data-ttu-id="c8881-149">Heap</span><span class="sxs-lookup"><span data-stu-id="c8881-149">Heap</span></span>](heap.md)

## <a name="examples"></a><span data-ttu-id="c8881-150">Esempio</span><span class="sxs-lookup"><span data-stu-id="c8881-150">Examples</span></span>

<span data-ttu-id="c8881-151">Per ulteriori informazioni sugli elementi API, vedere [riferimenti per servizi Web Windows](windows-web-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c8881-151">For more information about API elements, see [Windows Web Services Reference](windows-web-services-reference.md).</span></span> <span data-ttu-id="c8881-152">Per esempi relativi all'uso dell'API, vedere [uso di servizi Web Windows](using-windows-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="c8881-152">For examples of using the API, see [Using Windows Web Services](using-windows-web-services.md).</span></span>

 

 




