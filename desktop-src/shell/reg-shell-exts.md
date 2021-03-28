---
description: Un oggetto gestore dell'estensione della shell deve essere registrato prima che la shell possa usarlo. Questo argomento è una descrizione generale di come registrare un gestore dell'estensione della shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrazione di gestori estensioni della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980202"
---
# <a name="registering-shell-extension-handlers"></a><span data-ttu-id="63897-104">Registrazione di gestori estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="63897-104">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="63897-105">Un oggetto gestore dell'estensione della shell deve essere registrato prima che la shell possa usarlo.</span><span class="sxs-lookup"><span data-stu-id="63897-105">A Shell extension handler object must be registered before the Shell can use it.</span></span> <span data-ttu-id="63897-106">Questo argomento è una descrizione generale di come registrare un gestore dell'estensione della shell.</span><span class="sxs-lookup"><span data-stu-id="63897-106">This topic is a general discussion of how to register a Shell extension handler.</span></span>

<span data-ttu-id="63897-107">Ogni volta che si crea o si modifica un gestore dell'estensione della shell, è importante notificare al sistema che è stata apportata una modifica.</span><span class="sxs-lookup"><span data-stu-id="63897-107">Any time you create or change a Shell extension handler, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="63897-108">A tale scopo, chiamare [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specificando l'evento **SHCNE \_ ASSOCCHANGED** .</span><span class="sxs-lookup"><span data-stu-id="63897-108">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="63897-109">Se non si chiama **SHChangeNotify**, è possibile che la modifica non venga riconosciuta fino al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="63897-109">If you do not call **SHChangeNotify**, the change might not be recognized until the system is rebooted.</span></span>

<span data-ttu-id="63897-110">Esistono alcuni fattori aggiuntivi che si applicano ai sistemi Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="63897-110">There are some additional factors that apply to Windows 2000 systems.</span></span> <span data-ttu-id="63897-111">Per informazioni dettagliate, vedere la sezione relativa alla [registrazione dei gestori estensioni della shell in sistemi Windows 2000](#registering-shell-extension-handlers) .</span><span class="sxs-lookup"><span data-stu-id="63897-111">For details, see the [Registering Shell Extension Handlers on Windows 2000 Systems](#registering-shell-extension-handlers) section.</span></span>

<span data-ttu-id="63897-112">Come con tutti gli oggetti Component Object Model (COM), è necessario creare un GUID per il gestore usando uno strumento come Guidgen.exe, fornito con Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="63897-112">As with all Component Object Model (COM) objects, you must create a GUID for the handler using a tool such as Guidgen.exe, which is provided with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="63897-113">Creare una sottochiave in **HKEY \_ classi \_ radice** \\ **CLSID** il cui nome è il formato stringa del GUID.</span><span class="sxs-lookup"><span data-stu-id="63897-113">Create a subkey under **HKEY\_CLASSES\_ROOT**\\**CLSID** whose name is the string form of that GUID.</span></span> <span data-ttu-id="63897-114">Poiché i gestori di estensioni della shell sono server in-process, è necessario creare anche una sottochiave **InprocServer32** sotto tale sottochiave GUID con il valore (predefinito) impostato sul percorso della dll del gestore.</span><span class="sxs-lookup"><span data-stu-id="63897-114">Because Shell extension handlers are in-process servers, you also must create an **InprocServer32** subkey under that GUID subkey with the (Default) value set to the path of the handler's DLL.</span></span> <span data-ttu-id="63897-115">Utilizzare il modello di threading dell'Apartment.</span><span class="sxs-lookup"><span data-stu-id="63897-115">Use the apartment threading model.</span></span> <span data-ttu-id="63897-116">Di seguito è riportato un esempio:</span><span class="sxs-lookup"><span data-stu-id="63897-116">An example is shown here:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

<span data-ttu-id="63897-117">Ogni volta che la shell esegue un'azione che può coinvolgere un gestore dell'estensione della shell, verifica la sottochiave del registro di sistema appropriata.</span><span class="sxs-lookup"><span data-stu-id="63897-117">Any time the Shell takes an action that can involve a Shell extension handler, it checks the appropriate registry subkey.</span></span> <span data-ttu-id="63897-118">La sottochiave nella quale viene registrato un gestore di estensione controlla quando verrà chiamato.</span><span class="sxs-lookup"><span data-stu-id="63897-118">The subkey under which an extension handler is registered controls when it will be called.</span></span> <span data-ttu-id="63897-119">Ad esempio, è pratica comune avere un gestore di menu di scelta rapida chiamato quando la shell Visualizza un menu di scelta rapida per un membro di un [tipo di file](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="63897-119">For instance, it is a common practice to have a shortcut menu handler called when the Shell displays a shortcut menu for a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="63897-120">In questo caso, il gestore deve essere registrato nella sottochiave **ProgID** del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="63897-120">In this case, the handler must be registered under the file type's **ProgID** subkey.</span></span>

<span data-ttu-id="63897-121">In questo argomento vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="63897-121">This topic discusses the following subjects:</span></span>

-   [<span data-ttu-id="63897-122">Nomi dei gestori</span><span class="sxs-lookup"><span data-stu-id="63897-122">Handler Names</span></span>](#handler-names)
-   [<span data-ttu-id="63897-123">Oggetti shell predefiniti</span><span class="sxs-lookup"><span data-stu-id="63897-123">Predefined Shell Objects</span></span>](#predefined-shell-objects)
-   [<span data-ttu-id="63897-124">Esempio di registrazione di un gestore estensioni</span><span class="sxs-lookup"><span data-stu-id="63897-124">Example of an Extension Handler Registration</span></span>](#example-of-an-extension-handler-registration)
    -   [<span data-ttu-id="63897-125">Registrazione di gestori estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="63897-125">Registering Shell Extension Handlers</span></span>](#registering-shell-extension-handlers)
-   [<span data-ttu-id="63897-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63897-126">Related topics</span></span>](#related-topics)

## <a name="handler-names"></a><span data-ttu-id="63897-127">Nomi dei gestori</span><span class="sxs-lookup"><span data-stu-id="63897-127">Handler Names</span></span>

<span data-ttu-id="63897-128">Per abilitare un gestore dell'estensione della shell, creare una sottochiave con il nome della sottochiave del gestore (vedere di seguito) nella sottochiave **ShellEx** del **ProgID** (per i tipi di file) o il nome del tipo di oggetto della shell (per [ \_ \_ gli oggetti shell predefiniti](handlers.md)).</span><span class="sxs-lookup"><span data-stu-id="63897-128">To enable a Shell extension handler, create a subkey with the handler subkey name (see below) under the **ShellEx** subkey of either the **ProgID** (for file types) or the Shell object type name (for [predefined\_shell\_objects](handlers.md)).</span></span>

<span data-ttu-id="63897-129">Ad esempio, se si desidera registrare un gestore dell'estensione del menu di scelta rapida per il programma. 1, iniziare creando la sottochiave seguente:</span><span class="sxs-lookup"><span data-stu-id="63897-129">For example, if you wanted to register a shortcut menu extension handler for MyProgram.1, you begin by creating the following subkey:</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

<span data-ttu-id="63897-130">Per i gestori seguenti, creare una sottochiave sotto la sottochiave "gestore della sottochiave" denominata come versione in formato stringa dell'identificatore di classe (CLSID) dell'estensione della shell.</span><span class="sxs-lookup"><span data-stu-id="63897-130">For the following handlers, create a subkey underneath the "Handler Subkey name" subkey named as the string version of the class identifier (CLSID) of the Shell extension.</span></span> <span data-ttu-id="63897-131">È possibile registrare più estensioni nel nome della sottochiave del gestore creando più sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="63897-131">Multiple extensions can be registered under the handler subkey name by creating multiple subkeys.</span></span>



| <span data-ttu-id="63897-132">Gestore</span><span class="sxs-lookup"><span data-stu-id="63897-132">Handler</span></span>                 | <span data-ttu-id="63897-133">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="63897-133">Interface</span></span>          | <span data-ttu-id="63897-134">Nome sottochiave gestore</span><span class="sxs-lookup"><span data-stu-id="63897-134">Handler Subkey Name</span></span>       |
|-------------------------|--------------------|---------------------------|
| <span data-ttu-id="63897-135">Gestore del provider di colonne</span><span class="sxs-lookup"><span data-stu-id="63897-135">Column provider handler</span></span> | <span data-ttu-id="63897-136">IColumnProvider</span><span class="sxs-lookup"><span data-stu-id="63897-136">IColumnProvider</span></span>    | <span data-ttu-id="63897-137">**ColumnHandlers**</span><span class="sxs-lookup"><span data-stu-id="63897-137">**ColumnHandlers**</span></span>        |
| <span data-ttu-id="63897-138">Gestore del menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="63897-138">Shortcut menu handler</span></span>   | <span data-ttu-id="63897-139">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="63897-139">IContextMenu</span></span>       | <span data-ttu-id="63897-140">**ContextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="63897-140">**ContextMenuHandlers**</span></span>   |
| <span data-ttu-id="63897-141">Gestore CopyHook</span><span class="sxs-lookup"><span data-stu-id="63897-141">Copyhook handler</span></span>        | <span data-ttu-id="63897-142">ICopyHook</span><span class="sxs-lookup"><span data-stu-id="63897-142">ICopyHook</span></span>          | <span data-ttu-id="63897-143">**CopyHookHandlers**</span><span class="sxs-lookup"><span data-stu-id="63897-143">**CopyHookHandlers**</span></span>      |
| <span data-ttu-id="63897-144">Gestore di trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="63897-144">Drag-and-drop handler</span></span>   | <span data-ttu-id="63897-145">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="63897-145">IContextMenu</span></span>       | <span data-ttu-id="63897-146">**DragDropHandlers**</span><span class="sxs-lookup"><span data-stu-id="63897-146">**DragDropHandlers**</span></span>      |
| <span data-ttu-id="63897-147">Gestore della finestra delle proprietà</span><span class="sxs-lookup"><span data-stu-id="63897-147">Property sheet handler</span></span>  | <span data-ttu-id="63897-148">IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="63897-148">IShellPropSheetExt</span></span> | <span data-ttu-id="63897-149">**PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="63897-149">**PropertySheetHandlers**</span></span> |



 

<span data-ttu-id="63897-150">Per i gestori seguenti, il valore predefinito della chiave del nome della sottochiave del gestore è la versione in formato stringa del CLSID dell'estensione della shell.</span><span class="sxs-lookup"><span data-stu-id="63897-150">For the following handlers, the default value of the "Handler Subkey Name" key is the string version of the CLSID of the Shell extension.</span></span> <span data-ttu-id="63897-151">Per questi gestori è possibile registrare solo un'estensione.</span><span class="sxs-lookup"><span data-stu-id="63897-151">Only one extension can be registered for these handlers.</span></span>



| <span data-ttu-id="63897-152">Gestore</span><span class="sxs-lookup"><span data-stu-id="63897-152">Handler</span></span>                 | <span data-ttu-id="63897-153">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="63897-153">Interface</span></span>            | <span data-ttu-id="63897-154">Nome sottochiave gestore</span><span class="sxs-lookup"><span data-stu-id="63897-154">Handler Subkey Name</span></span>                        |
|-------------------------|----------------------|--------------------------------------------|
| <span data-ttu-id="63897-155">Gestore dati</span><span class="sxs-lookup"><span data-stu-id="63897-155">Data handler</span></span>            | <span data-ttu-id="63897-156">IDataObject</span><span class="sxs-lookup"><span data-stu-id="63897-156">IDataObject</span></span>          | <span data-ttu-id="63897-157">**DataHandler**</span><span class="sxs-lookup"><span data-stu-id="63897-157">**DataHandler**</span></span>                            |
| <span data-ttu-id="63897-158">Gestore di trascinamento</span><span class="sxs-lookup"><span data-stu-id="63897-158">Drop handler</span></span>            | <span data-ttu-id="63897-159">IDropTarget</span><span class="sxs-lookup"><span data-stu-id="63897-159">IDropTarget</span></span>          | <span data-ttu-id="63897-160">**DropHandler**</span><span class="sxs-lookup"><span data-stu-id="63897-160">**DropHandler**</span></span>                            |
| <span data-ttu-id="63897-161">Gestore icone</span><span class="sxs-lookup"><span data-stu-id="63897-161">Icon handler</span></span>            | <span data-ttu-id="63897-162">IExtractIconA/W</span><span class="sxs-lookup"><span data-stu-id="63897-162">IExtractIconA/W</span></span>      | <span data-ttu-id="63897-163">**IconHandler**</span><span class="sxs-lookup"><span data-stu-id="63897-163">**IconHandler**</span></span>                            |
| <span data-ttu-id="63897-164">Gestore immagini di anteprima</span><span class="sxs-lookup"><span data-stu-id="63897-164">Thumbnail image handler</span></span> | <span data-ttu-id="63897-165">IThumbnailProvider</span><span class="sxs-lookup"><span data-stu-id="63897-165">IThumbnailProvider</span></span>   | <span data-ttu-id="63897-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span><span class="sxs-lookup"><span data-stu-id="63897-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span></span> |
| <span data-ttu-id="63897-167">Gestore della finestra popup</span><span class="sxs-lookup"><span data-stu-id="63897-167">Infotip handler</span></span>         | <span data-ttu-id="63897-168">IQueryInfo</span><span class="sxs-lookup"><span data-stu-id="63897-168">IQueryInfo</span></span>           | <span data-ttu-id="63897-169">**{00021500-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="63897-169">**{00021500-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="63897-170">Collegamento della shell (ANSI)</span><span class="sxs-lookup"><span data-stu-id="63897-170">Shell link (ANSI)</span></span>       | <span data-ttu-id="63897-171">IShellLinkA</span><span class="sxs-lookup"><span data-stu-id="63897-171">IShellLinkA</span></span>          | <span data-ttu-id="63897-172">**{000214EE-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="63897-172">**{000214EE-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="63897-173">Collegamento Shell (UNICODE)</span><span class="sxs-lookup"><span data-stu-id="63897-173">Shell link (UNICODE)</span></span>    | <span data-ttu-id="63897-174">IShellLinkW</span><span class="sxs-lookup"><span data-stu-id="63897-174">IShellLinkW</span></span>          | <span data-ttu-id="63897-175">**{000214F9-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="63897-175">**{000214F9-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="63897-176">Archiviazione strutturata</span><span class="sxs-lookup"><span data-stu-id="63897-176">Structured storage</span></span>      | <span data-ttu-id="63897-177">IStorage</span><span class="sxs-lookup"><span data-stu-id="63897-177">IStorage</span></span>             | <span data-ttu-id="63897-178">**{0000000B-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="63897-178">**{0000000B-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="63897-179">Metadati</span><span class="sxs-lookup"><span data-stu-id="63897-179">Metadata</span></span>                | <span data-ttu-id="63897-180">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="63897-180">IPropertySetStorage</span></span>  | <span data-ttu-id="63897-181">**Gestoreproprietà**</span><span class="sxs-lookup"><span data-stu-id="63897-181">**PropertyHandler**</span></span>                        |
| <span data-ttu-id="63897-182">Aggiungi a menu Start</span><span class="sxs-lookup"><span data-stu-id="63897-182">Pin to Start Menu</span></span>       | <span data-ttu-id="63897-183">IStartMenuPinnedList</span><span class="sxs-lookup"><span data-stu-id="63897-183">IStartMenuPinnedList</span></span> | <span data-ttu-id="63897-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span><span class="sxs-lookup"><span data-stu-id="63897-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span></span> |
| <span data-ttu-id="63897-185">Aggiungere alla barra delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="63897-185">Pin to Taskbar</span></span>          |                      | <span data-ttu-id="63897-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span><span class="sxs-lookup"><span data-stu-id="63897-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span></span> |



 

<span data-ttu-id="63897-187">Le sottochiavi specificate per aggiungere **pin al menu Start** e aggiungere **alla barra delle applicazioni** al menu di scelta rapida di un elemento sono necessarie solo per i tipi di file che includono la voce di [collegamento](./links.md) .</span><span class="sxs-lookup"><span data-stu-id="63897-187">The subkeys specified to add **Pin to Start Menu** and **Pin to Taskbar** to an item's shortcut menu are only required for file types that include the [IsShortCut](./links.md) entry.</span></span>

## <a name="predefined-shell-objects"></a><span data-ttu-id="63897-188">Oggetti shell predefiniti</span><span class="sxs-lookup"><span data-stu-id="63897-188">Predefined Shell Objects</span></span>

<span data-ttu-id="63897-189">La shell definisce oggetti aggiuntivi sotto **la \_ \_ radice delle classi HKEY** che possono essere estese in modo analogo ai tipi di file.</span><span class="sxs-lookup"><span data-stu-id="63897-189">The Shell defines additional objects under **HKEY\_CLASSES\_ROOT** which can be extended in the same way as file types.</span></span> <span data-ttu-id="63897-190">Per aggiungere un gestore della finestra delle proprietà per tutti i file, ad esempio, è possibile eseguire la registrazione nella sottochiave **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="63897-190">For example, to add a property sheet handler for all files, you can register under the **PropertySheetHandlers** subkey.</span></span>

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

<span data-ttu-id="63897-191">La tabella seguente fornisce le varie sottochiavi della **\_ \_ radice delle classi HKEY** in cui è possibile registrare i gestori di estensione.</span><span class="sxs-lookup"><span data-stu-id="63897-191">The following table gives the various subkeys of **HKEY\_CLASSES\_ROOT** under which extension handlers can be registered.</span></span> <span data-ttu-id="63897-192">Si noti che molti gestori di estensioni non possono essere registrati in tutte le sottochiavi elencate.</span><span class="sxs-lookup"><span data-stu-id="63897-192">Note that many extension handlers cannot be registered under all of the listed subkeys.</span></span> <span data-ttu-id="63897-193">Per ulteriori informazioni, vedere la documentazione del gestore specifico.</span><span class="sxs-lookup"><span data-stu-id="63897-193">For further details, see the specific handler's documentation.</span></span>



| <span data-ttu-id="63897-194">Sottochiave</span><span class="sxs-lookup"><span data-stu-id="63897-194">Subkey</span></span>                    | <span data-ttu-id="63897-195">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63897-195">Description</span></span>                                                          | <span data-ttu-id="63897-196">Possibili gestori</span><span class="sxs-lookup"><span data-stu-id="63897-196">Possible Handlers</span></span>                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="63897-197">\**\** _</span><span class="sxs-lookup"><span data-stu-id="63897-197">\**\** _</span></span>                    | <span data-ttu-id="63897-198">Tutti i file</span><span class="sxs-lookup"><span data-stu-id="63897-198">All files</span></span>                                                            | <span data-ttu-id="63897-199">Menu di scelta rapida, finestra delle proprietà, verbi (vedere di seguito)</span><span class="sxs-lookup"><span data-stu-id="63897-199">Shortcut Menu, Property Sheet, Verbs (see below)</span></span> |
| <span data-ttu-id="63897-200">_ *AllFileSystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="63897-200">_ *AllFileSystemObjects*\*</span></span>  | <span data-ttu-id="63897-201">Tutti i file e le cartelle di file</span><span class="sxs-lookup"><span data-stu-id="63897-201">All files and file folders</span></span>                                           | <span data-ttu-id="63897-202">Menu di scelta rapida, finestra delle proprietà, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-202">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="63897-203">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="63897-203">**Folder**</span></span>                | <span data-ttu-id="63897-204">Tutte le cartelle</span><span class="sxs-lookup"><span data-stu-id="63897-204">All folders</span></span>                                                          | <span data-ttu-id="63897-205">Menu di scelta rapida, finestra delle proprietà, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-205">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="63897-206">**Directory**</span><span class="sxs-lookup"><span data-stu-id="63897-206">**Directory**</span></span>             | <span data-ttu-id="63897-207">Cartelle di file</span><span class="sxs-lookup"><span data-stu-id="63897-207">File folders</span></span>                                                         | <span data-ttu-id="63897-208">Menu di scelta rapida, finestra delle proprietà, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-208">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="63897-209">**\\Sfondo directory**</span><span class="sxs-lookup"><span data-stu-id="63897-209">**Directory\\Background**</span></span> | <span data-ttu-id="63897-210">Sfondo cartella file</span><span class="sxs-lookup"><span data-stu-id="63897-210">File folder background</span></span>                                               | <span data-ttu-id="63897-211">Solo menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="63897-211">Shortcut Menu only</span></span>                               |
| <span data-ttu-id="63897-212">**DesktopBackground**</span><span class="sxs-lookup"><span data-stu-id="63897-212">**DesktopBackground**</span></span>     | <span data-ttu-id="63897-213">Sfondo del desktop (Windows 7 e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="63897-213">Desktop background (Windows 7 and higher)</span></span>                            | <span data-ttu-id="63897-214">Menu di scelta rapida, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-214">Shortcut Menu, Verbs</span></span>                             |
| <span data-ttu-id="63897-215">**Unità**</span><span class="sxs-lookup"><span data-stu-id="63897-215">**Drive**</span></span>                 | <span data-ttu-id="63897-216">Tutte le unità in computer, ad esempio "C: \\ "</span><span class="sxs-lookup"><span data-stu-id="63897-216">All drives in MyComputer, such as "C:\\"</span></span>                             | <span data-ttu-id="63897-217">Menu di scelta rapida, finestra delle proprietà, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-217">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="63897-218">**Network**</span><span class="sxs-lookup"><span data-stu-id="63897-218">**Network**</span></span>               | <span data-ttu-id="63897-219">Intera rete (in risorse di rete)</span><span class="sxs-lookup"><span data-stu-id="63897-219">Entire network (under My Network Places)</span></span>                             | <span data-ttu-id="63897-220">Menu di scelta rapida, finestra delle proprietà, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-220">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="63897-221">**Tipo di rete \\\\\#**</span><span class="sxs-lookup"><span data-stu-id="63897-221">**Network\\Type\\\#**</span></span>     | <span data-ttu-id="63897-222">Tutti gli oggetti di tipo \# (vedere di seguito)</span><span class="sxs-lookup"><span data-stu-id="63897-222">All objects of type \# (see below)</span></span>                                   | <span data-ttu-id="63897-223">Menu di scelta rapida, finestra delle proprietà, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-223">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="63897-224">**NetShare**</span><span class="sxs-lookup"><span data-stu-id="63897-224">**NetShare**</span></span>              | <span data-ttu-id="63897-225">Tutte le condivisioni di rete</span><span class="sxs-lookup"><span data-stu-id="63897-225">All network shares</span></span>                                                   | <span data-ttu-id="63897-226">Menu di scelta rapida, finestra delle proprietà, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-226">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="63897-227">**NetServer**</span><span class="sxs-lookup"><span data-stu-id="63897-227">**NetServer**</span></span>             | <span data-ttu-id="63897-228">Tutti i server di rete</span><span class="sxs-lookup"><span data-stu-id="63897-228">All network servers</span></span>                                                  | <span data-ttu-id="63897-229">Menu di scelta rapida, finestra delle proprietà, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-229">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="63897-230">*\_Nome provider di rete \_*</span><span class="sxs-lookup"><span data-stu-id="63897-230">*network\_provider\_name*</span></span> | <span data-ttu-id="63897-231">Tutti gli oggetti forniti dal provider di rete "*Network \_ provider \_ Name*"</span><span class="sxs-lookup"><span data-stu-id="63897-231">All objects provided by network provider "*network\_provider\_name*"</span></span> | <span data-ttu-id="63897-232">Menu di scelta rapida, finestra delle proprietà, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-232">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="63897-233">**Stampanti**</span><span class="sxs-lookup"><span data-stu-id="63897-233">**Printers**</span></span>              | <span data-ttu-id="63897-234">Tutte le stampanti</span><span class="sxs-lookup"><span data-stu-id="63897-234">All printers</span></span>                                                         | <span data-ttu-id="63897-235">Menu di scelta rapida, finestra delle proprietà</span><span class="sxs-lookup"><span data-stu-id="63897-235">Shortcut Menu, Property Sheet</span></span>                    |
| <span data-ttu-id="63897-236">**AudioCD**</span><span class="sxs-lookup"><span data-stu-id="63897-236">**AudioCD**</span></span>               | <span data-ttu-id="63897-237">CD audio nell'unità CD</span><span class="sxs-lookup"><span data-stu-id="63897-237">Audio CD in CD drive</span></span>                                                 | <span data-ttu-id="63897-238">Solo verbi</span><span class="sxs-lookup"><span data-stu-id="63897-238">Verbs only</span></span>                                       |
| <span data-ttu-id="63897-239">**DVD**</span><span class="sxs-lookup"><span data-stu-id="63897-239">**DVD**</span></span>                   | <span data-ttu-id="63897-240">Unità DVD (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="63897-240">DVD drive (Windows 2000)</span></span>                                             | <span data-ttu-id="63897-241">Menu di scelta rapida, finestra delle proprietà, verbi</span><span class="sxs-lookup"><span data-stu-id="63897-241">Shortcut Menu, Property Sheet, Verbs</span></span>             |



 

### <a name="notes"></a><span data-ttu-id="63897-242">Note</span><span class="sxs-lookup"><span data-stu-id="63897-242">Notes</span></span>

-   <span data-ttu-id="63897-243">Per accedere al menu di scelta rapida dello sfondo della cartella file, fare clic con il pulsante destro del mouse all'interno di una cartella di file, ma non su uno dei contenuti della cartella.</span><span class="sxs-lookup"><span data-stu-id="63897-243">The file folder background shortcut menu is accessed by right-clicking within a file folder, but not over any of the folder's contents.</span></span>
-   <span data-ttu-id="63897-244">I "verbi" sono comandi speciali registrati nel verbo della shell della sottochiave **\_ \_ radice delle classi HKEY** \\  \\  \\ .</span><span class="sxs-lookup"><span data-stu-id="63897-244">"Verbs" are special commands registered under **HKEY\_CLASSES\_ROOT**\\*Subkey*\\**Shell**\\**Verb**.</span></span>
-   <span data-ttu-id="63897-245">Per il tipo di **rete** \\  \\ **\#** , " \# " è un codice del tipo di provider di rete in decimale.</span><span class="sxs-lookup"><span data-stu-id="63897-245">For **Network**\\**Type**\\**\#**, "\#" is a network provider type code in decimal.</span></span> <span data-ttu-id="63897-246">Il codice del tipo di provider di rete è la parola più elevata di un tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="63897-246">The network provider type code is the high word of a network type.</span></span> <span data-ttu-id="63897-247">L'elenco dei tipi di rete viene specificato nel file di intestazione Winnetwk. h (WNNC \_ net \_ \* Values).</span><span class="sxs-lookup"><span data-stu-id="63897-247">The list of network types is given in the Winnetwk.h header file (WNNC\_NET\_\* values).</span></span> <span data-ttu-id="63897-248">Ad esempio, WNNC \_ net \_ Shiva è 0x00330000, quindi la sottochiave di tipo corrispondente sarà **HKEY \_ classi \_ radice** tipo di \\ **rete** \\  \\ **51**.</span><span class="sxs-lookup"><span data-stu-id="63897-248">For example, WNNC\_NET\_SHIVA is 0x00330000, so the corresponding type subkey would be **HKEY\_CLASSES\_ROOT**\\**Network**\\**Type**\\**51**.</span></span>
-   <span data-ttu-id="63897-249">"*Network \_ provider \_ Name*" è un nome di provider di rete come specificato da [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), con gli spazi convertiti in caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="63897-249">"*network\_provider\_name*" is a network provider name as specified by [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), with the spaces converted into underscores.</span></span> <span data-ttu-id="63897-250">Ad esempio, se è installato il provider rete Microsoft Networking, il nome del provider è "rete Microsoft Windows" e il *nome del \_ provider \_ di rete* corrispondente è **\_ \_ rete Microsoft Windows**.</span><span class="sxs-lookup"><span data-stu-id="63897-250">For example, if the Microsoft Networking network provider is installed, its provider name is "Microsoft Windows Network", and the corresponding *network\_provider\_name* is **Microsoft\_Windows\_Network**.</span></span>

## <a name="example-of-an-extension-handler-registration"></a><span data-ttu-id="63897-251">Esempio di registrazione di un gestore estensioni</span><span class="sxs-lookup"><span data-stu-id="63897-251">Example of an Extension Handler Registration</span></span>

<span data-ttu-id="63897-252">Per abilitare un particolare gestore, creare una sottochiave nella sottochiave del tipo di gestore dell'estensione con il nome del gestore.</span><span class="sxs-lookup"><span data-stu-id="63897-252">To enable a particular handler, create a subkey under the extension handler type subkey with the name of the handler.</span></span> <span data-ttu-id="63897-253">La shell non usa il nome del gestore, ma deve essere diverso da tutti gli altri nomi sotto tale sottochiave di tipo.</span><span class="sxs-lookup"><span data-stu-id="63897-253">The Shell does not use the handler's name, but it must be different from all other names under that type subkey.</span></span> <span data-ttu-id="63897-254">Impostare il valore predefinito della sottochiave Name sul formato stringa del GUID del gestore.</span><span class="sxs-lookup"><span data-stu-id="63897-254">Set the default value of the name subkey to the string form of the handler's GUID.</span></span>

<span data-ttu-id="63897-255">Nell'esempio seguente vengono illustrate le voci del registro di sistema che consentono il menu di scelta rapida e i gestori dell'estensione della finestra delle proprietà, utilizzando un tipo di file MYP.</span><span class="sxs-lookup"><span data-stu-id="63897-255">The following example illustrates registry entries that enable shortcut menu and property sheet extension handlers, using an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a><span data-ttu-id="63897-256">Registrazione di gestori estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="63897-256">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="63897-257">La procedura di registrazione descritta in questa sezione deve essere seguita per tutti i sistemi Windows.</span><span class="sxs-lookup"><span data-stu-id="63897-257">The registration procedure discussed in this section must be followed for all Windows systems.</span></span> <span data-ttu-id="63897-258">Tuttavia, con i sistemi successivi, potrebbe essere necessario un passaggio aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="63897-258">However, with later systems, an additional step might be necessary.</span></span> <span data-ttu-id="63897-259">Poiché queste versioni successive di Windows sono progettate per essere usate in un ambiente gestito, l'accesso al registro di sistema può essere limitato a livello amministrativo, richiedendo un approccio leggermente diverso rispetto a quello descritto nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="63897-259">Because these later versions of Windows are designed to be used in a managed environment, access to the registry could be administratively restricted, requiring a somewhat different approach to installation than described in the previous section.</span></span>

> [!Note]  
> <span data-ttu-id="63897-260">Generalmente, i programmi di installazione non devono scrivere direttamente nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="63897-260">Setup programs should generally not write directly to the registry.</span></span> <span data-ttu-id="63897-261">Al contrario, il programma di installazione deve essere eseguito con Windows Installer pacchetti.</span><span class="sxs-lookup"><span data-stu-id="63897-261">Instead, setup should be accomplished with Windows Installer packages.</span></span> <span data-ttu-id="63897-262">Questi strumenti garantiscono che il software venga eseguito correttamente e fornisca l'accesso a funzionalità come la registrazione di classi per utente.</span><span class="sxs-lookup"><span data-stu-id="63897-262">These tools ensure that software runs well and provides access to capabilities such as per-user class registration.</span></span>

 

<span data-ttu-id="63897-263">I gestori di estensioni della shell vengono eseguiti nel processo della shell.</span><span class="sxs-lookup"><span data-stu-id="63897-263">Shell extension handlers run in the Shell process.</span></span> <span data-ttu-id="63897-264">Poiché si tratta di un processo di sistema, l'amministratore di un sistema può limitare i gestori di estensioni della shell a quelli in un elenco approvato impostando il valore EnforceShellExtensionSecurity della chiave **Explorer** su 1, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="63897-264">Because it is a system process, the administrator of a system can limit Shell extension handlers to those on an approved list by setting the EnforceShellExtensionSecurity value of the **Explorer** key to 1 as shown here:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

<span data-ttu-id="63897-265">Per inserire un gestore dell'estensione della shell nell'elenco approvato, creare un valore **reg \_ SZ** il cui nome sia il formato stringa del GUID del gestore nella sottochiave **Approved** .</span><span class="sxs-lookup"><span data-stu-id="63897-265">To place a Shell extension handler on the approved list, create a **REG\_SZ** value whose name is the string form of the handler's GUID under the **Approved** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

<span data-ttu-id="63897-266">Nell'esempio seguente, ad esempio, i gestori di *comando* e *MyPropSheet* vengono aggiunti all'elenco approvato.</span><span class="sxs-lookup"><span data-stu-id="63897-266">For example, the following example adds the *MyCommand* and *MyPropSheet* handlers to the approved list.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

<span data-ttu-id="63897-267">La shell non utilizza il valore assegnato al GUID, ma deve essere impostato in modo da semplificare il controllo del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="63897-267">The Shell does not use the value that is assigned to the GUID, but it should be set to make inspecting the registry easier.</span></span>

<span data-ttu-id="63897-268">L'applicazione di installazione può aggiungere valori alla sottochiave **approvata** solo se l'utente che installa l'applicazione dispone di privilegi sufficienti.</span><span class="sxs-lookup"><span data-stu-id="63897-268">Your setup application can add values to the **Approved** subkey only if the person installing the application has sufficient privileges.</span></span> <span data-ttu-id="63897-269">Se il tentativo di aggiungere un gestore di estensione ha esito negativo, è necessario informare l'utente che sono necessari privilegi amministrativi per installare completamente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="63897-269">If the attempt to add an extension handler fails, you should inform the user that administrative privileges are required to fully install the application.</span></span> <span data-ttu-id="63897-270">Se il gestore è essenziale per l'applicazione, è necessario interrompere l'installazione e inviare una notifica all'utente per contattare un amministratore.</span><span class="sxs-lookup"><span data-stu-id="63897-270">If the handler is essential to the application, you should fail the setup and notify the user to contact an administrator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63897-271">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63897-271">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63897-272">Inizializzazione di gestori estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="63897-272">Initializing Shell Extension Handlers</span></span>](int-shell-exts.md)
</dt> </dl>

 

 
