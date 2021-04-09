---
description: Negli argomenti seguenti vengono descritti i file di simboli e la funzionalità fornita dalle funzioni DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Informazioni su DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126246"
---
# <a name="about-dbghelp"></a><span data-ttu-id="c964c-103">Informazioni su DbgHelp</span><span class="sxs-lookup"><span data-stu-id="c964c-103">About DbgHelp</span></span>

<span data-ttu-id="c964c-104">Negli argomenti seguenti vengono descritti i file di simboli e la funzionalità fornita dalle [funzioni DbgHelp](dbghelp-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c964c-104">The following topics describe symbol files and the functionality provided by the [DbgHelp functions](dbghelp-functions.md).</span></span>

-   [<span data-ttu-id="c964c-105">Versioni di DbgHelp</span><span class="sxs-lookup"><span data-stu-id="c964c-105">DbgHelp Versions</span></span>](dbghelp-versions.md)
-   [<span data-ttu-id="c964c-106">File di simboli</span><span class="sxs-lookup"><span data-stu-id="c964c-106">Symbol Files</span></span>](symbol-files.md)
-   [<span data-ttu-id="c964c-107">Gestione dei simboli</span><span class="sxs-lookup"><span data-stu-id="c964c-107">Symbol Handling</span></span>](symbol-handling.md)
-   [<span data-ttu-id="c964c-108">Server di simboli e archivi simboli</span><span class="sxs-lookup"><span data-stu-id="c964c-108">Symbol Servers and Symbol Stores</span></span>](symbol-servers-and-symbol-stores.md)
-   [<span data-ttu-id="c964c-109">File minidump</span><span class="sxs-lookup"><span data-stu-id="c964c-109">Minidump Files</span></span>](minidump-files.md)
-   [<span data-ttu-id="c964c-110">Server di origine</span><span class="sxs-lookup"><span data-stu-id="c964c-110">Source Server</span></span>](source-server-and-source-indexing.md)
-   [<span data-ttu-id="c964c-111">Supporto aggiornato della piattaforma</span><span class="sxs-lookup"><span data-stu-id="c964c-111">Updated Platform Support</span></span>](updated-platform-support.md)

<span data-ttu-id="c964c-112">Si noti che tutte le [funzioni DbgHelp](dbghelp-functions.md) sono a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="c964c-112">Note that all [DbgHelp functions](dbghelp-functions.md) are single threaded.</span></span> <span data-ttu-id="c964c-113">Pertanto, le chiamate da più thread a questa funzione potrebbero causare un comportamento imprevisto o un danneggiamento della memoria.</span><span class="sxs-lookup"><span data-stu-id="c964c-113">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="c964c-114">Per evitare questo problema, è necessario sincronizzare tutte le chiamate simultanee da più di un thread a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="c964c-114">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

 

 



