---
title: Aggiunta di icone e menu di scelta rapida con le estensioni della shell
description: È possibile migliorare l'esperienza degli utenti con Microsoft Windows Desktop Search (WDS) e il gestore di protocollo implementando le estensioni della shell.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "104223418"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a><span data-ttu-id="a6b91-103">Aggiunta di icone e menu di scelta rapida con le estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="a6b91-103">Adding Icons and Context Menus with Shell Extensions</span></span>

> [!NOTE]
> <span data-ttu-id="a6b91-104">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a6b91-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a6b91-105">Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="a6b91-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="a6b91-106">È possibile migliorare l'esperienza degli utenti con Microsoft Windows Desktop Search (WDS) e il gestore di protocollo implementando le estensioni della shell.</span><span class="sxs-lookup"><span data-stu-id="a6b91-106">You can improve your users' experience with Microsoft Windows Desktop Search (WDS) and your protocol handler by implementing Shell extensions.</span></span> <span data-ttu-id="a6b91-107">Senza ulteriore estensione, il gestore di protocollo creato non includerà le esperienze utente seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6b91-107">Without further extension, the protocol handler you create will not include the following user experiences:</span></span>

-   <span data-ttu-id="a6b91-108">In WDS non vengono visualizzate icone specifiche per i risultati.</span><span class="sxs-lookup"><span data-stu-id="a6b91-108">WDS will not display specific icons for your results.</span></span>
-   <span data-ttu-id="a6b91-109">Quando si fa doppio clic su un elemento, l'interfaccia utente non risponderà all'evento.</span><span class="sxs-lookup"><span data-stu-id="a6b91-109">When users double-click an item, the user interface will not respond to the event.</span></span>
-   <span data-ttu-id="a6b91-110">Quando gli utenti fanno clic con il pulsante destro del mouse su un elemento, il menu di scelta rapida non supporta alcuna operazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a6b91-110">When users right-click an item, the context menu will not support any operations for the item.</span></span>

<span data-ttu-id="a6b91-111">Le implementazioni minime di **IPersist** e **IPersistFolder** sono richieste da **IShellFolder** ed è necessaria un'implementazione minima di **IShellFolder** per **IContextMenu** e **IExtractIcon**, le due interfacce che forniscono un'esperienza utente più trasparente.</span><span class="sxs-lookup"><span data-stu-id="a6b91-111">Minimal implementations of **IPersist** and **IPersistFolder** are required by **IShellFolder**, and a minimal implementation of **IShellFolder** is required for **IContextMenu** and **IExtractIcon**, the two interfaces that provide a more seamless user experience.</span></span>

 

## <a name="ipersist"></a><span data-ttu-id="a6b91-112">IPersist</span><span class="sxs-lookup"><span data-stu-id="a6b91-112">IPersist</span></span>

<span data-ttu-id="a6b91-113">L'interfaccia **IPersist** definisce il singolo metodo **GetClassID**, progettato per fornire il CLSID di un oggetto che può essere archiviato in modo permanente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a6b91-113">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="a6b91-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="a6b91-114">Method</span></span>       | <span data-ttu-id="a6b91-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6b91-115">Description</span></span>                                 |
|--------------|---------------------------------------------|
| <span data-ttu-id="a6b91-116">GetClassID ()</span><span class="sxs-lookup"><span data-stu-id="a6b91-116">GetClassID()</span></span> | <span data-ttu-id="a6b91-117">Restituisce il ClassID del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="a6b91-117">Returns the ClassID of the protocol handler</span></span> |



 

> [!Note]
>
> <span data-ttu-id="a6b91-118">È necessario implementare lo stesso CLSID per **IPersist**, **IPersistFolder** e **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="a6b91-118">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

 

## <a name="ipersistfolder"></a><span data-ttu-id="a6b91-119">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="a6b91-119">IPersistFolder</span></span>

<span data-ttu-id="a6b91-120">L'interfaccia **IPersistFolder** viene utilizzata per inizializzare gli oggetti cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="a6b91-120">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="a6b91-121">L'implementazione di questa interfaccia, derivata da **IPersist**, è il modo in cui viene indicato alla cartella dove si trova nello spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="a6b91-121">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span>



| <span data-ttu-id="a6b91-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="a6b91-122">Method</span></span>       | <span data-ttu-id="a6b91-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6b91-123">Description</span></span>                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b91-124">Initialize ()</span><span class="sxs-lookup"><span data-stu-id="a6b91-124">Initialize()</span></span> | <span data-ttu-id="a6b91-125">Indica a un oggetto cartella della shell di inizializzarsi in base alle informazioni passate e restituisce \_ OK</span><span class="sxs-lookup"><span data-stu-id="a6b91-125">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

> [!Note]
>
> <span data-ttu-id="a6b91-126">È necessario implementare lo stesso CLSID per **IPersist**, **IPersistFolder** e **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="a6b91-126">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="a6b91-127">Questa interfaccia non viene usata direttamente.</span><span class="sxs-lookup"><span data-stu-id="a6b91-127">You do not use this interface directly.</span></span> <span data-ttu-id="a6b91-128">Viene usato dall'implementazione file system dell'interfaccia IShellFolder:: BindToObject Quando Inizializza un oggetto cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="a6b91-128">It is used by the file system implementation of the IShellFolder::BindToObject interface when it initializes a Shell folder object.</span></span>

 

## <a name="ishellfolder"></a><span data-ttu-id="a6b91-129">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="a6b91-129">IShellFolder</span></span>

<span data-ttu-id="a6b91-130">L'interfaccia **IShellFolder** viene utilizzata per gestire le cartelle ed è necessaria un'implementazione parziale in modo che l'icona e le interfacce di contesto implementate per un gestore di protocollo si comportino correttamente nell'interfaccia utente dei risultati della ricerca desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="a6b91-130">The **IShellFolder** interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Desktop Search results user interface.</span></span> <span data-ttu-id="a6b91-131">La maggior parte delle funzionalità richieste viene esposta tramite il metodo **GetUIObjectOf** .</span><span class="sxs-lookup"><span data-stu-id="a6b91-131">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="a6b91-132">Questo metodo consente a un componente aggiuntivo di eseguire una query per le interfacce **IExtractIcon** e **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="a6b91-132">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="a6b91-133">L'interfaccia **IShellFolder** USA PIDL anziché URL.</span><span class="sxs-lookup"><span data-stu-id="a6b91-133">The **IShellFolder** interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="a6b91-134">Diversamente dai requisiti di un'estensione dello spazio dei nomi completa, i componenti aggiuntivi possono utilizzare una semplice struttura IDL che contiene solo l'URL.</span><span class="sxs-lookup"><span data-stu-id="a6b91-134">In contrast to the requirements of a complete Namespace extension, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="a6b91-135">È necessario implementare i metodi di **IShellFolder** seguenti.</span><span class="sxs-lookup"><span data-stu-id="a6b91-135">The following methods of **IShellFolder** must be implemented.</span></span> <span data-ttu-id="a6b91-136">Si noti che cinque di questi metodi richiedono un'implementazione minima.</span><span class="sxs-lookup"><span data-stu-id="a6b91-136">Note that five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="a6b91-137">Metodo</span><span class="sxs-lookup"><span data-stu-id="a6b91-137">Method</span></span>             | <span data-ttu-id="a6b91-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6b91-138">Description</span></span>                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b91-139">BindToObject ()</span><span class="sxs-lookup"><span data-stu-id="a6b91-139">BindToObject()</span></span>     | <span data-ttu-id="a6b91-140">Restituisce E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a6b91-140">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="a6b91-141">BindToStorage ()</span><span class="sxs-lookup"><span data-stu-id="a6b91-141">BindToStorage()</span></span>    | <span data-ttu-id="a6b91-142">Restituisce E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a6b91-142">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="a6b91-143">CreateViewObject()</span><span class="sxs-lookup"><span data-stu-id="a6b91-143">CreateViewObject()</span></span> | <span data-ttu-id="a6b91-144">Restituisce E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a6b91-144">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="a6b91-145">SetNameOf()</span><span class="sxs-lookup"><span data-stu-id="a6b91-145">SetNameOf()</span></span>        | <span data-ttu-id="a6b91-146">Restituisce E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a6b91-146">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="a6b91-147">ParseDisplayName ()</span><span class="sxs-lookup"><span data-stu-id="a6b91-147">ParseDisplayName()</span></span> | <span data-ttu-id="a6b91-148">Converte un URL nella struttura PIDL</span><span class="sxs-lookup"><span data-stu-id="a6b91-148">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                        |
| <span data-ttu-id="a6b91-149">CompareIDs()</span><span class="sxs-lookup"><span data-stu-id="a6b91-149">CompareIDs()</span></span>       | <span data-ttu-id="a6b91-150">Confronta due valori PIDL</span><span class="sxs-lookup"><span data-stu-id="a6b91-150">Compares two PIDL values</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="a6b91-151">GetDisplayNameOf ()</span><span class="sxs-lookup"><span data-stu-id="a6b91-151">GetDisplayNameOf()</span></span> | <span data-ttu-id="a6b91-152">Restituisce l'URL per un PIDL</span><span class="sxs-lookup"><span data-stu-id="a6b91-152">Returns the URL for a PIDL</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="a6b91-153">GetUIObjectOf()</span><span class="sxs-lookup"><span data-stu-id="a6b91-153">GetUIObjectOf()</span></span>    | <span data-ttu-id="a6b91-154">Questo metodo è simile al metodo OLE COM QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="a6b91-154">This method is similar to the OLE COM QueryInterface method.</span></span> <span data-ttu-id="a6b91-155">Se viene richiesta un'icona, il chiamante richiede l'IID \_ IExtractIcon; se viene richiesto un menu di scelta rapida, il chiamante richiede \_ il IContextMenu IID.</span><span class="sxs-lookup"><span data-stu-id="a6b91-155">If an icon is requested, the caller requests the IID\_IExtractIcon; if a context menu is requested, the caller requests the IID\_IContextMenu.</span></span> |



 

> [!Note]
>
> <span data-ttu-id="a6b91-156">È necessario implementare lo stesso CLSID per **IPersist**, **IPersistFolder** e **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="a6b91-156">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="a6b91-157">**IShellFolder** non viene utilizzato per enumerare le cartelle.</span><span class="sxs-lookup"><span data-stu-id="a6b91-157">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="a6b91-158">Ciò significa che il nome visualizzato di una cartella sarà l'URL fisico.</span><span class="sxs-lookup"><span data-stu-id="a6b91-158">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="a6b91-159">Questo potrebbe cambiare in futuro.</span><span class="sxs-lookup"><span data-stu-id="a6b91-159">This may change in the future.</span></span>

 

## <a name="icontextmenu"></a><span data-ttu-id="a6b91-160">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="a6b91-160">IContextMenu</span></span>

<span data-ttu-id="a6b91-161">Quando WDS Visualizza i risultati per l'utente, l'utente può fare clic con il pulsante destro del mouse su un elemento e visualizzare un menu di scelta rapida definito dall'interfaccia **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="a6b91-161">When WDS displays results to the user, the user can right-click an item and see a context menu defined by your **IContextMenu** interface.</span></span>

<span data-ttu-id="a6b91-162">L'azione predefinita nel menu di scelta rapida è identica a quella eseguita quando si fa doppio clic sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="a6b91-162">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="a6b91-163">Senza le interfacce **IShellFolder** o **IContextMenu** corrispondenti per l'elemento, il comportamento predefinito per un evento di doppio clic consiste nel passare l'URL come argomento alla funzione ShellExecute.</span><span class="sxs-lookup"><span data-stu-id="a6b91-163">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the ShellExecute function.</span></span>

 

## <a name="iextracticon"></a><span data-ttu-id="a6b91-164">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="a6b91-164">IExtractIcon</span></span>

<span data-ttu-id="a6b91-165">**IExtractIcon** recupera un'icona per l'interfaccia utente di WDS basata sull'URL nel PIDL fornito dal gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="a6b91-165">**IExtractIcon** retrieves an icon for the WDS user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

 

## <a name="code-sample"></a><span data-ttu-id="a6b91-166">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="a6b91-166">Code Sample</span></span>

<span data-ttu-id="a6b91-167">Il [codice di esempio dell'interfaccia utente del gestore di protocollo personalizzato](-search-2x-wds-ph-ui-samplecode.md) illustra un'implementazione di **IShellFolder** e le interfacce di supporto e include il supporto per la modifica di PIDL.</span><span class="sxs-lookup"><span data-stu-id="a6b91-167">The [Custom Protocol Handler User Interface Sample Code](-search-2x-wds-ph-ui-samplecode.md) demonstrates an implementation of **IShellFolder** and supporting interfaces and includes support for manipulating the PIDLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6b91-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6b91-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a6b91-169">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a6b91-169">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a6b91-170">Codice di esempio dell'interfaccia utente del gestore di protocollo personalizzato</span><span class="sxs-lookup"><span data-stu-id="a6b91-170">Custom Protocol Handler User Interface Sample Code</span></span>](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="a6b91-171">Installazione e registrazione di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="a6b91-171">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




