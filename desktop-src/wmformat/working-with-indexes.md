---
title: Operazioni con gli indici
description: Operazioni con gli indici
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media Format SDK, indici
- ASF (Advanced Systems Format), indici
- ASF (formato avanzato dei sistemi), indici
- indici, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855765"
---
# <a name="working-with-indexes"></a><span data-ttu-id="484a2-107">Operazioni con gli indici</span><span class="sxs-lookup"><span data-stu-id="484a2-107">Working with Indexes</span></span>

<span data-ttu-id="484a2-108">Windows Media Format SDK supporta la ricerca e l'ingrandimento del contenuto.</span><span class="sxs-lookup"><span data-stu-id="484a2-108">The Windows Media Format SDK supports seeking and striding through content.</span></span> <span data-ttu-id="484a2-109">La ricerca consente di specificare una posizione nella sequenza temporale del file per iniziare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="484a2-109">Seeking enables you to specify a place on the file's timeline to begin playback.</span></span> <span data-ttu-id="484a2-110">A grandi passi è possibile velocizzare e riavvolgere l'output di un file.</span><span class="sxs-lookup"><span data-stu-id="484a2-110">Striding enables you to fast-forward and rewind the output of a file.</span></span> <span data-ttu-id="484a2-111">Per sfruttare i vantaggi di queste funzionalità, è necessario indicizzare i file.</span><span class="sxs-lookup"><span data-stu-id="484a2-111">Files must be indexed to take advantage of these features.</span></span> <span data-ttu-id="484a2-112">Un indice è una serie di valori che rappresentano le posizioni nel file (tempi di presentazione, numeri di fotogrammi o codici temporali SMTP) con offset corrispondenti nella sezione dei dati del file per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="484a2-112">An index is a series of values representing positions in the file (either presentation times, frame numbers, or SMTPE time codes) with corresponding offsets into the data section of the file for each.</span></span> <span data-ttu-id="484a2-113">L'indicizzazione è particolarmente importante per i flussi video, in quanto il tempo di presentazione del flusso audio può essere facilmente stimato.</span><span class="sxs-lookup"><span data-stu-id="484a2-113">Indexing is most important for video streams, as audio stream presentation time can be easily estimated.</span></span> <span data-ttu-id="484a2-114">Tuttavia, alcuni flussi audio possono richiedere anche indici.</span><span class="sxs-lookup"><span data-stu-id="484a2-114">However, some audio streams may require indexes as well.</span></span> <span data-ttu-id="484a2-115">Per impostazione predefinita, ogni nuovo file ASF viene indicizzato dal writer.</span><span class="sxs-lookup"><span data-stu-id="484a2-115">By default, the writer will index every new ASF file.</span></span> <span data-ttu-id="484a2-116">Se vengono apportate modifiche al contenuto di un file, è necessario aggiornare l'indice manualmente utilizzando l'oggetto indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="484a2-116">If changes are made to the content of a file, you must refresh the index yourself using the indexer object.</span></span>

<span data-ttu-id="484a2-117">L'indicizzatore supporta l'indicizzazione temporale e basata su frame, nonché l'indicizzazione basata sui codici temporali SMPTE (se presente).</span><span class="sxs-lookup"><span data-stu-id="484a2-117">The indexer supports both temporal and frame-based indexing as well as indexing based on SMPTE time codes (if present).</span></span> <span data-ttu-id="484a2-118">Per impostazione predefinita, il writer creerà un indice temporale per ogni nuovo flusso video codificato in un file.</span><span class="sxs-lookup"><span data-stu-id="484a2-118">The writer will create a temporal index by default for every new video stream encoded to a file.</span></span> <span data-ttu-id="484a2-119">È necessario configurare e chiamare l'indicizzatore in modo esplicito per creare un indice del codice ora SMPTE o basato su frame.</span><span class="sxs-lookup"><span data-stu-id="484a2-119">You must explicitly configure and call the indexer to create a frame-based or SMPTE time code index.</span></span>

<span data-ttu-id="484a2-120">Quando vengono apportate modifiche al contenuto di un file ASF, è necessario indicizzarlo di nuovo.</span><span class="sxs-lookup"><span data-stu-id="484a2-120">When changes are made to the content of an ASF file, it must be indexed again.</span></span>

<span data-ttu-id="484a2-121">Nelle sezioni seguenti è presente un codice di esempio per l'esecuzione di attività di indicizzazione comuni.</span><span class="sxs-lookup"><span data-stu-id="484a2-121">The following sections present example code for performing common indexing tasks.</span></span>

-   [<span data-ttu-id="484a2-122">Per disabilitare l'indicizzazione automatica</span><span class="sxs-lookup"><span data-stu-id="484a2-122">To Disable Automatic Indexing</span></span>](to-disable-automatic-indexing.md)
-   [<span data-ttu-id="484a2-123">Per configurare l'indicizzatore</span><span class="sxs-lookup"><span data-stu-id="484a2-123">To Configure the Indexer</span></span>](to-configure-the-indexer.md)
-   [<span data-ttu-id="484a2-124">Per indicizzare un file ASF</span><span class="sxs-lookup"><span data-stu-id="484a2-124">To Index an ASF File</span></span>](to-index-an-asf-file.md)
-   [<span data-ttu-id="484a2-125">Per arrestare l'indicizzazione in corso</span><span class="sxs-lookup"><span data-stu-id="484a2-125">To Stop Indexing in Progress</span></span>](to-stop-indexing-in-progress.md)

<span data-ttu-id="484a2-126">Inoltre, l'applicazione di esempio DSCopy illustra l'uso dell'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="484a2-126">In addition, the DSCopy sample application illustrates the use of the indexer.</span></span> <span data-ttu-id="484a2-127">Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="484a2-127">For more information, see [Sample Applications](sample-applications.md).</span></span>

 

 




