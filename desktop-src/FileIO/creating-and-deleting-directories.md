---
description: Un'applicazione può creare ed eliminare le directory a livello di codice.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Creazione ed eliminazione di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130454"
---
# <a name="creating-and-deleting-directories"></a><span data-ttu-id="05d9c-103">Creazione ed eliminazione di directory</span><span class="sxs-lookup"><span data-stu-id="05d9c-103">Creating and Deleting Directories</span></span>

<span data-ttu-id="05d9c-104">Un'applicazione può creare ed eliminare le directory a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="05d9c-104">An application can programmatically create and delete directories.</span></span>

<span data-ttu-id="05d9c-105">Per creare una nuova directory, usare la funzione [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)o [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="05d9c-105">To create a new directory, use the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa), or [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) function.</span></span> <span data-ttu-id="05d9c-106">A una directory viene assegnato il nome specificato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="05d9c-106">A directory is given the name specified when it is created.</span></span> <span data-ttu-id="05d9c-107">Le convenzioni per la denominazione di una directory seguono le convenzioni per la denominazione di un file.</span><span class="sxs-lookup"><span data-stu-id="05d9c-107">The conventions for naming a directory follow the conventions for naming a file.</span></span> <span data-ttu-id="05d9c-108">Per una descrizione di queste convenzioni, vedere [denominazione di un file](naming-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="05d9c-108">For a description of these conventions, see [Naming a File](naming-a-file.md).</span></span>

<span data-ttu-id="05d9c-109">Per eliminare una directory esistente, usare la funzione [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) o [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="05d9c-109">To delete an existing directory, use the [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) or [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) function.</span></span> <span data-ttu-id="05d9c-110">Prima di rimuovere una directory, è necessario assicurarsi che la directory sia vuota e che si disponga del privilegio di accesso DELETE per la directory.</span><span class="sxs-lookup"><span data-stu-id="05d9c-110">Before removing a directory, you must ensure that the directory is empty and that you have the delete access privilege for the directory.</span></span> <span data-ttu-id="05d9c-111">Per eseguire quest'ultima operazione, chiamare la funzione [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="05d9c-111">To do the latter, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span>

 

 
