---
title: Servizi personalizzati
description: Servizi personalizzati
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- I/O di file multimediali, servizi personalizzati
- I/O di file, servizi personalizzati
- input e output (I/O), servizi personalizzati
- I/O (input e output), servizi personalizzati
- I/O personalizzato
- mmioInstallIOProc (funzione)
- mmioOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046697"
---
# <a name="custom-services"></a><span data-ttu-id="18378-110">Servizi personalizzati</span><span class="sxs-lookup"><span data-stu-id="18378-110">Custom Services</span></span>

<span data-ttu-id="18378-111">I servizi di I/O dei file multimediali usano le procedure di I/O per gestire l'input fisico e l'output associato alla lettura e alla scrittura in diversi tipi di sistemi di archiviazione, ad esempio sistemi di archiviazione di file e sistemi di archiviazione di database.</span><span class="sxs-lookup"><span data-stu-id="18378-111">Multimedia file I/O services use I/O procedures to handle the physical input and output associated with reading and writing to different types of storage systems, such as file-archival systems and database-storage systems.</span></span> <span data-ttu-id="18378-112">Per i file System standard e per i file di memoria sono disponibili procedure di I/O predefinite, ma è possibile fornire una procedura di I/O personalizzata per accedere a un sistema di archiviazione univoco tramite la funzione [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) .</span><span class="sxs-lookup"><span data-stu-id="18378-112">Predefined I/O procedures exist for the standard file systems and for memory files, but you can supply a custom I/O procedure for accessing a unique storage system by using the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function.</span></span>

<span data-ttu-id="18378-113">Per aprire un file usando una routine di I/O personalizzata, usare la funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="18378-113">To open a file by using a custom I/O procedure, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="18378-114">Includere un segno più (+) o la costante CFSEPCHAR nel nome file per separare il nome del file fisico dal nome dell'elemento del file che si vuole aprire.</span><span class="sxs-lookup"><span data-stu-id="18378-114">Include a plus sign (+) or the CFSEPCHAR constant in the filename to separate the name of the physical file from the name of the element of the file you want to open.</span></span> <span data-ttu-id="18378-115">Nell'esempio seguente viene aperto un elemento file denominato "element" da un file denominato FILENAME. ARCO</span><span class="sxs-lookup"><span data-stu-id="18378-115">The following example opens a file element named "element" from a file named FILENAME.ARC:</span></span>


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



<span data-ttu-id="18378-116">Quando il gestore di I/O dei file rileva un segno più in un nome di file, esamina l'estensione del nome file per determinare quale procedura di I/O associare al file.</span><span class="sxs-lookup"><span data-stu-id="18378-116">When the file I/O manager encounters a plus sign in a filename, it examines the filename extension to determine which I/O procedure to associate with the file.</span></span> <span data-ttu-id="18378-117">Nell'esempio precedente, il gestore di I/O dei file tenterà di utilizzare la procedura di I/O associata a. Estensione del nome file ARC; Questa procedura di I/O sarebbe stata installata usando [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span><span class="sxs-lookup"><span data-stu-id="18378-117">In the previous example, the file I/O manager would attempt to use the I/O procedure associated with the .ARC filename extension; this I/O procedure would have been installed by using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span></span> <span data-ttu-id="18378-118">Se non è installata alcuna routine di I/O, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="18378-118">If no I/O procedure is installed, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) returns an error.</span></span>

<span data-ttu-id="18378-119">Le procedure di i/O devono rispondere ai messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="18378-119">I/O procedures must respond to the following messages:</span></span>

-   [<span data-ttu-id="18378-120">**chiusura di MMIOM \_**</span><span class="sxs-lookup"><span data-stu-id="18378-120">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="18378-121">**MMIOM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="18378-121">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="18378-122">**MMIOM di \_ lettura**</span><span class="sxs-lookup"><span data-stu-id="18378-122">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="18378-123">**\_scrittura MMIOM**</span><span class="sxs-lookup"><span data-stu-id="18378-123">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="18378-124">**MMIOM \_ Seek**</span><span class="sxs-lookup"><span data-stu-id="18378-124">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="18378-125">**ridenominazione MMIOM \_**</span><span class="sxs-lookup"><span data-stu-id="18378-125">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="18378-126">**\_WRITEFLUSH MMIOM**</span><span class="sxs-lookup"><span data-stu-id="18378-126">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)

<span data-ttu-id="18378-127">È anche possibile creare messaggi personalizzati e inviarli alla routine di I/O tramite la funzione [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) .</span><span class="sxs-lookup"><span data-stu-id="18378-127">You can also create custom messages and send them to your I/O procedure by using the [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) function.</span></span> <span data-ttu-id="18378-128">Se si definiscono messaggi personalizzati, assicurarsi che siano definiti in corrispondenza o superiore al valore definito dalla \_ costante utente MMIOM.</span><span class="sxs-lookup"><span data-stu-id="18378-128">If you define your own messages, make sure they are defined at or above the value defined by the MMIOM\_USER constant.</span></span>

<span data-ttu-id="18378-129">Oltre all'elaborazione dei messaggi, una routine di I/O deve mantenere il membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) (a cui fa riferimento il parametro *lpmmioinfo* della funzione **mmioOpen** ).</span><span class="sxs-lookup"><span data-stu-id="18378-129">In addition to processing messages, an I/O procedure must maintain the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure (pointed to by the *lpmmioinfo* parameter of the **mmioOpen** function).</span></span> <span data-ttu-id="18378-130">Il membro **lDiskOffset** deve sempre contenere l'offset del file nel percorso a cui avrà accesso il successivo messaggio di scrittura MMIOM di \_ lettura o MMIOM \_ .</span><span class="sxs-lookup"><span data-stu-id="18378-130">The **lDiskOffset** member must always contain the file offset to the location that the next MMIOM\_READ or MMIOM\_WRITE message will access.</span></span> <span data-ttu-id="18378-131">L'offset viene specificato in byte ed è relativo all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="18378-131">The offset is specified in bytes and is relative to the beginning of the file.</span></span> <span data-ttu-id="18378-132">La procedura di I/O può utilizzare il membro **adwInfo** per mantenere le informazioni sullo stato richieste.</span><span class="sxs-lookup"><span data-stu-id="18378-132">The I/O procedure can use the **adwInfo** member to maintain any required state information.</span></span> <span data-ttu-id="18378-133">La procedura di I/O non deve modificare altri membri nella struttura **MMIOINFO** .</span><span class="sxs-lookup"><span data-stu-id="18378-133">The I/O procedure should not modify any other members in the **MMIOINFO** structure.</span></span>

 

 