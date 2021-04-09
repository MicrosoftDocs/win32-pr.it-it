---
title: Scelta del tipo di handle di associazione da usare
description: Scelta del tipo di handle di associazione da usare
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044428"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a><span data-ttu-id="c36e9-103">Scelta del tipo di handle di associazione da usare</span><span class="sxs-lookup"><span data-stu-id="c36e9-103">Choosing the Type of Binding Handles to Use</span></span>

<span data-ttu-id="c36e9-104">**Procedura consigliata:** Se si sa quale server sarà utilizzato dall'applicazione, utilizzare handle espliciti.</span><span class="sxs-lookup"><span data-stu-id="c36e9-104">**Best practice:** If you know which server the application will use, use explicit handles.</span></span> <span data-ttu-id="c36e9-105">In caso contrario, utilizzare il costrutto di handle espliciti ogni volta oppure utilizzare handle generici con routine **\_ Bind** e **\_ UNBIND** .</span><span class="sxs-lookup"><span data-stu-id="c36e9-105">If you don't, use explicit handles construct every time, or use generic handles with **\_bind** and **\_unbind** routines.</span></span>

<span data-ttu-id="c36e9-106">Non usare handle impliciti o handle automatici.</span><span class="sxs-lookup"><span data-stu-id="c36e9-106">Do not use implicit handles or auto handles.</span></span> <span data-ttu-id="c36e9-107">Gli handle impliciti non sono thread-safe e anche se thread safety potrebbe sembrare superfluo, potrebbe essere necessario in seguito.</span><span class="sxs-lookup"><span data-stu-id="c36e9-107">Implicit handles are not thread safe, and even though thread safety may seem unnecessary, it could become necessary later.</span></span> <span data-ttu-id="c36e9-108">Gli handle automatici hanno un sovraccarico elevato e richiedono un funzionamento corretto del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="c36e9-108">Auto handles have large overhead and require a lot of setup to work properly.</span></span> <span data-ttu-id="c36e9-109">Le funzionalità di ricerca sono state sostituite dai servizi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c36e9-109">Their search capabilities have been superseded by Active Directory services.</span></span>

<span data-ttu-id="c36e9-110">Gli handle espliciti sono estremamente efficienti e molte funzionalità interessanti sono disponibili solo per gli handle espliciti.</span><span class="sxs-lookup"><span data-stu-id="c36e9-110">Explicit handles are highly efficient, and many attractive capabilities are available only for explicit handles.</span></span> <span data-ttu-id="c36e9-111">Se, ad esempio, più chiamate RPC saranno destinate allo stesso server, sarà possibile costruire il gestore dell'associazione una sola volta ed effettuare tutte le chiamate.</span><span class="sxs-lookup"><span data-stu-id="c36e9-111">For example, if several RPC calls will be going to the same server, you can construct the binding handle once and make all calls with it.</span></span> <span data-ttu-id="c36e9-112">Questo approccio è molto più efficiente rispetto a qualsiasi altro metodo.</span><span class="sxs-lookup"><span data-stu-id="c36e9-112">This approach is much more efficient than any other method.</span></span> <span data-ttu-id="c36e9-113">Se il server a cui la chiamata passerà è sconosciuto, costruire un handle di binding esplicito per ogni chiamata o utilizzare handle di associazione generici.</span><span class="sxs-lookup"><span data-stu-id="c36e9-113">If the server to which the call will go is unknown, construct an explicit binding handle for every call, or use generic binding handles.</span></span>

<span data-ttu-id="c36e9-114">In Microsoft™ Windows XP, il tempo di esecuzione RPC è piuttosto efficiente per riutilizzare e memorizzare nella cache le chiamate, pertanto se la chiamata *n*+ 1 termina nello stesso server della chiamata *n*, RPC riutilizza le risorse allocate *per la chiamata n,* eludendo la necessità di memorizzare nella cache gli handle di binding per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c36e9-114">In Microsoft™ Windows XP, the RPC run time is quite efficient in re-using and caching calls, so if the *n*+1st call ends up on the same server as the *n* th call, RPC re-uses the resources allocated for the *n* th call, circumventing the need to cache binding handles to improve performance.</span></span>

 

 




