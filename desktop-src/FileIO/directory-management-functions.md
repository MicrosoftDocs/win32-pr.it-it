---
description: Funzioni utilizzate nella gestione delle directory.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Funzioni di gestione della directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bc10d0f8d7caddc1ea821c397e16edf600d92c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233161"
---
# <a name="directory-management-functions"></a><span data-ttu-id="c4a02-103">Funzioni di gestione della directory</span><span class="sxs-lookup"><span data-stu-id="c4a02-103">Directory Management Functions</span></span>

<span data-ttu-id="c4a02-104">Le funzioni seguenti vengono utilizzate per la gestione delle directory.</span><span class="sxs-lookup"><span data-stu-id="c4a02-104">The following functions are used in directory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c4a02-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c4a02-105">In this section</span></span>



| <span data-ttu-id="c4a02-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="c4a02-106">Function</span></span>                                                                      | <span data-ttu-id="c4a02-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4a02-107">Description</span></span>                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4a02-108">**CreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="c4a02-108">**CreateDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | <span data-ttu-id="c4a02-109">Crea una nuova directory.</span><span class="sxs-lookup"><span data-stu-id="c4a02-109">Creates a new directory.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="c4a02-110">**CreateDirectoryEx**</span><span class="sxs-lookup"><span data-stu-id="c4a02-110">**CreateDirectoryEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | <span data-ttu-id="c4a02-111">Crea una nuova directory con gli attributi di una directory di modello specificata.</span><span class="sxs-lookup"><span data-stu-id="c4a02-111">Creates a new directory with the attributes of a specified template directory.</span></span><br/>                                                                                 |
| [<span data-ttu-id="c4a02-112">**CreateDirectoryTransacted**</span><span class="sxs-lookup"><span data-stu-id="c4a02-112">**CreateDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | <span data-ttu-id="c4a02-113">Crea una nuova directory come operazione transazionale, con gli attributi di una directory di modello specificata.</span><span class="sxs-lookup"><span data-stu-id="c4a02-113">Creates a new directory as a transacted operation, with the attributes of a specified template directory.</span></span><br/>                                                      |
| [<span data-ttu-id="c4a02-114">**FindCloseChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="c4a02-114">**FindCloseChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | <span data-ttu-id="c4a02-115">Arresta il monitoraggio dell'handle della notifica di modifica.</span><span class="sxs-lookup"><span data-stu-id="c4a02-115">Stops change notification handle monitoring.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="c4a02-116">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="c4a02-116">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | <span data-ttu-id="c4a02-117">Crea un handle notifica di modifica e configura le condizioni di filtro della notifica di modifica iniziale.</span><span class="sxs-lookup"><span data-stu-id="c4a02-117">Creates a change notification handle and sets up initial change notification filter conditions.</span></span><br/>                                                                |
| [<span data-ttu-id="c4a02-118">**FindNextChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="c4a02-118">**FindNextChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | <span data-ttu-id="c4a02-119">Richiede che il sistema operativo segnali un handle della notifica di modifica alla successiva rilevazione di una modifica appropriata.</span><span class="sxs-lookup"><span data-stu-id="c4a02-119">Requests that the operating system signal a change notification handle the next time it detects an appropriate change.</span></span><br/>                                         |
| [<span data-ttu-id="c4a02-120">**GetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="c4a02-120">**GetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | <span data-ttu-id="c4a02-121">Recupera la directory corrente per il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="c4a02-121">Retrieves the current directory for the current process.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c4a02-122">**ReadDirectoryChangesExW**</span><span class="sxs-lookup"><span data-stu-id="c4a02-122">**ReadDirectoryChangesExW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | <span data-ttu-id="c4a02-123">Recupera le informazioni che descrivono le modifiche all'interno della directory specificata, che possono includere informazioni estese se è specificato il tipo di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c4a02-123">Retrieves information that describes the changes within the specified directory, which can include extended information if that information type is specified.</span></span><br/> |
| [<span data-ttu-id="c4a02-124">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="c4a02-124">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | <span data-ttu-id="c4a02-125">Recupera le informazioni che descrivono le modifiche all'interno della directory specificata.</span><span class="sxs-lookup"><span data-stu-id="c4a02-125">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                               |
| [<span data-ttu-id="c4a02-126">**RemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="c4a02-126">**RemoveDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | <span data-ttu-id="c4a02-127">Elimina una directory vuota esistente.</span><span class="sxs-lookup"><span data-stu-id="c4a02-127">Deletes an existing empty directory.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="c4a02-128">**RemoveDirectoryTransacted**</span><span class="sxs-lookup"><span data-stu-id="c4a02-128">**RemoveDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | <span data-ttu-id="c4a02-129">Elimina una directory vuota esistente come operazione transazionale.</span><span class="sxs-lookup"><span data-stu-id="c4a02-129">Deletes an existing empty directory as a transacted operation.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="c4a02-130">**SetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="c4a02-130">**SetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | <span data-ttu-id="c4a02-131">Modifica la directory corrente per il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="c4a02-131">Changes the current directory for the current process.</span></span><br/>                                                                                                         |



 

 

 




