---
description: Un processo figlio può ereditare handle dal processo padre. Un handle ereditato è valido solo nel contesto del processo figlio. Per consentire a un processo figlio di ereditare gli handle aperti dal processo padre, attenersi alla procedura riportata di seguito.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Gestisci ereditarietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317661"
---
# <a name="handle-inheritance"></a><span data-ttu-id="aee1a-105">Gestisci ereditarietà</span><span class="sxs-lookup"><span data-stu-id="aee1a-105">Handle Inheritance</span></span>

<span data-ttu-id="aee1a-106">Un processo figlio può ereditare handle dal processo padre.</span><span class="sxs-lookup"><span data-stu-id="aee1a-106">A child process can inherit handles from its parent process.</span></span> <span data-ttu-id="aee1a-107">Un handle ereditato è valido solo nel contesto del processo figlio.</span><span class="sxs-lookup"><span data-stu-id="aee1a-107">An inherited handle is valid only in the context of the child process.</span></span> <span data-ttu-id="aee1a-108">Per consentire a un processo figlio di ereditare gli handle aperti dal processo padre, attenersi alla procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="aee1a-108">To enable a child process to inherit open handles from its parent process, use the following steps.</span></span>

1.  <span data-ttu-id="aee1a-109">Creare l'handle con il membro **bInheritHandle** della struttura [**degli \_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-109">Create the handle with the **bInheritHandle** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure set to **TRUE**.</span></span>
2.  <span data-ttu-id="aee1a-110">Creare il processo figlio utilizzando la funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , con il parametro *BInheritHandles* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-110">Create the child process using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, with the *bInheritHandles* parameter set to **TRUE**.</span></span>

<span data-ttu-id="aee1a-111">La funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) duplica un handle da usare nel processo corrente o in un altro processo.</span><span class="sxs-lookup"><span data-stu-id="aee1a-111">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function duplicates a handle to be used in the current process or in another process.</span></span> <span data-ttu-id="aee1a-112">Se un'applicazione Duplica uno dei relativi handle per un altro processo, l'handle duplicato è valido solo nel contesto dell'altro processo.</span><span class="sxs-lookup"><span data-stu-id="aee1a-112">If an application duplicates one of its handles for another process, the duplicated handle is valid only in the context of the other process.</span></span>

<span data-ttu-id="aee1a-113">Un handle duplicato o ereditato è un valore univoco, ma fa riferimento allo stesso oggetto dell'handle originale.</span><span class="sxs-lookup"><span data-stu-id="aee1a-113">A duplicated or inherited handle is a unique value, but it refers to the same object as the original handle.</span></span> <span data-ttu-id="aee1a-114">I processi possono ereditare o duplicare gli handle per i tipi di oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="aee1a-114">Processes can inherit or duplicate handles to the following types of objects:</span></span>

-   <span data-ttu-id="aee1a-115">Token di accesso</span><span class="sxs-lookup"><span data-stu-id="aee1a-115">Access Token</span></span>
-   <span data-ttu-id="aee1a-116">Dispositivo di comunicazione</span><span class="sxs-lookup"><span data-stu-id="aee1a-116">Communications device</span></span>
-   <span data-ttu-id="aee1a-117">Input console</span><span class="sxs-lookup"><span data-stu-id="aee1a-117">Console input</span></span>
-   <span data-ttu-id="aee1a-118">Buffer dello schermo della console</span><span class="sxs-lookup"><span data-stu-id="aee1a-118">Console screen buffer</span></span>
-   <span data-ttu-id="aee1a-119">Desktop</span><span class="sxs-lookup"><span data-stu-id="aee1a-119">Desktop</span></span>
-   <span data-ttu-id="aee1a-120">Directory</span><span class="sxs-lookup"><span data-stu-id="aee1a-120">Directory</span></span>
-   <span data-ttu-id="aee1a-121">Evento</span><span class="sxs-lookup"><span data-stu-id="aee1a-121">Event</span></span>
-   <span data-ttu-id="aee1a-122">File</span><span class="sxs-lookup"><span data-stu-id="aee1a-122">File</span></span>
-   <span data-ttu-id="aee1a-123">Mapping dei file</span><span class="sxs-lookup"><span data-stu-id="aee1a-123">File mapping</span></span>
-   <span data-ttu-id="aee1a-124">Processo</span><span class="sxs-lookup"><span data-stu-id="aee1a-124">Job</span></span>
-   <span data-ttu-id="aee1a-125">Inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="aee1a-125">Mailslot</span></span>
-   <span data-ttu-id="aee1a-126">Mutex</span><span class="sxs-lookup"><span data-stu-id="aee1a-126">Mutex</span></span>
-   <span data-ttu-id="aee1a-127">Pipe</span><span class="sxs-lookup"><span data-stu-id="aee1a-127">Pipe</span></span>
-   <span data-ttu-id="aee1a-128">Processo</span><span class="sxs-lookup"><span data-stu-id="aee1a-128">Process</span></span>
-   <span data-ttu-id="aee1a-129">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="aee1a-129">Registry key</span></span>
-   <span data-ttu-id="aee1a-130">Semaphore</span><span class="sxs-lookup"><span data-stu-id="aee1a-130">Semaphore</span></span>
-   <span data-ttu-id="aee1a-131">Presa elettrica</span><span class="sxs-lookup"><span data-stu-id="aee1a-131">Socket</span></span>
-   <span data-ttu-id="aee1a-132">Thread</span><span class="sxs-lookup"><span data-stu-id="aee1a-132">Thread</span></span>
-   <span data-ttu-id="aee1a-133">Timer</span><span class="sxs-lookup"><span data-stu-id="aee1a-133">Timer</span></span>
-   <span data-ttu-id="aee1a-134">Stazione finestra</span><span class="sxs-lookup"><span data-stu-id="aee1a-134">Window station</span></span>

<span data-ttu-id="aee1a-135">Tutti gli altri oggetti sono privati del processo che li ha creati; i rispettivi handle di oggetto non possono essere duplicati o ereditati.</span><span class="sxs-lookup"><span data-stu-id="aee1a-135">All other objects are private to the process that created them; their object handles cannot be duplicated or inherited.</span></span>

<span data-ttu-id="aee1a-136">Per altre informazioni, vedere [Ereditarietà](/windows/desktop/ProcThread/inheritance).</span><span class="sxs-lookup"><span data-stu-id="aee1a-136">For more information, see [Inheritance](/windows/desktop/ProcThread/inheritance).</span></span>

 

 
