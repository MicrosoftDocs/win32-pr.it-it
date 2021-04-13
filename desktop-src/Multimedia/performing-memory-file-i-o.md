---
title: Esecuzione di operazioni di I/O su file di memoria
description: Esecuzione di operazioni di I/O su file di memoria
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- I/O file multimediale, memoria
- I/O file, memoria
- input e output (I/O), memoria
- I/O (input e output), memoria
- I/O memoria
- mmioOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472750"
---
# <a name="performing-memory-file-io"></a><span data-ttu-id="37f3d-109">Esecuzione di operazioni di I/O su file di memoria</span><span class="sxs-lookup"><span data-stu-id="37f3d-109">Performing Memory File I/O</span></span>

<span data-ttu-id="37f3d-110">I servizi di I/O dei file multimediali consentono di trattare un blocco di memoria come file.</span><span class="sxs-lookup"><span data-stu-id="37f3d-110">The multimedia file I/O services let you treat a block of memory as a file.</span></span> <span data-ttu-id="37f3d-111">Questa operazione può essere utile se si dispone già di un'immagine del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="37f3d-111">This can be useful if you already have a file image in memory.</span></span> <span data-ttu-id="37f3d-112">I file di memoria consentono di ridurre il numero di condizioni del caso speciale nel codice perché, per finalità di I/O, è possibile considerare i file di memoria come se fossero file basati su disco.</span><span class="sxs-lookup"><span data-stu-id="37f3d-112">Memory files let you reduce the number of special-case conditions in your code because, for I/O purposes, you can treat memory files as if they were disk-based files.</span></span> <span data-ttu-id="37f3d-113">È inoltre possibile utilizzare i file di memoria con gli Appunti.</span><span class="sxs-lookup"><span data-stu-id="37f3d-113">You can also use memory files with the clipboard.</span></span>

<span data-ttu-id="37f3d-114">Come per I buffer di I/O, i file di memoria possono usare la memoria allocata dall'applicazione o dal gestore di I/O file.</span><span class="sxs-lookup"><span data-stu-id="37f3d-114">As with I/O buffers, memory files can use memory allocated by the application or by the file I/O manager.</span></span> <span data-ttu-id="37f3d-115">Inoltre, i file di memoria possono essere espandibili o non espandibili.</span><span class="sxs-lookup"><span data-stu-id="37f3d-115">In addition, memory files can be either expandable or nonexpandable.</span></span> <span data-ttu-id="37f3d-116">Quando il gestore di I/O dei file raggiunge la fine di un file di memoria espandibile, espande il file di memoria in base a un incremento predefinito.</span><span class="sxs-lookup"><span data-stu-id="37f3d-116">When the file I/O manager reaches the end of an expandable memory file, it expands the memory file by a predefined increment.</span></span>

<span data-ttu-id="37f3d-117">Per aprire un file di memoria, usare la funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) con il parametro *SzFilename* impostato su **null** e il \_ flag MMIO ReadWrite impostato nel parametro *dwOpenFlags* .</span><span class="sxs-lookup"><span data-stu-id="37f3d-117">To open a memory file, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function with the *szFilename* parameter set to **NULL** and the MMIO\_READWRITE flag set in the *dwOpenFlags* parameter.</span></span> <span data-ttu-id="37f3d-118">Impostare il parametro *lpmmioinfo* in modo che punti a una struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) configurata nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="37f3d-118">Set the *lpmmioinfo* parameter to point to an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure that has been set up as follows:</span></span>

1.  <span data-ttu-id="37f3d-119">Impostare il membro **pIOProc** su **null**.</span><span class="sxs-lookup"><span data-stu-id="37f3d-119">Set the **pIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="37f3d-120">Impostare il membro **fccIOProc** su FourCC \_ MEM.</span><span class="sxs-lookup"><span data-stu-id="37f3d-120">Set the **fccIOProc** member to FOURCC\_MEM.</span></span>
3.  <span data-ttu-id="37f3d-121">Impostare il membro **pchBuffer** in modo che punti al blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="37f3d-121">Set the **pchBuffer** member to point to the memory block.</span></span> <span data-ttu-id="37f3d-122">Per richiedere al gestore di I/O dei file di allocare il blocco di memoria, impostare **pchBuffer** su **null**.</span><span class="sxs-lookup"><span data-stu-id="37f3d-122">To request that the file I/O manager allocate the memory block, set **pchBuffer** to **NULL**.</span></span>
4.  <span data-ttu-id="37f3d-123">Impostare il membro **cchBuffer** sulle dimensioni iniziali del blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="37f3d-123">Set the **cchBuffer** member to the initial size of the memory block.</span></span>
5.  <span data-ttu-id="37f3d-124">Impostare il membro **adwInfo** sulle dimensioni di espansione minime del blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="37f3d-124">Set the **adwInfo** member to the minimum expansion size of the memory block.</span></span> <span data-ttu-id="37f3d-125">Per un file di memoria non espandibile, impostare **adwInfo** su **null**.</span><span class="sxs-lookup"><span data-stu-id="37f3d-125">For a nonexpandable memory file, set **adwInfo** to **NULL**.</span></span>
6.  <span data-ttu-id="37f3d-126">Impostare tutti gli altri membri su zero.</span><span class="sxs-lookup"><span data-stu-id="37f3d-126">Set all other members to zero.</span></span>

<span data-ttu-id="37f3d-127">Non sono previste restrizioni per l'allocazione della memoria da utilizzare come file di memoria non espandibile.</span><span class="sxs-lookup"><span data-stu-id="37f3d-127">There are no restrictions on allocating memory for use as a nonexpandable memory file.</span></span>

 

 