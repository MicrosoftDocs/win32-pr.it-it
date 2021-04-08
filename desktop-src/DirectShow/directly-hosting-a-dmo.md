---
description: Hosting diretto di un DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hosting diretto di un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747658"
---
# <a name="directly-hosting-a-dmo"></a><span data-ttu-id="fc204-103">Hosting diretto di un DMO</span><span class="sxs-lookup"><span data-stu-id="fc204-103">Directly Hosting a DMO</span></span>

<span data-ttu-id="fc204-104">Questa sezione descrive il modo in cui un'applicazione può fungere da client diretto di un DMO.</span><span class="sxs-lookup"><span data-stu-id="fc204-104">This section describes how an application can act as the direct client of a DMO.</span></span> <span data-ttu-id="fc204-105">L'applicazione recapita input a DMO, DMO crea l'output e l'applicazione usa l'output per il rendering, l'ulteriore elaborazione o qualsiasi altro elemento.</span><span class="sxs-lookup"><span data-stu-id="fc204-105">The application delivers input to the DMO, the DMO creates output, and the application uses the output for rendering, further processing, or anything else.</span></span> <span data-ttu-id="fc204-106">L'applicazione è responsabile di problemi quali allocazione della memoria, temporizzazione e sincronizzazione e Threading.</span><span class="sxs-lookup"><span data-stu-id="fc204-106">The application is responsible for issues such as memory allocation, timing and synchronization, and threading.</span></span> <span data-ttu-id="fc204-107">Questi requisiti variano in base alla natura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc204-107">These requirements will depend on the nature of the application.</span></span>

<span data-ttu-id="fc204-108">Le informazioni contenute in questa sezione si applicano anche se si sta scrivendo un componente che funge da livello tra un'applicazione e un DMO (ad esempio, un controllo ActiveX che ospita un DMO).</span><span class="sxs-lookup"><span data-stu-id="fc204-108">The information in this section also applies if you are writing a component that acts as a layer between an application and a DMO (for example, an ActiveX Control that hosts a DMO).</span></span> <span data-ttu-id="fc204-109">Inoltre, è consigliabile leggere questa sezione se si sta scrivendo un DMO, perché descrive le funzionalità che devono essere implementate da DMO.</span><span class="sxs-lookup"><span data-stu-id="fc204-109">In addition, you should read this section if you are writing a DMO, because it describes the functionality that your DMO must implement.</span></span>

<span data-ttu-id="fc204-110">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="fc204-110">This section contains the following topics:</span></span>

-   [<span data-ttu-id="fc204-111">Impostazione dei tipi di supporto in un DMO</span><span class="sxs-lookup"><span data-stu-id="fc204-111">Setting Media Types on a DMO</span></span>](setting-media-types-on-a-dmo.md)
-   [<span data-ttu-id="fc204-112">Elaborazione di dati in un DMO</span><span class="sxs-lookup"><span data-stu-id="fc204-112">Processing Data in a DMO</span></span>](processing-data-in-a-dmo.md)
-   [<span data-ttu-id="fc204-113">Elaborazione sul posto</span><span class="sxs-lookup"><span data-stu-id="fc204-113">In-Place Processing</span></span>](in-place-processing.md)
-   [<span data-ttu-id="fc204-114">Flussi facoltativi</span><span class="sxs-lookup"><span data-stu-id="fc204-114">Optional Streams</span></span>](optional-streams.md)
-   [<span data-ttu-id="fc204-115">Implementazione di IMediaBuffer</span><span class="sxs-lookup"><span data-stu-id="fc204-115">Implementing IMediaBuffer</span></span>](implementing-imediabuffer.md)

## <a name="related-topics"></a><span data-ttu-id="fc204-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc204-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc204-117">Uso di DMOs</span><span class="sxs-lookup"><span data-stu-id="fc204-117">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



