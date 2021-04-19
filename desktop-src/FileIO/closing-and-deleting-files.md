---
description: Per utilizzare in modo efficiente le risorse del sistema operativo, un'applicazione deve chiudere i file quando non sono più necessari tramite la funzione CloseHandle. Se un file è aperto al termine di un'applicazione, il sistema lo chiude automaticamente.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Chiusura ed eliminazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317800"
---
# <a name="closing-and-deleting-files"></a><span data-ttu-id="f1390-104">Chiusura ed eliminazione di file</span><span class="sxs-lookup"><span data-stu-id="f1390-104">Closing and Deleting Files</span></span>

<span data-ttu-id="f1390-105">Per utilizzare in modo efficiente le risorse del sistema operativo, un'applicazione deve chiudere i file quando non sono più necessari tramite la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="f1390-105">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="f1390-106">Se un file è aperto al termine di un'applicazione, il sistema lo chiude automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f1390-106">If a file is open when an application terminates, the system closes it automatically.</span></span>

<span data-ttu-id="f1390-107">La funzione [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) può essere usata per eliminare un file alla chiusura.</span><span class="sxs-lookup"><span data-stu-id="f1390-107">The [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function can be used to delete a file on close.</span></span> <span data-ttu-id="f1390-108">Non è possibile eliminare un file finché non vengono chiusi tutti gli handle.</span><span class="sxs-lookup"><span data-stu-id="f1390-108">A file cannot be deleted until all handles to it are closed.</span></span> <span data-ttu-id="f1390-109">Se non è possibile eliminare un file, non è possibile riutilizzarne il nome.</span><span class="sxs-lookup"><span data-stu-id="f1390-109">If a file cannot be deleted, its name cannot be reused.</span></span> <span data-ttu-id="f1390-110">Per riutilizzare immediatamente il nome di un file, rinominare il file esistente.</span><span class="sxs-lookup"><span data-stu-id="f1390-110">To reuse a file name immediately, rename the existing file.</span></span>

<span data-ttu-id="f1390-111">Se si elimina un file o una directory aperta in un computer remoto ed è già stata aperta nel computer remoto senza il set di autorizzazioni lettura condivisione, non chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) per aprire prima il file o la directory per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="f1390-111">If you are deleting an open file or directory on a remote machine and it has already been opened on the remote machine without the read share permission set, do not call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) to open the file or directory for deletion first.</span></span> <span data-ttu-id="f1390-112">Questa operazione comporterà una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="f1390-112">Doing so will result in a sharing violation.</span></span>

 

 
