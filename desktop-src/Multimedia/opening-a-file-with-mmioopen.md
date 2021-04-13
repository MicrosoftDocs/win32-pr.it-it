---
title: Apertura di un file con mmioOpen
description: Apertura di un file con mmioOpen
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- I/O file multimediale, apertura di file
- I/O di file, apertura di file
- input e output (I/O), apertura di file
- I/O (input e output), apertura di file
- I/O file multimediale, funzione mmioOpen
- I/O di file, funzione mmioOpen
- input e output (I/O), funzione mmioOpen
- I/O (input e output), funzione mmioOpen
- mmioOpen (funzione)
- apertura dei file di I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2123b73c5f3a93cbb6e72711a7137652f7534b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473070"
---
# <a name="opening-a-file-with-mmioopen"></a><span data-ttu-id="0a60f-113">Apertura di un file con mmioOpen</span><span class="sxs-lookup"><span data-stu-id="0a60f-113">Opening a File with mmioOpen</span></span>

<span data-ttu-id="0a60f-114">Per aprire un file per le operazioni di I/O di base, impostare il parametro *lpmmioinfo* della funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) su **null**.</span><span class="sxs-lookup"><span data-stu-id="0a60f-114">To open a file for basic I/O operations, set the *lpmmioinfo* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to **NULL**.</span></span> <span data-ttu-id="0a60f-115">Nell'esempio seguente viene aperto un file denominato "C: \\ samples \\SAMPLE1.TXT" per la lettura e viene verificato il valore restituito per Error.</span><span class="sxs-lookup"><span data-stu-id="0a60f-115">The following example opens a file named "C:\\SAMPLES\\SAMPLE1.TXT" for reading, and checks the return value for error.</span></span>


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



<span data-ttu-id="0a60f-116">Usare il parametro *dwFlags* di **mmioOpen** per specificare i flag per l'apertura di un file.</span><span class="sxs-lookup"><span data-stu-id="0a60f-116">Use the *dwFlags* parameter of **mmioOpen** to specify flags for opening a file.</span></span>

 

 