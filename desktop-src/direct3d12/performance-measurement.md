---
title: Contatori, query e misurazione delle prestazioni
description: Le sezioni seguenti descrivono le funzionalità da usare per il test delle prestazioni e il miglioramento, ad esempio query, contatori, temporizzazione e predicazione.
ms.assetid: C7AEF1A0-36FB-4026-9CCF-ED0206961A58
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf316978f3dd0928692f378dd8d72b8453ad0aae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103996"
---
# <a name="counters-queries-and-performance-measurement"></a><span data-ttu-id="3cb2a-103">Contatori, query e misurazione delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="3cb2a-103">Counters, Queries and Performance Measurement</span></span>

<span data-ttu-id="3cb2a-104">Le sezioni seguenti descrivono le funzionalità da usare per il test delle prestazioni e il miglioramento, ad esempio query, contatori, temporizzazione e predicazione.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-104">The following sections describe features for use in performance testing and improvement, such as queries, counters, timing, and predication.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3cb2a-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3cb2a-105">In this section</span></span>



| <span data-ttu-id="3cb2a-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="3cb2a-106">Topic</span></span>                                                                                                 | <span data-ttu-id="3cb2a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cb2a-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3cb2a-108">Contatori di output di flusso, contatori UAV, query e predicazione</span><span class="sxs-lookup"><span data-stu-id="3cb2a-108">Stream-Output Counters, UAV Counters, Queries, and Predication</span></span>](counters-and-queries.md)<br/> | <span data-ttu-id="3cb2a-109">I contatori output del flusso e UAV funzionano in Direct3D 12 in un metodo simile a Direct3D 11, sebbene ora la memoria per i contatori debba essere allocata dall'app, il driver non esegue questa operazione.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-109">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="3cb2a-110">Le query in Direct3D 12 sono più diverse da quelle in Direct3D 11, con l'aggiunta di barriere e altri processi che eliminano la necessità di alcuni tipi di query.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-110">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span><br/> |
| [<span data-ttu-id="3cb2a-111">Intervallo</span><span class="sxs-lookup"><span data-stu-id="3cb2a-111">Timing</span></span>](timing.md)<br/>                                                                       | <span data-ttu-id="3cb2a-112">In questa sezione viene illustrata l'esecuzione di query sui timestamp e la calibratura dei contatori di timestamp CPU e GPU.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-112">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="3cb2a-113">Predicazione</span><span class="sxs-lookup"><span data-stu-id="3cb2a-113">Predication</span></span>](predication.md)<br/>                                                             | <span data-ttu-id="3cb2a-114">Predicazione è una funzionalità che consente alla GPU anziché alla CPU di determinare di non creare, copiare o inviare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="3cb2a-114">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span><br/>                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="3cb2a-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3cb2a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cb2a-116">Guida per programmatori Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3cb2a-116">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





