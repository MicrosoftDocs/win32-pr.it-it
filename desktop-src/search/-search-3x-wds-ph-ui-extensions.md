---
description: Per assicurarsi che i dati vengano indicizzati e presentati correttamente all'utente durante le ricerche, è necessario implementare gli archivi dati della shell (noti anche come estensioni dello spazio dei nomi della Shell) e i gestori di tipi di file (noti anche come estensioni della shell, gestori di estensioni o gestori di estensioni della Shell).
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: Aggiunta di icone, anteprime e menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525531"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a><span data-ttu-id="d63bd-103">Aggiunta di icone, anteprime e menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="d63bd-103">Adding Icons, Previews and Shortcut Menus</span></span>

<span data-ttu-id="d63bd-104">Per assicurarsi che i dati vengano indicizzati e presentati correttamente all'utente durante le ricerche, è necessario implementare gli archivi dati della shell (noti anche come [estensioni dello spazio dei nomi della shell](../shell/nse-works.md)) e i gestori di tipi di file (noti anche come estensioni della shell, [gestori](../shell/handlers.md)di estensioni o gestori di estensioni della Shell).</span><span class="sxs-lookup"><span data-stu-id="d63bd-104">To ensure that your data is indexed and presented correctly to the user during searches, you need to implement Shell data stores (also known as [Shell Namespace Extensions](../shell/nse-works.md)), and file type handlers (also known as Shell extensions, [extension handlers](../shell/handlers.md), or Shell extension handlers).</span></span>

<span data-ttu-id="d63bd-105">In questo argomento vengono descritte le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="d63bd-105">This topic describes the following interfaces:</span></span>

-   [<span data-ttu-id="d63bd-106">Implementazione di gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="d63bd-106">Implementing File Type Handlers</span></span>](#implementing-file-type-handlers)
    -   [<span data-ttu-id="d63bd-107">IPersist</span><span class="sxs-lookup"><span data-stu-id="d63bd-107">IPersist</span></span>](#ipersist)
    -   [<span data-ttu-id="d63bd-108">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="d63bd-108">IPersistFolder</span></span>](#ipersistfolder)
    -   [<span data-ttu-id="d63bd-109">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="d63bd-109">IShellFolder</span></span>](#ishellfolder)
    -   [<span data-ttu-id="d63bd-110">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="d63bd-110">IContextMenu</span></span>](#icontextmenu)
    -   [<span data-ttu-id="d63bd-111">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="d63bd-111">IExtractIcon</span></span>](#iextracticon)
    -   [<span data-ttu-id="d63bd-112">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="d63bd-112">IPreviewHandler</span></span>](#ipreviewhandler)
-   [<span data-ttu-id="d63bd-113">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="d63bd-113">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="d63bd-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d63bd-114">Related topics</span></span>](#related-topics)

## <a name="implementing-file-type-handlers"></a><span data-ttu-id="d63bd-115">Implementazione di gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="d63bd-115">Implementing File Type Handlers</span></span>

<span data-ttu-id="d63bd-116">Queste estensioni della shell o gestori di tipi di file forniscono agli utenti le seguenti esperienze della shell:</span><span class="sxs-lookup"><span data-stu-id="d63bd-116">These Shell extensions or file type handlers provide your users with the following Shell experiences:</span></span>

-   <span data-ttu-id="d63bd-117">La visualizzazione dei risultati Visualizza un'icona specifica per il tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="d63bd-117">The results view displays a specific icon for your item type.</span></span>
-   <span data-ttu-id="d63bd-118">La visualizzazione risultati Visualizza un'anteprima dell'elemento quando l'utente seleziona l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d63bd-118">The results view displays a preview of the item when the user selects the item.</span></span>
-   <span data-ttu-id="d63bd-119">Gli utenti possono fare doppio clic sugli elementi per avviare eventi quali l'apertura del file.</span><span class="sxs-lookup"><span data-stu-id="d63bd-119">Users can double-click items to initiate events such as opening the file.</span></span>
-   <span data-ttu-id="d63bd-120">Gli utenti possono fare clic con il pulsante destro del mouse sugli elementi per accedere a un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="d63bd-120">Users can right-click items to access a shortcut (context) menu.</span></span>
-   <span data-ttu-id="d63bd-121">Gli utenti possono trascinare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="d63bd-121">Users can drag-and-drop items.</span></span>

<span data-ttu-id="d63bd-122">Come tutti gli oggetti Component Object Model (COM), i gestori di tipi di file devono implementare un'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) e una class factory.</span><span class="sxs-lookup"><span data-stu-id="d63bd-122">Like all Component Object Model (COM) objects, file type handlers must implement an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a class factory.</span></span>

<span data-ttu-id="d63bd-123">In Windows XP o versioni precedenti, i gestori devono implementare anche:</span><span class="sxs-lookup"><span data-stu-id="d63bd-123">In Windows XP or earlier, handlers should also implement:</span></span>

-   <span data-ttu-id="d63bd-124">[Interfaccia IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span><span class="sxs-lookup"><span data-stu-id="d63bd-124">Either [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span></span>
-   <span data-ttu-id="d63bd-125">O [interfaccia IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span><span class="sxs-lookup"><span data-stu-id="d63bd-125">Or [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span></span>

<span data-ttu-id="d63bd-126">In Windows Vista, l'interfaccia [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e l' [interfaccia IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) sono state sostituite dalle tre interfacce seguenti per la Shell per inizializzare il gestore:</span><span class="sxs-lookup"><span data-stu-id="d63bd-126">In Windows Vista, [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) were replaced by the following three interfaces for Shell to initialize the handler:</span></span>

-   [<span data-ttu-id="d63bd-127">Interfaccia IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="d63bd-127">IInitializeWithStream Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="d63bd-128">Interfaccia IInitializeWithItem</span><span class="sxs-lookup"><span data-stu-id="d63bd-128">IInitializeWithItem Interface</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="d63bd-129">Interfaccia IInitializeWithFile</span><span class="sxs-lookup"><span data-stu-id="d63bd-129">IInitializeWithFile Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="d63bd-130">Per offrire un'esperienza utente ragionevole, è necessario fornire un archivio dati della shell con il gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="d63bd-130">To provide a reasonable user experience you must provide a Shell data store with your protocol handler.</span></span> <span data-ttu-id="d63bd-131">Tale archivio dati funge quindi da "Factory" per i gestori di icone, i gestori di menu di scelta rapida, i gestori di anteprime e così via.</span><span class="sxs-lookup"><span data-stu-id="d63bd-131">That data store then serves as the "factory" for icon handlers, shortcut menu handlers, preview handlers, and so forth.</span></span> <span data-ttu-id="d63bd-132">Le implementazioni minime dell'interfaccia [IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist) e dell'interfaccia [IPersistFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) sono richieste dall' [interfaccia IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)ed è necessaria un'implementazione minima dell'interfaccia IShellFolder per [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) e [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span><span class="sxs-lookup"><span data-stu-id="d63bd-132">Minimal implementations of [IPersist Interface](/windows/desktop/api/objidl/nn-objidl-ipersist) and [IPersistFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) are required by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), and a minimal implementation of IShellFolder Interface is required for the [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) and [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span></span>

> [!Note]  
> <span data-ttu-id="d63bd-133">È necessario implementare lo stesso identificatore di classe (CLSID) per **IPersist**, **IPersistFolder** e **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="d63bd-133">The same class identifier (CLSID) should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="d63bd-134">Per ulteriori informazioni sulla creazione di un archivio dati della Shell per supportare un gestore di protocollo, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d63bd-134">For more information about creating a Shell data store to support a protocol handler, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

### <a name="ipersist"></a><span data-ttu-id="d63bd-135">IPersist</span><span class="sxs-lookup"><span data-stu-id="d63bd-135">IPersist</span></span>

<span data-ttu-id="d63bd-136">L'interfaccia **IPersist** definisce il singolo metodo **GetClassID**, progettato per fornire il CLSID di un oggetto che può essere archiviato in modo permanente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="d63bd-136">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="d63bd-137">Metodo</span><span class="sxs-lookup"><span data-stu-id="d63bd-137">Method</span></span>     | <span data-ttu-id="d63bd-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d63bd-138">Description</span></span>                                      |
|------------|--------------------------------------------------|
| <span data-ttu-id="d63bd-139">GetClassID</span><span class="sxs-lookup"><span data-stu-id="d63bd-139">GetClassID</span></span> | <span data-ttu-id="d63bd-140">Restituisce il CLSID dell'oggetto archivio dati della shell</span><span class="sxs-lookup"><span data-stu-id="d63bd-140">Returns the CLSID of the Shell data store object</span></span> |



 

### <a name="ipersistfolder"></a><span data-ttu-id="d63bd-141">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="d63bd-141">IPersistFolder</span></span>

<span data-ttu-id="d63bd-142">L'interfaccia **IPersistFolder** viene utilizzata per inizializzare gli oggetti cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="d63bd-142">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="d63bd-143">L'implementazione di questa interfaccia, derivata da **IPersist**, è il modo in cui viene indicato alla cartella dove si trova nello spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="d63bd-143">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span> <span data-ttu-id="d63bd-144">Questa interfaccia non viene usata direttamente.</span><span class="sxs-lookup"><span data-stu-id="d63bd-144">You do not use this interface directly.</span></span> <span data-ttu-id="d63bd-145">Viene usato dall'implementazione file system del [metodo IShellFolder:: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) Quando Inizializza un oggetto cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="d63bd-145">It is used by the file system implementation of [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) when it initializes a Shell folder object.</span></span>



| <span data-ttu-id="d63bd-146">Metodo</span><span class="sxs-lookup"><span data-stu-id="d63bd-146">Method</span></span>     | <span data-ttu-id="d63bd-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d63bd-147">Description</span></span>                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d63bd-148">Inizializzare</span><span class="sxs-lookup"><span data-stu-id="d63bd-148">Initialize</span></span> | <span data-ttu-id="d63bd-149">Indica a un oggetto cartella della shell di inizializzarsi in base alle informazioni passate e restituisce \_ OK</span><span class="sxs-lookup"><span data-stu-id="d63bd-149">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

### <a name="ishellfolder"></a><span data-ttu-id="d63bd-150">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="d63bd-150">IShellFolder</span></span>

<span data-ttu-id="d63bd-151">L'interfaccia [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) viene utilizzata per gestire le cartelle ed è necessaria un'implementazione parziale in modo che l'icona e le interfacce di contesto implementate per un gestore di protocollo si comportino correttamente nell'interfaccia utente dei risultati di Windows Search.</span><span class="sxs-lookup"><span data-stu-id="d63bd-151">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Search results user interface.</span></span> <span data-ttu-id="d63bd-152">La maggior parte delle funzionalità richieste viene esposta tramite il metodo **GetUIObjectOf** .</span><span class="sxs-lookup"><span data-stu-id="d63bd-152">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="d63bd-153">Questo metodo consente a un componente aggiuntivo di eseguire una query per le interfacce **IExtractIcon** e **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="d63bd-153">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="d63bd-154">L'interfaccia [IShellFolder interfaccia](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) USA PIDL anziché URL.</span><span class="sxs-lookup"><span data-stu-id="d63bd-154">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="d63bd-155">Diversamente dai requisiti di un archivio dati Shell completo, i componenti aggiuntivi possono utilizzare una semplice struttura IDL che contiene solo l'URL.</span><span class="sxs-lookup"><span data-stu-id="d63bd-155">In contrast to the requirements of a complete Shell data store, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="d63bd-156">È necessario implementare i metodi seguenti dell' [interfaccia IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="d63bd-156">The following methods of [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) must be implemented.</span></span> <span data-ttu-id="d63bd-157">Cinque di questi metodi richiedono un'implementazione minima.</span><span class="sxs-lookup"><span data-stu-id="d63bd-157">Five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="d63bd-158">Metodo</span><span class="sxs-lookup"><span data-stu-id="d63bd-158">Method</span></span>           | <span data-ttu-id="d63bd-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d63bd-159">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d63bd-160">BindToObject</span><span class="sxs-lookup"><span data-stu-id="d63bd-160">BindToObject</span></span>     | <span data-ttu-id="d63bd-161">Restituisce E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="d63bd-161">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d63bd-162">BindToStorage</span><span class="sxs-lookup"><span data-stu-id="d63bd-162">BindToStorage</span></span>    | <span data-ttu-id="d63bd-163">Restituisce E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="d63bd-163">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d63bd-164">CreateViewObject</span><span class="sxs-lookup"><span data-stu-id="d63bd-164">CreateViewObject</span></span> | <span data-ttu-id="d63bd-165">Restituisce E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="d63bd-165">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d63bd-166">SetNameOf</span><span class="sxs-lookup"><span data-stu-id="d63bd-166">SetNameOf</span></span>        | <span data-ttu-id="d63bd-167">Restituisce E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="d63bd-167">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d63bd-168">ParseDisplayName</span><span class="sxs-lookup"><span data-stu-id="d63bd-168">ParseDisplayName</span></span> | <span data-ttu-id="d63bd-169">Converte un URL nella struttura PIDL</span><span class="sxs-lookup"><span data-stu-id="d63bd-169">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="d63bd-170">CompareIDs</span><span class="sxs-lookup"><span data-stu-id="d63bd-170">CompareIDs</span></span>       | <span data-ttu-id="d63bd-171">Confronta due valori PIDL</span><span class="sxs-lookup"><span data-stu-id="d63bd-171">Compares two PIDL values</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d63bd-172">GetDisplayNameOf</span><span class="sxs-lookup"><span data-stu-id="d63bd-172">GetDisplayNameOf</span></span> | <span data-ttu-id="d63bd-173">Restituisce l'URL per un PIDL</span><span class="sxs-lookup"><span data-stu-id="d63bd-173">Returns the URL for a PIDL</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d63bd-174">GetUIObjectOf</span><span class="sxs-lookup"><span data-stu-id="d63bd-174">GetUIObjectOf</span></span>    | <span data-ttu-id="d63bd-175">Questo metodo è simile al [metodo IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="d63bd-175">This method is similar to the [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="d63bd-176">Se viene richiesta un'icona, il chiamante richiede l'IID \_ IExtractIcon; se viene richiesto un menu di scelta rapida, il chiamante richiede l'IID \_ IContextMenu</span><span class="sxs-lookup"><span data-stu-id="d63bd-176">If an icon is requested, the caller requests the IID\_IExtractIcon; if a shortcut menu is requested, the caller requests the IID\_IContextMenu</span></span> |



 

<span data-ttu-id="d63bd-177">**IShellFolder** non viene utilizzato per enumerare le cartelle.</span><span class="sxs-lookup"><span data-stu-id="d63bd-177">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="d63bd-178">Ciò significa che il nome visualizzato di una cartella sarà l'URL fisico.</span><span class="sxs-lookup"><span data-stu-id="d63bd-178">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="d63bd-179">Questo potrebbe cambiare in futuro.</span><span class="sxs-lookup"><span data-stu-id="d63bd-179">This may change in the future.</span></span>

### <a name="icontextmenu"></a><span data-ttu-id="d63bd-180">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="d63bd-180">IContextMenu</span></span>

<span data-ttu-id="d63bd-181">Quando Windows Search Visualizza i risultati per l'utente, l'utente può fare clic con il pulsante destro del mouse su un elemento e visualizzare un menu di scelta rapida definito dall'interfaccia **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="d63bd-181">When Windows Search displays results to the user, the user can right-click an item and see a shortcut menu defined by your **IContextMenu** interface.</span></span> <span data-ttu-id="d63bd-182">I menu di scelta rapida sono noti anche come menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="d63bd-182">Shortcut menus are also known as context menus.</span></span>

<span data-ttu-id="d63bd-183">L'azione predefinita nel menu di scelta rapida è identica a quella eseguita quando si fa doppio clic sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="d63bd-183">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="d63bd-184">Senza le interfacce **IShellFolder** o **IContextMenu** corrispondenti per l'elemento, il comportamento predefinito per un evento di doppio clic consiste nel passare l'URL come argomento alla funzione della [funzione ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="d63bd-184">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the [ShellExecute Function](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function.</span></span>

<span data-ttu-id="d63bd-185">Per ulteriori informazioni sulla creazione di gestori di menu di scelta rapida e per le [estensioni shell per i gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md) per il codice di esempio, vedere [creazione di gestori di menu](../shell/context-menu-handlers.md) di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="d63bd-185">Refer to [Creating Context Menu Handlers](../shell/context-menu-handlers.md) for more information on creating shortcut menu handlers, and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="iextracticon"></a><span data-ttu-id="d63bd-186">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="d63bd-186">IExtractIcon</span></span>

<span data-ttu-id="d63bd-187">**IExtractIcon** recupera un'icona per l'interfaccia utente di Windows Search basata sull'URL nel PIDL fornito dal gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="d63bd-187">**IExtractIcon** retrieves an icon for the Windows Search user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

<span data-ttu-id="d63bd-188">Per ulteriori informazioni sulla creazione di gestori di icone ed [esempi: estensioni della Shell per i gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md) per il codice di esempio, vedere [creazione di gestori di icone](../shell/how-to-create-icon-handlers.md) .</span><span class="sxs-lookup"><span data-stu-id="d63bd-188">Refer to [Creating Icon Handlers](../shell/how-to-create-icon-handlers.md) for more information on creating icon handlers and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="ipreviewhandler"></a><span data-ttu-id="d63bd-189">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="d63bd-189">IPreviewHandler</span></span>

<span data-ttu-id="d63bd-190">[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) esegue il rendering di un'anteprima dettagliata di un elemento selezionato in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="d63bd-190">The [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) renders a rich preview of a selected item in Windows Explorer.</span></span> <span data-ttu-id="d63bd-191">Le anteprime sono disponibili in Windows Search 4,0 o in Windows Vista con Windows Desktop Search 3. x.</span><span class="sxs-lookup"><span data-stu-id="d63bd-191">Previews are available in Windows Search 4.0, or in Windows Vista with Windows Desktop Search 3.x.</span></span>

<span data-ttu-id="d63bd-192">Per creare un gestore di anteprime personalizzato:</span><span class="sxs-lookup"><span data-stu-id="d63bd-192">To create a custom preview handler:</span></span>

1.  <span data-ttu-id="d63bd-193">Implementare un [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) che accetta un [IStream](/windows/win32/api/objidl/nn-objidl-istream), seguendo le linee guida fornite nei [gestori di anteprime](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="d63bd-193">Implement an [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) that takes an [IStream](/windows/win32/api/objidl/nn-objidl-istream), following the guidelines provided in [Preview Handlers](../shell/preview-handlers.md).</span></span>
2.  <span data-ttu-id="d63bd-194">Registrare il gestore di anteprime:</span><span class="sxs-lookup"><span data-stu-id="d63bd-194">Register your preview handler:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  <span data-ttu-id="d63bd-195">Completare i due passaggi seguenti per implementare una cartella della Shell per l'URL:</span><span class="sxs-lookup"><span data-stu-id="d63bd-195">Complete the following two steps to implement a Shell folder for your URL:</span></span>
    1.  <span data-ttu-id="d63bd-196">Nel [metodo IShellFolder:: GetUIObjectOf](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof)gestire [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) e restituire l'associazione per gli elementi della shell, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="d63bd-196">In [IShellFolder::GetUIObjectOf Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), handle [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) and return your association for your Shell items, as shown in the following code sample.</span></span>

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  <span data-ttu-id="d63bd-197">Dopo che la shell ha eseguito una query sulla cartella della Shell per il flusso di dati per inizializzare il gestore di anteprime, passare al metodo [IShellFolder:: BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) , gestire IID \_ IStream e restituire un [IStream](/windows/win32/api/objidl/nn-objidl-istream) all'URL.</span><span class="sxs-lookup"><span data-stu-id="d63bd-197">After the Shell queries your Shell folder for the data stream to initialize the preview handler, go to your [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) method, handle IID\_IStream and return an [IStream](/windows/win32/api/objidl/nn-objidl-istream) to your URL.</span></span>

<span data-ttu-id="d63bd-198">Per riutilizzare un gestore di anteprime esistente per il tipo di file, effettuare i due passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d63bd-198">To reuse an existing preview handler for your file type, follow these two steps:</span></span>

1.  <span data-ttu-id="d63bd-199">Registrare il gestore di anteprime per il tipo di file usando il CLSID del gestore di anteprime esistente al posto di <\_ \_ GUID PreviewHandler>.</span><span class="sxs-lookup"><span data-stu-id="d63bd-199">Register that preview handler for your file type using the CLSID of the existing preview handler in place of <Your\_PreviewHandler\_GUID>.</span></span>
2.  <span data-ttu-id="d63bd-200">Implementare una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="d63bd-200">Implement a Shell folder.</span></span>

<span data-ttu-id="d63bd-201">Per ulteriori informazioni sulla creazione di gestori di anteprime, vedere [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) e [gestori di anteprime](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="d63bd-201">For more information on creating preview handlers, see [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d63bd-202">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="d63bd-202">Additional Resources</span></span>

-   <span data-ttu-id="d63bd-203">Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d63bd-203">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="d63bd-204">Per informazioni sulla creazione di gestori, vedere [registrazione di estensioni della shell](../shell/reg-shell-exts.md), [creazione di gestori](../shell/handlers.md)di estensioni della shell, [menu di scelta rapida](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [estensioni dello spazio dei nomi shell](../shell/nse-works.md) e [gestori di anteprime](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="d63bd-204">For information about creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [Shell Namespace Extensions](../shell/nse-works.md) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d63bd-205">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d63bd-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d63bd-206">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d63bd-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d63bd-207">Sviluppo di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="d63bd-207">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="d63bd-208">Informazioni sui gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="d63bd-208">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="d63bd-209">Notifica dell'indice delle modifiche</span><span class="sxs-lookup"><span data-stu-id="d63bd-209">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="d63bd-210">Esempio di codice: estensioni della Shell per i gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="d63bd-210">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="d63bd-211">Installazione e registrazione di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="d63bd-211">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="d63bd-212">Creazione di un connettore di ricerca per un gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="d63bd-212">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="d63bd-213">Debug di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="d63bd-213">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
