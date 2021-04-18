---
description: Gestione Quality-Control
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Gestione Quality-Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303702"
---
# <a name="quality-control-management"></a><span data-ttu-id="cfa9b-103">Gestione Quality-Control</span><span class="sxs-lookup"><span data-stu-id="cfa9b-103">Quality-Control Management</span></span>

<span data-ttu-id="cfa9b-104">Il controllo qualità è un meccanismo che consente di regolare la frequenza del flusso di dati attraverso il grafico filtro in risposta alle prestazioni in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-104">Quality control is a mechanism for adjusting the rate of data flow through the filter graph in response to run-time performance.</span></span> <span data-ttu-id="cfa9b-105">Se un filtro renderer riceve una quantità eccessiva di dati o di dati troppo piccoli, può inviare un *messaggio di qualità*.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-105">If a renderer filter is receiving too much data or too little data, it can send a *quality message*.</span></span> <span data-ttu-id="cfa9b-106">Il messaggio qualitativo richiede la regolazione della velocità dei dati.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-106">The quality message requests an adjustment in the data rate.</span></span> <span data-ttu-id="cfa9b-107">Per impostazione predefinita, i messaggi di qualità viaggiano a Monte dal renderer fino a quando non raggiungono un filtro in grado di rispondere (se presente).</span><span class="sxs-lookup"><span data-stu-id="cfa9b-107">By default, quality messages travel upstream from the renderer until they reach a filter that can respond (if any).</span></span> <span data-ttu-id="cfa9b-108">Un'applicazione può anche implementare un gestore di qualità personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-108">An application can also implement a custom quality manager.</span></span> <span data-ttu-id="cfa9b-109">In tal caso, il renderer passa i messaggi di qualità direttamente al gestore qualità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-109">In that case, the renderer passes quality messages directly to the application's quality manager.</span></span>

<span data-ttu-id="cfa9b-110">Questo articolo contiene gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-110">This article contains the following topics.</span></span>

-   [<span data-ttu-id="cfa9b-111">Messaggi di qualità</span><span class="sxs-lookup"><span data-stu-id="cfa9b-111">Quality Messages</span></span>](quality-messages.md)
-   [<span data-ttu-id="cfa9b-112">Controllo qualità predefinito</span><span class="sxs-lookup"><span data-stu-id="cfa9b-112">Default Quality Control</span></span>](default-quality-control.md)

## <a name="related-topics"></a><span data-ttu-id="cfa9b-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cfa9b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfa9b-114">Flusso di dati per sviluppatori di filtri</span><span class="sxs-lookup"><span data-stu-id="cfa9b-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="cfa9b-115">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="cfa9b-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



