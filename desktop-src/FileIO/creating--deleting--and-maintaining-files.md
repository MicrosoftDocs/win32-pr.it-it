---
description: Funzioni da utilizzare per creare, eliminare e gestire i file.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Creazione, eliminazione e gestione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317803"
---
# <a name="creating-deleting-and-maintaining-files"></a><span data-ttu-id="4f311-103">Creazione, eliminazione e gestione di file</span><span class="sxs-lookup"><span data-stu-id="4f311-103">Creating, Deleting, and Maintaining Files</span></span>

<span data-ttu-id="4f311-104">Negli argomenti seguenti viene descritto come creare, eliminare e gestire i file.</span><span class="sxs-lookup"><span data-stu-id="4f311-104">The following topics describe how to create, delete, and maintain files.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4f311-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="4f311-105">In this section</span></span>



| <span data-ttu-id="4f311-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="4f311-106">Topic</span></span>                                                                   | <span data-ttu-id="4f311-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f311-107">Description</span></span>                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f311-108">Denominazione di file, percorsi e spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f311-108">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)<br/>     | <span data-ttu-id="4f311-109">Regole, convenzioni e limitazioni dei nomi per i file e le directory, incluse le convenzioni di denominazione, i nomi di file brevi e i nomi di file lunghi, i percorsi completi e i percorsi relativi, il limite massimo per la lunghezza del percorso, i nomi file 8,3 e gli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4f311-109">Rules, conventions, and limitations of names for files and directories, including naming conventions, short file names vs. long file names, fully qualified paths vs. relative paths, maximum path length limitation, 8.3 file names, and namespaces.</span></span><br/>            |
| [<span data-ttu-id="4f311-110">Creazione e apertura di file</span><span class="sxs-lookup"><span data-stu-id="4f311-110">Creating and Opening Files</span></span>](creating-and-opening-files.md)<br/> | <span data-ttu-id="4f311-111">Considerazioni per la creazione o l'apertura di un file tramite la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="4f311-111">Considerations for creating or opening a file by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="4f311-112">Trasferimento e sostituzione di file</span><span class="sxs-lookup"><span data-stu-id="4f311-112">Moving and Replacing Files</span></span>](moving-and-replacing-files.md)<br/> | <span data-ttu-id="4f311-113">Considerazioni per lo spostamento e la sostituzione dei file tramite le funzioni CopyFileEx, CreateFile, ReplaceFile e MoveFileEx.</span><span class="sxs-lookup"><span data-stu-id="4f311-113">Considerations for moving and replacing files by using the CopyFileEx, CreateFile, Replacefile, and MoveFileEx functions.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="4f311-114">Chiusura ed eliminazione di file</span><span class="sxs-lookup"><span data-stu-id="4f311-114">Closing and Deleting Files</span></span>](closing-and-deleting-files.md)<br/> | <span data-ttu-id="4f311-115">Per utilizzare in modo efficiente le risorse del sistema operativo, un'applicazione deve chiudere i file quando non sono più necessari tramite la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="4f311-115">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="4f311-116">Se un file è aperto al termine di un'applicazione, il sistema lo chiude automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4f311-116">If a file is open when an application terminates, the system closes it automatically.</span></span><br/> |
| [<span data-ttu-id="4f311-117">Deframmentazione di file</span><span class="sxs-lookup"><span data-stu-id="4f311-117">Defragmenting Files</span></span>](defragmenting-files.md)<br/>               | <span data-ttu-id="4f311-118">La *deframmentazione* è il processo di trasferimento di parti di file in un disco per deframmentare i file, ovvero il processo di trasferimento dei cluster di file su un disco per renderli contigui.</span><span class="sxs-lookup"><span data-stu-id="4f311-118">*Defragmentation* is the process of moving portions of files around on a disk to defragment files, that is, the process of moving file clusters on a disk to make them contiguous.</span></span><br/>                                                                               |



 

 

