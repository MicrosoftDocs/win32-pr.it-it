---
description: Gestire directory con la tabella voce di directory, gli handle di directory e i reparse point.
title: File system locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755159"
---
# <a name="local-file-systems"></a><span data-ttu-id="2836c-103">File system locali</span><span class="sxs-lookup"><span data-stu-id="2836c-103">Local File Systems</span></span>

<span data-ttu-id="2836c-104">Un *file System* consente alle applicazioni di archiviare e recuperare file nei dispositivi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2836c-104">A *file system* enables applications to store and retrieve files on storage devices.</span></span> <span data-ttu-id="2836c-105">I file vengono inseriti in una struttura gerarchica.</span><span class="sxs-lookup"><span data-stu-id="2836c-105">Files are placed in a hierarchical structure.</span></span> <span data-ttu-id="2836c-106">Il file system specifica le convenzioni di denominazione per i file e il formato per specificare il percorso di un file nella struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="2836c-106">The file system specifies naming conventions for files and the format for specifying the path to a file in the tree structure.</span></span>

<span data-ttu-id="2836c-107">Ogni file system è costituita da uno o più driver e librerie a collegamento dinamico che definiscono i formati di dati e le funzionalità del file system.</span><span class="sxs-lookup"><span data-stu-id="2836c-107">Each file system consists of one or more drivers and dynamic-link libraries that define the data formats and features of the file system.</span></span> <span data-ttu-id="2836c-108">I file System possono esistere in molti tipi diversi di dispositivi di archiviazione, tra cui dischi rigidi, jukebox, dischi ottici rimovibili, unità di backup su nastro e schede di memoria.</span><span class="sxs-lookup"><span data-stu-id="2836c-108">File systems can exist on many different types of storage devices, including hard disks, jukeboxes, removable optical disks, tape back-up units, and memory cards.</span></span>

<span data-ttu-id="2836c-109">Per tutti i file system supportati da Windows sono disponibili i componenti di archiviazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="2836c-109">All file systems supported by Windows have the following storage components:</span></span>

-   <span data-ttu-id="2836c-110">Volumi.</span><span class="sxs-lookup"><span data-stu-id="2836c-110">Volumes.</span></span> <span data-ttu-id="2836c-111">Un *volume* è una raccolta di directory e file.</span><span class="sxs-lookup"><span data-stu-id="2836c-111">A *volume* is a collection of directories and files.</span></span>
-   <span data-ttu-id="2836c-112">Directory.</span><span class="sxs-lookup"><span data-stu-id="2836c-112">Directories.</span></span> <span data-ttu-id="2836c-113">Una *directory* è una raccolta gerarchica di directory e file.</span><span class="sxs-lookup"><span data-stu-id="2836c-113">A *directory* is a hierarchical collection of directories and files.</span></span>
-   <span data-ttu-id="2836c-114">File</span><span class="sxs-lookup"><span data-stu-id="2836c-114">Files.</span></span> <span data-ttu-id="2836c-115">Un *file* è un raggruppamento logico di dati correlati.</span><span class="sxs-lookup"><span data-stu-id="2836c-115">A *file* is a logical grouping of related data.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2836c-116">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="2836c-116">In this section</span></span>



| <span data-ttu-id="2836c-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="2836c-117">Topic</span></span>                                                                | <span data-ttu-id="2836c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2836c-118">Description</span></span>                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2836c-119">Gestione directory</span><span class="sxs-lookup"><span data-stu-id="2836c-119">Directory Management</span></span>](directory-management.md)<br/>          | <span data-ttu-id="2836c-120">Una *directory* è una raccolta gerarchica di directory e file.</span><span class="sxs-lookup"><span data-stu-id="2836c-120">A *directory* is a hierarchical collection of directories and files.</span></span> <span data-ttu-id="2836c-121">L'unico vincolo sul numero di file che possono essere contenuti in una singola directory è la dimensione fisica del disco in cui si trova la directory.</span><span class="sxs-lookup"><span data-stu-id="2836c-121">The only constraint on the number of files that can be contained in a single directory is the physical size of the disk on which the directory is located.</span></span><br/> |
| [<span data-ttu-id="2836c-122">Gestione disco</span><span class="sxs-lookup"><span data-stu-id="2836c-122">Disk Management</span></span>](disk-management.md)<br/>                    | <span data-ttu-id="2836c-123">Un *disco rigido* è un disco rigido all'interno di un computer che archivia e fornisce accesso relativamente rapido a grandi quantità di dati.</span><span class="sxs-lookup"><span data-stu-id="2836c-123">A *hard disk* is a rigid disk inside a computer that stores and provides relatively quick access to large amounts of data.</span></span> <span data-ttu-id="2836c-124">Si tratta del tipo di archiviazione usato più di frequente con Windows.</span><span class="sxs-lookup"><span data-stu-id="2836c-124">It is the type of storage most often used with Windows.</span></span> <span data-ttu-id="2836c-125">Il sistema supporta inoltre supporti rimovibili.</span><span class="sxs-lookup"><span data-stu-id="2836c-125">The system also supports removable media.</span></span><br/>    |
| [<span data-ttu-id="2836c-126">Gestione dei file</span><span class="sxs-lookup"><span data-stu-id="2836c-126">File Management</span></span>](file-management.md)<br/>                    | <span data-ttu-id="2836c-127">Un *oggetto file* fornisce una rappresentazione di una risorsa, ovvero un dispositivo fisico o una risorsa che si trova in un dispositivo fisico, che può essere gestita dal sistema i/O.</span><span class="sxs-lookup"><span data-stu-id="2836c-127">A *file object* provides a representation of a resource (either a physical device or a resource located on a physical device) that can be managed by the I/O system.</span></span><br/>                                                            |
| [<span data-ttu-id="2836c-128">Transactional NTFS (TxF)</span><span class="sxs-lookup"><span data-stu-id="2836c-128">Transactional NTFS (TxF)</span></span>](transactional-ntfs-portal.md)<br/> | <span data-ttu-id="2836c-129">Transactional NTFS (TxF) consente di eseguire operazioni su file su un volume file system NTFS in una transazione.</span><span class="sxs-lookup"><span data-stu-id="2836c-129">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="2836c-130">Gestione dei volumi</span><span class="sxs-lookup"><span data-stu-id="2836c-130">Volume Management</span></span>](volume-management.md)<br/>                | <span data-ttu-id="2836c-131">Il livello più elevato di organizzazione nella file system è il *volume*.</span><span class="sxs-lookup"><span data-stu-id="2836c-131">The highest level of organization in the file system is the *volume*.</span></span> <span data-ttu-id="2836c-132">Un file system risiede in un volume.</span><span class="sxs-lookup"><span data-stu-id="2836c-132">A file system resides on a volume.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="2836c-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2836c-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2836c-134">[Riferimento tecnico FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2836c-134">[FAT Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="2836c-135">[Tecnologie per file System](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2836c-135">[File Systems Technologies](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="2836c-136">[Riferimento tecnico per NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2836c-136">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

