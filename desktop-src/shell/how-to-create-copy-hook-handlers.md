---
description: Uso delle estensioni della Shell per implementare un gestore di hook di copia.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Come creare gestori di hook di copia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227439"
---
# <a name="how-to-create-copy-hook-handlers"></a><span data-ttu-id="91c9c-103">Come creare gestori di hook di copia</span><span class="sxs-lookup"><span data-stu-id="91c9c-103">How to Create Copy Hook Handlers</span></span>

<span data-ttu-id="91c9c-104">Le procedure generali per l'implementazione e la registrazione di un gestore di estensione della shell sono descritte in [creazione di gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="91c9c-104">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="91c9c-105">Questo documento è incentrato sugli aspetti dell'implementazione specifici dei gestori di hook di copia.</span><span class="sxs-lookup"><span data-stu-id="91c9c-105">This document focuses on those aspects of implementation that are specific to copy hook handlers.</span></span>

-   [<span data-ttu-id="91c9c-106">Implementazione di gestori di hook di copia</span><span class="sxs-lookup"><span data-stu-id="91c9c-106">Implementing Copy Hook Handlers</span></span>](#step-1-implementing-copy-hook-handlers)
-   [<span data-ttu-id="91c9c-107">Registrazione di gestori di hook di copia</span><span class="sxs-lookup"><span data-stu-id="91c9c-107">Registering Copy Hook Handlers</span></span>](#step-2-registering-copy-hook-handlers)
-   [<span data-ttu-id="91c9c-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91c9c-108">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="91c9c-109">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="91c9c-109">Instructions</span></span>

### <a name="step-1-implementing-copy-hook-handlers"></a><span data-ttu-id="91c9c-110">Passaggio 1: implementazione di gestori di hook di copia</span><span class="sxs-lookup"><span data-stu-id="91c9c-110">Step 1: Implementing Copy Hook Handlers</span></span>

<span data-ttu-id="91c9c-111">Come tutti i gestori di estensioni della shell, i gestori di hook di copia sono oggetti COM (Component Object Model in-process) implementati come dll.</span><span class="sxs-lookup"><span data-stu-id="91c9c-111">Like all Shell extension handlers, copy hook handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="91c9c-112">Esportano un'interfaccia oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="91c9c-112">They export one interface in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span></span> <span data-ttu-id="91c9c-113">La shell Inizializza direttamente il gestore, pertanto non è necessaria un'interfaccia di inizializzazione, ad esempio [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span><span class="sxs-lookup"><span data-stu-id="91c9c-113">The Shell initializes the handler directly, so there is no need for an initialization interface such as [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span></span>

<span data-ttu-id="91c9c-114">L'interfaccia [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) ha un singolo metodo, [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="91c9c-114">The [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) interface has a single method, [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span></span> <span data-ttu-id="91c9c-115">Quando una cartella sta per essere spostata, la shell chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="91c9c-115">When a folder is about to be moved, the Shell calls this method.</span></span> <span data-ttu-id="91c9c-116">Viene passata una serie di informazioni, tra cui:</span><span class="sxs-lookup"><span data-stu-id="91c9c-116">It passes in a variety of information, including:</span></span>

-   <span data-ttu-id="91c9c-117">Nome della cartella.</span><span class="sxs-lookup"><span data-stu-id="91c9c-117">The folder's name.</span></span>
-   <span data-ttu-id="91c9c-118">Destinazione o nuovo nome della cartella.</span><span class="sxs-lookup"><span data-stu-id="91c9c-118">The folder's destination or new name.</span></span>
-   <span data-ttu-id="91c9c-119">Operazione tentata.</span><span class="sxs-lookup"><span data-stu-id="91c9c-119">The operation that is being attempted.</span></span>
-   <span data-ttu-id="91c9c-120">Attributi delle cartelle di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="91c9c-120">The attributes of the source and destination folders.</span></span>
-   <span data-ttu-id="91c9c-121">Handle di finestra che può essere utilizzato per visualizzare un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="91c9c-121">A window handle that can be used to display a user interface.</span></span>

<span data-ttu-id="91c9c-122">Quando viene chiamato il metodo [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) del gestore, viene restituito uno dei tre valori seguenti per indicare alla shell come procedere.</span><span class="sxs-lookup"><span data-stu-id="91c9c-122">When your handler's [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) method is called, it returns one of the three following values to indicate to the Shell how it should proceed.</span></span>



| <span data-ttu-id="91c9c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="91c9c-123">Value</span></span>    | <span data-ttu-id="91c9c-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91c9c-124">Description</span></span>                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c9c-125">IDYES</span><span class="sxs-lookup"><span data-stu-id="91c9c-125">IDYES</span></span>    | <span data-ttu-id="91c9c-126">Consente l'operazione.</span><span class="sxs-lookup"><span data-stu-id="91c9c-126">Allows the operation.</span></span>                                                                                                                            |
| <span data-ttu-id="91c9c-127">IDNO</span><span class="sxs-lookup"><span data-stu-id="91c9c-127">IDNO</span></span>     | <span data-ttu-id="91c9c-128">Impedisce l'operazione in questa cartella.</span><span class="sxs-lookup"><span data-stu-id="91c9c-128">Prevents the operation on this folder.</span></span> <span data-ttu-id="91c9c-129">La shell può continuare con qualsiasi altra operazione approvata, ad esempio un'operazione di copia batch.</span><span class="sxs-lookup"><span data-stu-id="91c9c-129">The Shell can continue with any other operations that have been approved, such as a batch copy operation.</span></span> |
| <span data-ttu-id="91c9c-130">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="91c9c-130">IDCANCEL</span></span> | <span data-ttu-id="91c9c-131">Impedisce l'operazione corrente e Annulla tutte le operazioni in sospeso.</span><span class="sxs-lookup"><span data-stu-id="91c9c-131">Prevents the current operation and cancels any pending operations.</span></span>                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a><span data-ttu-id="91c9c-132">Passaggio 2: registrazione di gestori di hook di copia</span><span class="sxs-lookup"><span data-stu-id="91c9c-132">Step 2: Registering Copy Hook Handlers</span></span>

<span data-ttu-id="91c9c-133">I gestori di hook di copia per le cartelle sono registrati nella **\_ \_** \\  \\  \\ sottochiave shellex **CopyHookHandlers** della directory radice delle classi HKEY.</span><span class="sxs-lookup"><span data-stu-id="91c9c-133">Copy hook handlers for folders are registered under the **HKEY\_CLASSES\_ROOT**\\**Directory**\\**shellex**\\**CopyHookHandlers** subkey.</span></span> <span data-ttu-id="91c9c-134">Creare una sottochiave di **CopyHookHandlers** denominata per il gestore, quindi impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe del gestore (CLSID).</span><span class="sxs-lookup"><span data-stu-id="91c9c-134">Create a subkey of **CopyHookHandlers** named for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="91c9c-135">Nell'esempio seguente la sottochiave **MyCopyHandler** viene aggiunta all'elenco di gestori di hook di copia della shell.</span><span class="sxs-lookup"><span data-stu-id="91c9c-135">The following example adds the **MyCopyHandler** subkey to the Shell's list of copy hook handlers.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

<span data-ttu-id="91c9c-136">I gestori di hook di copia per gli oggetti stampante sono registrati in modo sostanzialmente analogo.</span><span class="sxs-lookup"><span data-stu-id="91c9c-136">Copy hook handlers for printer objects are registered in essentially the same way.</span></span> <span data-ttu-id="91c9c-137">L'unica differenza è che è necessario registrarli nella sottochiave delle stampanti **\_ \_ radice delle classi HKEY** \\  .</span><span class="sxs-lookup"><span data-stu-id="91c9c-137">The only difference is that you must register them under the **HKEY\_CLASSES\_ROOT**\\**Printers** subkey.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c9c-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="91c9c-138">Remarks</span></span>

<span data-ttu-id="91c9c-139">In genere, gli utenti e le applicazioni possono copiare, spostare, eliminare o rinominare cartelle con poche restrizioni.</span><span class="sxs-lookup"><span data-stu-id="91c9c-139">Normally, users and applications can copy, move, delete, or rename folders with few restrictions.</span></span> <span data-ttu-id="91c9c-140">Implementando un gestore di hook di copia, è possibile controllare se queste operazioni vengono eseguite.</span><span class="sxs-lookup"><span data-stu-id="91c9c-140">By implementing a copy hook handler, you can control whether these operations take place.</span></span> <span data-ttu-id="91c9c-141">Ad esempio, l'implementazione di un gestore di questo tipo consente di impedire la ridenominazione o l'eliminazione di cartelle critiche.</span><span class="sxs-lookup"><span data-stu-id="91c9c-141">For instance, implementing such a handler allows you to prevent critical folders from being renamed or deleted.</span></span> <span data-ttu-id="91c9c-142">I gestori di hook di copia possono essere implementati anche per gli oggetti Printer.</span><span class="sxs-lookup"><span data-stu-id="91c9c-142">Copy hook handlers can also be implemented for printer objects.</span></span>

<span data-ttu-id="91c9c-143">I gestori di hook di copia sono globali.</span><span class="sxs-lookup"><span data-stu-id="91c9c-143">Copy hook handlers are global.</span></span> <span data-ttu-id="91c9c-144">La shell chiama tutti i gestori registrati ogni volta che un'applicazione o un utente tenta di copiare, spostare, eliminare o rinominare una cartella o un oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="91c9c-144">The Shell calls all registered handlers every time an application or user attempts to copy, move, delete, or rename a folder or printer object.</span></span> <span data-ttu-id="91c9c-145">Il gestore non esegue l'operazione stessa.</span><span class="sxs-lookup"><span data-stu-id="91c9c-145">The handler does not perform the operation itself.</span></span> <span data-ttu-id="91c9c-146">Viene approvata o bloccata.</span><span class="sxs-lookup"><span data-stu-id="91c9c-146">It only approves or vetoes it.</span></span> <span data-ttu-id="91c9c-147">Se tutti i gestori approvano, la shell esegue l'operazione.</span><span class="sxs-lookup"><span data-stu-id="91c9c-147">If all handlers approve, the Shell does the operation.</span></span> <span data-ttu-id="91c9c-148">Se un gestore oppone l'operazione, viene annullato e i gestori rimanenti non vengono chiamati.</span><span class="sxs-lookup"><span data-stu-id="91c9c-148">If any handler vetoes the operation, it is canceled and the remaining handlers are not called.</span></span> <span data-ttu-id="91c9c-149">I gestori di hook di copia non sono informati dell'esito positivo o negativo dell'operazione, quindi non possono essere usati per monitorare le operazioni sui file.</span><span class="sxs-lookup"><span data-stu-id="91c9c-149">Copy hook handlers are not informed of the success or failure of the operation, so they cannot be used to monitor file operations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91c9c-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91c9c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91c9c-151">Creazione di gestori di estensione della shell</span><span class="sxs-lookup"><span data-stu-id="91c9c-151">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

<span data-ttu-id="91c9c-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91c9c-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span></span>
</dt> </dl>

 

 
