---
description: Le applicazioni possono gestire un contesto di attivazione chiamando direttamente le funzioni del contesto di attivazione.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Uso dell'API del contesto di attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128810"
---
# <a name="using-the-activation-context-api"></a><span data-ttu-id="aa1dd-103">Uso dell'API del contesto di attivazione</span><span class="sxs-lookup"><span data-stu-id="aa1dd-103">Using the Activation Context API</span></span>

<span data-ttu-id="aa1dd-104">Le applicazioni possono gestire un [contesto di attivazione](activation-contexts.md) chiamando direttamente le funzioni del contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-104">Applications can manage an [activation context](activation-contexts.md) by directly calling the activation context functions.</span></span> <span data-ttu-id="aa1dd-105">I contesti di attivazione sono strutture dei dati in memoria.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-105">Activation contexts are data structures in memory.</span></span> <span data-ttu-id="aa1dd-106">Il sistema può utilizzare le informazioni nel contesto di attivazione per reindirizzare un'applicazione in modo da caricare una particolare versione della DLL, un'istanza dell'oggetto COM o una versione della finestra personalizzata.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-106">The system can use the information in the activation context to redirect an application to load a particular DLL version, COM object instance, or custom window version.</span></span> <span data-ttu-id="aa1dd-107">Per altre informazioni, vedere [riferimento al contesto di attivazione](activation-context-reference.md).</span><span class="sxs-lookup"><span data-stu-id="aa1dd-107">For more information, see [Activation Context Reference](activation-context-reference.md).</span></span>

<span data-ttu-id="aa1dd-108">Il Application Programming Interface (API) può essere usato per gestire il contesto di attivazione e creare oggetti con nome di versione con [manifesti](manifests.md).</span><span class="sxs-lookup"><span data-stu-id="aa1dd-108">The application programming interface (API) can be used to manage the activation context and create version-named objects with [manifests](manifests.md).</span></span> <span data-ttu-id="aa1dd-109">Nei due scenari seguenti viene illustrato il modo in cui un'applicazione può gestire un contesto di attivazione chiamando direttamente le funzioni del contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-109">The following two scenarios illustrate how an application can manage an activation context by directly calling the activation context functions.</span></span> <span data-ttu-id="aa1dd-110">Nella maggior parte dei casi, tuttavia, il contesto di attivazione è gestito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-110">In most cases however, the activation context is managed by the system.</span></span> <span data-ttu-id="aa1dd-111">Gli sviluppatori di applicazioni e i provider di assembly non devono in genere effettuare chiamate allo stack per gestire il contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-111">Application developers and assembly providers do not commonly need to make calls to the stack to manage the activation context.</span></span>

-   <span data-ttu-id="aa1dd-112">Processi e applicazioni che implementano livelli di riferimento indiretto o di invio.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-112">Processes and applications that implement indirection or dispatch layers.</span></span>

    <span data-ttu-id="aa1dd-113">Ad esempio, un utente che gestisce i contesti di attivazione nel ciclo di eventi.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-113">For example, a user managing activation contexts in the event loop.</span></span> <span data-ttu-id="aa1dd-114">Ogni volta che si accede alla finestra, ad esempio spostando il puntatore del mouse sulla finestra, viene chiamato [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) , che attiva il contesto di attivazione corrente per la risorsa, come illustrato nel frammento di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-114">Each time the window is accessed, such as by moving the mouse over the window, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) is called, which activates the current activation context for the resource, as shown in the following code fragment.</span></span>

    <dl> <span data-ttu-id="aa1dd-115">GESTISCi hActCtx;</span><span class="sxs-lookup"><span data-stu-id="aa1dd-115">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="aa1dd-116">CreateWindow ();</span><span class="sxs-lookup"><span data-stu-id="aa1dd-116">CreateWindow();</span></span>  
    <span data-ttu-id="aa1dd-117">...</span><span class="sxs-lookup"><span data-stu-id="aa1dd-117">...</span></span>  
    <span data-ttu-id="aa1dd-118">GetCurrentActCtx (&ActCtx);</span><span class="sxs-lookup"><span data-stu-id="aa1dd-118">GetCurrentActCtx(&ActCtx);</span></span>  
    <span data-ttu-id="aa1dd-119">...</span><span class="sxs-lookup"><span data-stu-id="aa1dd-119">...</span></span>  
    <span data-ttu-id="aa1dd-120">ReleaseActCtx (&ActCtx);</span><span class="sxs-lookup"><span data-stu-id="aa1dd-120">ReleaseActCtx(&ActCtx);</span></span>  
    </dl>

    <span data-ttu-id="aa1dd-121">Nel frammento di codice seguente la funzione API attiva i contesti di attivazione appropriati prima di chiamare [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span><span class="sxs-lookup"><span data-stu-id="aa1dd-121">In the following code fragment, the API function activates the appropriate activation contexts before calling [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span></span> <span data-ttu-id="aa1dd-122">Quando viene chiamato **CallWindowProc** , questo contesto viene usato per passare un messaggio a Windows.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-122">When **CallWindowProc** is called, it uses this context to pass a message to Windows.</span></span> <span data-ttu-id="aa1dd-123">Al termine di tutte le operazioni sulle risorse, la funzione disattiverà il contesto.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-123">When all resource operations have completed, the function will deactivate the context.</span></span>

    <dl> <span data-ttu-id="aa1dd-124">\_UlpCookie PTR ULONG;</span><span class="sxs-lookup"><span data-stu-id="aa1dd-124">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="aa1dd-125">GESTISCi hActCtx;</span><span class="sxs-lookup"><span data-stu-id="aa1dd-125">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="aa1dd-126">if (ActivateActCtx (hActCtx, &ulpCookie))</span><span class="sxs-lookup"><span data-stu-id="aa1dd-126">if(ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="aa1dd-127">{</span><span class="sxs-lookup"><span data-stu-id="aa1dd-127">{</span></span>  
    <span data-ttu-id="aa1dd-128">...</span><span class="sxs-lookup"><span data-stu-id="aa1dd-128">...</span></span>  
    <span data-ttu-id="aa1dd-129">CallWindowProc (...);</span><span class="sxs-lookup"><span data-stu-id="aa1dd-129">CallWindowProc(...);</span></span>  
    <span data-ttu-id="aa1dd-130">...</span><span class="sxs-lookup"><span data-stu-id="aa1dd-130">...</span></span>  
    <span data-ttu-id="aa1dd-131">DeactivateActCtx (0, ulpCookie);</span><span class="sxs-lookup"><span data-stu-id="aa1dd-131">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="aa1dd-132">}</span><span class="sxs-lookup"><span data-stu-id="aa1dd-132">}</span></span>  
    </dl>

-   <span data-ttu-id="aa1dd-133">Livello di invio del delegato.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-133">Delegator dispatch layer.</span></span>

    <span data-ttu-id="aa1dd-134">Questo scenario si applica ai manager che gestiscono più entità con un livello API comune, ad esempio una gestione driver.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-134">This scenario applies to managers that manage multiple entities with a common API layer, such as a driver manager.</span></span> <span data-ttu-id="aa1dd-135">Sebbene non sia ancora stato implementato, un esempio è costituito dal driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-135">Although it has not yet been implemented, an example of this would be the ODBC driver.</span></span>

    <span data-ttu-id="aa1dd-136">In questo scenario, il livello intermedio diventa in grado di elaborare le associazioni di assembly.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-136">In this scenario, the middle layer becomes capable of processing assembly bindings.</span></span> <span data-ttu-id="aa1dd-137">Per ottenere il driver di associazione specifico della versione, è necessario che i Publisher forniscano un manifesto e specifichino le dipendenze da componenti specifici del manifesto.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-137">To get the version-specific binding driver, publishers must provide a manifest and specify dependencies on specific components in that manifest.</span></span> <span data-ttu-id="aa1dd-138">L'applicazione di base non esegue un'associazione dinamica ai componenti; in fase di esecuzione, gestione driver gestisce le chiamate.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-138">The base application does not dynamically bind to the components; at run time, the driver manager manages the calls.</span></span> <span data-ttu-id="aa1dd-139">Quando il driver ODBC viene chiamato in base alla stringa di connessione, carica il driver appropriato.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-139">When the ODBC driver is called based on the connect string it loads the appropriate driver.</span></span> <span data-ttu-id="aa1dd-140">Quindi crea il contesto di attivazione usando le informazioni contenute nel file manifesto dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-140">It then creates the activation context using the information in the assembly manifest file.</span></span>

    <span data-ttu-id="aa1dd-141">Senza il manifesto, l'azione predefinita per il driver prevede l'uso dello stesso contesto di quello specificato dall'applicazione, in questo esempio la versione 2 di MSVCRT.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-141">Without the manifest, the default action for the driver is to use the same context as that specified by the application—in this example, version 2 of MSVCRT.</span></span> <span data-ttu-id="aa1dd-142">Poiché un manifesto esiste, viene stabilito un contesto di attivazione separato.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-142">Since a manifest does exist, a separate activation context is established.</span></span> <span data-ttu-id="aa1dd-143">Quando il driver ODBC viene eseguito, viene associato alla versione 1 dell'assembly MSVCRT.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-143">When the ODBC driver runs, it binds to version 1 of the MSVCRT assembly.</span></span>

    <span data-ttu-id="aa1dd-144">Ogni volta che Gestione driver chiama il livello di invio, ad esempio per ottenere il set di dati successivo, USA gli assembly appropriati in base al contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-144">Each time the driver manager calls the dispatch layer—for example, to get the next set of data—it uses the appropriate assemblies based on the activation context.</span></span> <span data-ttu-id="aa1dd-145">Il frammento di codice seguente illustra questa operazione.</span><span class="sxs-lookup"><span data-stu-id="aa1dd-145">The following code fragment illustrates this.</span></span>

    <dl> <span data-ttu-id="aa1dd-146">GESTISCi hActCtx;</span><span class="sxs-lookup"><span data-stu-id="aa1dd-146">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="aa1dd-147">\_UlpCookie PTR ULONG;</span><span class="sxs-lookup"><span data-stu-id="aa1dd-147">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="aa1dd-148">ACTCTX ActCtxToCreate = {...};</span><span class="sxs-lookup"><span data-stu-id="aa1dd-148">ACTCTX ActCtxToCreate = {...};</span></span>  
    <span data-ttu-id="aa1dd-149">hActCtx = CreateActCtx (&ActCtxToCreate);</span><span class="sxs-lookup"><span data-stu-id="aa1dd-149">hActCtx = CreateActCtx(&ActCtxToCreate);</span></span>  
    <span data-ttu-id="aa1dd-150">...;</span><span class="sxs-lookup"><span data-stu-id="aa1dd-150">...;</span></span>  
    <span data-ttu-id="aa1dd-151">if (ActivateActCtx (hActCtx, &ulpCookie))</span><span class="sxs-lookup"><span data-stu-id="aa1dd-151">if (ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="aa1dd-152">{</span><span class="sxs-lookup"><span data-stu-id="aa1dd-152">{</span></span>  
    <span data-ttu-id="aa1dd-153">...</span><span class="sxs-lookup"><span data-stu-id="aa1dd-153">...</span></span>  
    <span data-ttu-id="aa1dd-154">ConnectDb(...);</span><span class="sxs-lookup"><span data-stu-id="aa1dd-154">ConnectDb(...);</span></span>  
    <span data-ttu-id="aa1dd-155">DeactivateActCtx (0, ulpCookie);</span><span class="sxs-lookup"><span data-stu-id="aa1dd-155">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="aa1dd-156">}</span><span class="sxs-lookup"><span data-stu-id="aa1dd-156">}</span></span>  
    <span data-ttu-id="aa1dd-157">...</span><span class="sxs-lookup"><span data-stu-id="aa1dd-157">...</span></span>  
    <span data-ttu-id="aa1dd-158">ReleaseActCtx(hActCtx);</span><span class="sxs-lookup"><span data-stu-id="aa1dd-158">ReleaseActCtx(hActCtx);</span></span>  
    </dl>

 

 
