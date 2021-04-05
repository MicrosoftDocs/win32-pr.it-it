---
description: Una named pipe è una pipe denominata, unidirezionale o duplex per la comunicazione tra il server pipe e uno o più client pipe.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Named Pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0675244e09b7c202b4fa6b67f6268392b1b260f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967640"
---
# <a name="named-pipes"></a><span data-ttu-id="8b6b9-103">Named Pipe</span><span class="sxs-lookup"><span data-stu-id="8b6b9-103">Named Pipes</span></span>

<span data-ttu-id="8b6b9-104">Una *named pipe* è una pipe denominata, unidirezionale o duplex per la comunicazione tra il server pipe e uno o più client pipe.</span><span class="sxs-lookup"><span data-stu-id="8b6b9-104">A *named pipe* is a named, one-way or duplex pipe for communication between the pipe server and one or more pipe clients.</span></span> <span data-ttu-id="8b6b9-105">Tutte le istanze di un named pipe condividono lo stesso nome di pipe, ma ogni istanza ha i propri buffer e handle e fornisce un canale separato per la comunicazione client/server.</span><span class="sxs-lookup"><span data-stu-id="8b6b9-105">All instances of a named pipe share the same pipe name, but each instance has its own buffers and handles, and provides a separate conduit for client/server communication.</span></span> <span data-ttu-id="8b6b9-106">L'utilizzo delle istanze consente a più client pipe di utilizzare contemporaneamente lo stesso named pipe.</span><span class="sxs-lookup"><span data-stu-id="8b6b9-106">The use of instances enables multiple pipe clients to use the same named pipe simultaneously.</span></span>

<span data-ttu-id="8b6b9-107">Qualsiasi processo può accedere a named pipe, in base ai controlli di sicurezza, rendendo le named pipe una semplice forma di comunicazione tra processi correlati o non correlati.</span><span class="sxs-lookup"><span data-stu-id="8b6b9-107">Any process can access named pipes, subject to security checks, making named pipes an easy form of communication between related or unrelated processes.</span></span>

<span data-ttu-id="8b6b9-108">Qualsiasi processo può fungere sia da server che da client, rendendo possibile la comunicazione peer-to-peer.</span><span class="sxs-lookup"><span data-stu-id="8b6b9-108">Any process can act as both a server and a client, making peer-to-peer communication possible.</span></span> <span data-ttu-id="8b6b9-109">Come usato in questo caso, il termine pipe server fa riferimento a un processo che crea un named pipe e il termine client pipe fa riferimento a un processo che si connette a un'istanza di un named pipe.</span><span class="sxs-lookup"><span data-stu-id="8b6b9-109">As used here, the term pipe server refers to a process that creates a named pipe, and the term pipe client refers to a process that connects to an instance of a named pipe.</span></span> <span data-ttu-id="8b6b9-110">La funzione lato server per la creazione di un'istanza di un named pipe è [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).</span><span class="sxs-lookup"><span data-stu-id="8b6b9-110">The server-side function for instantiating a named pipe is [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).</span></span> <span data-ttu-id="8b6b9-111">La funzione lato server per l'accettazione di una connessione è [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span><span class="sxs-lookup"><span data-stu-id="8b6b9-111">The server-side function for accepting a connection is [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span></span> <span data-ttu-id="8b6b9-112">Un processo client si connette a un named pipe tramite la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) .</span><span class="sxs-lookup"><span data-stu-id="8b6b9-112">A client process connects to a named pipe by using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function.</span></span>

<span data-ttu-id="8b6b9-113">È possibile utilizzare le named pipe per fornire la comunicazione tra processi nello stesso computer o tra processi in computer diversi in una rete.</span><span class="sxs-lookup"><span data-stu-id="8b6b9-113">Named pipes can be used to provide communication between processes on the same computer or between processes on different computers across a network.</span></span> <span data-ttu-id="8b6b9-114">Se il servizio Server è in esecuzione, tutte le named pipe sono accessibili in remoto.</span><span class="sxs-lookup"><span data-stu-id="8b6b9-114">If the server service is running, all named pipes are accessible remotely.</span></span> <span data-ttu-id="8b6b9-115">Se si intende utilizzare un named pipe solo localmente, negare l'accesso alla rete NT AUTHORITY \\ o passare alla RPC locale.</span><span class="sxs-lookup"><span data-stu-id="8b6b9-115">If you intend to use a named pipe locally only, deny access to NT AUTHORITY\\NETWORK or switch to local RPC.</span></span>

<span data-ttu-id="8b6b9-116">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="8b6b9-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8b6b9-117">Nomi pipe</span><span class="sxs-lookup"><span data-stu-id="8b6b9-117">Pipe Names</span></span>](pipe-names.md)
-   [<span data-ttu-id="8b6b9-118">Modalità di apertura named pipe</span><span class="sxs-lookup"><span data-stu-id="8b6b9-118">Named Pipe Open Modes</span></span>](named-pipe-open-modes.md)
-   [<span data-ttu-id="8b6b9-119">Tipo di named pipe, modalità lettura e attesa</span><span class="sxs-lookup"><span data-stu-id="8b6b9-119">Named Pipe Type, Read, and Wait Modes</span></span>](named-pipe-type-read-and-wait-modes.md)
-   [<span data-ttu-id="8b6b9-120">Istanze named pipe</span><span class="sxs-lookup"><span data-stu-id="8b6b9-120">Named Pipe Instances</span></span>](named-pipe-instances.md)
-   [<span data-ttu-id="8b6b9-121">Operazioni named pipe</span><span class="sxs-lookup"><span data-stu-id="8b6b9-121">Named Pipe Operations</span></span>](named-pipe-operations.md)
-   [<span data-ttu-id="8b6b9-122">Input e output sincroni e sovrapposti</span><span class="sxs-lookup"><span data-stu-id="8b6b9-122">Synchronous and Overlapped Input and Output</span></span>](synchronous-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="8b6b9-123">Diritti di accesso e sicurezza della named pipe</span><span class="sxs-lookup"><span data-stu-id="8b6b9-123">Named Pipe Security and Access Rights</span></span>](named-pipe-security-and-access-rights.md)
-   [<span data-ttu-id="8b6b9-124">Rappresentazione di un client named pipe</span><span class="sxs-lookup"><span data-stu-id="8b6b9-124">Impersonating a Named Pipe Client</span></span>](impersonating-a-named-pipe-client.md)
-   [<span data-ttu-id="8b6b9-125">Uso di pipe</span><span class="sxs-lookup"><span data-stu-id="8b6b9-125">Using Pipes</span></span>](using-pipes.md)

 

 
