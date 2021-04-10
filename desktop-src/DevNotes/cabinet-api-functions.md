---
description: "Altre informazioni su: funzioni dell'API cabinet"
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Funzioni dell'API cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877554"
---
# <a name="cabinet-api-functions"></a><span data-ttu-id="30f2d-103">Funzioni dell'API cabinet</span><span class="sxs-lookup"><span data-stu-id="30f2d-103">Cabinet API Functions</span></span>

<span data-ttu-id="30f2d-104">In questa sezione vengono descritte le funzioni dell'API CAB seguenti:</span><span class="sxs-lookup"><span data-stu-id="30f2d-104">This section describes the following Cabinet API functions:</span></span>

## <a name="fci-functions"></a><span data-ttu-id="30f2d-105">Funzioni FCI</span><span class="sxs-lookup"><span data-stu-id="30f2d-105">FCI Functions</span></span>

<span data-ttu-id="30f2d-106">La libreria FCI (file compression Interface) offre la possibilità di creare armadi (noti anche come "file CAB").</span><span class="sxs-lookup"><span data-stu-id="30f2d-106">The FCI (File Compression Interface) library provides the ability to create cabinets (also known as "CAB files").</span></span> <span data-ttu-id="30f2d-107">Inoltre, la libreria fornisce la compressione per ridurre le dimensioni dei dati dei file archiviati nei file CAB.</span><span class="sxs-lookup"><span data-stu-id="30f2d-107">Additionally, the library provides compression to reduce the size of the file data stored in cabinets.</span></span>



| <span data-ttu-id="30f2d-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="30f2d-108">Function</span></span>                                   | <span data-ttu-id="30f2d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30f2d-109">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30f2d-110">**FCIAddFile**</span><span class="sxs-lookup"><span data-stu-id="30f2d-110">**FCIAddFile**</span></span>](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | <span data-ttu-id="30f2d-111">Aggiunge un file al file CAB attualmente in fase di contructed.</span><span class="sxs-lookup"><span data-stu-id="30f2d-111">Adds a file to the cabinet currently being contructed.</span></span><br/>                                           |
| [<span data-ttu-id="30f2d-112">**FCICreate**</span><span class="sxs-lookup"><span data-stu-id="30f2d-112">**FCICreate**</span></span>](/windows/desktop/api/Fci/nf-fci-fcicreate)             | <span data-ttu-id="30f2d-113">Crea un contesto dell'istanza del cluster di failover.</span><span class="sxs-lookup"><span data-stu-id="30f2d-113">Creates an FCI context.</span></span><br/>                                                                          |
| [<span data-ttu-id="30f2d-114">**FCIDestroy**</span><span class="sxs-lookup"><span data-stu-id="30f2d-114">**FCIDestroy**</span></span>](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | <span data-ttu-id="30f2d-115">Elimina un contesto FCI aperto, liberando tutti i file di memoria e temporanei associati al contesto.</span><span class="sxs-lookup"><span data-stu-id="30f2d-115">Deletes an open FCI context, freeing any memory and temporary files associated with the context.</span></span><br/> |
| [<span data-ttu-id="30f2d-116">**FCIFlushCabinet**</span><span class="sxs-lookup"><span data-stu-id="30f2d-116">**FCIFlushCabinet**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | <span data-ttu-id="30f2d-117">Completa il file CAB corrente.</span><span class="sxs-lookup"><span data-stu-id="30f2d-117">Completes the current cabinet.</span></span><br/>                                                                   |
| [<span data-ttu-id="30f2d-118">**FCIFlushFolder**</span><span class="sxs-lookup"><span data-stu-id="30f2d-118">**FCIFlushFolder**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | <span data-ttu-id="30f2d-119">Impone il completamento immediato della cartella corrente in costruzione.</span><span class="sxs-lookup"><span data-stu-id="30f2d-119">Forces the current folder under construction to be completed immediately.</span></span><br/>                        |



 

## <a name="fdi-functions"></a><span data-ttu-id="30f2d-120">Funzioni IDE</span><span class="sxs-lookup"><span data-stu-id="30f2d-120">FDI Functions</span></span>

<span data-ttu-id="30f2d-121">La libreria IDE (file Decompression Interface) offre la possibilità di estrarre i file dai file CAB.</span><span class="sxs-lookup"><span data-stu-id="30f2d-121">The FDI (File Decompression Interface) library provides the ability to extract files from cabinets.</span></span>



| <span data-ttu-id="30f2d-122">Funzione</span><span class="sxs-lookup"><span data-stu-id="30f2d-122">Function</span></span>                                         | <span data-ttu-id="30f2d-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30f2d-123">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30f2d-124">**FDICopy**</span><span class="sxs-lookup"><span data-stu-id="30f2d-124">**FDICopy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | <span data-ttu-id="30f2d-125">Estrae i file dai file CAB.</span><span class="sxs-lookup"><span data-stu-id="30f2d-125">Extracts files from cabinets.</span></span><br/>                                                          |
| [<span data-ttu-id="30f2d-126">**FDICreate**</span><span class="sxs-lookup"><span data-stu-id="30f2d-126">**FDICreate**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | <span data-ttu-id="30f2d-127">Crea un contesto IDE.</span><span class="sxs-lookup"><span data-stu-id="30f2d-127">Creates an FDI context.</span></span><br/>                                                                |
| [<span data-ttu-id="30f2d-128">**FDIDestroy**</span><span class="sxs-lookup"><span data-stu-id="30f2d-128">**FDIDestroy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | <span data-ttu-id="30f2d-129">Elimina un contesto IDE aperto.</span><span class="sxs-lookup"><span data-stu-id="30f2d-129">Deletes an open FDI context.</span></span><br/>                                                           |
| [<span data-ttu-id="30f2d-130">**FDIIsCabinet**</span><span class="sxs-lookup"><span data-stu-id="30f2d-130">**FDIIsCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | <span data-ttu-id="30f2d-131">Determina se un file è un file CAB e, in caso contrario, restituisce informazioni descrittive.</span><span class="sxs-lookup"><span data-stu-id="30f2d-131">Determines whether a file is a cabinet and, if it is, returns descriptive information.</span></span><br/> |
| [<span data-ttu-id="30f2d-132">**FDITruncateCabinet**</span><span class="sxs-lookup"><span data-stu-id="30f2d-132">**FDITruncateCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | <span data-ttu-id="30f2d-133">Tronca un file CAB a partire dal numero di cartella specificato.</span><span class="sxs-lookup"><span data-stu-id="30f2d-133">Truncates a cabinet file starting at the specified folder number.</span></span><br/>                      |



 

## <a name="deprecated-functions"></a><span data-ttu-id="30f2d-134">Funzioni deprecate</span><span class="sxs-lookup"><span data-stu-id="30f2d-134">Deprecated Functions</span></span>

-   [<span data-ttu-id="30f2d-135">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="30f2d-135">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
-   [<span data-ttu-id="30f2d-136">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="30f2d-136">**DllGetVersion**</span></span>](dllgetversion.md)
-   [<span data-ttu-id="30f2d-137">**Estrarre**</span><span class="sxs-lookup"><span data-stu-id="30f2d-137">**Extract**</span></span>](extract.md)
-   [<span data-ttu-id="30f2d-138">**GetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="30f2d-138">**GetDllVersion**</span></span>](getdllversion.md)

## <a name="related-topics"></a><span data-ttu-id="30f2d-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30f2d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30f2d-140">Informazioni di riferimento sull'API cabinet</span><span class="sxs-lookup"><span data-stu-id="30f2d-140">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="30f2d-141">Uso dell'API cabinet</span><span class="sxs-lookup"><span data-stu-id="30f2d-141">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




