---
description: Windows archivia i dati nelle operazioni di lettura e scrittura dei file nei buffer di dati gestiti dal sistema per ottimizzare le prestazioni del disco.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Scaricamento di System-Buffered dati di I/O su disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530000"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a><span data-ttu-id="db97e-103">Scaricamento di System-Buffered dati di I/O su disco</span><span class="sxs-lookup"><span data-stu-id="db97e-103">Flushing System-Buffered I/O Data to Disk</span></span>

<span data-ttu-id="db97e-104">Windows archivia i dati nelle operazioni di lettura e scrittura dei file nei buffer di dati gestiti dal sistema per ottimizzare le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="db97e-104">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span> <span data-ttu-id="db97e-105">Quando un'applicazione scrive in un file, il sistema in genere memorizza i dati nel buffer e scrive i dati sul disco a intervalli regolari.</span><span class="sxs-lookup"><span data-stu-id="db97e-105">When an application writes to a file, the system usually buffers the data and writes the data to the disk on a regular basis.</span></span> <span data-ttu-id="db97e-106">Un'applicazione può forzare il sistema operativo a scrivere il contenuto di questi buffer di dati sul disco tramite la funzione [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .</span><span class="sxs-lookup"><span data-stu-id="db97e-106">An application can force the operating system to write the contents of these data buffers to the disk by using the [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) function.</span></span> <span data-ttu-id="db97e-107">In alternativa, un'applicazione può specificare che le operazioni di scrittura devono ignorare il buffer dei dati e scrivere direttamente sul disco impostando il **flag di file senza flag di \_ \_ \_ buffering** quando il file viene creato o aperto utilizzando la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="db97e-107">Alternatively, an application can specify that write operations are to bypass the data buffer and write directly to the disk by setting the **FILE\_FLAG\_NO\_BUFFERING** flag when the file is created or opened using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

<span data-ttu-id="db97e-108">Se sono presenti dati nel buffer interno quando il file viene chiuso, il sistema operativo non scrive automaticamente il contenuto del buffer sul disco prima di chiudere il file.</span><span class="sxs-lookup"><span data-stu-id="db97e-108">If there is data in the internal buffer when the file is closed, the operating system does not automatically write the contents of the buffer to the disk before closing the file.</span></span> <span data-ttu-id="db97e-109">Se l'applicazione non impone al sistema operativo di scrivere il buffer su disco prima di chiudere il file, l'algoritmo di memorizzazione nella cache determina quando viene scritto il buffer.</span><span class="sxs-lookup"><span data-stu-id="db97e-109">If the application does not force the operating system to write the buffer to disk before closing the file, the caching algorithm determines when the buffer is written.</span></span>

> [!Note]  
> <span data-ttu-id="db97e-110">L'accesso a un buffer di dati durante l'utilizzo di un'operazione di lettura o scrittura può danneggiare il buffer.</span><span class="sxs-lookup"><span data-stu-id="db97e-110">Accessing a data buffer while a read or write operation is using it may corrupt the buffer.</span></span> <span data-ttu-id="db97e-111">Le applicazioni non devono leggere, scrivere in, riallocare o liberare il buffer di dati utilizzato da un'operazione di lettura o scrittura fino al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="db97e-111">Applications must not read from, write to, reallocate, or free the data buffer that a read or write operation is using until the operation completes.</span></span>

 

 

 



