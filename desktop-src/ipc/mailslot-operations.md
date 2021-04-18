---
description: Descrizioni delle funzioni da utilizzare quando si utilizzano mailslot, client e server.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Operazioni inserimento/espulsione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313057"
---
# <a name="mailslot-operations"></a><span data-ttu-id="cc11c-103">Operazioni inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="cc11c-103">Mailslot Operations</span></span>

<span data-ttu-id="cc11c-104">Quando si utilizza mailslot, i client e i server devono utilizzare solo le funzioni descritte nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="cc11c-104">When working with mailslots, clients and servers should use only the functions discussed in the following tables.</span></span> <span data-ttu-id="cc11c-105">Non usare altre funzioni, anche se accettano gli handle di file o i nomi di file come parametri, perché non sono progettati per funzionare con mailslot.</span><span class="sxs-lookup"><span data-stu-id="cc11c-105">Do not use other functions, even if they accept file handles or file names as parameters, as they are not designed to work with mailslots.</span></span>

## <a name="mailslot-server-functions"></a><span data-ttu-id="cc11c-106">Funzioni del server inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="cc11c-106">Mailslot Server Functions</span></span>

<span data-ttu-id="cc11c-107">I server inserimento/espulsione hanno un utilizzo esclusivo di tre funzioni, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cc11c-107">Mailslot servers have exclusive use of three functions, as shown in the following table.</span></span>



| <span data-ttu-id="cc11c-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="cc11c-108">Function</span></span>                                   | <span data-ttu-id="cc11c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc11c-109">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc11c-110">**CreateMailslot**</span><span class="sxs-lookup"><span data-stu-id="cc11c-110">**CreateMailslot**</span></span>](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | <span data-ttu-id="cc11c-111">Crea un inserimento/espulsione e restituisce un handle inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-111">Creates a mailslot and returns a mailslot handle.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="cc11c-112">**GetMailslotInfo**</span><span class="sxs-lookup"><span data-stu-id="cc11c-112">**GetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | <span data-ttu-id="cc11c-113">Recupera le dimensioni massime del messaggio, le dimensioni inserimento/espulsione, le dimensioni del messaggio successivo in inserimento/espulsione, il numero di messaggi nel inserimento/espulsione e l'intervallo di tempo durante il quale un'operazione di lettura può attendere un messaggio.</span><span class="sxs-lookup"><span data-stu-id="cc11c-113">Retrieves the maximum message size, the mailslot size, the size of the next message in the mailslot, the number of messages in the mailslot, and the amount of time a read operation can wait for a message.</span></span> |
| [<span data-ttu-id="cc11c-114">**SetMailslotInfo**</span><span class="sxs-lookup"><span data-stu-id="cc11c-114">**SetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | <span data-ttu-id="cc11c-115">Modifica il timeout di lettura per un inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-115">Changes the read time-out for a mailslot.</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="cc11c-116">Le funzioni seguenti sono usate anche dai server inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-116">The following functions are also used by mailslot servers.</span></span>



| <span data-ttu-id="cc11c-117">Funzione</span><span class="sxs-lookup"><span data-stu-id="cc11c-117">Function</span></span>                                                         | <span data-ttu-id="cc11c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc11c-118">Description</span></span>                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="cc11c-119">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="cc11c-119">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | <span data-ttu-id="cc11c-120">Duplica l'handle inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-120">Duplicates the mailslot handle.</span></span>                     |
| <span data-ttu-id="cc11c-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span><span class="sxs-lookup"><span data-stu-id="cc11c-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span></span> | <span data-ttu-id="cc11c-122">Recupera i messaggi da un inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-122">Retrieves messages from a mailslot.</span></span>                 |
| [<span data-ttu-id="cc11c-123">**GetFileTime ha provocato**</span><span class="sxs-lookup"><span data-stu-id="cc11c-123">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="cc11c-124">Recupera la data e l'ora di creazione di un inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-124">Retrieves the date and time a mailslot was created.</span></span> |
| [<span data-ttu-id="cc11c-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="cc11c-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="cc11c-126">Imposta la data e l'ora di creazione di un inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-126">Sets the date and time a mailslot was created.</span></span>      |
| [<span data-ttu-id="cc11c-127">**GetHandleInformation**</span><span class="sxs-lookup"><span data-stu-id="cc11c-127">**GetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | <span data-ttu-id="cc11c-128">Recupera le proprietà dell'handle inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-128">Retrieves properties of the mailslot handle.</span></span>        |
| [<span data-ttu-id="cc11c-129">**SetHandleInformation**</span><span class="sxs-lookup"><span data-stu-id="cc11c-129">**SetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | <span data-ttu-id="cc11c-130">Imposta le proprietà dell'handle inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-130">Sets properties of the mailslot handle.</span></span>             |



 

## <a name="mailslot-client-functions"></a><span data-ttu-id="cc11c-131">Funzioni client inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="cc11c-131">Mailslot Client Functions</span></span>

<span data-ttu-id="cc11c-132">Un processo client usa le funzioni seguenti quando si interagisce con un inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-132">A client process uses the following functions when interacting with a mailslot.</span></span>



| <span data-ttu-id="cc11c-133">Funzione</span><span class="sxs-lookup"><span data-stu-id="cc11c-133">Function</span></span>                                                             | <span data-ttu-id="cc11c-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc11c-134">Description</span></span>                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="cc11c-135">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="cc11c-135">**CloseHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | <span data-ttu-id="cc11c-136">Chiude un handle inserimento/espulsione per un processo client.</span><span class="sxs-lookup"><span data-stu-id="cc11c-136">Closes a mailslot handle for a client process.</span></span>  |
| [<span data-ttu-id="cc11c-137">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="cc11c-137">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | <span data-ttu-id="cc11c-138">Crea un handle inserimento/espulsione per un processo client.</span><span class="sxs-lookup"><span data-stu-id="cc11c-138">Creates a mailslot handle for a client process.</span></span> |
| [<span data-ttu-id="cc11c-139">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="cc11c-139">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | <span data-ttu-id="cc11c-140">Duplica un handle inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-140">Duplicates a mailslot handle.</span></span>                   |
| <span data-ttu-id="cc11c-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span><span class="sxs-lookup"><span data-stu-id="cc11c-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span></span> | <span data-ttu-id="cc11c-142">Scrive i dati in un inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="cc11c-142">Writes data to a mailslot.</span></span>                      |



 

 

 
