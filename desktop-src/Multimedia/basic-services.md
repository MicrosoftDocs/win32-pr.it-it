---
title: Servizi di base
description: Servizi di base
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- I/O file multimediale, servizi di base
- I/O di file, servizi di base
- input e output (I/O), servizi di base
- I/O (input e output), servizi di base
- I/O di base
- mmioOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398986"
---
# <a name="basic-services"></a><span data-ttu-id="d535e-109">Servizi di base</span><span class="sxs-lookup"><span data-stu-id="d535e-109">Basic Services</span></span>

<span data-ttu-id="d535e-110">L'utilizzo dei servizi di I/O di base è simile all'utilizzo dei servizi di I/O dei file di runtime della libreria di runtime del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="d535e-110">Using the basic I/O services is similar to using the run-time file I/O services of the C run-time library.</span></span> <span data-ttu-id="d535e-111">Per poter essere letti o scritti, è necessario aprire i file.</span><span class="sxs-lookup"><span data-stu-id="d535e-111">Files must be opened before they can be read or written.</span></span> <span data-ttu-id="d535e-112">Dopo la lettura o la scrittura, il file deve essere chiuso.</span><span class="sxs-lookup"><span data-stu-id="d535e-112">After reading or writing, the file must be closed.</span></span> <span data-ttu-id="d535e-113">È anche possibile modificare il percorso di lettura o scrittura corrente all'interno di un file aperto.</span><span class="sxs-lookup"><span data-stu-id="d535e-113">You can also change the current read or write location within an open file.</span></span>

<span data-ttu-id="d535e-114">Prima di iniziare qualsiasi operazione di I/O in un file, è necessario aprire il file utilizzando la funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="d535e-114">Before you begin any I/O operations to a file, you must open the file by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="d535e-115">Questa funzione restituisce un handle di file di tipo **HMMIO**.</span><span class="sxs-lookup"><span data-stu-id="d535e-115">This function returns a file handle of type **HMMIO**.</span></span> <span data-ttu-id="d535e-116">È possibile utilizzare questo handle di file per identificare il file aperto quando si chiamano altre funzioni di I/O di file.</span><span class="sxs-lookup"><span data-stu-id="d535e-116">You can use this file handle to identify the open file when calling other file I/O functions.</span></span>

> [!Note]  
> <span data-ttu-id="d535e-117">Un handle di file **HMMIO** non è un handle di file standard.</span><span class="sxs-lookup"><span data-stu-id="d535e-117">An **HMMIO** file handle is not a standard file handle.</span></span> <span data-ttu-id="d535e-118">Non usare gli handle di file **HMMIO** con le funzioni di I/O dei file di runtime Win32 o C.</span><span class="sxs-lookup"><span data-stu-id="d535e-118">Do not use **HMMIO** file handles with Win32 or C run-time file I/O functions.</span></span>

 

<span data-ttu-id="d535e-119">Quando si usa [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) per aprire un file, si usa un flag per specificare se si sta aprendo per la lettura, la scrittura o entrambi.</span><span class="sxs-lookup"><span data-stu-id="d535e-119">When you use [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) to open a file, you use a flag to specify whether you are opening it for reading, writing, or both.</span></span> <span data-ttu-id="d535e-120">È inoltre possibile specificare i flag che consentono di creare o eliminare un file.</span><span class="sxs-lookup"><span data-stu-id="d535e-120">You can also specify flags that enable you to create or delete a file.</span></span> <span data-ttu-id="d535e-121">Utilizzare la funzione [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) per chiudere un file al termine della lettura o della scrittura.</span><span class="sxs-lookup"><span data-stu-id="d535e-121">Use the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to close a file when you are finished reading or writing to it.</span></span>

<span data-ttu-id="d535e-122">È possibile leggere e scrivere file usando rispettivamente le funzioni [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) e [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) .</span><span class="sxs-lookup"><span data-stu-id="d535e-122">You can read and write files by using the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) and [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) functions respectively.</span></span> <span data-ttu-id="d535e-123">La successiva operazione di lettura o scrittura si verifica in corrispondenza della posizione corrente del file o del puntatore del file in un file.</span><span class="sxs-lookup"><span data-stu-id="d535e-123">The next read or write operation occurs at the current file position or file pointer in a file.</span></span> <span data-ttu-id="d535e-124">La posizione del file corrente è avanzata ogni volta che un file viene letto o scritto.</span><span class="sxs-lookup"><span data-stu-id="d535e-124">The current file position is advanced each time a file is read or written.</span></span>

<span data-ttu-id="d535e-125">È anche possibile modificare la posizione del file corrente usando la funzione [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .</span><span class="sxs-lookup"><span data-stu-id="d535e-125">You can also change the current file position by using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span> <span data-ttu-id="d535e-126">È necessario assicurarsi di specificare un percorso valido in un file.</span><span class="sxs-lookup"><span data-stu-id="d535e-126">You should ensure that you specify a valid location in a file.</span></span> <span data-ttu-id="d535e-127">Se si specifica un percorso non valido, ad esempio dopo la fine del file, **mmioSeek** potrebbe non restituire un errore, ma le operazioni di I/O successive potrebbero non riuscire.</span><span class="sxs-lookup"><span data-stu-id="d535e-127">If you specify an invalid location, such as past the end of the file, **mmioSeek** may not return an error, but subsequent I/O operations could fail.</span></span>

<span data-ttu-id="d535e-128">Sono disponibili flag che è possibile usare con la funzione **mmioOpen** per le operazioni successive all'i/O di file di base.</span><span class="sxs-lookup"><span data-stu-id="d535e-128">There are flags you can use with the **mmioOpen** function for operations beyond basic file I/O.</span></span> <span data-ttu-id="d535e-129">Specificando una struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) , ad esempio, è possibile aprire file di memoria, specificare una routine di i/o personalizzata o fornire un buffer per i/o memorizzato nel buffer.</span><span class="sxs-lookup"><span data-stu-id="d535e-129">By specifying an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure, for example, you can open memory files, specify a custom I/O procedure, or supply a buffer for buffered I/O.</span></span>

 

 