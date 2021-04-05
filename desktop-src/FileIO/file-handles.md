---
description: Quando un file viene aperto da un processo che utilizza la funzione CreateFile, a esso viene associato un handle di file fino al termine del processo o alla chiusura dell'handle tramite la funzione CloseHandle.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Handle di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884889"
---
# <a name="file-handles"></a><span data-ttu-id="4b61d-103">Handle di file</span><span class="sxs-lookup"><span data-stu-id="4b61d-103">File Handles</span></span>

<span data-ttu-id="4b61d-104">Quando un file viene aperto da un processo che utilizza la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , a esso viene associato un *handle di file* fino al termine del processo o alla chiusura dell'handle tramite la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="4b61d-104">When a file is opened by a process using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, a *file handle* is associated with it until either the process terminates or the handle is closed using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="4b61d-105">L'handle di file viene usato per identificare il file in molte chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="4b61d-105">The file handle is used to identify the file in many function calls.</span></span>

<span data-ttu-id="4b61d-106">Ogni handle di file e oggetto file è in genere univoco per ogni processo che apre un file: le uniche eccezioni si verificano quando un handle di file utilizzato da un processo viene duplicato o quando un processo figlio eredita gli handle di file del processo padre.</span><span class="sxs-lookup"><span data-stu-id="4b61d-106">Each file handle and file object is generally unique to each process that opens a file—the only exceptions to this are when a file handle held by a process is duplicated, or when a child process inherits the file handles of the parent process.</span></span> <span data-ttu-id="4b61d-107">In queste situazioni, questi handle di file sono univoci, ma visualizzano un singolo oggetto file condiviso.</span><span class="sxs-lookup"><span data-stu-id="4b61d-107">In these situations, these file handles are unique, but see a single, shared file object.</span></span> <span data-ttu-id="4b61d-108">Per ulteriori informazioni sulla duplicazione degli handle di file mantenuti dai processi, vedere [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="4b61d-108">See [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) for more information on duplicating file handles held by processes.</span></span>

<span data-ttu-id="4b61d-109">Si noti che mentre gli handle di file sono in genere privati di un processo, i dati del file a cui il file fa riferimento non lo sono.</span><span class="sxs-lookup"><span data-stu-id="4b61d-109">Note that while the file handles are typically private to a process, the file data that the file handles point to is not.</span></span> <span data-ttu-id="4b61d-110">Pertanto, i processi e i thread che condividono lo stesso file devono sincronizzarne l'accesso.</span><span class="sxs-lookup"><span data-stu-id="4b61d-110">Therefore, processes and threads that share the same file must synchronize their access.</span></span> <span data-ttu-id="4b61d-111">Per la maggior parte delle operazioni su un file, un processo identifica il file tramite il pool di handle privato.</span><span class="sxs-lookup"><span data-stu-id="4b61d-111">For most operations on a file, a process identifies the file through its private pool of handles.</span></span>

 

 
