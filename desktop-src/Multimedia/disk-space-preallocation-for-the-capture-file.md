---
title: Preallocazione dello spazio su disco per il file di acquisizione
description: Preallocazione dello spazio su disco per il file di acquisizione
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- Messaggio WM_CAP_FILE_ALLOCATE
- capFileAlloc (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329628"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a><span data-ttu-id="3017a-105">Preallocazione dello spazio su disco per il file di acquisizione</span><span class="sxs-lookup"><span data-stu-id="3017a-105">Disk Space Preallocation for the Capture File</span></span>

<span data-ttu-id="3017a-106">La preallocazione dello spazio su disco per il file di acquisizione compila un file di dimensioni specificate sul disco prima dell'avvio di un'operazione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3017a-106">Preallocating disk space for the capture file builds a file of a specified size on the disk before the start of a capture operation.</span></span> <span data-ttu-id="3017a-107">La preallocazione di un file di acquisizione riduce l'elaborazione richiesta quando è in corso l'acquisizione e comporta un minor numero di frame eliminati.</span><span class="sxs-lookup"><span data-stu-id="3017a-107">Preallocating a capture file reduces the processing required while capture is in progress and results in fewer dropped frames.</span></span> <span data-ttu-id="3017a-108">È possibile preallocare un file di acquisizione usando il messaggio di [**\_ \_ \_ allocazione file di WM Cap**](wm-cap-file-allocate.md) (o la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) ).</span><span class="sxs-lookup"><span data-stu-id="3017a-108">You can preallocate a capture file by using the [**WM\_CAP\_FILE\_ALLOCATE**](wm-cap-file-allocate.md) message (or the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro).</span></span>

<span data-ttu-id="3017a-109">In genere, l'applicazione deve preallocare spazio su disco sufficiente per contenere il file di acquisizione più grande previsto.</span><span class="sxs-lookup"><span data-stu-id="3017a-109">Typically, your application should preallocate enough disk space to contain the largest capture file anticipated.</span></span> <span data-ttu-id="3017a-110">La preallocazione dello spazio su disco non limita le dimensioni del file acquisito.</span><span class="sxs-lookup"><span data-stu-id="3017a-110">Preallocating disk space does not restrict the size of the captured file.</span></span> <span data-ttu-id="3017a-111">Le dimensioni del file vengono ingrandite automaticamente se i dati acquisiti superano lo spazio allocato.</span><span class="sxs-lookup"><span data-stu-id="3017a-111">The file size is automatically enlarged if the captured data exceeds the allocated space.</span></span> <span data-ttu-id="3017a-112">Le successive operazioni di scrittura nel file di acquisizione riutilizzeranno le parti dello spazio su disco allocate per il file, mantenendo le dimensioni e la frammentazione del file.</span><span class="sxs-lookup"><span data-stu-id="3017a-112">Subsequent write operations to the capture file reuse the portions of disk space allocated for the file, preserving the size and fragmentation of the file.</span></span>

<span data-ttu-id="3017a-113">È inoltre possibile migliorare le prestazioni di acquisizione deframmentando il file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3017a-113">You can also improve capture performance by defragmenting the capture file.</span></span> <span data-ttu-id="3017a-114">Per deframmentare il file, utilizzare un'utilità di deframmentazione, ad esempio utilità di deframmentazione dischi.</span><span class="sxs-lookup"><span data-stu-id="3017a-114">To defragment the file, use a defragmentation utility such as Disk Defragmenter.</span></span> <span data-ttu-id="3017a-115">Se si utilizza un file di acquisizione deframmentato e successivamente lo si ingrandisce, è necessario deframmentare il file ingrandito.</span><span class="sxs-lookup"><span data-stu-id="3017a-115">If you use a defragmented capture file and later enlarge it, you should defragment the enlarged file.</span></span> <span data-ttu-id="3017a-116">L'ingrandimento di un file di acquisizione deframmentato può frammentare la parte espansa del file e ridurre le prestazioni nell'operazione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3017a-116">Enlarging a defragmented capture file can fragment the expanded portion of the file and reduce performance in the capture operation.</span></span>

<span data-ttu-id="3017a-117">È anche possibile migliorare le prestazioni usando un disco non compresso per l'acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="3017a-117">You might also improve performance by using an uncompressed disk for video capture.</span></span> <span data-ttu-id="3017a-118">La compressione dei dati durante l'acquisizione può limitare la velocità effettiva di acquisizione sul disco.</span><span class="sxs-lookup"><span data-stu-id="3017a-118">Compressing data during capture can limit capture throughput to the disk.</span></span>

<span data-ttu-id="3017a-119">Un'applicazione può riservare un file di acquisizione permanente per eliminare il tempo necessario per preallocare e deframmentare un file ogni volta che viene avviato.</span><span class="sxs-lookup"><span data-stu-id="3017a-119">An application can reserve a permanent capture file to eliminate the time required to preallocate and defragment a file each time it is started.</span></span> <span data-ttu-id="3017a-120">Poiché un file di acquisizione può richiedere una notevole quantità di spazio su disco e la preallocazione di un file di acquisizione rimuove tutti i dati da un file di acquisizione esistente, un'applicazione deve consentire all'utente di decidere se il file è permanente o temporaneo.</span><span class="sxs-lookup"><span data-stu-id="3017a-120">Because a capture file can require considerable disk space, and preallocating a capture file removes all data from an existing capture file, an application should let the user decide if the file is permanent or temporary.</span></span>

 

 




