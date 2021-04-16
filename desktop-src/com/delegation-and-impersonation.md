---
title: Delega e rappresentazione
description: Negli scenari client/server è normale che un server chiami un altro server per eseguire alcune attività per conto di un client. La situazione in cui un server ha la facoltà di agire per conto di un cliente è detta delega.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104571440"
---
# <a name="delegation-and-impersonation"></a><span data-ttu-id="079ef-104">Delega e rappresentazione</span><span class="sxs-lookup"><span data-stu-id="079ef-104">Delegation and Impersonation</span></span>

<span data-ttu-id="079ef-105">Negli scenari client/server è normale che un server chiami un altro server per eseguire alcune attività per conto di un client.</span><span class="sxs-lookup"><span data-stu-id="079ef-105">In client/server scenarios, it is common for one server to call another server to accomplish some task on a client's behalf.</span></span> <span data-ttu-id="079ef-106">La situazione in cui un server ha la facoltà di agire per conto di un cliente è detta *delega*.</span><span class="sxs-lookup"><span data-stu-id="079ef-106">The situation where a server is given the authority to act on a client's behalf is called *delegation*.</span></span>

<span data-ttu-id="079ef-107">Dal punto di vista della sicurezza, si verificano due problemi relativi alla delega:</span><span class="sxs-lookup"><span data-stu-id="079ef-107">From a security standpoint, two issues arise regarding delegation:</span></span>

-   <span data-ttu-id="079ef-108">Cosa può fare il server quando agisce per conto del client?</span><span class="sxs-lookup"><span data-stu-id="079ef-108">What should the server be allowed to do when acting on the client's behalf?</span></span>
-   <span data-ttu-id="079ef-109">Quale identità viene presentata dal server quando chiama altri server per conto di un client?</span><span class="sxs-lookup"><span data-stu-id="079ef-109">What identity is presented by the server when it calls other servers on behalf of a client?</span></span>

<span data-ttu-id="079ef-110">Per risolvere questi problemi, COM offre le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="079ef-110">To deal with these issues, COM provides the following functionality.</span></span> <span data-ttu-id="079ef-111">Il client può impostare un *livello di rappresentazione* che determina in quale misura il server sarà in grado di fungere da client.</span><span class="sxs-lookup"><span data-stu-id="079ef-111">The client can set an *impersonation level* that determines to what extent the server will be able to act as the client.</span></span> <span data-ttu-id="079ef-112">Se il client concede un'autorità sufficiente al server, il server può *rappresentare* (fingere) il client.</span><span class="sxs-lookup"><span data-stu-id="079ef-112">If the client grants enough authority to the server, the server can *impersonate* (pretend to be) the client.</span></span> <span data-ttu-id="079ef-113">Quando si rappresenta il client, al server viene concesso l'accesso solo agli oggetti o alle risorse che il client è autorizzato a utilizzare.</span><span class="sxs-lookup"><span data-stu-id="079ef-113">When impersonating the client, the server is given access to only those objects or resources that the client has permission to use.</span></span> <span data-ttu-id="079ef-114">Il server, che funge da client, può anche abilitare il *cloaking* per mascherare la propria identità e proiettare l'identità del client nelle chiamate ad altri componenti com.</span><span class="sxs-lookup"><span data-stu-id="079ef-114">The server, acting as a client, can also enable *cloaking* to mask its own identity and project the client's identity in calls to other COM components.</span></span>

![Diagramma che illustra in che modo il server che funge da client può abilitare il mascheramento.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

<span data-ttu-id="079ef-116">Si consideri lo scenario illustrato nella figura precedente, dove A e B sono processi in un computer diverso da C. elaborare A chiama B e B chiama C. il client A imposta il livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="079ef-116">Consider the scenario illustrated by the preceding figure, where A and B are processes on a different machine from C. Process A calls B, and B calls C. Client A sets the impersonation level.</span></span> <span data-ttu-id="079ef-117">B imposta la funzionalità di mascheramento.</span><span class="sxs-lookup"><span data-stu-id="079ef-117">B sets the cloaking capability.</span></span> <span data-ttu-id="079ef-118">Se un oggetto imposta un livello di rappresentazione che consente la rappresentazione, B può rappresentare un oggetto quando si chiama C per conto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="079ef-118">If A sets an impersonation level that permits impersonation, B can impersonate A when calling C on A's behalf.</span></span> <span data-ttu-id="079ef-119">L'identità presentata al processo C sarà Identity o B, a seconda che il mascheramento sia stato abilitato da B. Se il mascheramento è abilitato, l'identità presentata al processo C sarà quella di un oggetto. Se il cloaking non è abilitato, l'identità di B verrà visualizzata in C.</span><span class="sxs-lookup"><span data-stu-id="079ef-119">The identity that is presented to process C will be either A's identity or B's identity, depending on whether cloaking was enabled by B. If cloaking is enabled, the identity presented to process C will be that of A. If cloaking is not enabled, B's identity will be presented to C.</span></span>

<span data-ttu-id="079ef-120">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="079ef-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="079ef-121">Rappresentazione</span><span class="sxs-lookup"><span data-stu-id="079ef-121">Impersonation</span></span>](impersonation.md)
-   [<span data-ttu-id="079ef-122">Livelli di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="079ef-122">Impersonation Levels</span></span>](impersonation-levels.md)
-   [<span data-ttu-id="079ef-123">Cloaking</span><span class="sxs-lookup"><span data-stu-id="079ef-123">Cloaking</span></span>](cloaking.md)

 

 




