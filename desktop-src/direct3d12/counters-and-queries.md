---
title: Contatori, query e predicazione
description: I contatori output del flusso e UAV funzionano in Direct3D 12 in un metodo simile a Direct3D 11, sebbene ora la memoria per i contatori debba essere allocata dall'app, il driver non esegue questa operazione.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548882"
---
# <a name="counters-queries-and-predication"></a><span data-ttu-id="b1293-103">Contatori, query e predicazione</span><span class="sxs-lookup"><span data-stu-id="b1293-103">Counters, queries, and predication</span></span>

<span data-ttu-id="b1293-104">Questo argomento descrive i contatori di output di flusso, i contatori UAV, le query e predicazione.</span><span class="sxs-lookup"><span data-stu-id="b1293-104">This topic covers stream-output counters, UAV counters, queries, and predication.</span></span>

<span data-ttu-id="b1293-105">I contatori output del flusso e UAV funzionano in Direct3D 12 in un metodo simile a Direct3D 11, sebbene ora la memoria per i contatori debba essere allocata dall'app, il driver non esegue questa operazione.</span><span class="sxs-lookup"><span data-stu-id="b1293-105">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="b1293-106">Le query in Direct3D 12 sono più diverse da quelle in Direct3D 11, con l'aggiunta di barriere e altri processi che eliminano la necessità di alcuni tipi di query.</span><span class="sxs-lookup"><span data-stu-id="b1293-106">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b1293-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b1293-107">In this section</span></span>



| <span data-ttu-id="b1293-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="b1293-108">Topic</span></span>                                                           | <span data-ttu-id="b1293-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1293-109">Description</span></span>                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1293-110">Contatori output flusso</span><span class="sxs-lookup"><span data-stu-id="b1293-110">Stream Output Counters</span></span>](stream-output-counters.md)<br/> | <span data-ttu-id="b1293-111">L'output del flusso è la capacità della GPU di scrivere i vertici in un buffer.</span><span class="sxs-lookup"><span data-stu-id="b1293-111">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="b1293-112">Lo stato del monitoraggio dei contatori di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="b1293-112">The stream output counters monitor progress.</span></span><br/>                                                               |
| [<span data-ttu-id="b1293-113">Contatori UAV</span><span class="sxs-lookup"><span data-stu-id="b1293-113">UAV Counters</span></span>](uav-counters.md)<br/>                     | <span data-ttu-id="b1293-114">I contatori UAV possono essere usati per associare un contatore atomico a 32 bit a una visualizzazione non ordinata (UAV).</span><span class="sxs-lookup"><span data-stu-id="b1293-114">UAV counters can be used to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span><br/>                                                                                |
| [<span data-ttu-id="b1293-115">Query</span><span class="sxs-lookup"><span data-stu-id="b1293-115">Queries</span></span>](queries.md)<br/>                               | <span data-ttu-id="b1293-116">In Direct3D 12, le query vengono raggruppate in matrici di query chiamate heap di query.</span><span class="sxs-lookup"><span data-stu-id="b1293-116">In Direct3D 12, queries are grouped into arrays of queries called a query heap.</span></span> <span data-ttu-id="b1293-117">Un heap di query dispone di un tipo che definisce i tipi di query validi che possono essere utilizzati con tale heap.</span><span class="sxs-lookup"><span data-stu-id="b1293-117">A query heap has a type which defines the valid types of queries that can be used with that heap.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b1293-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1293-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1293-119">Misurazione delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="b1293-119">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>

 

 





