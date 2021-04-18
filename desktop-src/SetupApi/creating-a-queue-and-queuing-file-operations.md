---
description: L'accodamento delle operazioni dei file è utile perché consente di elaborare l'intera installazione, anziché tramite la sezione INF.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Creazione di una coda e operazioni di Accodamento di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313706"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a><span data-ttu-id="4e7c2-103">Creazione di una coda e operazioni di Accodamento di file</span><span class="sxs-lookup"><span data-stu-id="4e7c2-103">Creating a Queue and Queuing File Operations</span></span>

<span data-ttu-id="4e7c2-104">L'accodamento delle operazioni dei file è utile perché consente di elaborare l'intera installazione, anziché tramite la sezione INF.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-104">Queuing the file operations is useful because it enables you to process the installation as a whole, instead of by INF section.</span></span>

<span data-ttu-id="4e7c2-105">Per creare una coda di file, dichiarare una variabile per archiviare l'handle della coda, quindi chiamare la funzione [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) .</span><span class="sxs-lookup"><span data-stu-id="4e7c2-105">To create a file queue, declare a variable to store the queue handle, then call the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function.</span></span> <span data-ttu-id="4e7c2-106">Dopo la creazione della coda, è possibile accodare le operazioni di copia, ridenominazione ed eliminazione, nonché analizzare la coda dei file per verificare le operazioni accodate.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-106">After the queue is created, you can queue copy, rename, and delete operations, as well as scan the file queue to verify enqueued operations.</span></span>

<span data-ttu-id="4e7c2-107">Per aggiungere singole operazioni su file alla coda, usare le funzioni [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)e [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) .</span><span class="sxs-lookup"><span data-stu-id="4e7c2-107">To add single file operations to the queue, use the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea), and [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) functions.</span></span>

<span data-ttu-id="4e7c2-108">Tutte le operazioni sui file elencate nella sezione **copiare file**, **eliminare file** o **rinominare file** possono essere aggiunte alla coda usando rispettivamente [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)o [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span><span class="sxs-lookup"><span data-stu-id="4e7c2-108">All the file operations listed in a **Copy Files**, **Delete Files**, or **Rename Files** section can be added to the queue by using [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona), or [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectively.</span></span>

<span data-ttu-id="4e7c2-109">Un altro modo per accodare tutti i file nelle sezioni **copia file** elencati in una sezione di **installazione** di un file inf consiste nell'usare la funzione [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span><span class="sxs-lookup"><span data-stu-id="4e7c2-109">Another way to queue all the files in the **Copy Files** sections listed in an **Install** section of an INF is to use the function, [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span></span>

<span data-ttu-id="4e7c2-110">Nell'esempio seguente viene usata la funzione [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) per accodare le operazioni di copia per tutti i file elencati in una sezione **copy files** di un file inf.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-110">The following example uses the [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) function to enqueue copy operations for all the files listed in a **Copy Files** section of an INF file.</span></span>

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

<span data-ttu-id="4e7c2-111">Nell'esempio, la coda è la coda a cui aggiungere le operazioni di copia, "A: \\ " specifica il percorso dell'origine e MyInf è l'handle per il file inf aperto.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-111">In the example, MyQueue is the queue to add copy operations to, "A:\\" specifies the path to the source, and MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="4e7c2-112">Il parametro *ListInfHandle* è impostato su **null**, a indicare che la sezione per la copia si trova in MyInf.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-112">The parameter *ListInfHandle* is set to **NULL**, indicating that the section for copying is in MyInf.</span></span> <span data-ttu-id="4e7c2-113">Section è la sezione in MyInf contenente i file da accodare per la copia.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-113">MySection is the section in MyInf containing the files to queue for copying.</span></span>

<span data-ttu-id="4e7c2-114">I flag SP \_ copy \_ NOSKIP e SP \_ copy \_ nobrows sono stati combinati usando un operatore OR per indicare che all'utente non devono essere offerte opzioni per ignorare o cercare i file se si verificano errori.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-114">The flags SP\_COPY\_NOSKIP and SP\_COPY\_NOBROWSE have been combined using an OR operator to indicate that the user should not be offered options to skip or browse for files if errors occur.</span></span>

 

 



