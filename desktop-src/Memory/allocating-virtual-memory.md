---
description: Le funzioni di memoria virtuale modificano le pagine di memoria. Le funzioni utilizzano le dimensioni di una pagina nel computer corrente per arrotondare le dimensioni e gli indirizzi specificati.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Allocazione della memoria virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345371"
---
# <a name="allocating-virtual-memory"></a><span data-ttu-id="4d729-104">Allocazione della memoria virtuale</span><span class="sxs-lookup"><span data-stu-id="4d729-104">Allocating Virtual Memory</span></span>

<span data-ttu-id="4d729-105">Le funzioni di memoria virtuale modificano le pagine di memoria.</span><span class="sxs-lookup"><span data-stu-id="4d729-105">The virtual memory functions manipulate pages of memory.</span></span> <span data-ttu-id="4d729-106">Le funzioni utilizzano le dimensioni di una pagina nel computer corrente per arrotondare le dimensioni e gli indirizzi specificati.</span><span class="sxs-lookup"><span data-stu-id="4d729-106">The functions use the size of a page on the current computer to round off specified sizes and addresses.</span></span>

<span data-ttu-id="4d729-107">La funzione [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) esegue una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d729-107">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function performs one of the following operations:</span></span>

-   <span data-ttu-id="4d729-108">Riserva una o più pagine gratuite.</span><span class="sxs-lookup"><span data-stu-id="4d729-108">Reserves one or more free pages.</span></span>
-   <span data-ttu-id="4d729-109">Viene eseguito il commit di una o più pagine riservate.</span><span class="sxs-lookup"><span data-stu-id="4d729-109">Commits one or more reserved pages.</span></span>
-   <span data-ttu-id="4d729-110">Consente di riservare ed eseguire il commit di una o più pagine gratuite.</span><span class="sxs-lookup"><span data-stu-id="4d729-110">Reserves and commits one or more free pages.</span></span>

<span data-ttu-id="4d729-111">È possibile specificare l'indirizzo iniziale delle pagine da riservare o sottoposte a commit oppure è possibile consentire al sistema di determinare l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="4d729-111">You can specify the starting address of the pages to be reserved or committed, or you can allow the system to determine the address.</span></span> <span data-ttu-id="4d729-112">La funzione arrotonda l'indirizzo specificato al limite della pagina appropriato.</span><span class="sxs-lookup"><span data-stu-id="4d729-112">The function rounds the specified address to the appropriate page boundary.</span></span> <span data-ttu-id="4d729-113">Le pagine riservate non sono accessibili, ma le pagine di cui è stato eseguito il commit possono essere allocate con l'accesso alla pagina **\_ ReadWrite**, alla **pagina \_ ReadOnly** o alla **pagina \_** .</span><span class="sxs-lookup"><span data-stu-id="4d729-113">Reserved pages are not accessible, but committed pages can be allocated with **PAGE\_READWRITE**, **PAGE\_READONLY**, or **PAGE\_NOACCESS** access.</span></span> <span data-ttu-id="4d729-114">Quando si esegue il commit delle pagine, gli addebiti per la memoria vengono allocati dalla dimensione complessiva della RAM e dai file di paging sul disco, ma ogni pagina viene inizializzata e caricata nella memoria fisica solo al primo tentativo di lettura o scrittura in tale pagina.</span><span class="sxs-lookup"><span data-stu-id="4d729-114">When pages are committed, memory charges are allocated from the overall size of RAM and paging files on disk, but each page is initialized and loaded into physical memory only at the first attempt to read from or write to that page.</span></span> <span data-ttu-id="4d729-115">È possibile usare i riferimenti al puntatore normali per accedere alla memoria di cui è stato eseguito il commit dalla funzione [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .</span><span class="sxs-lookup"><span data-stu-id="4d729-115">You can use normal pointer references to access memory committed by the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function.</span></span>

 

 
