---
description: La configurazione corretta dei simboli per il debug può essere un'attività complessa, in particolare per il debug del kernel.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  Server di simboli e archivi simboli"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225597"
---
# <a name="symbol-server-and-symbol-stores"></a><span data-ttu-id="65c04-103">  Server di simboli e archivi simboli</span><span class="sxs-lookup"><span data-stu-id="65c04-103">Symbol Server and Symbol Stores</span></span>

<span data-ttu-id="65c04-104">La configurazione corretta dei simboli per il debug può essere un'attività complessa, in particolare per il debug del kernel.</span><span class="sxs-lookup"><span data-stu-id="65c04-104">Setting up symbols correctly for debugging can be a challenging task, particularly for kernel debugging.</span></span> <span data-ttu-id="65c04-105">Spesso è necessario che si conoscano i nomi e le versioni di tutti i prodotti nel computer.</span><span class="sxs-lookup"><span data-stu-id="65c04-105">It often requires that you know the names and releases of all products on your computer.</span></span> <span data-ttu-id="65c04-106">Il debugger deve essere in grado di individuare i file di simboli che corrispondono a ogni versione del prodotto e Service Pack.</span><span class="sxs-lookup"><span data-stu-id="65c04-106">The debugger must be able to locate the symbol files that correspond to each product release and service pack.</span></span> <span data-ttu-id="65c04-107">Questo può comportare un percorso di simboli estremamente lungo costituito da un lungo elenco di directory.</span><span class="sxs-lookup"><span data-stu-id="65c04-107">This can result in an extremely long symbol path consisting of a long list of directories.</span></span>

<span data-ttu-id="65c04-108">Per semplificare queste difficoltà nel coordinamento dei file di simboli, usare il *server di simboli*.</span><span class="sxs-lookup"><span data-stu-id="65c04-108">To simplify these difficulties in coordinating symbol files, use the *symbol server*.</span></span> <span data-ttu-id="65c04-109">Il server di simboli consente ai debugger di recuperare automaticamente i file di simboli corretti senza nomi di prodotto, versioni o numeri di Build.</span><span class="sxs-lookup"><span data-stu-id="65c04-109">The symbol server enables the debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="65c04-110">Strumenti di debug per Windows contiene il server di simboli SymSrv.</span><span class="sxs-lookup"><span data-stu-id="65c04-110">Debugging Tools for Windows contains the SymSrv symbol server.</span></span>

<span data-ttu-id="65c04-111">Il server di simboli viene attivato includendo una determinata stringa di testo nel percorso dei simboli.</span><span class="sxs-lookup"><span data-stu-id="65c04-111">The symbol server is activated by including a certain text string in the symbol path.</span></span> <span data-ttu-id="65c04-112">Ogni volta che il debugger deve caricare i simboli per un modulo appena caricato, chiama il server di simboli per individuare i file di simboli appropriati.</span><span class="sxs-lookup"><span data-stu-id="65c04-112">Each time the debugger needs to load symbols for a newly loaded module, it calls the symbol server to locate the appropriate symbol files.</span></span> <span data-ttu-id="65c04-113">Il server dei simboli individua i file in un *Archivio di simboli*.</span><span class="sxs-lookup"><span data-stu-id="65c04-113">The symbol server locates the files in a *symbol store*.</span></span> <span data-ttu-id="65c04-114">Si tratta di una raccolta di file di simboli, di un indice e di uno strumento che può essere utilizzato da un amministratore per aggiungere ed eliminare file.</span><span class="sxs-lookup"><span data-stu-id="65c04-114">This is a collection of symbol files, an index, and a tool that can be used by an administrator to add and delete files.</span></span> <span data-ttu-id="65c04-115">I file vengono indicizzati in base a parametri univoci, ad esempio il timestamp e le dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="65c04-115">The files are indexed according to unique parameters such as the time stamp and image size.</span></span> <span data-ttu-id="65c04-116">Strumenti di debug per Windows contiene uno strumento di archiviazione simboli denominato SymStore.</span><span class="sxs-lookup"><span data-stu-id="65c04-116">Debugging Tools for Windows contains a symbol store tool called SymStore.</span></span>

<span data-ttu-id="65c04-117">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="65c04-117">For more information, see:</span></span>

-   [<span data-ttu-id="65c04-118">Uso di SymSrv</span><span class="sxs-lookup"><span data-stu-id="65c04-118">Using SymSrv</span></span>](using-symsrv.md)
-   [<span data-ttu-id="65c04-119">Uso di SymStore</span><span class="sxs-lookup"><span data-stu-id="65c04-119">Using SymStore</span></span>](using-symstore.md)
-   [<span data-ttu-id="65c04-120">Uso di altri archivi simboli</span><span class="sxs-lookup"><span data-stu-id="65c04-120">Using Other Symbol Stores</span></span>](using-other-symbol-stores.md)
-   [<span data-ttu-id="65c04-121">Opzioni Command-Line SymStore</span><span class="sxs-lookup"><span data-stu-id="65c04-121">SymStore Command-Line Options</span></span>](symstore-command-line-options.md)
-   [<span data-ttu-id="65c04-122">Server di simboli e firewall Internet</span><span class="sxs-lookup"><span data-stu-id="65c04-122">Symbol Server and Internet Firewalls</span></span>](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a><span data-ttu-id="65c04-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65c04-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65c04-124">File di simboli</span><span class="sxs-lookup"><span data-stu-id="65c04-124">Symbol Files</span></span>](symbol-files.md)
</dt> </dl>

 

 



