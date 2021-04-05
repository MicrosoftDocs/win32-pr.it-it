---
description: Usare le funzioni PDH per raccogliere i dati sulle prestazioni.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Utilizzo delle funzioni PDH per utilizzare i dati del contatore
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881733"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a><span data-ttu-id="8bbf2-103">Utilizzo delle funzioni PDH per utilizzare i dati del contatore</span><span class="sxs-lookup"><span data-stu-id="8bbf2-103">Using the PDH Functions to Consume Counter Data</span></span>

<span data-ttu-id="8bbf2-104">Usare le funzioni PDH per raccogliere i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8bbf2-104">Use the PDH functions to collect performance data.</span></span> <span data-ttu-id="8bbf2-105">Le funzioni PDH sono più facili da utilizzare rispetto alle [funzioni del registro di sistema](using-the-registry-functions-to-consume-counter-data.md) e possono essere utilizzate per accedere ai dati dei contatori sia per i provider v1 che per quelli V2.</span><span class="sxs-lookup"><span data-stu-id="8bbf2-105">The PDH functions are easier to use than the [registry functions](using-the-registry-functions-to-consume-counter-data.md) and can be used to access counter data both V1 and V2 providers.</span></span> <span data-ttu-id="8bbf2-106">PDH dispone di API per la raccolta dei dati sulle prestazioni correnti, il salvataggio dei dati sulle prestazioni nei file di log e la lettura dei dati dai file di log.</span><span class="sxs-lookup"><span data-stu-id="8bbf2-106">PDH has APIs for collecting current performance data, saving performance data to log files, and reading data from log files.</span></span>

> [!Note]
> <span data-ttu-id="8bbf2-107">Non è possibile usare le funzioni del livello di astrazione dei dati sulle prestazioni se si scrivono app OneCore di Windows.</span><span class="sxs-lookup"><span data-stu-id="8bbf2-107">You cannot use the Performance Data Helper abstraction-layer functions if you are writing Windows OneCore apps.</span></span> <span data-ttu-id="8bbf2-108">Usare invece le [funzioni consumer Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="8bbf2-108">Instead, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

<span data-ttu-id="8bbf2-109">PDH è un'API di alto livello che semplifica la raccolta dei dati dei contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8bbf2-109">PDH is a high-level API that simplifies collecting performance counter data.</span></span> <span data-ttu-id="8bbf2-110">Consente l'analisi delle query, la memorizzazione dei metadati nella cache, la corrispondenza delle istanze tra gli esempi, l'elaborazione di valori formattati da valori non elaborati, la lettura dei dati dai file di log e il salvataggio dei dati nei file di log.</span><span class="sxs-lookup"><span data-stu-id="8bbf2-110">It helps with query parsing, metadata caching, matching up instances between samples, computing formatted values from raw values, reading data from log files, and saving data to log files.</span></span> <span data-ttu-id="8bbf2-111">PDH usa automaticamente le [funzioni del registro di sistema](using-the-registry-functions-to-consume-counter-data.md) durante la raccolta dei dati dai **provider v1** e usa le [funzioni consumer v2](using-the-perflib-functions-to-consume-counter-data.md) durante la raccolta dei dati dai **provider v2**.</span><span class="sxs-lookup"><span data-stu-id="8bbf2-111">PDH automatically uses the [registry functions](using-the-registry-functions-to-consume-counter-data.md) when collecting data from **V1 providers** and it uses the [V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) when collecting data from **V2 providers**.</span></span>

<span data-ttu-id="8bbf2-112">Per raccogliere dati sulle prestazioni usando le funzioni PDH, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="8bbf2-112">To collect performance data using the PDH functions, perform the following steps.</span></span>

1. [<span data-ttu-id="8bbf2-113">Creare una query</span><span class="sxs-lookup"><span data-stu-id="8bbf2-113">Create a query</span></span>](creating-a-query.md)
2. [<span data-ttu-id="8bbf2-114">Aggiungere contatori alla query</span><span class="sxs-lookup"><span data-stu-id="8bbf2-114">Add counters to the query</span></span>](creating-a-query.md)
3. [<span data-ttu-id="8bbf2-115">Raccogliere i dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="8bbf2-115">Collect the performance data</span></span>](collecting-performance-data.md)
4. [<span data-ttu-id="8bbf2-116">Visualizzare i dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="8bbf2-116">Display the performance data</span></span>](displaying-performance-data.md)
5. [<span data-ttu-id="8bbf2-117">Chiudere la query</span><span class="sxs-lookup"><span data-stu-id="8bbf2-117">Close the query</span></span>](creating-a-query.md)

<span data-ttu-id="8bbf2-118">È possibile raccogliere dati sulle prestazioni da origini in tempo reale o da file di log.</span><span class="sxs-lookup"><span data-stu-id="8bbf2-118">You can collect performance data from either real-time sources or log files.</span></span> <span data-ttu-id="8bbf2-119">Per ulteriori informazioni su come scrivere i dati sulle prestazioni nei file di log, vedere [utilizzo dei file di log](working-with-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="8bbf2-119">For more information on how to write performance data to log files, see [Working with Log Files](working-with-log-files.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8bbf2-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bbf2-120">See also</span></span>

- [<span data-ttu-id="8bbf2-121">Raccolta dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="8bbf2-121">Collecting Performance Data</span></span>](collecting-performance-data.md)
- [<span data-ttu-id="8bbf2-122">Esplorazione dei contatori</span><span class="sxs-lookup"><span data-stu-id="8bbf2-122">Browsing Counters</span></span>](browsing-counters.md)
- [<span data-ttu-id="8bbf2-123">Verifica dei valori restituiti dell'interfaccia PDH</span><span class="sxs-lookup"><span data-stu-id="8bbf2-123">Checking PDH Interface Return Values</span></span>](checking-pdh-interface-return-values.md)
- [<span data-ttu-id="8bbf2-124">esempi</span><span class="sxs-lookup"><span data-stu-id="8bbf2-124">Examples</span></span>](examples.md)
