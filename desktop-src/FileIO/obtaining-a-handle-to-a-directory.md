---
description: Ogni volta che un processo crea o apre un oggetto directory, riceve un handle per l'oggetto.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Handle di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319067"
---
# <a name="directory-handles"></a><span data-ttu-id="d4dc4-103">Handle di directory</span><span class="sxs-lookup"><span data-stu-id="d4dc4-103">Directory Handles</span></span>

<span data-ttu-id="d4dc4-104">Ogni volta che un processo crea o apre un oggetto directory, riceve un handle per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d4dc4-104">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span>

<span data-ttu-id="d4dc4-105">Per ottenere un handle per una directory esistente, chiamare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il flag del **backup della \_ \_ \_ semantica del flag di file** .</span><span class="sxs-lookup"><span data-stu-id="d4dc4-105">To obtain a handle to an existing directory, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_BACKUP\_SEMANTICS** flag.</span></span>

<span data-ttu-id="d4dc4-106">È possibile passare un handle di directory alle funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="d4dc4-106">You can pass a directory handle to the following functions.</span></span>



| <span data-ttu-id="d4dc4-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="d4dc4-107">Function</span></span>                                                         | <span data-ttu-id="d4dc4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4dc4-108">Description</span></span>                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4dc4-109">**BackupRead**</span><span class="sxs-lookup"><span data-stu-id="d4dc4-109">**BackupRead**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupread)                              | <span data-ttu-id="d4dc4-110">Eseguire il backup di un file o di una directory, incluse le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d4dc4-110">Back up a file or directory, including the security information.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d4dc4-111">**BackupSeek**</span><span class="sxs-lookup"><span data-stu-id="d4dc4-111">**BackupSeek**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | <span data-ttu-id="d4dc4-112">Cerca in futuro in un flusso di dati a cui si accede inizialmente tramite la funzione [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) o [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) .</span><span class="sxs-lookup"><span data-stu-id="d4dc4-112">Seeks forward in a data stream initially accessed by using the [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) or [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) function.</span></span><br/> |
| [<span data-ttu-id="d4dc4-113">**BackupWrite**</span><span class="sxs-lookup"><span data-stu-id="d4dc4-113">**BackupWrite**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | <span data-ttu-id="d4dc4-114">Ripristinare un file o una directory di cui è stato eseguito il backup con [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span><span class="sxs-lookup"><span data-stu-id="d4dc4-114">Restore a file or directory that was backed up using [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span></span><br/>                                                             |
| [<span data-ttu-id="d4dc4-115">**GetFileInformationByHandle**</span><span class="sxs-lookup"><span data-stu-id="d4dc4-115">**GetFileInformationByHandle**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | <span data-ttu-id="d4dc4-116">Recupera le informazioni sui file per il file specificato.</span><span class="sxs-lookup"><span data-stu-id="d4dc4-116">Retrieves file information for the specified file.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="d4dc4-117">**GetFileSize**</span><span class="sxs-lookup"><span data-stu-id="d4dc4-117">**GetFileSize**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | <span data-ttu-id="d4dc4-118">Recupera le dimensioni in byte del file specificato.</span><span class="sxs-lookup"><span data-stu-id="d4dc4-118">Retrieves the size of the specified file, in bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="d4dc4-119">**GetFileTime ha provocato**</span><span class="sxs-lookup"><span data-stu-id="d4dc4-119">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="d4dc4-120">Recupera la data e l'ora di creazione di un file o di una directory, dell'ultimo accesso e dell'Ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="d4dc4-120">Retrieves the date and time that a file or directory was created, last accessed, and last modified.</span></span><br/>                                                   |
| [<span data-ttu-id="d4dc4-121">**Filetype**</span><span class="sxs-lookup"><span data-stu-id="d4dc4-121">**GetFileType**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | <span data-ttu-id="d4dc4-122">Recupera il tipo di file del file specificato.</span><span class="sxs-lookup"><span data-stu-id="d4dc4-122">Retrieves the file type of the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="d4dc4-123">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="d4dc4-123">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | <span data-ttu-id="d4dc4-124">Recupera le informazioni che descrivono le modifiche all'interno della directory specificata.</span><span class="sxs-lookup"><span data-stu-id="d4dc4-124">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                      |
| [<span data-ttu-id="d4dc4-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="d4dc4-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="d4dc4-126">Imposta la data e l'ora in cui è stato creato, ultimo accesso o Ultima modifica la directory o il file specificato.</span><span class="sxs-lookup"><span data-stu-id="d4dc4-126">Sets the date and time that the specified file or directory was created, last accessed, or last modified.</span></span><br/>                                             |



 

 

