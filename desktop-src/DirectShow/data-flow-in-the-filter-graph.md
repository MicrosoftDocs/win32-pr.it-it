---
description: Flusso di dati nel grafico del filtro
ms.assetid: 3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3
title: Flusso di dati nel grafico del filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38e0e730dd78e3a42a1121e4a63a053e6016402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103877013"
---
# <a name="data-flow-in-the-filter-graph"></a><span data-ttu-id="3300e-103">Flusso di dati nel grafico del filtro</span><span class="sxs-lookup"><span data-stu-id="3300e-103">Data Flow in the Filter Graph</span></span>

<span data-ttu-id="3300e-104">In questa sezione viene descritto il modo in cui i dati multimediali vengono spostati nel grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="3300e-104">This section describes how media data moves through the filter graph.</span></span> <span data-ttu-id="3300e-105">In genere, non è necessario conoscere questi dettagli per scrivere un'applicazione DirectShow, sebbene in alcune situazioni possa risultare utile.</span><span class="sxs-lookup"><span data-stu-id="3300e-105">Usually, you do not need to know these details to write a DirectShow application, although in some situations you may find it helpful.</span></span> <span data-ttu-id="3300e-106">Se si sta scrivendo un filtro DirectShow, sarà necessario comprendere questo materiale.</span><span class="sxs-lookup"><span data-stu-id="3300e-106">If you are writing a DirectShow filter, you will need to understand this material.</span></span>

<span data-ttu-id="3300e-107">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="3300e-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="3300e-108">Panoramica del flusso di dati in DirectShow</span><span class="sxs-lookup"><span data-stu-id="3300e-108">Overview of Data Flow in DirectShow</span></span>](overview-of-data-flow-in-directshow.md)
-   [<span data-ttu-id="3300e-109">Trasporti</span><span class="sxs-lookup"><span data-stu-id="3300e-109">Transports</span></span>](transports.md)
-   [<span data-ttu-id="3300e-110">Esempi e allocatori</span><span class="sxs-lookup"><span data-stu-id="3300e-110">Samples and Allocators</span></span>](samples-and-allocators.md)
-   [<span data-ttu-id="3300e-111">Stati filtro</span><span class="sxs-lookup"><span data-stu-id="3300e-111">Filter States</span></span>](filter-states.md)
-   [<span data-ttu-id="3300e-112">Modello di pull</span><span class="sxs-lookup"><span data-stu-id="3300e-112">Pull Model</span></span>](pull-model.md)

## <a name="related-topics"></a><span data-ttu-id="3300e-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3300e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3300e-114">Flusso di dati per sviluppatori di filtri</span><span class="sxs-lookup"><span data-stu-id="3300e-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> </dl>

 

 



