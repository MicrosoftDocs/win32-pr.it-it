---
title: Creazione ed eliminazione di un file
description: Creazione ed eliminazione di un file
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- I/O file multimediale, creazione di file
- I/O di file, creazione di file
- input e output (I/O), creazione di file
- I/O (input e output), creazione di file
- creazione di file di I/O
- I/O file multimediale, eliminazione di file
- I/O di file, eliminazione di file
- input e output (I/O), eliminazione di file
- I/O (input e output), eliminazione di file
- eliminazione dei file di I/O
- mmioOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725370"
---
# <a name="creating-and-deleting-a-file"></a><span data-ttu-id="ff4b1-114">Creazione ed eliminazione di un file</span><span class="sxs-lookup"><span data-stu-id="ff4b1-114">Creating and Deleting a File</span></span>

<span data-ttu-id="ff4b1-115">Per creare un file, impostare il parametro *dwOpenFlags* della funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) su MMIO \_ create.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-115">To create a file, set the *dwOpenFlags* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to MMIO\_CREATE.</span></span> <span data-ttu-id="ff4b1-116">Nell'esempio seguente viene creato un file che viene aperto per la lettura e la scrittura.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-116">The following example creates a file and opens it for reading and writing.</span></span>


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



<span data-ttu-id="ff4b1-117">Se il file che si sta creando esiste già, verrà troncato con una lunghezza pari a zero.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-117">If the file you are creating already exists, it will be truncated to zero length.</span></span>

<span data-ttu-id="ff4b1-118">Per eliminare un file, impostare il parametro *dwOpenFlags* della funzione **mmioOpen** su MMIO \_ Delete.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-118">To delete a file, set the *dwOpenFlags* parameter of the **mmioOpen** function to MMIO\_DELETE.</span></span> <span data-ttu-id="ff4b1-119">Dopo aver eliminato un file, non è possibile recuperarlo con alcun mezzo standard.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-119">After you delete a file, it cannot be recovered by any standard means.</span></span> <span data-ttu-id="ff4b1-120">Se l'applicazione sta eliminando un file alla richiesta di un utente, eseguire una query sull'utente prima di eliminare il file per assicurarsi che l'utente voglia eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-120">If your application is deleting a file at the request of a user, query the user before deleting the file to make sure the user wants to delete it.</span></span>

 

 