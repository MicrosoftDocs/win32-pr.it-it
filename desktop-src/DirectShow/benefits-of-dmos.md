---
description: Vantaggi di DMOs
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Vantaggi di DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225458"
---
# <a name="benefits-of-dmos"></a><span data-ttu-id="26420-103">Vantaggi di DMOs</span><span class="sxs-lookup"><span data-stu-id="26420-103">Benefits of DMOs</span></span>

<span data-ttu-id="26420-104">DMOs offre i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="26420-104">DMOs offer the following advantages:</span></span>

-   <span data-ttu-id="26420-105">Sono in genere più piccoli e più semplici dei filtri DirectShow, perché supportano meno funzionalità.</span><span class="sxs-lookup"><span data-stu-id="26420-105">They are generally smaller and simpler than DirectShow filters, because they support less functionality.</span></span>
-   <span data-ttu-id="26420-106">Sono più flessibili dei filtri DirectShow perché non richiedono un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="26420-106">They are more flexible than DirectShow filters because they do not require a filter graph.</span></span> <span data-ttu-id="26420-107">È possibile usarli con DirectShow quando sono necessari i servizi forniti da DirectShow, ad esempio sincronizzazione, connessione intelligente, gestione automatica del flusso di dati e gestione dei thread.</span><span class="sxs-lookup"><span data-stu-id="26420-107">You can use them with DirectShow when you need the services that DirectShow provides, such as synchronization, intelligent connection, automatic handling of data flow, and thread management.</span></span> <span data-ttu-id="26420-108">I client che non necessitano di questi servizi possono accedere direttamente a DMOs.</span><span class="sxs-lookup"><span data-stu-id="26420-108">Clients that do not need these services can access DMOs directly.</span></span>
-   <span data-ttu-id="26420-109">DMOs eseguono sempre l'elaborazione sincrona dei dati, che elimina molti dei problemi di threading che è necessario prendere in considerazione se si scrive un filtro.</span><span class="sxs-lookup"><span data-stu-id="26420-109">DMOs always perform synchronous data processing, which eliminates many of the threading issues that you must consider if you write a filter.</span></span>
-   <span data-ttu-id="26420-110">A differenza dei codec ACM e VCM tradizionali, DMOs sono basati sulla Component Object Model (COM), quindi possono essere estesi tramite **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="26420-110">Unlike traditional ACM and VCM codecs, DMOs are based on the Component Object Model (COM), so they can be extended through **QueryInterface**.</span></span>
-   <span data-ttu-id="26420-111">DMOs supporta un modello di streaming più generalizzato rispetto ai codec ACM o VCM.</span><span class="sxs-lookup"><span data-stu-id="26420-111">DMOs support a more generalized streaming model than ACM or VCM codecs.</span></span> <span data-ttu-id="26420-112">Analogamente ai filtri DirectShow, DMOs può supportare più input e più output.</span><span class="sxs-lookup"><span data-stu-id="26420-112">Like DirectShow filters, DMOs can support multiple inputs and multiple outputs.</span></span>

<span data-ttu-id="26420-113">Per questi motivi, è ora consigliabile usare DMOs come soluzione per la scrittura di codificatori, decodificatori e effetti audio.</span><span class="sxs-lookup"><span data-stu-id="26420-113">For these reasons, DMOs are now recommended as the solution for writing encoders, decoders, and audio effects.</span></span> <span data-ttu-id="26420-114">Sono possibili anche molti altri scenari, a seconda delle esigenze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26420-114">Many other scenarios are possible as well, depending on the needs of the application.</span></span>

<span data-ttu-id="26420-115">Differenze tra DMOs e filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="26420-115">How DMOs Differ from DirectShow Filters</span></span>

<span data-ttu-id="26420-116">I filtri DirectShow non possono funzionare al di fuori di un grafico filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="26420-116">DirectShow filters cannot function outside of a DirectShow filter graph.</span></span> <span data-ttu-id="26420-117">In DirectShow, il gestore del grafico del filtro intermedia tra l'applicazione e i filtri.</span><span class="sxs-lookup"><span data-stu-id="26420-117">In DirectShow, the Filter Graph Manager mediates between the application and the filters.</span></span> <span data-ttu-id="26420-118">I filtri DirectShow eseguono la maggior parte delle operazioni necessarie per lo streaming dei dati, tra cui:</span><span class="sxs-lookup"><span data-stu-id="26420-118">DirectShow filters do most of the work required to stream data, including:</span></span>

-   <span data-ttu-id="26420-119">Allocazione dei buffer.</span><span class="sxs-lookup"><span data-stu-id="26420-119">Allocating buffers.</span></span>
-   <span data-ttu-id="26420-120">Negoziazione di tipi di supporto e connessioni ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="26420-120">Negotiating media types and connections to other filters.</span></span>
-   <span data-ttu-id="26420-121">Push dei dati tramite il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="26420-121">Pushing data through the filter graph.</span></span>
-   <span data-ttu-id="26420-122">Invio di eventi a Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="26420-122">Sending events to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="26420-123">Sincronizzazione di più thread.</span><span class="sxs-lookup"><span data-stu-id="26420-123">Synchronizing multiple threads.</span></span>

<span data-ttu-id="26420-124">Al contrario, un DMO non esegue nessuna di queste operazioni.</span><span class="sxs-lookup"><span data-stu-id="26420-124">In contrast, a DMO does none of these things.</span></span> <span data-ttu-id="26420-125">Questi tipi di attività sono invece responsabilità del client che utilizza DMO.</span><span class="sxs-lookup"><span data-stu-id="26420-125">Instead, these kinds of tasks are the responsibility of the client using the DMO.</span></span> <span data-ttu-id="26420-126">Il client alloca i buffer, li compila con i dati e li recapita a DMO.</span><span class="sxs-lookup"><span data-stu-id="26420-126">The client allocates buffers, fills them with data, and delivers them to the DMO.</span></span> <span data-ttu-id="26420-127">Il DMO elabora i dati e il client recupera i buffer di output risultanti.</span><span class="sxs-lookup"><span data-stu-id="26420-127">The DMO processes the data, and the client retrieves the resulting output buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26420-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26420-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26420-129">Informazioni su DMOs</span><span class="sxs-lookup"><span data-stu-id="26420-129">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



