---
description: La compressione dei file che contengono principalmente zeri consente un uso efficiente dello spazio su disco.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: File sparse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c282ca89c9dc9e44800a2a7fc969c3f883006b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307932"
---
# <a name="sparse-files"></a><span data-ttu-id="13038-103">File sparse</span><span class="sxs-lookup"><span data-stu-id="13038-103">Sparse Files</span></span>

<span data-ttu-id="13038-104">Un file in cui la maggior parte dei dati è pari a zero viene detto che contiene un *set di dati di tipo sparse*.</span><span class="sxs-lookup"><span data-stu-id="13038-104">A file in which much of the data is zeros is said to contain a *sparse data set*.</span></span> <span data-ttu-id="13038-105">File come questi sono in genere molto grandi, ad esempio, un file che contiene i dati dell'immagine da elaborare o una matrice all'interno di un database ad alta velocità.</span><span class="sxs-lookup"><span data-stu-id="13038-105">Files like these are typically very large for example, a file that contains image data to be processed or a matrix within a high-speed database.</span></span> <span data-ttu-id="13038-106">Il problema con i file che contengono set di dati di tipo sparse è che la maggior parte del file non contiene dati utili e, per questo motivo, rappresentano un uso inefficiente dello spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="13038-106">The problem with files that contain sparse data sets is that the majority of the file does not contain useful data and, because of this, they are an inefficient use of disk space.</span></span>

<span data-ttu-id="13038-107">La compressione dei file nel file system NTFS è una soluzione parziale al problema.</span><span class="sxs-lookup"><span data-stu-id="13038-107">The file compression in the NTFS file system is a partial solution to the problem.</span></span> <span data-ttu-id="13038-108">Tutti i dati del file non scritti in modo esplicito vengono impostati in modo esplicito su zero.</span><span class="sxs-lookup"><span data-stu-id="13038-108">All data in the file that is not explicitly written is explicitly set to zero.</span></span> <span data-ttu-id="13038-109">Compressione file compatta questi intervalli di zeri.</span><span class="sxs-lookup"><span data-stu-id="13038-109">File compression compacts these ranges of zeros.</span></span> <span data-ttu-id="13038-110">Tuttavia, uno svantaggio della compressione dei file è che il tempo di accesso può aumentare a causa della compressione e della decompressione dei dati.</span><span class="sxs-lookup"><span data-stu-id="13038-110">However, a drawback of file compression is that access time may increase due to data compression and decompression.</span></span>

<span data-ttu-id="13038-111">Il supporto per i file sparse è stato introdotto nel file system NTFS come un altro modo per rendere più efficiente l'utilizzo dello spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="13038-111">Support for sparse files is introduced in the NTFS file system as another way to make disk space usage more efficient.</span></span> <span data-ttu-id="13038-112">Quando è abilitata la funzionalità file sparse, il sistema non alloca lo spazio su disco rigido a un file, tranne nelle aree in cui contiene dati diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="13038-112">When sparse file functionality is enabled, the system does not allocate hard disk drive space to a file except in regions where it contains nonzero data.</span></span> <span data-ttu-id="13038-113">Quando si tenta di eseguire un'operazione di scrittura in cui una grande quantità di dati nel buffer è pari a zero, gli zeri non vengono scritti nel file.</span><span class="sxs-lookup"><span data-stu-id="13038-113">When a write operation is attempted where a large amount of the data in the buffer is zeros, the zeros are not written to the file.</span></span> <span data-ttu-id="13038-114">Il file system crea invece un elenco interno contenente le posizioni degli zeri nel file e questo elenco viene consultato durante tutte le operazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="13038-114">Instead, the file system creates an internal list containing the locations of the zeros in the file, and this list is consulted during all read operations.</span></span> <span data-ttu-id="13038-115">Quando viene eseguita un'operazione di lettura in aree del file in cui sono stati individuati zeri, il file system restituisce il numero appropriato di zeri nel buffer allocato per l'operazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="13038-115">When a read operation is performed in areas of the file where zeros were located, the file system returns the appropriate number of zeros in the buffer allocated for the read operation.</span></span> <span data-ttu-id="13038-116">In questo modo, la manutenzione del file sparse è trasparente per tutti i processi che vi accedono ed è più efficiente della compressione per questo particolare scenario.</span><span class="sxs-lookup"><span data-stu-id="13038-116">In this way, maintenance of the sparse file is transparent to all processes that access it, and is more efficient than compression for this particular scenario.</span></span>

<span data-ttu-id="13038-117">Il valore di dati predefinito di un file sparse è zero; Tuttavia, può essere impostato su altri valori.</span><span class="sxs-lookup"><span data-stu-id="13038-117">The default data value of a sparse file is zero; however, it can be set to other values.</span></span>

<span data-ttu-id="13038-118">Per ulteriori informazioni sui file sparse, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="13038-118">For more information about sparse files, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="13038-119">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="13038-119">In this section</span></span>



| <span data-ttu-id="13038-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="13038-120">Topic</span></span>                                                                                     | <span data-ttu-id="13038-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13038-121">Description</span></span>                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13038-122">Operazioni su file sparse</span><span class="sxs-lookup"><span data-stu-id="13038-122">Sparse File Operations</span></span>](sparse-file-operations.md)<br/>                           | <span data-ttu-id="13038-123">Determinare se un file system supporta i file sparse chiamando la funzione GetVolumeInformation.</span><span class="sxs-lookup"><span data-stu-id="13038-123">Determine whether a file system supports sparse files by calling the GetVolumeInformation function.</span></span><br/>                                                                                |
| [<span data-ttu-id="13038-124">Recupero delle dimensioni di un file sparse</span><span class="sxs-lookup"><span data-stu-id="13038-124">Obtaining the Size of a Sparse File</span></span>](obtaining-the-size-of-a-sparse-file.md)<br/> | <span data-ttu-id="13038-125">Ottenere la dimensione allocata o la dimensione totale per un file usando la funzione [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) o [**Filesize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) .</span><span class="sxs-lookup"><span data-stu-id="13038-125">Get the allocated size or the total size for a file by using either the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) or the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function.</span></span><br/> |
| [<span data-ttu-id="13038-126">File sparse e quote disco</span><span class="sxs-lookup"><span data-stu-id="13038-126">Sparse Files and Disk Quotas</span></span>](sparse-files-and-disk-quota.md)<br/>                | <span data-ttu-id="13038-127">Un file sparse influiscono sulle quote utente in base alle dimensioni nominali del file, non alla quantità effettiva di spazio su disco allocata.</span><span class="sxs-lookup"><span data-stu-id="13038-127">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span><br/>                                                                  |



 

 

 




