---
description: I gestori dei menu di scelta rapida sono noti anche come gestori di menu di scelta rapida o gestori di verbi. Un gestore di menu di scelta rapida è un tipo di gestore di tipi di file.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Personalizzazione di un menu di scelta rapida tramite verbi dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980183"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a><span data-ttu-id="6f495-104">Personalizzazione di un menu di scelta rapida tramite verbi dinamici</span><span class="sxs-lookup"><span data-stu-id="6f495-104">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>

<span data-ttu-id="6f495-105">I gestori dei menu di scelta rapida sono noti anche come gestori di menu di scelta rapida o gestori di verbi.</span><span class="sxs-lookup"><span data-stu-id="6f495-105">Shortcut menu handlers are also known as context menu handlers or verb handlers.</span></span> <span data-ttu-id="6f495-106">Un gestore di menu di scelta rapida è un tipo di gestore di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="6f495-106">A shortcut menu handler is a type of file type handler.</span></span>

<span data-ttu-id="6f495-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="6f495-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="6f495-108">Informazioni sui verbi statici e dinamici</span><span class="sxs-lookup"><span data-stu-id="6f495-108">About Static and Dynamic Verbs</span></span>](#about-static-and-dynamic-verbs)
-   [<span data-ttu-id="6f495-109">Funzionamento dei gestori dei menu di scelta rapida con verbi dinamici</span><span class="sxs-lookup"><span data-stu-id="6f495-109">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [<span data-ttu-id="6f495-110">Evitare collisioni a causa di nomi di verbi non qualificati</span><span class="sxs-lookup"><span data-stu-id="6f495-110">Avoiding Collisions Due to Unqualified Verb Names</span></span>](#avoiding-collisions-due-to-unqualified-verb-names)
-   [<span data-ttu-id="6f495-111">Registrazione di un gestore di menu di scelta rapida con un verbo dinamico</span><span class="sxs-lookup"><span data-stu-id="6f495-111">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [<span data-ttu-id="6f495-112">Implementazione dell'interfaccia IContextMenu</span><span class="sxs-lookup"><span data-stu-id="6f495-112">Implementing the IContextMenu Interface</span></span>](#implementing-the-icontextmenu-interface)
    -   [<span data-ttu-id="6f495-113">Metodo IContextMenu:: GetCommandString</span><span class="sxs-lookup"><span data-stu-id="6f495-113">IContextMenu::GetCommandString Method</span></span>](#icontextmenugetcommandstring-method)
    -   [<span data-ttu-id="6f495-114">Metodo IContextMenu:: InvokeCommand</span><span class="sxs-lookup"><span data-stu-id="6f495-114">IContextMenu::InvokeCommand Method</span></span>](#icontextmenuinvokecommand-method)
    -   [<span data-ttu-id="6f495-115">Metodo IContextMenu:: QueryContextMenu</span><span class="sxs-lookup"><span data-stu-id="6f495-115">IContextMenu::QueryContextMenu Method</span></span>](#icontextmenuquerycontextmenu-method)
-   [<span data-ttu-id="6f495-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f495-116">Related topics</span></span>](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a><span data-ttu-id="6f495-117">Informazioni sui verbi statici e dinamici</span><span class="sxs-lookup"><span data-stu-id="6f495-117">About Static and Dynamic Verbs</span></span>

<span data-ttu-id="6f495-118">Si consiglia di implementare un menu di scelta rapida usando uno dei metodi del verbo statico.</span><span class="sxs-lookup"><span data-stu-id="6f495-118">We strongly encourage you to implement a shortcut menu using one of the static verb methods.</span></span> <span data-ttu-id="6f495-119">È consigliabile seguire le istruzioni fornite nella sezione "personalizzazione di un menu di scelta rapida con verbi statici" di creazione di [gestori di menu di scelta rapida](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="6f495-119">We recommend that you follow the instructions provided in the "Customizing a Shortcut Menu using Static Verbs" section of [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="6f495-120">Per ottenere il comportamento dinamico per i verbi statici in Windows 7 e versioni successive, vedere la sezione relativa all'acquisizione del comportamento dinamico per i verbi statici in [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="6f495-120">To get dynamic behavior for static verbs in Windows 7 and later, see "Getting Dynamic Behavior for Static Verbs" in [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="6f495-121">Per informazioni dettagliate sull'implementazione del verbo statico e sui verbi dinamici da evitare, vedere [scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="6f495-121">For details on static verb implementation, and which dynamic verbs to avoid, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span>

<span data-ttu-id="6f495-122">Se è necessario estendere il menu di scelta rapida per un tipo di file registrando un verbo dinamico per il tipo di file, seguire le istruzioni fornite più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="6f495-122">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided later in this topic.</span></span>

> [!Note]  
> <span data-ttu-id="6f495-123">Quando si registrano i gestori che operano nel contesto di applicazioni a 32 bit, è necessario tenere presenti alcune considerazioni speciali per Windows a 64 bit: quando i verbi della shell vengono richiamati nel contesto di un'applicazione a 32 bit, il sottosistema WOW64 reindirizza file system accesso ad alcuni percorsi.</span><span class="sxs-lookup"><span data-stu-id="6f495-123">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="6f495-124">Se il gestore. exe viene archiviato in uno di questi percorsi, non è accessibile in questo contesto.</span><span class="sxs-lookup"><span data-stu-id="6f495-124">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="6f495-125">Pertanto, come soluzione alternativa, archiviare il file con estensione exe in un percorso che non viene reindirizzato oppure archiviare una versione stub del file exe che avvia la versione reale.</span><span class="sxs-lookup"><span data-stu-id="6f495-125">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a><span data-ttu-id="6f495-126">Funzionamento dei gestori dei menu di scelta rapida con verbi dinamici</span><span class="sxs-lookup"><span data-stu-id="6f495-126">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>

<span data-ttu-id="6f495-127">Oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), i gestori dei menu di scelta rapida esportano le seguenti interfacce aggiuntive per gestire la messaggistica necessaria per implementare voci di menu create dal proprietario:</span><span class="sxs-lookup"><span data-stu-id="6f495-127">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), shortcut menu handlers export the following additional interfaces to handle the messaging needed to implement owner-drawn menu items:</span></span>

-   <span data-ttu-id="6f495-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="6f495-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (mandatory)</span></span>
-   <span data-ttu-id="6f495-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="6f495-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (mandatory)</span></span>
-   <span data-ttu-id="6f495-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="6f495-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (optional)</span></span>
-   <span data-ttu-id="6f495-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="6f495-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (optional)</span></span>

<span data-ttu-id="6f495-132">Per ulteriori informazioni sulle voci di menu create dal proprietario, vedere la sezione *creazione di Owner-Drawn voci di menu* in [utilizzo di menu](../menurc/using-menus.md).</span><span class="sxs-lookup"><span data-stu-id="6f495-132">For more information on owner-drawn menu items, see the *Creating Owner-Drawn Menu Items* section in [Using Menus](../menurc/using-menus.md).</span></span>

<span data-ttu-id="6f495-133">Shell usa l'interfaccia [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) per inizializzare il gestore.</span><span class="sxs-lookup"><span data-stu-id="6f495-133">Shell uses the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface to initialize the handler.</span></span> <span data-ttu-id="6f495-134">Quando la shell chiama [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), passa un oggetto dati con il nome dell'oggetto e un puntatore a un elenco di identificatori di elemento (PIDL) della cartella che contiene il file.</span><span class="sxs-lookup"><span data-stu-id="6f495-134">When the Shell calls [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), it passes in a data object with the object's name and a pointer to an item identifier list (PIDL) of the folder that contains the file.</span></span> <span data-ttu-id="6f495-135">Il parametro *hkeyProgID* è il percorso del registro di sistema in cui è registrato il punto di controllo del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="6f495-135">The *hkeyProgID* parameter is the registry location under which the shortcut menu handle is registered.</span></span> <span data-ttu-id="6f495-136">Il metodo **IShellExtInit:: Initialize** deve estrarre il nome del file dall'oggetto dati e archiviare il nome e il puntatore della cartella in un elenco di identificatori di elemento (PIDL) per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="6f495-136">The **IShellExtInit::Initialize** method must extract the file name from the data object and store the name and the folder's pointer to an item identifier list (PIDL) for later use.</span></span> <span data-ttu-id="6f495-137">Per ulteriori informazioni sull'inizializzazione del gestore, vedere [implementazione di IShellExtInit](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="6f495-137">For more information on handler initialization, see [Implementing IShellExtInit](handlers.md).</span></span>

<span data-ttu-id="6f495-138">Quando i verbi vengono presentati in un menu di scelta rapida, vengono prima individuati, quindi presentati all'utente e infine richiamati.</span><span class="sxs-lookup"><span data-stu-id="6f495-138">When verbs are presented in a shortcut menu, they are first discovered, then presented to the user, and finally invoked.</span></span> <span data-ttu-id="6f495-139">Nell'elenco seguente vengono descritti in modo più dettagliato questi tre passaggi:</span><span class="sxs-lookup"><span data-stu-id="6f495-139">The following list describes these three steps in more detail:</span></span>

1.  <span data-ttu-id="6f495-140">La shell chiama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), che restituisce un set di verbi che possono essere basati sullo stato degli elementi o del sistema.</span><span class="sxs-lookup"><span data-stu-id="6f495-140">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which returns a set of verbs that can be based on the state of the items or the system.</span></span>
2.  <span data-ttu-id="6f495-141">Il sistema passa un handle **HMENU** che il metodo può usare per aggiungere elementi al menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="6f495-141">The system passes in an **HMENU** handle that the method can use to add items to the shortcut menu.</span></span>
3.  <span data-ttu-id="6f495-142">Se l'utente fa clic su uno degli elementi del gestore, la shell chiama [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="6f495-142">If the user clicks one of the handler's items, the Shell calls [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span> <span data-ttu-id="6f495-143">Il gestore può quindi eseguire il comando appropriato.</span><span class="sxs-lookup"><span data-stu-id="6f495-143">The handler can then execute the appropriate command.</span></span>

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a><span data-ttu-id="6f495-144">Evitare collisioni a causa di nomi di verbi non qualificati</span><span class="sxs-lookup"><span data-stu-id="6f495-144">Avoiding Collisions Due to Unqualified Verb Names</span></span>

<span data-ttu-id="6f495-145">Poiché i verbi sono registrati per tipo, è possibile usare lo stesso nome di verbo per i verbi su elementi diversi.</span><span class="sxs-lookup"><span data-stu-id="6f495-145">Because verbs are registered per type, the same verb name can be used for verbs on different items.</span></span> <span data-ttu-id="6f495-146">In questo modo, le applicazioni fanno riferimento a verbi comuni indipendenti dal tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="6f495-146">Doing so enables applications to refer to common verbs independent of the item type.</span></span> <span data-ttu-id="6f495-147">Sebbene questa funzionalità sia utile, l'utilizzo di nomi non qualificati può comportare conflitti con più fornitori di software indipendenti (ISV) che scelgono lo stesso nome del verbo.</span><span class="sxs-lookup"><span data-stu-id="6f495-147">While this functionality is useful, the use of unqualified names can result in collisions with multiple independent software vendors (ISVs) that choose the same verb name.</span></span> <span data-ttu-id="6f495-148">Per evitare questo problema, anteporre sempre i verbi al nome ISV come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6f495-148">To avoid this, always prefix verbs with the ISV name as follows:</span></span>

`ISV_Name.verb`

<span data-ttu-id="6f495-149">Usare sempre un ProgID specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f495-149">Always use an application specific ProgID.</span></span> <span data-ttu-id="6f495-150">L'adozione della convenzione di mapping dell'estensione di file a un ProgID fornito da ISV evita potenziali collisioni.</span><span class="sxs-lookup"><span data-stu-id="6f495-150">Adopting the convention of mapping the file name extension to an ISV provided ProgID avoids potential collisions.</span></span> <span data-ttu-id="6f495-151">Tuttavia, poiché alcuni tipi di elemento non utilizzano questo mapping, è necessario disporre di nomi univoci del fornitore.</span><span class="sxs-lookup"><span data-stu-id="6f495-151">However, because some item types do not use this mapping, there is a need for vendor-unique names.</span></span> <span data-ttu-id="6f495-152">Quando si aggiunge un verbo a un ProgID esistente che potrebbe avere già registrato il verbo, è necessario prima rimuovere la chiave del registro di sistema per il verbo precedente prima di aggiungere il proprio verbo.</span><span class="sxs-lookup"><span data-stu-id="6f495-152">When adding a verb to an existing ProgID that might already have that verb registered, you must first remove the registry key for the old verb before adding your own verb.</span></span> <span data-ttu-id="6f495-153">È necessario eseguire questa operazione per evitare di unire le informazioni sui verbi dai due verbi.</span><span class="sxs-lookup"><span data-stu-id="6f495-153">You must do so to avoid merging the verb information from the two verbs.</span></span> <span data-ttu-id="6f495-154">In caso contrario, viene restituito un comportamento imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="6f495-154">Failure to do so results in unpredictable behavior.</span></span>

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a><span data-ttu-id="6f495-155">Registrazione di un gestore di menu di scelta rapida con un verbo dinamico</span><span class="sxs-lookup"><span data-stu-id="6f495-155">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>

<span data-ttu-id="6f495-156">I gestori dei menu di scelta rapida sono associati a un tipo di file o a una cartella.</span><span class="sxs-lookup"><span data-stu-id="6f495-156">Shortcut menu handlers are associated with either a file type or a folder.</span></span> <span data-ttu-id="6f495-157">Per i tipi di file, il gestore viene registrato nella sottochiave seguente.</span><span class="sxs-lookup"><span data-stu-id="6f495-157">For file types, the handler is registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="6f495-158">Per associare un gestore di menu di scelta rapida a un tipo di file o a una cartella, creare prima una sottochiave nella sottochiave **ContextMenuHandlers** .</span><span class="sxs-lookup"><span data-stu-id="6f495-158">To associate a shortcut menu handler with either a file type or a folder, first create a subkey under the **ContextMenuHandlers** subkey.</span></span> <span data-ttu-id="6f495-159">Assegnare un nome alla sottochiave per il gestore, quindi impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe del gestore (CLSID).</span><span class="sxs-lookup"><span data-stu-id="6f495-159">Name the subkey for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="6f495-160">Quindi, per associare un gestore di menu di scelta rapida con diversi tipi di cartelle, registrare il gestore nello stesso modo in cui si farebbe per un tipo di file, ma sotto la sottochiave *FolderType* , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="6f495-160">Then to associate a shortcut menu handler with different kinds of folders, register the handler the same way you would for a file type, but under the *FolderType* subkey as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="6f495-161">Per ulteriori informazioni sui tipi di cartelle per i quali è possibile registrare i gestori, vedere la pagina relativa alla [registrazione dei gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="6f495-161">For more information about about which folder types you can register handlers for, see [Registering Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="6f495-162">Se a un tipo di file è associato un menu di scelta rapida, facendo doppio clic su un oggetto viene normalmente avviato il comando predefinito e il metodo [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) del gestore non viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="6f495-162">If a file type has a shortcut menu associated with it, then double-clicking an object normally launches the default command, and the handler's [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) method is not called.</span></span> <span data-ttu-id="6f495-163">Per specificare che il metodo **IContextMenu:: QueryContextMenu** del gestore deve essere chiamato quando si fa doppio clic su un oggetto, creare una sottochiave sotto la sottochiave **CLSID** del gestore, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="6f495-163">To specify that the handler's **IContextMenu::QueryContextMenu** method should be called when an object is double-clicked, create a subkey under the handler's **CLSID** subkey as shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

<span data-ttu-id="6f495-164">Quando si fa doppio clic su un oggetto associato al gestore, [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) viene chiamato con il flag **CMF \_ DEFAULTONLY** impostato nel parametro *uFlags* .</span><span class="sxs-lookup"><span data-stu-id="6f495-164">When an object associated with the handler is double-clicked, [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) is called with the **CMF\_DEFAULTONLY** flag set in the *uFlags* parameter.</span></span>

<span data-ttu-id="6f495-165">I gestori dei menu di scelta rapida devono impostare la sottochiave **MayChangeDefaultMenu** solo se potrebbero dover modificare il verbo predefinito del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="6f495-165">Shortcut menu handlers should set the **MayChangeDefaultMenu** subkey only if they might need to change the shortcut menu's default verb.</span></span> <span data-ttu-id="6f495-166">L'impostazione di questa sottochiave impone al sistema di caricare la DLL del gestore quando si fa doppio clic su un elemento associato.</span><span class="sxs-lookup"><span data-stu-id="6f495-166">Setting this subkey forces the system to load the handler's DLL when an associated item is double-clicked.</span></span> <span data-ttu-id="6f495-167">Se il gestore non modifica il verbo predefinito, è consigliabile non impostare questa sottochiave perché in questo modo il sistema carica la DLL inutilmente.</span><span class="sxs-lookup"><span data-stu-id="6f495-167">If your handler does not change the default verb, you should not set this subkey because doing so causes the system to load your DLL unnecessarily.</span></span>

<span data-ttu-id="6f495-168">Nell'esempio seguente vengono illustrate le voci del registro di sistema che consentono un gestore di menu di scelta rapida per un tipo di file con estensione MYP.</span><span class="sxs-lookup"><span data-stu-id="6f495-168">The following example illustrates registry entries that enable a shortcut menu handler for an .myp file type.</span></span> <span data-ttu-id="6f495-169">La sottochiave **CLSID** del gestore include una sottochiave **MayChangeDefaultMenu** per garantire che il gestore venga chiamato quando l'utente fa doppio clic su un oggetto correlato.</span><span class="sxs-lookup"><span data-stu-id="6f495-169">The handler's **CLSID** subkey includes a **MayChangeDefaultMenu** subkey to guarantee that the handler is called when the user double-clicks a related object.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a><span data-ttu-id="6f495-170">Implementazione dell'interfaccia IContextMenu</span><span class="sxs-lookup"><span data-stu-id="6f495-170">Implementing the IContextMenu Interface</span></span>

<span data-ttu-id="6f495-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) è il metodo più potente ma anche il più complesso da implementare.</span><span class="sxs-lookup"><span data-stu-id="6f495-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="6f495-172">Si consiglia di implementare un verbo utilizzando uno dei metodi del verbo statico.</span><span class="sxs-lookup"><span data-stu-id="6f495-172">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="6f495-173">Per ulteriori informazioni, vedere [scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="6f495-173">For more information, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span> <span data-ttu-id="6f495-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) dispone di tre metodi, **GetCommandString**, **InvokeCommand** e **QueryContextMenu**, descritti in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="6f495-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, **GetCommandString**, **InvokeCommand**, and **QueryContextMenu**, which are discussed here in detail.</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="6f495-175">Metodo IContextMenu:: GetCommandString</span><span class="sxs-lookup"><span data-stu-id="6f495-175">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="6f495-176">Il metodo [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) del gestore viene usato per restituire il nome canonico per un verbo.</span><span class="sxs-lookup"><span data-stu-id="6f495-176">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="6f495-177">È facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6f495-177">This method is optional.</span></span> <span data-ttu-id="6f495-178">In Windows XP e nelle versioni precedenti di Windows, quando Esplora risorse dispone di una barra di stato, questo metodo viene utilizzato per recuperare il testo della Guida visualizzato nella barra di stato per una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="6f495-178">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="6f495-179">Il parametro *idCmd* include l'offset dell'identificatore del comando definito al momento della chiamata a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="6f495-179">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="6f495-180">Se viene richiesta una stringa della guida, *uFlags* verrà impostato su **cataloghi globali \_ HELPTEXTW**.</span><span class="sxs-lookup"><span data-stu-id="6f495-180">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="6f495-181">Copiare la stringa della guida nel buffer *pszName* , eseguendone il cast in un **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="6f495-181">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="6f495-182">La stringa del verbo viene richiesta impostando *uFlags* su **cataloghi globali \_ VERBW**.</span><span class="sxs-lookup"><span data-stu-id="6f495-182">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="6f495-183">Copiare la stringa appropriata in *pszName*, proprio come con la stringa della guida.</span><span class="sxs-lookup"><span data-stu-id="6f495-183">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="6f495-184">I flag **GC \_ validatea** e **GC \_ VALIDATEW** non vengono utilizzati dai gestori dei menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="6f495-184">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="6f495-185">Nell'esempio seguente viene illustrata un'implementazione semplice di [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) che corrisponde all'esempio [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fornito nella sezione [metodo IContextMenu:: QueryContextMenu](#icontextmenuquerycontextmenu-method) di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="6f495-185">The following example shows a simple implementation of [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](#icontextmenuquerycontextmenu-method) section of this topic.</span></span> <span data-ttu-id="6f495-186">Poiché il gestore aggiunge solo una voce di menu, è possibile restituire un solo set di stringhe.</span><span class="sxs-lookup"><span data-stu-id="6f495-186">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="6f495-187">Il metodo verifica se *idCmd* è valido e, in caso contrario, restituisce la stringa richiesta.</span><span class="sxs-lookup"><span data-stu-id="6f495-187">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="6f495-188">La funzione [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) viene usata per copiare la stringa richiesta in *pszName* per assicurarsi che la stringa copiata non superi le dimensioni del buffer specificato da *cchName*.</span><span class="sxs-lookup"><span data-stu-id="6f495-188">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="6f495-189">Questo esempio implementa solo il supporto per i valori Unicode di *uFlags*, in quanto solo quelli sono stati usati in Esplora risorse da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6f495-189">This example only implements support for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```C++
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="6f495-190">Metodo IContextMenu:: InvokeCommand</span><span class="sxs-lookup"><span data-stu-id="6f495-190">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="6f495-191">Questo metodo viene chiamato quando un utente fa clic su una voce di menu per indicare al gestore di eseguire il comando associato.</span><span class="sxs-lookup"><span data-stu-id="6f495-191">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="6f495-192">Il parametro *pici* punta a una struttura che contiene le informazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="6f495-192">The *pici* parameter points to a structure that contains the information required.</span></span>

<span data-ttu-id="6f495-193">Sebbene *pici* sia dichiarato in Shlobj. h come struttura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , in pratica spesso punta a una struttura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) .</span><span class="sxs-lookup"><span data-stu-id="6f495-193">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="6f495-194">Questa struttura è una versione estesa di **CMINVOKECOMMANDINFO** e include diversi membri aggiuntivi che rendono possibile il passaggio di stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="6f495-194">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="6f495-195">Verificare il membro **cbSize** di *pici* per determinare la struttura passata.</span><span class="sxs-lookup"><span data-stu-id="6f495-195">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="6f495-196">Se si tratta di una struttura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) e per il membro **fmask** è impostato il flag **\_ \_ Unicode CMIC mask** , eseguire il cast di *pici* a **CMINVOKECOMMANDINFOEX**.</span><span class="sxs-lookup"><span data-stu-id="6f495-196">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="6f495-197">Ciò consente all'applicazione di utilizzare le informazioni Unicode contenute negli ultimi cinque membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="6f495-197">This enables your application to use the Unicode information contained in the last five members of the structure.</span></span>

<span data-ttu-id="6f495-198">Il membro **lpVerb** o **lpVerbW** della struttura viene usato per identificare il comando da eseguire.</span><span class="sxs-lookup"><span data-stu-id="6f495-198">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="6f495-199">I comandi sono identificati in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f495-199">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="6f495-200">Dalla stringa del verbo del comando</span><span class="sxs-lookup"><span data-stu-id="6f495-200">By the command's verb string</span></span>
-   <span data-ttu-id="6f495-201">In base all'offset dell'identificatore del comando</span><span class="sxs-lookup"><span data-stu-id="6f495-201">By the command's identifier offset</span></span>

<span data-ttu-id="6f495-202">Per distinguere tra questi due casi, controllare la parola più ordinata di **lpVerb** per il caso ANSI o **lpVerbW** per il caso Unicode.</span><span class="sxs-lookup"><span data-stu-id="6f495-202">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="6f495-203">Se la parola più ordinata è diversa da zero, **lpVerb** o **lpVerbW** include una stringa verbo.</span><span class="sxs-lookup"><span data-stu-id="6f495-203">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="6f495-204">Se la parola più ordinata è pari a zero, l'offset del comando è nella parola più bassa dell'ordine di **lpVerb**.</span><span class="sxs-lookup"><span data-stu-id="6f495-204">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="6f495-205">Nell'esempio seguente viene illustrata un'implementazione semplice di [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) che corrisponde agli esempi [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) forniti prima e dopo questa sezione.</span><span class="sxs-lookup"><span data-stu-id="6f495-205">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="6f495-206">Il metodo determina prima di tutto la struttura che viene passata.</span><span class="sxs-lookup"><span data-stu-id="6f495-206">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="6f495-207">Quindi determina se il comando viene identificato in base al relativo offset o al relativo verbo.</span><span class="sxs-lookup"><span data-stu-id="6f495-207">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="6f495-208">Se **lpVerb** o **lpVerbW** contiene un verbo o un offset valido, il metodo Visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f495-208">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```C++
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="6f495-209">Metodo IContextMenu:: QueryContextMenu</span><span class="sxs-lookup"><span data-stu-id="6f495-209">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="6f495-210">La shell chiama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) per abilitare il gestore del menu di scelta rapida per aggiungere le voci di menu al menu.</span><span class="sxs-lookup"><span data-stu-id="6f495-210">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="6f495-211">Passa l'handle **HMENU** nel parametro *HMENU* .</span><span class="sxs-lookup"><span data-stu-id="6f495-211">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="6f495-212">Il parametro *indexMenu* è impostato sull'indice da utilizzare per la prima voce di menu da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="6f495-212">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="6f495-213">Tutte le voci di menu aggiunte dal gestore devono contenere identificatori che rientrano tra i valori nei parametri *idCmdFirst* e *idCmdLast* .</span><span class="sxs-lookup"><span data-stu-id="6f495-213">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="6f495-214">In genere, il primo identificatore del comando è impostato su *idCmdFirst*, che viene incrementato di uno (1) per ogni comando aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="6f495-214">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="6f495-215">Questa procedura consente di evitare il superamento di *idCmdLast* e massimizza il numero di identificatori disponibili nel caso in cui la shell chiami più di un gestore.</span><span class="sxs-lookup"><span data-stu-id="6f495-215">This practice helps you avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="6f495-216">L' *offset del comando* di un identificatore di elemento è la differenza tra l'identificatore e il valore in *idCmdFirst*.</span><span class="sxs-lookup"><span data-stu-id="6f495-216">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="6f495-217">Archiviare l'offset di ogni elemento aggiunto dal gestore al menu di scelta rapida perché può essere utilizzato dalla Shell per identificare l'elemento se successivamente viene chiamato [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="6f495-217">Store the offset of each item that your handler adds to the shortcut menu because the Shell might use it to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="6f495-218">È inoltre consigliabile assegnare un [verbo](launch.md) a ogni comando aggiunto.</span><span class="sxs-lookup"><span data-stu-id="6f495-218">You should also assign a [verb](launch.md) to each command you add.</span></span> <span data-ttu-id="6f495-219">Un verbo è una stringa che può essere utilizzata al posto dell'offset per identificare il comando quando viene chiamato [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="6f495-219">A verb is a string that can be used instead of the offset to identify the command when [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="6f495-220">Viene anche usato da funzioni come [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per eseguire i comandi del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="6f495-220">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="6f495-221">Sono disponibili tre flag che possono essere passati tramite il parametro *uFlags* rilevanti per i gestori dei menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="6f495-221">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="6f495-222">descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6f495-222">They are described in the following table.</span></span>



| <span data-ttu-id="6f495-223">Flag</span><span class="sxs-lookup"><span data-stu-id="6f495-223">Flag</span></span>             | <span data-ttu-id="6f495-224">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f495-224">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f495-225">DEFAULTONLY di CMF \_</span><span class="sxs-lookup"><span data-stu-id="6f495-225">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="6f495-226">L'utente ha selezionato il comando predefinito, in genere facendo doppio clic sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6f495-226">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="6f495-227">[**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deve restituire il controllo alla shell senza modificare il menu.</span><span class="sxs-lookup"><span data-stu-id="6f495-227">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="6f495-228">CMF \_ NOdefault</span><span class="sxs-lookup"><span data-stu-id="6f495-228">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="6f495-229">Nessun elemento nel menu deve essere l'elemento predefinito.</span><span class="sxs-lookup"><span data-stu-id="6f495-229">No item in the menu should be the default item.</span></span> <span data-ttu-id="6f495-230">Il metodo deve aggiungere i comandi al menu.</span><span class="sxs-lookup"><span data-stu-id="6f495-230">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="6f495-231">\_normale CMF</span><span class="sxs-lookup"><span data-stu-id="6f495-231">CMF\_NORMAL</span></span>      | <span data-ttu-id="6f495-232">Il menu di scelta rapida verrà visualizzato normalmente.</span><span class="sxs-lookup"><span data-stu-id="6f495-232">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="6f495-233">Il metodo deve aggiungere i comandi al menu.</span><span class="sxs-lookup"><span data-stu-id="6f495-233">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="6f495-234">Usare [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) o [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) per aggiungere voci di menu all'elenco.</span><span class="sxs-lookup"><span data-stu-id="6f495-234">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="6f495-235">Restituire quindi un valore **HRESULT** con gravità impostato su **gravità \_ riuscita**.</span><span class="sxs-lookup"><span data-stu-id="6f495-235">Then return an **HRESULT** value with the severity set to **SEVERITY\_SUCCESS**.</span></span> <span data-ttu-id="6f495-236">Impostare il valore del codice sull'offset dell'identificatore di comando più grande assegnato, più uno (1).</span><span class="sxs-lookup"><span data-stu-id="6f495-236">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="6f495-237">Si supponga, ad esempio, che *idCmdFirst* sia impostato su 5 e che vengano aggiunti tre elementi al menu con gli identificatori dei comandi 5, 7 e 8.</span><span class="sxs-lookup"><span data-stu-id="6f495-237">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="6f495-238">Il valore restituito deve essere `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .</span><span class="sxs-lookup"><span data-stu-id="6f495-238">The return value should be `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)`.</span></span>

<span data-ttu-id="6f495-239">Nell'esempio seguente viene illustrata un'implementazione semplice di [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) che inserisce un singolo comando.</span><span class="sxs-lookup"><span data-stu-id="6f495-239">The following example shows a simple implementation of [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="6f495-240">L'offset dell'identificatore per il comando è IDM \_ display, che è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="6f495-240">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="6f495-241">Le variabili **m \_ pszVerb** e **m \_ pwszVerb** sono variabili private usate per archiviare la stringa del verbo indipendente dal linguaggio associata nei formati ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="6f495-241">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```C++
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



<span data-ttu-id="6f495-242">Per altre attività di implementazione di verbi, vedere [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="6f495-242">For other verb implementation tasks, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f495-243">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f495-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f495-244">Menu di scelta rapida (contesto) e gestori di menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="6f495-244">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="6f495-245">Verbi e associazioni di file</span><span class="sxs-lookup"><span data-stu-id="6f495-245">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="6f495-246">Scelta di un verbo statico o dinamico per il menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="6f495-246">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="6f495-247">Procedure consigliate per i gestori di menu di scelta rapida e più verbi di selezione</span><span class="sxs-lookup"><span data-stu-id="6f495-247">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="6f495-248">Creazione di gestori di menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="6f495-248">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="6f495-249">Riferimento al menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="6f495-249">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
