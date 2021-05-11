---
description: I gestori del menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore del tipo di file. Come tutti questi gestori, si tratta di oggetti Component Object Model (COM) implementati come DLL.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Creazione di gestori di menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e102833453566f42d058ff82061f34ebc65691
ms.sourcegitcommit: 9655f82be96b11258276fdefff14423c30552fbb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/11/2021
ms.locfileid: "109740572"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="e2028-104">Creazione di gestori di menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="e2028-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="e2028-105">I gestori del menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="e2028-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="e2028-106">Questi gestori possono essere impelmentati in modo da caricarli nel proprio processo o in Esplora risorse o in altri processi di terze parti.</span><span class="sxs-lookup"><span data-stu-id="e2028-106">These handlers may be impelmented in a way that causes them to load in their own process or in the explorer, or other 3rd party processes.</span></span> <span data-ttu-id="e2028-107">Quando si creano gestori in-process, è necessario fare attenzione perché possono causare danni al processo che li carica.</span><span class="sxs-lookup"><span data-stu-id="e2028-107">Take care when creating in-process handlers as they can cause harm to the process that loads them.</span></span>

> [!Note]  
> <span data-ttu-id="e2028-108">Esistono considerazioni speciali per le versioni di Windows basate su 64 bit durante la registrazione di gestori che funzionano nel contesto di applicazioni a 32 bit: quando viene richiamato nel contesto di un'applicazione di bit diversi, il sottosistema WOW64 reindirizza l'accesso file system ad alcuni percorsi.</span><span class="sxs-lookup"><span data-stu-id="e2028-108">There are special considerations for 64-bit based versions of Windows when registering handlers that work in the context of 32-bit applications: when invoked in the context of an application of different bitness, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="e2028-109">Se il gestore .exe è archiviato in uno di questi percorsi, non è accessibile in questo contesto.</span><span class="sxs-lookup"><span data-stu-id="e2028-109">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="e2028-110">Pertanto, per risolvere il problema, archiviare il file exe in un percorso che non viene reindirizzato o archiviare una versione stub del file exe che avvia la versione reale.</span><span class="sxs-lookup"><span data-stu-id="e2028-110">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

<span data-ttu-id="e2028-111">Questo argomento è organizzato come segue:</span><span class="sxs-lookup"><span data-stu-id="e2028-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e2028-112">Verbi canonici</span><span class="sxs-lookup"><span data-stu-id="e2028-112">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="e2028-113">Verbi estesi</span><span class="sxs-lookup"><span data-stu-id="e2028-113">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="e2028-114">Verbi solo per l'accesso a livello di codice</span><span class="sxs-lookup"><span data-stu-id="e2028-114">Programmatic Access Only Verbs</span></span>](#programmaticaccessonly-verbs)
-   [<span data-ttu-id="e2028-115">Personalizzazione di un menu di scelta rapida tramite verbi statici</span><span class="sxs-lookup"><span data-stu-id="e2028-115">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="e2028-116">Attivazione del gestore tramite l'interfaccia IDropTarget</span><span class="sxs-lookup"><span data-stu-id="e2028-116">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="e2028-117">Specifica della posizione e dell'ordine dei verbi statici</span><span class="sxs-lookup"><span data-stu-id="e2028-117">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="e2028-118">Verbi di posizionamento nella parte superiore o inferiore del menu</span><span class="sxs-lookup"><span data-stu-id="e2028-118">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="e2028-119">Creazione di menu a cascata statici</span><span class="sxs-lookup"><span data-stu-id="e2028-119">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="e2028-120">Recupero del comportamento dinamico per i verbi statici tramite la sintassi di query avanzata</span><span class="sxs-lookup"><span data-stu-id="e2028-120">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="e2028-121">Deprecato: Associazione di verbi a Dynamic Data Exchange comandi</span><span class="sxs-lookup"><span data-stu-id="e2028-121">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="e2028-122">Completamento delle attività di implementazione dei verbi</span><span class="sxs-lookup"><span data-stu-id="e2028-122">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="e2028-123">Personalizzazione del menu di scelta rapida per gli oggetti predefiniti della shell</span><span class="sxs-lookup"><span data-stu-id="e2028-123">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="e2028-124">Estensione di un nuovo sottomenu</span><span class="sxs-lookup"><span data-stu-id="e2028-124">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="e2028-125">Eliminazione di verbi e controllo della visibilità</span><span class="sxs-lookup"><span data-stu-id="e2028-125">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="e2028-126">Utilizzo del modello di selezione dei verbi</span><span class="sxs-lookup"><span data-stu-id="e2028-126">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="e2028-127">Uso degli attributi degli elementi</span><span class="sxs-lookup"><span data-stu-id="e2028-127">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="e2028-128">Implementazione di verbi personalizzati per le cartelle tramite Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="e2028-128">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="e2028-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2028-129">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="e2028-130">Verbi canonici</span><span class="sxs-lookup"><span data-stu-id="e2028-130">Canonical Verbs</span></span>

<span data-ttu-id="e2028-131">Le applicazioni sono in genere responsabili di fornire stringhe di visualizzazione localizzate per i verbi definiti.</span><span class="sxs-lookup"><span data-stu-id="e2028-131">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="e2028-132">Tuttavia, per fornire un grado di indipendenza del linguaggio, il sistema definisce un set standard di verbi di uso comune denominati verbi canonici.</span><span class="sxs-lookup"><span data-stu-id="e2028-132">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="e2028-133">Un verbo canonico non viene mai visualizzato all'utente e può essere usato con qualsiasi lingua dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="e2028-133">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="e2028-134">Il sistema usa il nome canonico per generare automaticamente una stringa di visualizzazione localizzata correttamente.</span><span class="sxs-lookup"><span data-stu-id="e2028-134">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="e2028-135">Ad esempio, la stringa di visualizzazione del verbo aperto è impostata su **Open** in un sistema inglese e sull'equivalente tedesco in un sistema tedesco.</span><span class="sxs-lookup"><span data-stu-id="e2028-135">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>


| <span data-ttu-id="e2028-136">Verbo canonico</span><span class="sxs-lookup"><span data-stu-id="e2028-136">Canonical verb</span></span> | <span data-ttu-id="e2028-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2028-137">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="e2028-138">Apri</span><span class="sxs-lookup"><span data-stu-id="e2028-138">Open</span></span>           | <span data-ttu-id="e2028-139">Apre il file o la cartella.</span><span class="sxs-lookup"><span data-stu-id="e2028-139">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="e2028-140">Opennew</span><span class="sxs-lookup"><span data-stu-id="e2028-140">Opennew</span></span>        | <span data-ttu-id="e2028-141">Apre il file o la cartella in una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="e2028-141">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="e2028-142">Stampa</span><span class="sxs-lookup"><span data-stu-id="e2028-142">Print</span></span>          | <span data-ttu-id="e2028-143">Stampa il file.</span><span class="sxs-lookup"><span data-stu-id="e2028-143">Prints the file.</span></span>                                                     |
| <span data-ttu-id="e2028-144">Printto</span><span class="sxs-lookup"><span data-stu-id="e2028-144">Printto</span></span>        | <span data-ttu-id="e2028-145">Consente all'utente di stampare un file trascinandolo in un oggetto stampante.</span><span class="sxs-lookup"><span data-stu-id="e2028-145">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="e2028-146">Esplora</span><span class="sxs-lookup"><span data-stu-id="e2028-146">Explore</span></span>        | <span data-ttu-id="e2028-147">Apre Esplora risorse con la cartella selezionata.</span><span class="sxs-lookup"><span data-stu-id="e2028-147">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="e2028-148">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2028-148">Properties</span></span>     | <span data-ttu-id="e2028-149">Apre la finestra delle proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e2028-149">Opens the object's property sheet.</span></span>                                   |

> [!Note]  
> <span data-ttu-id="e2028-150">Anche **il verbo Printto** è canonico, ma non viene mai visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e2028-150">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="e2028-151">L'inclusione consente all'utente di stampare un file trascinandolo in un oggetto stampante.</span><span class="sxs-lookup"><span data-stu-id="e2028-151">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

<span data-ttu-id="e2028-152">I gestori del menu di scelta rapida possono fornire verbi canonici tramite [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) con **GCS \_ VERBW** o **GCS \_ VERBA.**</span><span class="sxs-lookup"><span data-stu-id="e2028-152">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="e2028-153">Il sistema userà i verbi canonici come secondo parametro (*lpOperation*) passato a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)e è [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). **Membro lpVerb** passato al [**metodo IContextMenu::InvokeCommand.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)</span><span class="sxs-lookup"><span data-stu-id="e2028-153">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="e2028-154">Verbi estesi</span><span class="sxs-lookup"><span data-stu-id="e2028-154">Extended Verbs</span></span>

<span data-ttu-id="e2028-155">Quando l'utente fa clic con il pulsante destro del mouse su un oggetto, nel menu di scelta rapida vengono visualizzati i verbi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="e2028-155">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="e2028-156">È possibile aggiungere e supportare comandi in alcuni menu di scelta rapida che non vengono visualizzati in ogni menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e2028-156">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="e2028-157">Ad esempio, è possibile avere comandi che non vengono comunemente usati o destinati a utenti esperti.</span><span class="sxs-lookup"><span data-stu-id="e2028-157">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="e2028-158">Per questo motivo, è anche possibile definire uno o più verbi estesi.</span><span class="sxs-lookup"><span data-stu-id="e2028-158">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="e2028-159">Questi verbi sono simili ai verbi normali, ma si distinguono dai verbi normali dal modo in cui vengono registrati.</span><span class="sxs-lookup"><span data-stu-id="e2028-159">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="e2028-160">Per accedere ai verbi estesi, l'utente deve fare clic con il pulsante destro del mouse su un oggetto mentre si preme MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="e2028-160">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="e2028-161">Quando l'utente esegue questa operazione, oltre ai verbi predefiniti vengono visualizzati i verbi estesi.</span><span class="sxs-lookup"><span data-stu-id="e2028-161">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="e2028-162">È possibile usare il Registro di sistema per definire uno o più verbi estesi.</span><span class="sxs-lookup"><span data-stu-id="e2028-162">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="e2028-163">I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto premendo anche MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="e2028-163">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="e2028-164">Per definire un verbo come esteso, aggiungere un valore **\_ REG SZ** "esteso" alla sottochiave del verbo.</span><span class="sxs-lookup"><span data-stu-id="e2028-164">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="e2028-165">Al valore non deve essere associato alcun dato.</span><span class="sxs-lookup"><span data-stu-id="e2028-165">The value should not have any data associated with it.</span></span>

## <a name="programmatic-access-only"></a><span data-ttu-id="e2028-166">Solo accesso a livello di codice</span><span class="sxs-lookup"><span data-stu-id="e2028-166">Programmatic Access Only</span></span>

<span data-ttu-id="e2028-167">Questi verbi non vengono mai visualizzati in un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e2028-167">These verbs are never displayed in a context menu.</span></span> <span data-ttu-id="e2028-168">È possibile accedervi tramite [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) e specificando il campo **lpVerb** del *parametro pExecInfo* (un [oggetto SHELLEXECUTEINFO).](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa)</span><span class="sxs-lookup"><span data-stu-id="e2028-168">These can be accessed by using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) and specifying the **lpVerb** field of the *pExecInfo* parameter (a [SHELLEXECUTEINFO](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) object).</span></span> <span data-ttu-id="e2028-169">Per definire un verbo solo come accesso a livello di codice, aggiungere un valore **\_ REG SZ** "ProgrammaticAccessOnly" alla sottochiave del verbo.</span><span class="sxs-lookup"><span data-stu-id="e2028-169">To define a verb as programmatic access only, add a "ProgrammaticAccessOnly" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="e2028-170">Al valore non deve essere associato alcun dato.</span><span class="sxs-lookup"><span data-stu-id="e2028-170">The value should not have any data associated with it.</span></span>

<span data-ttu-id="e2028-171">È possibile usare il Registro di sistema per definire uno o più verbi estesi.</span><span class="sxs-lookup"><span data-stu-id="e2028-171">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="e2028-172">I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto premendo anche MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="e2028-172">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="e2028-173">Per definire un verbo come esteso, aggiungere un valore **\_ REG SZ** "extended" alla sottochiave del verbo.</span><span class="sxs-lookup"><span data-stu-id="e2028-173">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="e2028-174">Al valore non deve essere associato alcun dato.</span><span class="sxs-lookup"><span data-stu-id="e2028-174">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="e2028-175">Personalizzazione di un menu di scelta rapida tramite verbi statici</span><span class="sxs-lookup"><span data-stu-id="e2028-175">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="e2028-176">Dopo [aver scelto un verbo](shortcut-choose-method.md) statico o dinamico per il menu di scelta rapida, è possibile estendere il menu di scelta rapida per un tipo di file registrando un verbo statico per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="e2028-176">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="e2028-177">A tale scopo, aggiungere una **sottochiave Shell** sotto la sottochiave per il ProgID dell'applicazione associata al tipo di file.</span><span class="sxs-lookup"><span data-stu-id="e2028-177">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="e2028-178">Facoltativamente, è possibile definire un verbo predefinito per il tipo di file impostandolo come valore predefinito della **sottochiave Shell.**</span><span class="sxs-lookup"><span data-stu-id="e2028-178">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="e2028-179">Il verbo predefinito viene visualizzato per primo nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e2028-179">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="e2028-180">Lo scopo è fornire alla shell un verbo che può usare quando viene chiamata la [**funzione ShellExecuteEx,**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ma non viene specificato alcun verbo.</span><span class="sxs-lookup"><span data-stu-id="e2028-180">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="e2028-181">Shell non seleziona necessariamente il verbo predefinito quando **shellExecuteEx** viene usato in questo modo.</span><span class="sxs-lookup"><span data-stu-id="e2028-181">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="e2028-182">La shell usa il primo verbo disponibile nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="e2028-182">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="e2028-183">Verbo predefinito</span><span class="sxs-lookup"><span data-stu-id="e2028-183">The default verb</span></span>
2.  <span data-ttu-id="e2028-184">Primo verbo nel Registro di sistema, se viene specificato l'ordine dei verbi</span><span class="sxs-lookup"><span data-stu-id="e2028-184">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="e2028-185">Verbo **Open**</span><span class="sxs-lookup"><span data-stu-id="e2028-185">The **Open** verb</span></span>
4.  <span data-ttu-id="e2028-186">Verbo **Open With**</span><span class="sxs-lookup"><span data-stu-id="e2028-186">The **Open With** verb</span></span>

<span data-ttu-id="e2028-187">Se nessuno dei verbi elencati è disponibile, l'operazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="e2028-187">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="e2028-188">Creare una sottochiave per ogni verbo da aggiungere nella sottochiave Shell.</span><span class="sxs-lookup"><span data-stu-id="e2028-188">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="e2028-189">Ognuna di queste sottochiavi deve avere un **valore REG \_ SZ** impostato sulla stringa di visualizzazione del verbo (stringa localizzata).</span><span class="sxs-lookup"><span data-stu-id="e2028-189">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="e2028-190">Per ogni sottochiave verbo, creare una sottochiave di comando con il valore predefinito impostato sulla riga di comando per l'attivazione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="e2028-190">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="e2028-191">Per i verbi canonici, ad esempio **Open** e **Print**, è possibile omettere la stringa di visualizzazione perché il sistema visualizza automaticamente una stringa localizzata correttamente.</span><span class="sxs-lookup"><span data-stu-id="e2028-191">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="e2028-192">Per i verbi non canonici, se si omette la stringa di visualizzazione, viene visualizzata la stringa del verbo.</span><span class="sxs-lookup"><span data-stu-id="e2028-192">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="e2028-193">Nell'esempio del Registro di sistema seguente si noti che:</span><span class="sxs-lookup"><span data-stu-id="e2028-193">In the following registry example, note that:</span></span>

-   <span data-ttu-id="e2028-194">Poiché **Doit** non è un verbo canonico, viene assegnato un nome visualizzato, che può essere selezionato premendo il tasto D.</span><span class="sxs-lookup"><span data-stu-id="e2028-194">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="e2028-195">Il **verbo Printto** non viene visualizzato nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e2028-195">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="e2028-196">Tuttavia, la sua inclusione nel Registro di sistema consente all'utente di stampare i file rilasciandoli su un'icona della stampante.</span><span class="sxs-lookup"><span data-stu-id="e2028-196">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="e2028-197">Per ogni verbo viene visualizzata una sottochiave.</span><span class="sxs-lookup"><span data-stu-id="e2028-197">One subkey is shown for each verb.</span></span> <span data-ttu-id="e2028-198">**%1** rappresenta il nome del file e **%2 il** nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="e2028-198">**%1** represents the file name and **%2** the printer name.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

<span data-ttu-id="e2028-199">Il diagramma seguente illustra l'estensione del menu di scelta rapida in base alle voci del Registro di sistema precedenti.</span><span class="sxs-lookup"><span data-stu-id="e2028-199">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="e2028-200">Questo menu di scelta rapida include verbi **Open**, **Do It** e **Print** nel menu, con Do **It** come verbo predefinito.</span><span class="sxs-lookup"><span data-stu-id="e2028-200">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![Screenshot del menu di scelta rapida del verbo predefinito do it](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="e2028-202">Attivazione del gestore tramite l'interfaccia IDropTarget</span><span class="sxs-lookup"><span data-stu-id="e2028-202">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="e2028-203">Dynamic Data Exchange (DDE) è deprecato. usare [**invece IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)</span><span class="sxs-lookup"><span data-stu-id="e2028-203">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="e2028-204">**IDropTarget è** più affidabile e ha un supporto di attivazione migliore perché usa l'attivazione COM del gestore.</span><span class="sxs-lookup"><span data-stu-id="e2028-204">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="e2028-205">Nel caso di selezione di più elementi, **IDropTarget** non è soggetto alle restrizioni relative alle dimensioni del buffer presenti sia in DDE che in [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="e2028-205">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="e2028-206">Inoltre, gli elementi vengono passati all'applicazione come oggetto dati che può essere convertito in una matrice di elementi usando la [**funzione SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)</span><span class="sxs-lookup"><span data-stu-id="e2028-206">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="e2028-207">Questa operazione è più semplice e non perde le informazioni sullo spazio dei nomi come si verifica quando l'elemento viene convertito in un percorso per i protocolli della riga di comando o DDE.</span><span class="sxs-lookup"><span data-stu-id="e2028-207">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="e2028-208">Per altre informazioni sulle query [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione di file, vedere [Tipi percepiti e Registrazione dell'applicazione.](fa-perceivedtypes.md)</span><span class="sxs-lookup"><span data-stu-id="e2028-208">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="e2028-209">Specifica della posizione e dell'ordine dei verbi statici</span><span class="sxs-lookup"><span data-stu-id="e2028-209">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="e2028-210">In genere i verbi vengono ordinati in un menu di scelta rapida in base alla modalità di enumerazione; L'enumerazione è basata prima sull'ordine della matrice di associazioni e quindi sull'ordine degli elementi nella matrice di associazione, come definito dall'ordinamento del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e2028-210">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="e2028-211">I verbi possono essere ordinati specificando il valore predefinito della sottochiave Shell per la voce di associazione.</span><span class="sxs-lookup"><span data-stu-id="e2028-211">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="e2028-212">Questo valore predefinito può includere un singolo elemento, che verrà visualizzato nella posizione superiore del menu di scelta rapida, o un elenco di elementi separati da spazi o virgole.</span><span class="sxs-lookup"><span data-stu-id="e2028-212">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="e2028-213">Nel secondo caso, il primo elemento dell'elenco è l'elemento predefinito e gli altri verbi vengono visualizzati immediatamente sotto di esso nell'ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="e2028-213">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="e2028-214">Ad esempio, la voce del Registro di sistema seguente produce verbi di menu di scelta rapida nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="e2028-214">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="e2028-215">Visualizza</span><span class="sxs-lookup"><span data-stu-id="e2028-215">Display</span></span>
2.  <span data-ttu-id="e2028-216">Gadget</span><span class="sxs-lookup"><span data-stu-id="e2028-216">Gadgets</span></span>
3.  <span data-ttu-id="e2028-217">Personalization</span><span class="sxs-lookup"><span data-stu-id="e2028-217">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="e2028-218">Analogamente, la voce del Registro di sistema seguente produce verbi di menu di scelta rapida nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="e2028-218">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="e2028-219">Personalization</span><span class="sxs-lookup"><span data-stu-id="e2028-219">Personalization</span></span>
2.  <span data-ttu-id="e2028-220">Gadget</span><span class="sxs-lookup"><span data-stu-id="e2028-220">Gadgets</span></span>
3.  <span data-ttu-id="e2028-221">Visualizza</span><span class="sxs-lookup"><span data-stu-id="e2028-221">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="e2028-222">Posizionamento dei verbi nella parte superiore o inferiore del menu</span><span class="sxs-lookup"><span data-stu-id="e2028-222">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="e2028-223">L'attributo del Registro di sistema seguente può essere usato per posizionare un verbo nella parte superiore o inferiore del menu.</span><span class="sxs-lookup"><span data-stu-id="e2028-223">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="e2028-224">Se sono presenti più verbi che specificano questo attributo, l'ultimo a tale scopo ottiene la priorità:</span><span class="sxs-lookup"><span data-stu-id="e2028-224">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="e2028-225">Creazione di menu a cascata statici</span><span class="sxs-lookup"><span data-stu-id="e2028-225">Creating Static Cascading Menus</span></span>

<span data-ttu-id="e2028-226">In Windows 7 e versioni successive l'implementazione del menu a cascata è supportata tramite le impostazioni del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e2028-226">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="e2028-227">Nelle versioni precedenti a Windows 7 la creazione di menu a cascata era possibile solo tramite l'implementazione [**dell'interfaccia IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)</span><span class="sxs-lookup"><span data-stu-id="e2028-227">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="e2028-228">In Windows 7 e versioni successive è consigliabile ricorrere a soluzioni basate su codice COM solo quando i metodi statici non sono sufficienti.</span><span class="sxs-lookup"><span data-stu-id="e2028-228">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="e2028-229">Lo screenshot seguente fornisce un esempio di menu a cascata.</span><span class="sxs-lookup"><span data-stu-id="e2028-229">The following screen shot provides an example of a cascading menu.</span></span>

![Screenshot che mostra un esempio di menu a cascata](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="e2028-231">In Windows 7 e versioni successive sono disponibili tre modi per creare menu a catena:</span><span class="sxs-lookup"><span data-stu-id="e2028-231">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="e2028-232">Creazione di menu a catena con la voce del Registro di sistema SubCommands</span><span class="sxs-lookup"><span data-stu-id="e2028-232">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="e2028-233">Creazione di menu a catena con la voce del Registro di sistema ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="e2028-233">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="e2028-234">Creazione di menu a cascata con l'interfaccia IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="e2028-234">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="e2028-235">Creazione di menu a catena con la voce del Registro di sistema SubCommands</span><span class="sxs-lookup"><span data-stu-id="e2028-235">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="e2028-236">In Windows 7 e versioni successive è possibile usare la voce Sottocomandi per creare menu a catena usando la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="e2028-236">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="e2028-237">**Per creare un menu a cascata usando la voce SubCommands**</span><span class="sxs-lookup"><span data-stu-id="e2028-237">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="e2028-238">Creare una sottochiave in **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* \\ **shell** per rappresentare il menu a cascata.</span><span class="sxs-lookup"><span data-stu-id="e2028-238">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="e2028-239">In questo esempio si assegna a questa sottochiave il nome *CascadeTest*.</span><span class="sxs-lookup"><span data-stu-id="e2028-239">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="e2028-240">Assicurarsi che il valore predefinito della *sottochiave CascadeTest* sia vuoto e visualizzato come **(valore non impostato).**</span><span class="sxs-lookup"><span data-stu-id="e2028-240">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="e2028-241">Alla *sottochiave CascadeTest* aggiungere una voce MUIVerb di tipo **REG \_ SZ** e assegnarle il testo che verrà visualizzato come nome nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e2028-241">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="e2028-242">In questo esempio viene assegnato "Test Cascade Menu".</span><span class="sxs-lookup"><span data-stu-id="e2028-242">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="e2028-243">Alla *sottochiave CascadeTest* aggiungere una voce SubCommands di tipo **REG \_ SZ** a cui è assegnato l'elenco, demlimitato da punti e virgola, dei verbi che devono essere visualizzati nel menu nell'ordine di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e2028-243">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="e2028-244">Ad esempio, qui viene assegnato un numero di verbi forniti dal sistema:</span><span class="sxs-lookup"><span data-stu-id="e2028-244">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="e2028-245">Nel caso di verbi personalizzati, implementarli usando uno dei metodi di implementazione dei verbi statici ed elencarli nella sottochiave **CommandStore,** come illustrato in questo esempio per un verbo *fittizio VerbName*:</span><span class="sxs-lookup"><span data-stu-id="e2028-245">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> <span data-ttu-id="e2028-246">Questo metodo ha il vantaggio che i verbi personalizzati possono essere registrati una sola volta e riutilizzati elencando il nome del verbo nella voce SubCommands.</span><span class="sxs-lookup"><span data-stu-id="e2028-246">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="e2028-247">Tuttavia, è necessario che l'applicazione abbia l'autorizzazione per modificare il Registro di sistema in **HKEY \_ LOCAL \_ MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="e2028-247">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="e2028-248">Creazione di menu a catena con la voce del Registro di sistema ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="e2028-248">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="e2028-249">In Windows 7 e versioni successive è possibile usare la voce ExtendedSubCommandKey per creare menu a cascata estesi: menu a cascata all'interno dei menu a cascata.</span><span class="sxs-lookup"><span data-stu-id="e2028-249">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="e2028-250">Lo screenshot seguente è un esempio di menu a cascata esteso.</span><span class="sxs-lookup"><span data-stu-id="e2028-250">The following screen shot is an example of an extended cascading menu.</span></span>

![Screenshot che mostra il menu a cascata esteso per i dispositivi](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="e2028-252">Poiché **HKEY \_ CLASSES \_ ROOT** è una combinazione di **HKEY CURRENT \_ \_ USER** e **HKEY LOCAL \_ \_ MACHINE,** è possibile registrare qualsiasi verbo personalizzato nella sottochiave **HKEY CURRENT \_ \_ USER** \\ **Software** \\ **Classes.**</span><span class="sxs-lookup"><span data-stu-id="e2028-252">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="e2028-253">Il vantaggio principale di questa operazione è che non è necessaria l'autorizzazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="e2028-253">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="e2028-254">Inoltre, altre associazioni di file possono riutilizzare l'intero set di verbi specificando la stessa sottochiave ExtendedSubCommandsKey.</span><span class="sxs-lookup"><span data-stu-id="e2028-254">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="e2028-255">Se non è necessario riutilizzare questo set di verbi, è possibile elencare i verbi sotto l'elemento padre, ma assicurarsi che il valore Predefinito dell'elemento padre sia vuoto.</span><span class="sxs-lookup"><span data-stu-id="e2028-255">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="e2028-256">**Per creare un menu a cascata usando una voce ExtendedSubCommandsKey**</span><span class="sxs-lookup"><span data-stu-id="e2028-256">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="e2028-257">Creare una sottochiave nella shell **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* \\  per rappresentare il menu a cascata.</span><span class="sxs-lookup"><span data-stu-id="e2028-257">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="e2028-258">In questo esempio a questa sottochiave viene dato il nome *CascadeTest2*.</span><span class="sxs-lookup"><span data-stu-id="e2028-258">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="e2028-259">Verificare che il valore predefinito della *sottochiave CascadeTest* sia vuoto e visualizzato come **(valore non impostato).**</span><span class="sxs-lookup"><span data-stu-id="e2028-259">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="e2028-260">Alla *sottochiave CascadeTest* aggiungere una voce MUIVerb di tipo **REG \_ SZ** e assegnarle il testo che verrà visualizzato come nome nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e2028-260">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="e2028-261">In questo esempio viene assegnato "Test Cascade Menu".</span><span class="sxs-lookup"><span data-stu-id="e2028-261">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="e2028-262">Nella *sottochiave CascadeTest* creata aggiungere una sottochiave **ExtendedSubCommandsKey** e quindi aggiungere i sottocomandi del documento (di tipo **REG \_ SZ),** ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e2028-262">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    <span data-ttu-id="e2028-263">Verificare che il valore predefinito della *sottochiave Test Cascade Menu 2* sia vuoto e visualizzato come **(valore non impostato).**</span><span class="sxs-lookup"><span data-stu-id="e2028-263">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="e2028-264">Popolare i sottoverbi usando una delle implementazioni di verbi statici seguenti.</span><span class="sxs-lookup"><span data-stu-id="e2028-264">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="e2028-265">Si noti che la sottochiave CommandFlags rappresenta i valori EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="e2028-265">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="e2028-266">Se si vuole aggiungere un separatore prima o dopo la voce di menu a catena, usare ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="e2028-266">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="e2028-267">Per una descrizione di questi flag di Windows 7 e versioni successive, vedere [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="e2028-267">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="e2028-268">ECF \_ SEPARATORBEFORE funziona solo per le voci di menu di primo livello.</span><span class="sxs-lookup"><span data-stu-id="e2028-268">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="e2028-269">MUIVerb è di tipo **REG \_ SZ** e CommandFlags è di tipo **REG \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e2028-269">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

<span data-ttu-id="e2028-270">Lo screenshot seguente è un'illustrazione degli esempi di voci di chiave del Registro di sistema precedenti.</span><span class="sxs-lookup"><span data-stu-id="e2028-270">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![Screenshot che mostra un esempio di menu a cascata che mostra le opzioni del Blocco note e del wordpad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="e2028-272">Creazione di menu a cascata con l'interfaccia IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="e2028-272">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="e2028-273">Un'altra opzione per l'aggiunta di verbi a un menu a cascata è [**tramite IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="e2028-273">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="e2028-274">Questo metodo consente alle origini dati che forniscono i comandi del modulo di comando [**tramite IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) di usare tali comandi come verbi in un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e2028-274">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="e2028-275">In Windows 7 e versioni successive è possibile fornire la stessa implementazione del verbo [**usando IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) come con [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="e2028-275">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="e2028-276">Le due schermate seguenti illustrano l'uso dei menu a cascata nella **cartella** Dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e2028-276">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Screenshot che mostra un esempio di menu a cascata nella cartella devices.](images/file-assoc/filecascademenu.png)

<span data-ttu-id="e2028-278">La schermata seguente illustra un'altra implementazione di un menu a cascata nella **cartella** Dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e2028-278">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![Screenshot che mostra un esempio di menu a cascata nella cartella devices](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="e2028-280">Poiché [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supporta solo l'attivazione in-process, è consigliabile usarlo dalle origini dati shell che devono condividere l'implementazione tra comandi e menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e2028-280">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="e2028-281">Recupero del comportamento dinamico per i verbi statici tramite la sintassi di query avanzata</span><span class="sxs-lookup"><span data-stu-id="e2028-281">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="e2028-282">Advanced Query Syntax (AQS) può esprimere una condizione che verrà valutata usando le proprietà dell'elemento per cui viene creata un'istanza del verbo.</span><span class="sxs-lookup"><span data-stu-id="e2028-282">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="e2028-283">Questo sistema funziona solo con proprietà veloci.</span><span class="sxs-lookup"><span data-stu-id="e2028-283">This system works only with fast properties.</span></span> <span data-ttu-id="e2028-284">Si tratta di proprietà segnalate dall'origine dati Shell con la velocità più rapida, perché non restituiscono [\*\*\*\*SHCOLSTATE \_ SLOW\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) da [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span><span class="sxs-lookup"><span data-stu-id="e2028-284">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="e2028-285">Windows 7 e versioni successive supportano valori canonici che evitano problemi nelle build localizzate.</span><span class="sxs-lookup"><span data-stu-id="e2028-285">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="e2028-286">La sintassi canonica seguente è necessaria nelle build localizzate per sfruttare i vantaggi di questo miglioramento di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e2028-286">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="e2028-287">Nella voce del Registro di sistema di esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="e2028-287">In the following example registry entry:</span></span>

-   <span data-ttu-id="e2028-288">Il **valore AppliesTo** controlla se il verbo viene visualizzato o nascosto.</span><span class="sxs-lookup"><span data-stu-id="e2028-288">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="e2028-289">Il valore DefaultAppliesTo controlla quale verbo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e2028-289">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="e2028-290">Il valore HasLUAShield controlla se viene visualizzata una schermatura di Controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="e2028-290">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="e2028-291">In questo esempio il **valore DefaultAppliesTo** rende questo verbo l'impostazione predefinita per qualsiasi file con la parola "exampleText1" nel nome file.</span><span class="sxs-lookup"><span data-stu-id="e2028-291">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="e2028-292">Il **valore AppliesTo** abilita il verbo per qualsiasi file con "exampleText1" nel nome.</span><span class="sxs-lookup"><span data-stu-id="e2028-292">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="e2028-293">Il **valore HasLUAShield visualizza** lo shield per i file con "exampleText2" nel nome.</span><span class="sxs-lookup"><span data-stu-id="e2028-293">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="e2028-294">Aggiungere la **sottochiave** Command e un valore:</span><span class="sxs-lookup"><span data-stu-id="e2028-294">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="e2028-295">Nel Registro di sistema di Windows 7, vedere HKEY CLASSES ROOT drive (Unità **HKEY \_ CLASSES \_ ROOT)** come esempio di \\  verbi bitlocker che adottano l'approccio seguente:</span><span class="sxs-lookup"><span data-stu-id="e2028-295">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="e2028-296">AppliesTo = System.Volume.BitlockerProtection:=2</span><span class="sxs-lookup"><span data-stu-id="e2028-296">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="e2028-297">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean \# True</span><span class="sxs-lookup"><span data-stu-id="e2028-297">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="e2028-298">Per altre informazioni su AQS, vedere [Sintassi di query avanzata.](../search/-search-3x-advancedquerysyntax.md)</span><span class="sxs-lookup"><span data-stu-id="e2028-298">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="e2028-299">Deprecato: Associazione di verbi a Dynamic Data Exchange comandi</span><span class="sxs-lookup"><span data-stu-id="e2028-299">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="e2028-300">DDE è deprecato. in [**alternativa, usare IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)</span><span class="sxs-lookup"><span data-stu-id="e2028-300">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="e2028-301">DDE è deprecato perché si basa su un messaggio di finestra di trasmissione per individuare il server DDE.</span><span class="sxs-lookup"><span data-stu-id="e2028-301">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="e2028-302">Un blocco del server DDE blocca il messaggio della finestra di trasmissione e pertanto blocca le conversazioni DDE per altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e2028-302">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="e2028-303">È comune che una singola applicazione bloccata causa blocchi successivi nell'esperienza dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e2028-303">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="e2028-304">Il [**metodo IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) è più affidabile e ha un supporto di attivazione migliore perché usa l'attivazione COM del gestore.</span><span class="sxs-lookup"><span data-stu-id="e2028-304">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="e2028-305">Nel caso di selezione di più elementi, **IDropTarget** non è soggetto alle restrizioni relative alle dimensioni del buffer presenti sia in DDE che in [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="e2028-305">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="e2028-306">Inoltre, gli elementi vengono passati all'applicazione come oggetto dati che può essere convertito in una matrice di elementi usando la [**funzione SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)</span><span class="sxs-lookup"><span data-stu-id="e2028-306">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="e2028-307">Questa operazione è più semplice e non perde le informazioni sullo spazio dei nomi come avviene quando l'elemento viene convertito in un percorso per i protocolli della riga di comando o DDE.</span><span class="sxs-lookup"><span data-stu-id="e2028-307">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="e2028-308">Per altre informazioni sulle [**query IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione file, vedere [Tipi percepiti e Registrazione dell'applicazione](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="e2028-308">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="e2028-309">Completamento delle attività di implementazione dei verbi</span><span class="sxs-lookup"><span data-stu-id="e2028-309">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="e2028-310">Le attività seguenti per l'implementazione dei verbi sono rilevanti per le implementazioni di verbi statici e dinamici.</span><span class="sxs-lookup"><span data-stu-id="e2028-310">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="e2028-311">Per altre informazioni sui verbi dinamici, vedere [Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="e2028-311">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="e2028-312">Personalizzazione del menu di scelta rapida per gli oggetti shell predefiniti</span><span class="sxs-lookup"><span data-stu-id="e2028-312">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="e2028-313">Molti oggetti shell predefiniti hanno menu di scelta rapida che possono essere personalizzati.</span><span class="sxs-lookup"><span data-stu-id="e2028-313">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="e2028-314">Registrare il comando nello stesso modo in cui si registrano tipi di file tipici, ma usare il nome dell'oggetto predefinito come nome del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="e2028-314">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="e2028-315">Un elenco di oggetti predefiniti è disponibile nella *sezione Oggetti shell predefiniti* di Creazione di gestori di estensioni della [shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="e2028-315">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="e2028-316">Gli oggetti shell predefiniti i cui menu di scelta rapida possono essere personalizzati aggiungendo verbi nel Registro di sistema sono contrassegnati nella tabella con la parola Verbo.</span><span class="sxs-lookup"><span data-stu-id="e2028-316">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="e2028-317">Estensione di un nuovo sottomenu</span><span class="sxs-lookup"><span data-stu-id="e2028-317">Extending a New Submenu</span></span>

<span data-ttu-id="e2028-318">Quando un utente apre il menu **File** Esplora risorse, uno dei comandi visualizzati è **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="e2028-318">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="e2028-319">Selezionando questo comando viene visualizzato un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="e2028-319">Selecting this command displays a submenu.</span></span> <span data-ttu-id="e2028-320">Per impostazione predefinita, il sottomenu contiene due comandi, **Cartella** e **Collegamento,** che consentono agli utenti di creare sottocartelle e collegamenti.</span><span class="sxs-lookup"><span data-stu-id="e2028-320">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="e2028-321">Questo sottomenu può essere esteso per includere i comandi di creazione di file per qualsiasi tipo di file.</span><span class="sxs-lookup"><span data-stu-id="e2028-321">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="e2028-322">Per aggiungere un comando di creazione file al sottomenu **Nuovo,** i file dell'applicazione devono avere un tipo di file associato.</span><span class="sxs-lookup"><span data-stu-id="e2028-322">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="e2028-323">Includere una **sottochiave ShellNew** sotto il nome del file.</span><span class="sxs-lookup"><span data-stu-id="e2028-323">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="e2028-324">Quando il comando Nuovo **del** menu **File** è selezionato, la shell aggiunge il tipo di file al **sottomenu** Nuovo.</span><span class="sxs-lookup"><span data-stu-id="e2028-324">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="e2028-325">La stringa di visualizzazione del comando è la stringa descrittiva assegnata al ProgID del programma.</span><span class="sxs-lookup"><span data-stu-id="e2028-325">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="e2028-326">Per specificare il metodo di creazione del file, assegnare uno o più valori di dati alla **sottochiave ShellNew.**</span><span class="sxs-lookup"><span data-stu-id="e2028-326">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="e2028-327">I valori disponibili sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e2028-327">The available values are listed in the following table.</span></span>



| <span data-ttu-id="e2028-328">ShellNuovo valore della sottochiave</span><span class="sxs-lookup"><span data-stu-id="e2028-328">ShellNew subkey value</span></span> | <span data-ttu-id="e2028-329">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2028-329">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2028-330">Comando</span><span class="sxs-lookup"><span data-stu-id="e2028-330">Command</span></span>               | <span data-ttu-id="e2028-331">Esegue un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e2028-331">Executes an application.</span></span> <span data-ttu-id="e2028-332">Questo **valore \_ REG SZ** specifica il percorso dell'applicazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="e2028-332">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="e2028-333">Ad esempio, è possibile impostarlo per avviare una procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="e2028-333">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="e2028-334">Data</span><span class="sxs-lookup"><span data-stu-id="e2028-334">Data</span></span>                  | <span data-ttu-id="e2028-335">Crea un file contenente i dati specificati.</span><span class="sxs-lookup"><span data-stu-id="e2028-335">Creates a file containing specified data.</span></span> <span data-ttu-id="e2028-336">Questo **valore \_ REG BINARY** specifica i dati del file.</span><span class="sxs-lookup"><span data-stu-id="e2028-336">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="e2028-337">**I** dati vengono ignorati **se viene specificato NullFile** o **FileName.**</span><span class="sxs-lookup"><span data-stu-id="e2028-337">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="e2028-338">FileName</span><span class="sxs-lookup"><span data-stu-id="e2028-338">FileName</span></span>              | <span data-ttu-id="e2028-339">Crea un file che è una copia di un file specificato.</span><span class="sxs-lookup"><span data-stu-id="e2028-339">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="e2028-340">Questo **valore \_ REG SZ** specifica il percorso completo del file da copiare.</span><span class="sxs-lookup"><span data-stu-id="e2028-340">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="e2028-341">NullFile</span><span class="sxs-lookup"><span data-stu-id="e2028-341">NullFile</span></span>              | <span data-ttu-id="e2028-342">Crea un file vuoto.</span><span class="sxs-lookup"><span data-stu-id="e2028-342">Creates an empty file.</span></span> <span data-ttu-id="e2028-343">**A NullFile** non è assegnato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="e2028-343">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="e2028-344">Se **viene specificato NullFile,** i valori **del Registro di sistema Data** **e FileName** vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="e2028-344">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="e2028-345">L'esempio di chiave del Registro di sistema e lo screenshot seguenti illustrano il sottomenu **Nuovo** per il tipo di file .myp-ms.</span><span class="sxs-lookup"><span data-stu-id="e2028-345">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="e2028-346">Include un comando **MyProgram Application**.</span><span class="sxs-lookup"><span data-stu-id="e2028-346">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="e2028-347">La schermata illustra il **sottomenu** Nuovo.</span><span class="sxs-lookup"><span data-stu-id="e2028-347">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="e2028-348">Quando un utente seleziona **MyProgram Application** dal sottomenu **Nuovo,** Shell crea un file denominato **New MyProgram Application.myp-ms** e lo **passa aMyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="e2028-348">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![Screenshot di Esplora risorse che mostra un nuovo comando "myprogram application" nel sottomenu "nuovo"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="e2028-350">Creazione di gestori di trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="e2028-350">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="e2028-351">La procedura di base per l'implementazione di un gestore di trascinamento della selezione è la stessa di per i gestori di menu di scelta rapida convenzionali.</span><span class="sxs-lookup"><span data-stu-id="e2028-351">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="e2028-352">Tuttavia, i gestori del menu di scelta rapida usano in genere solo il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passato al metodo [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del gestore per estrarre il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e2028-352">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="e2028-353">Un gestore di trascinamento della selezione può implementare un gestore dati più sofisticato per modificare il comportamento dell'oggetto trascinato.</span><span class="sxs-lookup"><span data-stu-id="e2028-353">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="e2028-354">Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell per trascinare un oggetto, viene visualizzato un menu di scelta rapida quando l'utente tenta di rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="e2028-354">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="e2028-355">La schermata seguente illustra un tipico menu di scelta rapida di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="e2028-355">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![Screenshot del menu di scelta rapida di trascinamento della selezione](images/context-menu/context-dragdrop.png)

<span data-ttu-id="e2028-357">Un gestore di trascinamento della selezione è un gestore del menu di scelta rapida che può aggiungere elementi a questo menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e2028-357">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="e2028-358">I gestori di trascinamento della selezione vengono in genere registrati nella sottochiave seguente.</span><span class="sxs-lookup"><span data-stu-id="e2028-358">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="e2028-359">Aggiungere una sottochiave nella sottochiave **DragDropHandlers** denominata per il gestore di trascinamento della selezione e impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe (CLSID) del gestore.</span><span class="sxs-lookup"><span data-stu-id="e2028-359">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="e2028-360">L'esempio seguente abilita il gestore di trascinamento della selezione **MyDD.**</span><span class="sxs-lookup"><span data-stu-id="e2028-360">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="e2028-361">Eliminazione di verbi e controllo della visibilità</span><span class="sxs-lookup"><span data-stu-id="e2028-361">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="e2028-362">È possibile usare le impostazioni dei criteri di Windows per controllare la visibilità dei verbi.</span><span class="sxs-lookup"><span data-stu-id="e2028-362">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="e2028-363">I verbi possono essere eliminati tramite le impostazioni dei criteri aggiungendo un valore **SuppressionPolicy** o un valore GUID **SuppressionPolicyEx** alla sottochiave del Registro di sistema del verbo.</span><span class="sxs-lookup"><span data-stu-id="e2028-363">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="e2028-364">Impostare il valore della **sottochiave SuppressionPolicy** sull'ID criteri.</span><span class="sxs-lookup"><span data-stu-id="e2028-364">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="e2028-365">Se il criterio è attivato, il verbo e la voce di menu di scelta rapida associata vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="e2028-365">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="e2028-366">Per i possibili valori id dei criteri, vedere [**l'enumerazione RESTRICTIONS.**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions)</span><span class="sxs-lookup"><span data-stu-id="e2028-366">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="e2028-367">Utilizzo del modello di selezione dei verbi</span><span class="sxs-lookup"><span data-stu-id="e2028-367">Employing the Verb Selection Model</span></span>

<span data-ttu-id="e2028-368">I valori del Registro di sistema devono essere impostati per i verbi per gestire situazioni in cui un utente può selezionare un singolo elemento, più elementi o una selezione da un elemento.</span><span class="sxs-lookup"><span data-stu-id="e2028-368">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="e2028-369">Un verbo richiede valori del Registro di sistema separati per ognuna di queste tre situazioni supportate dal verbo.</span><span class="sxs-lookup"><span data-stu-id="e2028-369">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="e2028-370">I valori possibili per il modello di selezione dei verbi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2028-370">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="e2028-371">Specificare il valore MultiSelectModel per tutti i verbi.</span><span class="sxs-lookup"><span data-stu-id="e2028-371">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="e2028-372">Se il valore MultiSelectModel non viene specificato, viene dedotto dal tipo di implementazione del verbo scelto.</span><span class="sxs-lookup"><span data-stu-id="e2028-372">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="e2028-373">Per i metodi basati su COM (ad esempio DropTarget ed ExecuteCommand) si presuppone **Player** e per gli altri metodi si presuppone **Document.**</span><span class="sxs-lookup"><span data-stu-id="e2028-373">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="e2028-374">Specificare **Single** per i verbi che supportano una sola selezione.</span><span class="sxs-lookup"><span data-stu-id="e2028-374">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="e2028-375">Specificare **Player** per i verbi che supportano un numero qualsiasi di elementi.</span><span class="sxs-lookup"><span data-stu-id="e2028-375">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="e2028-376">Specificare **Documento** per i verbi che creano una finestra di primo livello per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="e2028-376">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="e2028-377">In questo modo si limita il numero di elementi attivati e si evita l'estrazione di risorse di sistema se l'utente apre troppe finestre.</span><span class="sxs-lookup"><span data-stu-id="e2028-377">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="e2028-378">Quando il numero di elementi selezionati non corrisponde al modello di selezione del verbo o è maggiore dei limiti predefiniti descritti nella tabella seguente, il verbo non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e2028-378">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="e2028-379">Tipo di implementazione del verbo</span><span class="sxs-lookup"><span data-stu-id="e2028-379">Type of verb implementation</span></span> | <span data-ttu-id="e2028-380">Documento</span><span class="sxs-lookup"><span data-stu-id="e2028-380">Document</span></span> | <span data-ttu-id="e2028-381">Lettore</span><span class="sxs-lookup"><span data-stu-id="e2028-381">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="e2028-382">Legacy</span><span class="sxs-lookup"><span data-stu-id="e2028-382">Legacy</span></span>                      | <span data-ttu-id="e2028-383">15 elementi</span><span class="sxs-lookup"><span data-stu-id="e2028-383">15 items</span></span> | <span data-ttu-id="e2028-384">100 elementi</span><span class="sxs-lookup"><span data-stu-id="e2028-384">100 items</span></span> |
| <span data-ttu-id="e2028-385">COM</span><span class="sxs-lookup"><span data-stu-id="e2028-385">COM</span></span>                         | <span data-ttu-id="e2028-386">15 elementi</span><span class="sxs-lookup"><span data-stu-id="e2028-386">15 items</span></span> | <span data-ttu-id="e2028-387">Nessun limite</span><span class="sxs-lookup"><span data-stu-id="e2028-387">No limit</span></span>  |



 

<span data-ttu-id="e2028-388">Di seguito sono riportati esempi di voci del Registro di sistema che usano il valore MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="e2028-388">The following are example registry entries using the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a><span data-ttu-id="e2028-389">Uso degli attributi degli elementi</span><span class="sxs-lookup"><span data-stu-id="e2028-389">Using Item Attributes</span></span>

<span data-ttu-id="e2028-390">I valori del flag [**SFGAO**](sfgao.md) degli attributi della shell per un elemento possono essere testati per determinare se il verbo deve essere abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e2028-390">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="e2028-391">Per usare questa funzionalità dell'attributo, aggiungere i valori **\_ DWORD REG** seguenti sotto il verbo:</span><span class="sxs-lookup"><span data-stu-id="e2028-391">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="e2028-392">Il valore AttributeMask specifica il [**valore SFGAO**](sfgao.md) dei valori di bit della maschera con cui eseguire il test.</span><span class="sxs-lookup"><span data-stu-id="e2028-392">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="e2028-393">Il valore AttributeValue specifica il [**valore SFGAO**](sfgao.md) dei bit che vengono testati.</span><span class="sxs-lookup"><span data-stu-id="e2028-393">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="e2028-394">ImpliedSelectionModel specifica zero per i verbi elemento o diverso da zero per i verbi nel menu di scelta rapida in background.</span><span class="sxs-lookup"><span data-stu-id="e2028-394">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="e2028-395">Nella voce del Registro di sistema di esempio seguente AttributeMask è impostato su [**SFGAO \_ READONLY**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="e2028-395">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="e2028-396">Implementazione di verbi personalizzati per le cartelle tramite Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="e2028-396">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="e2028-397">In Windows 7 e versioni successive è possibile aggiungere verbi a una cartella tramite Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="e2028-397">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="e2028-398">Per altre informazioni sui Desktop.ini, vedere [Come personalizzare le cartelle con Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="e2028-398">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="e2028-399">Desktop.ini i file devono sempre essere contrassegnati come **Nascosti** dal sistema in modo che non  +   siano visualizzati agli utenti.</span><span class="sxs-lookup"><span data-stu-id="e2028-399">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="e2028-400">**Per aggiungere verbi personalizzati per le cartelle tramite un file Desktop.ini, seguire questa procedura:**</span><span class="sxs-lookup"><span data-stu-id="e2028-400">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="e2028-401">Creare una cartella contrassegnata come **Sola lettura** o **Sistema**.</span><span class="sxs-lookup"><span data-stu-id="e2028-401">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="e2028-402">Creare un Desktop.ini file che include un oggetto \[ . ShellClassInfo \] DirectoryClass=ProgID cartella.</span><span class="sxs-lookup"><span data-stu-id="e2028-402">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="e2028-403">Nel Registro di sistema creare **HKEY \_ CLASSES ROOT \_ Folder** \\ **ProgID** con il valore CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="e2028-403">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="e2028-404">Il valore CanUseForDirectory evita l'uso improprio dei ProgID impostati per non partecipare all'implementazione di verbi personalizzati per le cartelle tramite Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="e2028-404">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="e2028-405">Aggiungere verbi nella **sottochiave** ProgID della cartella, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e2028-405">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="e2028-406">Questi verbi possono essere il verbo predefinito, nel qual caso facendo doppio clic sulla cartella viene attivato il verbo.</span><span class="sxs-lookup"><span data-stu-id="e2028-406">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e2028-407">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2028-407">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2028-408">Procedure consigliate per i gestori del menu di scelta rapida e più verbi di selezione</span><span class="sxs-lookup"><span data-stu-id="e2028-408">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="e2028-409">Scelta di un verbo statico o dinamico per il menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="e2028-409">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="e2028-410">Personalizzazione di un menu di scelta rapida tramite verbi dinamici</span><span class="sxs-lookup"><span data-stu-id="e2028-410">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="e2028-411">Menu di scelta rapida e gestori del menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="e2028-411">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="e2028-412">Verbi e associazioni di file</span><span class="sxs-lookup"><span data-stu-id="e2028-412">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="e2028-413">Riferimento al menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="e2028-413">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
