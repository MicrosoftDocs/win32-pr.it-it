---
title: Modello di Data-Pull e modello di Data-Push
description: Modello di Data-Pull e modello di Data-Push
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399800"
---
# <a name="data-pull-model-and-data-push-model"></a><span data-ttu-id="fd02f-103">Modello di Data-Pull e modello di Data-Push</span><span class="sxs-lookup"><span data-stu-id="fd02f-103">Data-Pull Model and Data-Push Model</span></span>

<span data-ttu-id="fd02f-104">Un client di un moniker asincrono può scegliere tra un modello di pull dei dati e di push dei dati per la Guida di un'operazione di [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) asincrona e la ricezione di notifiche asincrone.</span><span class="sxs-lookup"><span data-stu-id="fd02f-104">A client of an asynchronous moniker can choose between a data-pull and data-push model for driving an asynchronous [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) operation and receiving asynchronous notifications.</span></span> <span data-ttu-id="fd02f-105">Nel modello di pull dei dati il client esegue l'operazione di associazione e il moniker fornisce i dati al client solo quando vengono letti.</span><span class="sxs-lookup"><span data-stu-id="fd02f-105">In the data-pull model, the client drives the bind operation and the moniker provides data to the client only as it is read.</span></span> <span data-ttu-id="fd02f-106">In altre parole, dopo la prima chiamata a [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), il moniker non fornisce alcun dato al client a meno che il client non abbia utilizzato tutti i dati già disponibili.</span><span class="sxs-lookup"><span data-stu-id="fd02f-106">In other words, after the first call to [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), the moniker does not provide any data to the client unless the client has consumed all of the data that is already available.</span></span>

<span data-ttu-id="fd02f-107">Poiché i dati vengono scaricati solo quando vengono richiesti, i client che scelgono il modello di pull dei dati devono assicurarsi di leggere questi dati in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="fd02f-107">Because data is downloaded only as it is requested, clients that choose the data-pull model must make sure to read this data in a timely manner.</span></span> <span data-ttu-id="fd02f-108">Nel caso di download di Internet con [moniker URL](url-monikers.md), l'operazione di associazione potrebbe non riuscire se un client è in attesa troppo a lungo prima di richiedere più dati.</span><span class="sxs-lookup"><span data-stu-id="fd02f-108">In the case of Internet downloads with [URL monikers](url-monikers.md), the bind operation may fail if a client waits too long before requesting more data.</span></span>

<span data-ttu-id="fd02f-109">Nel modello di push dei dati, il moniker guida l'operazione di associazione asincrona e notifica continuamente al client ogni volta che sono disponibili nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="fd02f-109">In the data-push model, the moniker drives the asynchronous bind operation and continuously notifies the client whenever new data is available.</span></span> <span data-ttu-id="fd02f-110">Il client può scegliere se leggere i dati in qualsiasi momento durante l'operazione di associazione, ma il moniker guiderà il completamento dell'operazione di associazione, indipendentemente dal fatto che.</span><span class="sxs-lookup"><span data-stu-id="fd02f-110">The client may choose whether to read the data at any point during the bind operation, but the moniker will drive the bind operation to completion regardless.</span></span>

<span data-ttu-id="fd02f-111">Inoltre, è necessario ricordare di seguire le regole COM per l'allocazione di memoria quando si usano moniker asincroni, in particolare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="fd02f-111">Also, you need to remember to follow the COM rules for memory allocation when using asynchronous monikers, specifically the following:</span></span>

-   <span data-ttu-id="fd02f-112">Ogni volta che un'interfaccia COM o una chiamata di funzione restituisce un buffer (String o other) al client, il client è responsabile della liberazione della memoria chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="fd02f-112">Whenever a COM interface or function call returns a buffer (string or other) to its client, the client is responsible for freeing the memory by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>
-   <span data-ttu-id="fd02f-113">Ogni volta che un'interfaccia o una funzione COM richiede un buffer dal client, il client deve allocare il buffer usando [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) e il chiamato deve liberarlo.</span><span class="sxs-lookup"><span data-stu-id="fd02f-113">Whenever a COM interface or function requires a buffer from its client, the client must allocate that buffer using [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) and the callee must free it.</span></span>

<span data-ttu-id="fd02f-114">Assicurarsi di seguire queste regole quando si allocano stringhe o buffer passati a moniker asincroni e si ricorda di liberare la memoria restituita dai moniker asincroni.</span><span class="sxs-lookup"><span data-stu-id="fd02f-114">Be sure to follow these rules when allocating strings or buffers that are passed to asynchronous monikers, and remember to free memory returned by asynchronous monikers.</span></span> <span data-ttu-id="fd02f-115">Per informazioni dettagliate, vedere [Managing Memory Allocation](the-com-library.md) and Related topics.</span><span class="sxs-lookup"><span data-stu-id="fd02f-115">See [Managing Memory Allocation](the-com-library.md) and related topics for complete details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd02f-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd02f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd02f-117">Moniker asincroni</span><span class="sxs-lookup"><span data-stu-id="fd02f-117">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 