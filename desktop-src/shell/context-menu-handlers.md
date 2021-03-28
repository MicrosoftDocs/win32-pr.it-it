---
description: I gestori dei menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore di tipi di file. Analogamente a tutti questi gestori, si tratta di oggetti COM (Component Object Model in-process) implementati come dll.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Creazione di gestori di menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "103885882"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="c21f1-104">Creazione di gestori di menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="c21f1-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="c21f1-105">I gestori dei menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="c21f1-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="c21f1-106">Analogamente a tutti questi gestori, si tratta di oggetti COM (Component Object Model in-process) implementati come dll.</span><span class="sxs-lookup"><span data-stu-id="c21f1-106">Like all such handlers, they are in-process Component Object Model (COM) objects implemented as DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="c21f1-107">Quando si registrano i gestori che operano nel contesto di applicazioni a 32 bit, è necessario tenere presenti alcune considerazioni speciali per Windows a 64 bit: quando i verbi della shell vengono richiamati nel contesto di un'applicazione a 32 bit, il sottosistema WOW64 reindirizza file system accesso ad alcuni percorsi.</span><span class="sxs-lookup"><span data-stu-id="c21f1-107">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="c21f1-108">Se il gestore. exe viene archiviato in uno di questi percorsi, non è accessibile in questo contesto.</span><span class="sxs-lookup"><span data-stu-id="c21f1-108">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="c21f1-109">Pertanto, come soluzione alternativa, archiviare il file con estensione exe in un percorso che non viene reindirizzato oppure archiviare una versione stub del file exe che avvia la versione reale.</span><span class="sxs-lookup"><span data-stu-id="c21f1-109">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

<span data-ttu-id="c21f1-110">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="c21f1-110">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c21f1-111">Verbi canonici</span><span class="sxs-lookup"><span data-stu-id="c21f1-111">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="c21f1-112">Verbi estesi</span><span class="sxs-lookup"><span data-stu-id="c21f1-112">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="c21f1-113">Personalizzazione di un menu di scelta rapida con verbi statici</span><span class="sxs-lookup"><span data-stu-id="c21f1-113">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="c21f1-114">Attivazione del gestore mediante l'interfaccia IDropTarget</span><span class="sxs-lookup"><span data-stu-id="c21f1-114">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="c21f1-115">Specifica della posizione e dell'ordine dei verbi statici</span><span class="sxs-lookup"><span data-stu-id="c21f1-115">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="c21f1-116">Posizionamento dei verbi nella parte superiore o inferiore del menu</span><span class="sxs-lookup"><span data-stu-id="c21f1-116">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="c21f1-117">Creazione di menu a cascata statici</span><span class="sxs-lookup"><span data-stu-id="c21f1-117">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="c21f1-118">Ottenere il comportamento dinamico per i verbi statici usando la sintassi di query avanzata</span><span class="sxs-lookup"><span data-stu-id="c21f1-118">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="c21f1-119">Deprecato: associazione di verbi a Dynamic Data Exchange comandi</span><span class="sxs-lookup"><span data-stu-id="c21f1-119">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="c21f1-120">Completamento delle attività di implementazione del verbo</span><span class="sxs-lookup"><span data-stu-id="c21f1-120">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="c21f1-121">Personalizzazione del menu di scelta rapida per oggetti shell predefiniti</span><span class="sxs-lookup"><span data-stu-id="c21f1-121">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="c21f1-122">Estensione di un nuovo sottomenu</span><span class="sxs-lookup"><span data-stu-id="c21f1-122">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="c21f1-123">Eliminazione di verbi e controllo della visibilità</span><span class="sxs-lookup"><span data-stu-id="c21f1-123">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="c21f1-124">Uso del modello di selezione dei verbi</span><span class="sxs-lookup"><span data-stu-id="c21f1-124">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="c21f1-125">Uso degli attributi degli elementi</span><span class="sxs-lookup"><span data-stu-id="c21f1-125">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="c21f1-126">Implementazione di verbi personalizzati per le cartelle tramite Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="c21f1-126">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="c21f1-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c21f1-127">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="c21f1-128">Verbi canonici</span><span class="sxs-lookup"><span data-stu-id="c21f1-128">Canonical Verbs</span></span>

<span data-ttu-id="c21f1-129">Le applicazioni sono in genere responsabili di fornire stringhe di visualizzazione localizzate per i verbi definiti.</span><span class="sxs-lookup"><span data-stu-id="c21f1-129">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="c21f1-130">Tuttavia, per fornire un livello di indipendenza dal linguaggio, il sistema definisce un set standard di verbi comunemente usati, detti verbi canonici.</span><span class="sxs-lookup"><span data-stu-id="c21f1-130">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="c21f1-131">Un verbo canonico non viene mai visualizzato all'utente e può essere usato con qualsiasi lingua dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c21f1-131">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="c21f1-132">Il sistema usa il nome canonico per generare automaticamente una stringa di visualizzazione localizzata correttamente.</span><span class="sxs-lookup"><span data-stu-id="c21f1-132">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="c21f1-133">Ad esempio, la stringa di visualizzazione del verbo aperto è impostata per essere **aperta** in un sistema in lingua inglese e per l'equivalente tedesco in un sistema tedesco.</span><span class="sxs-lookup"><span data-stu-id="c21f1-133">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>



| <span data-ttu-id="c21f1-134">Verbo canonico</span><span class="sxs-lookup"><span data-stu-id="c21f1-134">Canonical verb</span></span> | <span data-ttu-id="c21f1-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c21f1-135">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="c21f1-136">Apri</span><span class="sxs-lookup"><span data-stu-id="c21f1-136">Open</span></span>           | <span data-ttu-id="c21f1-137">Apre il file o la cartella.</span><span class="sxs-lookup"><span data-stu-id="c21f1-137">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="c21f1-138">OpenNew</span><span class="sxs-lookup"><span data-stu-id="c21f1-138">Opennew</span></span>        | <span data-ttu-id="c21f1-139">Apre il file o la cartella in una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="c21f1-139">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="c21f1-140">Stampa</span><span class="sxs-lookup"><span data-stu-id="c21f1-140">Print</span></span>          | <span data-ttu-id="c21f1-141">Stampa il file.</span><span class="sxs-lookup"><span data-stu-id="c21f1-141">Prints the file.</span></span>                                                     |
| <span data-ttu-id="c21f1-142">Printto</span><span class="sxs-lookup"><span data-stu-id="c21f1-142">Printto</span></span>        | <span data-ttu-id="c21f1-143">Consente all'utente di stampare un file trascinandolo in un oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="c21f1-143">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="c21f1-144">Esplora</span><span class="sxs-lookup"><span data-stu-id="c21f1-144">Explore</span></span>        | <span data-ttu-id="c21f1-145">Apre Esplora risorse con la cartella selezionata.</span><span class="sxs-lookup"><span data-stu-id="c21f1-145">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="c21f1-146">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c21f1-146">Properties</span></span>     | <span data-ttu-id="c21f1-147">Apre la finestra delle proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c21f1-147">Opens the object's property sheet.</span></span>                                   |



 

> [!Note]  
> <span data-ttu-id="c21f1-148">Anche il verbo **printto** è canonico, ma non viene mai visualizzato.</span><span class="sxs-lookup"><span data-stu-id="c21f1-148">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="c21f1-149">La relativa inclusione consente all'utente di stampare un file trascinandolo in un oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="c21f1-149">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

 

<span data-ttu-id="c21f1-150">I gestori dei menu di scelta rapida possono fornire i propri verbi canonici tramite [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) con **GC \_ VERBW** o **GC \_ Verba**.</span><span class="sxs-lookup"><span data-stu-id="c21f1-150">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="c21f1-151">Il sistema utilizzerà i verbi canonici come secondo parametro (*lpOperation*) passato a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)e sarà [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). membro **lpVerb** passato al metodo [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="c21f1-151">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="c21f1-152">Verbi estesi</span><span class="sxs-lookup"><span data-stu-id="c21f1-152">Extended Verbs</span></span>

<span data-ttu-id="c21f1-153">Quando l'utente fa clic con il pulsante destro del mouse su un oggetto, nel menu di scelta rapida vengono visualizzati i verbi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c21f1-153">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="c21f1-154">Potrebbe essere necessario aggiungere e supportare i comandi in alcuni menu di scelta rapida che non vengono visualizzati in ogni menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="c21f1-154">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="c21f1-155">Ad esempio, è possibile avere comandi che non sono comunemente usati o destinati a utenti esperti.</span><span class="sxs-lookup"><span data-stu-id="c21f1-155">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="c21f1-156">Per questo motivo, è anche possibile definire uno o più verbi estesi.</span><span class="sxs-lookup"><span data-stu-id="c21f1-156">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="c21f1-157">Questi verbi sono simili ai verbi normali, ma si distinguono dai verbi normali in base alla modalità di registrazione.</span><span class="sxs-lookup"><span data-stu-id="c21f1-157">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="c21f1-158">Per avere accesso ai verbi estesi, è necessario fare clic con il pulsante destro del mouse su un oggetto mentre si preme il tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="c21f1-158">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="c21f1-159">Quando l'utente esegue questa operazione, vengono visualizzati i verbi estesi oltre ai verbi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c21f1-159">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="c21f1-160">È possibile utilizzare il registro di sistema per definire uno o più verbi estesi.</span><span class="sxs-lookup"><span data-stu-id="c21f1-160">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="c21f1-161">I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto e preme anche il tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="c21f1-161">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="c21f1-162">Per definire un verbo come esteso, aggiungere un valore "Extended" **reg \_ SZ** alla sottochiave del verbo.</span><span class="sxs-lookup"><span data-stu-id="c21f1-162">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="c21f1-163">Al valore non devono essere associati dati.</span><span class="sxs-lookup"><span data-stu-id="c21f1-163">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="c21f1-164">Personalizzazione di un menu di scelta rapida con verbi statici</span><span class="sxs-lookup"><span data-stu-id="c21f1-164">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="c21f1-165">Dopo aver [scelto un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md) , è possibile estendere il menu di scelta rapida per un tipo di file registrando un verbo statico per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c21f1-165">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="c21f1-166">A tale scopo, aggiungere una sottochiave della **Shell** sotto la sottochiave per il ProgID dell'applicazione associata al tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c21f1-166">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="c21f1-167">Facoltativamente, è possibile definire un verbo predefinito per il tipo di file rendendolo il valore predefinito della sottochiave della **Shell** .</span><span class="sxs-lookup"><span data-stu-id="c21f1-167">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="c21f1-168">Il verbo predefinito viene visualizzato per primo nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="c21f1-168">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="c21f1-169">Il suo scopo è fornire alla shell un verbo che può usare quando viene chiamata la funzione [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) , ma non viene specificato alcun verbo.</span><span class="sxs-lookup"><span data-stu-id="c21f1-169">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="c21f1-170">La shell non seleziona necessariamente il verbo predefinito quando **ShellExecuteEx** viene usato in questo modo.</span><span class="sxs-lookup"><span data-stu-id="c21f1-170">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="c21f1-171">La shell usa il primo verbo disponibile nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="c21f1-171">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="c21f1-172">Verbo predefinito</span><span class="sxs-lookup"><span data-stu-id="c21f1-172">The default verb</span></span>
2.  <span data-ttu-id="c21f1-173">Primo verbo nel registro di sistema, se è specificato l'ordine dei verbi</span><span class="sxs-lookup"><span data-stu-id="c21f1-173">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="c21f1-174">Verbo di **apertura**</span><span class="sxs-lookup"><span data-stu-id="c21f1-174">The **Open** verb</span></span>
4.  <span data-ttu-id="c21f1-175">Il verbo **Apri con**</span><span class="sxs-lookup"><span data-stu-id="c21f1-175">The **Open With** verb</span></span>

<span data-ttu-id="c21f1-176">Se nessuno dei verbi elencati è disponibile, l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c21f1-176">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="c21f1-177">Creare una sottochiave per ogni verbo che si vuole aggiungere nella sottochiave della shell.</span><span class="sxs-lookup"><span data-stu-id="c21f1-177">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="c21f1-178">Ognuna di queste sottochiavi deve avere un valore **reg \_ SZ** impostato sulla stringa di visualizzazione del verbo (stringa localizzata).</span><span class="sxs-lookup"><span data-stu-id="c21f1-178">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="c21f1-179">Per ogni sottochiave verbo, creare una sottochiave del comando con il valore predefinito impostato sulla riga di comando per attivare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="c21f1-179">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="c21f1-180">Per i verbi canonici, ad esempio **Open** e **Print**, è possibile omettere la stringa di visualizzazione perché il sistema visualizza automaticamente una stringa localizzata correttamente.</span><span class="sxs-lookup"><span data-stu-id="c21f1-180">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="c21f1-181">Per i verbi non canonici, se si omette la stringa di visualizzazione, viene visualizzata la stringa del verbo.</span><span class="sxs-lookup"><span data-stu-id="c21f1-181">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="c21f1-182">Nell'esempio di registro di sistema seguente si noti che:</span><span class="sxs-lookup"><span data-stu-id="c21f1-182">In the following registry example, note that:</span></span>

-   <span data-ttu-id="c21f1-183">Poiché **doit** non è un verbo canonico, viene assegnato un nome visualizzato, che può essere selezionato premendo il tasto D.</span><span class="sxs-lookup"><span data-stu-id="c21f1-183">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="c21f1-184">Il verbo **printto** non viene visualizzato nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="c21f1-184">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="c21f1-185">Tuttavia, l'inclusione nel registro di sistema consente all'utente di stampare i file trascinandoli su un'icona della stampante.</span><span class="sxs-lookup"><span data-stu-id="c21f1-185">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="c21f1-186">Viene visualizzata una sottochiave per ogni verbo.</span><span class="sxs-lookup"><span data-stu-id="c21f1-186">One subkey is shown for each verb.</span></span> <span data-ttu-id="c21f1-187">**%1** rappresenta il nome del file e **%2** il nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="c21f1-187">**%1** represents the file name and **%2** the printer name.</span></span>

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

<span data-ttu-id="c21f1-188">Nel diagramma seguente viene illustrata l'estensione del menu di scelta rapida in base alle voci del registro di sistema riportate sopra.</span><span class="sxs-lookup"><span data-stu-id="c21f1-188">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="c21f1-189">Questo menu di scelta rapida presenta i verbi **Apri**, **Esegui** e **stampa** nel menu, con **Esegui** come verbo predefinito.</span><span class="sxs-lookup"><span data-stu-id="c21f1-189">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![screenshot del menu di scelta rapida per i verbi predefiniti](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="c21f1-191">Attivazione del gestore mediante l'interfaccia IDropTarget</span><span class="sxs-lookup"><span data-stu-id="c21f1-191">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="c21f1-192">Dynamic Data Exchange (DDE) è deprecato. in alternativa, usare [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="c21f1-192">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="c21f1-193">**IDropTarget** è più affidabile e offre un supporto migliore per l'attivazione perché usa l'attivazione com del gestore.</span><span class="sxs-lookup"><span data-stu-id="c21f1-193">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="c21f1-194">Nel caso di selezione di più elementi, **IDropTarget** non è soggetto alle limitazioni delle dimensioni del buffer presenti sia in DDE che in [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="c21f1-194">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="c21f1-195">Inoltre, gli elementi vengono passati all'applicazione come oggetto dati che può essere convertito in una matrice di elementi tramite la funzione [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="c21f1-195">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="c21f1-196">Questa operazione è più semplice e non perde le informazioni sullo spazio dei nomi come si verifica quando l'elemento viene convertito in un percorso per i protocolli della riga di comando o DDE.</span><span class="sxs-lookup"><span data-stu-id="c21f1-196">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="c21f1-197">Per ulteriori informazioni sulle query [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione file, vedere [tipi percepiti e registrazione di applicazioni](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="c21f1-197">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="c21f1-198">Specifica della posizione e dell'ordine dei verbi statici</span><span class="sxs-lookup"><span data-stu-id="c21f1-198">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="c21f1-199">In genere i verbi vengono ordinati in un menu di scelta rapida in base alla modalità di enumerazione. l'enumerazione è basata innanzitutto sull'ordine della matrice di associazioni, quindi sull'ordine degli elementi nella matrice di associazioni, come definito dall'ordinamento del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c21f1-199">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="c21f1-200">È possibile ordinare i verbi specificando il valore predefinito della sottochiave della Shell per la voce di associazione.</span><span class="sxs-lookup"><span data-stu-id="c21f1-200">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="c21f1-201">Questo valore predefinito può includere un singolo elemento, che verrà visualizzato nella posizione superiore del menu di scelta rapida o un elenco di elementi separati da spazi o virgole.</span><span class="sxs-lookup"><span data-stu-id="c21f1-201">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="c21f1-202">Nel secondo caso, il primo elemento dell'elenco è l'elemento predefinito e gli altri verbi vengono visualizzati immediatamente sotto nell'ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="c21f1-202">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="c21f1-203">Ad esempio, la voce del registro di sistema seguente produce i verbi del menu di scelta rapida nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="c21f1-203">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="c21f1-204">Visualizza</span><span class="sxs-lookup"><span data-stu-id="c21f1-204">Display</span></span>
2.  <span data-ttu-id="c21f1-205">Gadget</span><span class="sxs-lookup"><span data-stu-id="c21f1-205">Gadgets</span></span>
3.  <span data-ttu-id="c21f1-206">Personalization</span><span class="sxs-lookup"><span data-stu-id="c21f1-206">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="c21f1-207">Analogamente, la voce del registro di sistema seguente produce i verbi del menu di scelta rapida nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="c21f1-207">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="c21f1-208">Personalization</span><span class="sxs-lookup"><span data-stu-id="c21f1-208">Personalization</span></span>
2.  <span data-ttu-id="c21f1-209">Gadget</span><span class="sxs-lookup"><span data-stu-id="c21f1-209">Gadgets</span></span>
3.  <span data-ttu-id="c21f1-210">Visualizza</span><span class="sxs-lookup"><span data-stu-id="c21f1-210">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="c21f1-211">Posizionamento dei verbi nella parte superiore o inferiore del menu</span><span class="sxs-lookup"><span data-stu-id="c21f1-211">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="c21f1-212">L'attributo del registro di sistema seguente può essere usato per inserire un verbo nella parte superiore o inferiore del menu.</span><span class="sxs-lookup"><span data-stu-id="c21f1-212">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="c21f1-213">Se sono presenti più verbi che specificano questo attributo, l'ultimo a tale scopo ottiene la priorità:</span><span class="sxs-lookup"><span data-stu-id="c21f1-213">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="c21f1-214">Creazione di menu a cascata statici</span><span class="sxs-lookup"><span data-stu-id="c21f1-214">Creating Static Cascading Menus</span></span>

<span data-ttu-id="c21f1-215">In Windows 7 e versioni successive, l'implementazione del menu a cascata è supportata tramite le impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c21f1-215">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="c21f1-216">Prima di Windows 7, la creazione dei menu a cascata era possibile solo tramite l'implementazione dell'interfaccia [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="c21f1-216">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="c21f1-217">In Windows 7 e versioni successive, è consigliabile ricorrere alle soluzioni COM basate su codice solo quando i metodi statici sono insufficienti.</span><span class="sxs-lookup"><span data-stu-id="c21f1-217">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="c21f1-218">Lo screenshot seguente fornisce un esempio di menu a cascata.</span><span class="sxs-lookup"><span data-stu-id="c21f1-218">The following screen shot provides an example of a cascading menu.</span></span>

![screenshot che mostra un esempio di menu a cascata](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="c21f1-220">In Windows 7 e versioni successive sono disponibili tre modi per creare i menu a cascata:</span><span class="sxs-lookup"><span data-stu-id="c21f1-220">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="c21f1-221">Creazione di menu a cascata con la voce del registro di sistema subcommands</span><span class="sxs-lookup"><span data-stu-id="c21f1-221">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="c21f1-222">Creazione di menu a cascata con la voce del registro di sistema ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="c21f1-222">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="c21f1-223">Creazione di menu a cascata con l'interfaccia IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="c21f1-223">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="c21f1-224">Creazione di menu a cascata con la voce del registro di sistema subcommands</span><span class="sxs-lookup"><span data-stu-id="c21f1-224">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="c21f1-225">In Windows 7 e versioni successive, è possibile usare la voce sottocomandi per creare menu a cascata usando la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="c21f1-225">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="c21f1-226">**Per creare un menu a cascata utilizzando la voce sottocomandi**</span><span class="sxs-lookup"><span data-stu-id="c21f1-226">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="c21f1-227">Creare una sottochiave in **HKEY \_ classi \_ radice** \\ *ProgID* \\ **Shell** per rappresentare il menu a cascata.</span><span class="sxs-lookup"><span data-stu-id="c21f1-227">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="c21f1-228">In questo esempio viene assegnata questa sottochiave al nome *CascadeTest*.</span><span class="sxs-lookup"><span data-stu-id="c21f1-228">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="c21f1-229">Verificare che il valore predefinito della sottochiave *CascadeTest* sia vuoto e visualizzato come **(valore non impostato)**.</span><span class="sxs-lookup"><span data-stu-id="c21f1-229">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="c21f1-230">Nella sottochiave *CascadeTest* aggiungere una voce MUIVerb di tipo **reg \_ SZ** e assegnarle il testo che verrà visualizzato come nome nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="c21f1-230">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="c21f1-231">In questo esempio viene assegnato il "menu test Cascade".</span><span class="sxs-lookup"><span data-stu-id="c21f1-231">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="c21f1-232">Nella sottochiave *CascadeTest* aggiungere una voce di sottocomandi di tipo **reg \_ SZ** a cui viene assegnato un elenco, demlimited da punti e virgola, dei verbi che devono essere visualizzati nel menu in ordine di aspetto.</span><span class="sxs-lookup"><span data-stu-id="c21f1-232">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="c21f1-233">Ad esempio, di seguito viene assegnato un numero di verbi forniti dal sistema:</span><span class="sxs-lookup"><span data-stu-id="c21f1-233">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="c21f1-234">Nel caso di verbi personalizzati, implementarli usando uno dei metodi di implementazione del verbo statico ed elencarli sotto la sottochiave **CommandStore** , come illustrato in questo esempio per un verbo fittizio *verbname*:</span><span class="sxs-lookup"><span data-stu-id="c21f1-234">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

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
> <span data-ttu-id="c21f1-235">Questo metodo ha il vantaggio di poter registrare i verbi personalizzati una volta e riutilizzarli elencando il nome del verbo nella voce dei sottocomandi.</span><span class="sxs-lookup"><span data-stu-id="c21f1-235">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="c21f1-236">Tuttavia, richiede che l'applicazione disponga delle autorizzazioni necessarie per modificare il registro di sistema nel **\_ \_ computer locale HKEY**.</span><span class="sxs-lookup"><span data-stu-id="c21f1-236">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="c21f1-237">Creazione di menu a cascata con la voce del registro di sistema ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="c21f1-237">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="c21f1-238">In Windows 7 e versioni successive, è possibile usare la voce ExtendedSubCommandKey per creare menu a cascata estesi: menu a cascata nei menu a cascata.</span><span class="sxs-lookup"><span data-stu-id="c21f1-238">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="c21f1-239">Lo screenshot seguente è un esempio di menu a cascata esteso.</span><span class="sxs-lookup"><span data-stu-id="c21f1-239">The following screen shot is an example of an extended cascading menu.</span></span>

![screenshot che mostra il menu a cascata esteso per i dispositivi](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="c21f1-241">Poiché **la \_ \_ radice delle classi HKEY** è una combinazione di **HKEY \_ Current \_ User** e **HKEY \_ Local \_ computer**, è possibile registrare i verbi personalizzati nella sottochiave classi software **\_ \_ utente corrente HKEY** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="c21f1-241">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="c21f1-242">Il vantaggio principale di questa operazione è che non è necessaria l'autorizzazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="c21f1-242">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="c21f1-243">Inoltre, altre associazioni di file possono riutilizzare l'intero set di verbi specificando la stessa sottochiave ExtendedSubCommandsKey.</span><span class="sxs-lookup"><span data-stu-id="c21f1-243">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="c21f1-244">Se non è necessario riutilizzare questo set di verbi, è possibile elencare i verbi sotto l'elemento padre, ma assicurarsi che il valore predefinito dell'elemento padre sia vuoto.</span><span class="sxs-lookup"><span data-stu-id="c21f1-244">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="c21f1-245">**Per creare un menu a cascata utilizzando una voce ExtendedSubCommandsKey**</span><span class="sxs-lookup"><span data-stu-id="c21f1-245">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="c21f1-246">Creare una sottochiave in **HKEY \_ classi \_ radice** \\ *ProgID* \\ **Shell** per rappresentare il menu a cascata.</span><span class="sxs-lookup"><span data-stu-id="c21f1-246">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="c21f1-247">In questo esempio viene assegnata questa sottochiave al nome *CascadeTest2*.</span><span class="sxs-lookup"><span data-stu-id="c21f1-247">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="c21f1-248">Verificare che il valore predefinito della sottochiave *CascadeTest* sia vuoto e visualizzato come **(valore non impostato)**.</span><span class="sxs-lookup"><span data-stu-id="c21f1-248">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="c21f1-249">Nella sottochiave *CascadeTest* aggiungere una voce MUIVerb di tipo **reg \_ SZ** e assegnarle il testo che verrà visualizzato come nome nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="c21f1-249">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="c21f1-250">In questo esempio viene assegnato il "menu test Cascade".</span><span class="sxs-lookup"><span data-stu-id="c21f1-250">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="c21f1-251">Nella sottochiave *CascadeTest* creata aggiungere una sottochiave **ExtendedSubCommandsKey** e quindi aggiungere il documento sottocomandi (di tipo **reg \_ SZ** ), ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c21f1-251">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

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

    <span data-ttu-id="c21f1-252">Verificare che il valore predefinito della sottochiave del *menu 2 di test Cascade* sia vuoto e visualizzato come **(valore non impostato)**.</span><span class="sxs-lookup"><span data-stu-id="c21f1-252">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="c21f1-253">Popolare i sottoverbi utilizzando una delle seguenti implementazioni di verbi statici.</span><span class="sxs-lookup"><span data-stu-id="c21f1-253">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="c21f1-254">Si noti che la sottochiave CommandFlags rappresenta i valori EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="c21f1-254">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="c21f1-255">Se si desidera aggiungere un separatore prima o dopo la voce di menu a cascata, utilizzare ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="c21f1-255">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="c21f1-256">Per una descrizione di questi flag di Windows 7 e versioni successive, vedere [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="c21f1-256">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="c21f1-257">ECF \_ SEPARATORBEFORE funziona solo per le voci di menu di primo livello.</span><span class="sxs-lookup"><span data-stu-id="c21f1-257">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="c21f1-258">MUIVerb è di tipo **reg \_ SZ** e CommandFlags è di tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="c21f1-258">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

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

<span data-ttu-id="c21f1-259">Lo screenshot seguente illustra i precedenti esempi di voci della chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c21f1-259">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![screenshot che mostra un esempio di menu a cascata che mostra le scelte del blocco note e di WordPad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="c21f1-261">Creazione di menu a cascata con l'interfaccia IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="c21f1-261">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="c21f1-262">Un'altra opzione per l'aggiunta di verbi a un menu a cascata consiste nell'usare [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="c21f1-262">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="c21f1-263">Questo metodo consente alle origini dati che forniscono i comandi del modulo di comando tramite [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) di utilizzare tali comandi come verbi in un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="c21f1-263">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="c21f1-264">In Windows 7 e versioni successive, è possibile fornire la stessa implementazione del verbo usando [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , come è possibile con [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="c21f1-264">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="c21f1-265">Le due schermate seguenti illustrano l'uso dei menu a cascata nella cartella **Devices** .</span><span class="sxs-lookup"><span data-stu-id="c21f1-265">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Screenshot che mostra un esempio di menu a cascata nella cartella Devices (dispositivi).](images/file-assoc/filecascademenu.png)

<span data-ttu-id="c21f1-267">Lo screenshot seguente illustra un'altra implementazione di un menu a cascata nella cartella **Devices** .</span><span class="sxs-lookup"><span data-stu-id="c21f1-267">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![screenshot che mostra un esempio di menu a cascata nella cartella Devices](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="c21f1-269">Poiché [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supporta solo l'attivazione in-process, è consigliabile usare le origini dati della shell che devono condividere l'implementazione tra i comandi e i menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="c21f1-269">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="c21f1-270">Ottenere il comportamento dinamico per i verbi statici usando la sintassi di query avanzata</span><span class="sxs-lookup"><span data-stu-id="c21f1-270">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="c21f1-271">La sintassi di query avanzata (AQS) può esprimere una condizione che verrà valutata utilizzando le proprietà dell'elemento per cui viene creata un'istanza del verbo.</span><span class="sxs-lookup"><span data-stu-id="c21f1-271">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="c21f1-272">Questo sistema funziona solo con proprietà veloci.</span><span class="sxs-lookup"><span data-stu-id="c21f1-272">This system works only with fast properties.</span></span> <span data-ttu-id="c21f1-273">Si tratta di proprietà che l'origine dati della shell segnala come Fast senza restituire [\* \* \* \* SHCOLSTATE \_ Slow \* \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* \* da [**IShellFolder2:: GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span><span class="sxs-lookup"><span data-stu-id="c21f1-273">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="c21f1-274">Windows 7 e versioni successive supportano valori canonici che evitano problemi nelle compilazioni localizzate.</span><span class="sxs-lookup"><span data-stu-id="c21f1-274">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="c21f1-275">La sintassi canonica seguente è obbligatoria per le compilazioni localizzate per sfruttare i vantaggi di questa funzionalità avanzata di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c21f1-275">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="c21f1-276">Nell'esempio seguente voce del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="c21f1-276">In the following example registry entry:</span></span>

-   <span data-ttu-id="c21f1-277">Il valore **appliesTo** controlla se il verbo è visualizzato o nascosto.</span><span class="sxs-lookup"><span data-stu-id="c21f1-277">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="c21f1-278">Il valore DefaultAppliesTo controlla il verbo predefinito.</span><span class="sxs-lookup"><span data-stu-id="c21f1-278">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="c21f1-279">Il valore HasLUAShield controlla se viene visualizzato uno scudo controllo dell'account utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="c21f1-279">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="c21f1-280">In questo esempio il valore **DefaultAppliesTo** rende questo verbo l'impostazione predefinita per qualsiasi file con la parola "exampleText1" nel nome file.</span><span class="sxs-lookup"><span data-stu-id="c21f1-280">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="c21f1-281">Il valore **appliesTo** Abilita il verbo per tutti i file con "exampleText1" nel nome.</span><span class="sxs-lookup"><span data-stu-id="c21f1-281">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="c21f1-282">Il valore **HasLUAShield** Visualizza lo scudo per i file con "exampleText2" nel nome.</span><span class="sxs-lookup"><span data-stu-id="c21f1-282">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="c21f1-283">Aggiungere la sottochiave del **comando** e un valore:</span><span class="sxs-lookup"><span data-stu-id="c21f1-283">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="c21f1-284">Nel registro di sistema di Windows 7, vedere **HKEY \_ classi \_ radice** \\ **unità** come esempio di verbi BitLocker che usano l'approccio seguente:</span><span class="sxs-lookup"><span data-stu-id="c21f1-284">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="c21f1-285">AppliesTo = System. volume. BitlockerProtection: = 2</span><span class="sxs-lookup"><span data-stu-id="c21f1-285">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="c21f1-286">System. volume. BitlockerRequiresAdmin: = System. StructuredQueryType. Boolean \# true</span><span class="sxs-lookup"><span data-stu-id="c21f1-286">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="c21f1-287">Per ulteriori informazioni su AQS, vedere [sintassi di query avanzata](../search/-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="c21f1-287">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="c21f1-288">Deprecato: associazione di verbi a Dynamic Data Exchange comandi</span><span class="sxs-lookup"><span data-stu-id="c21f1-288">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="c21f1-289">Il DDE è deprecato; in alternativa, usare [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="c21f1-289">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="c21f1-290">Il DDE è deprecato perché si basa su un messaggio della finestra di trasmissione per individuare il server DDE.</span><span class="sxs-lookup"><span data-stu-id="c21f1-290">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="c21f1-291">Un blocco del server DDE blocca il messaggio della finestra di trasmissione e quindi blocca le conversazioni DDE per le altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c21f1-291">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="c21f1-292">Una singola applicazione bloccata può causare blocchi successivi nell'esperienza dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c21f1-292">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="c21f1-293">Il metodo [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) è più affidabile e offre un supporto migliore per l'attivazione perché utilizza l'attivazione com del gestore.</span><span class="sxs-lookup"><span data-stu-id="c21f1-293">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="c21f1-294">Nel caso di selezione di più elementi, **IDropTarget** non è soggetto alle limitazioni delle dimensioni del buffer presenti sia in DDE che in [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="c21f1-294">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="c21f1-295">Inoltre, gli elementi vengono passati all'applicazione come oggetto dati che può essere convertito in una matrice di elementi tramite la funzione [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="c21f1-295">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="c21f1-296">Questa operazione è più semplice e non perde le informazioni sullo spazio dei nomi come si verifica quando l'elemento viene convertito in un percorso per i protocolli della riga di comando o DDE.</span><span class="sxs-lookup"><span data-stu-id="c21f1-296">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="c21f1-297">Per ulteriori informazioni sulle query [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione file, vedere [tipi percepiti e registrazione di applicazioni](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="c21f1-297">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="c21f1-298">Completamento delle attività di implementazione del verbo</span><span class="sxs-lookup"><span data-stu-id="c21f1-298">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="c21f1-299">Le attività seguenti per l'implementazione dei verbi sono rilevanti per le implementazioni di verbi statici e dinamici.</span><span class="sxs-lookup"><span data-stu-id="c21f1-299">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="c21f1-300">Per altre informazioni sui verbi dinamici, vedere [personalizzazione di un menu di scelta rapida con verbi dinamici](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="c21f1-300">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="c21f1-301">Personalizzazione del menu di scelta rapida per oggetti shell predefiniti</span><span class="sxs-lookup"><span data-stu-id="c21f1-301">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="c21f1-302">Molti oggetti shell predefiniti dispongono di menu di scelta rapida che possono essere personalizzati.</span><span class="sxs-lookup"><span data-stu-id="c21f1-302">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="c21f1-303">Registrare il comando nello stesso modo in cui si registrano i tipi di file tipici, ma usare il nome dell'oggetto predefinito come nome del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c21f1-303">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="c21f1-304">Un elenco di oggetti predefiniti si trova nella sezione *oggetti shell predefiniti* della creazione di [gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="c21f1-304">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="c21f1-305">Gli oggetti shell predefiniti i cui menu di scelta rapida possono essere personalizzati aggiungendo verbi nel registro di sistema vengono contrassegnati nella tabella con il verbo di parola.</span><span class="sxs-lookup"><span data-stu-id="c21f1-305">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="c21f1-306">Estensione di un nuovo sottomenu</span><span class="sxs-lookup"><span data-stu-id="c21f1-306">Extending a New Submenu</span></span>

<span data-ttu-id="c21f1-307">Quando un utente apre il menu **file** in Esplora risorse, uno dei comandi visualizzati è **nuovo**.</span><span class="sxs-lookup"><span data-stu-id="c21f1-307">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="c21f1-308">Se si seleziona questo comando, verrà visualizzato un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="c21f1-308">Selecting this command displays a submenu.</span></span> <span data-ttu-id="c21f1-309">Per impostazione predefinita, il sottomenu contiene due comandi, **cartella** e **collegamento**, che consentono agli utenti di creare sottocartelle e collegamenti.</span><span class="sxs-lookup"><span data-stu-id="c21f1-309">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="c21f1-310">Questo sottomenu può essere esteso in modo da includere i comandi per la creazione di file per qualsiasi tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c21f1-310">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="c21f1-311">Per aggiungere un comando per la creazione di file al **nuovo** sottomenu, i file dell'applicazione devono avere un tipo di file associato.</span><span class="sxs-lookup"><span data-stu-id="c21f1-311">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="c21f1-312">Includere una sottochiave **ShellNew** sotto il nome del file.</span><span class="sxs-lookup"><span data-stu-id="c21f1-312">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="c21f1-313">Quando si seleziona il comando **nuovo** del menu **file** , la shell aggiunge il tipo di file al **nuovo** sottomenu.</span><span class="sxs-lookup"><span data-stu-id="c21f1-313">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="c21f1-314">La stringa di visualizzazione del comando è la stringa descrittiva assegnata al ProgID del programma.</span><span class="sxs-lookup"><span data-stu-id="c21f1-314">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="c21f1-315">Per specificare il metodo di creazione del file, assegnare uno o più valori di dati alla sottochiave **ShellNew** .</span><span class="sxs-lookup"><span data-stu-id="c21f1-315">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="c21f1-316">I valori disponibili sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c21f1-316">The available values are listed in the following table.</span></span>



| <span data-ttu-id="c21f1-317">Valore sottochiave ShellNew</span><span class="sxs-lookup"><span data-stu-id="c21f1-317">ShellNew subkey value</span></span> | <span data-ttu-id="c21f1-318">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c21f1-318">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21f1-319">Comando</span><span class="sxs-lookup"><span data-stu-id="c21f1-319">Command</span></span>               | <span data-ttu-id="c21f1-320">Esegue un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c21f1-320">Executes an application.</span></span> <span data-ttu-id="c21f1-321">Questo valore **reg \_ SZ** specifica il percorso dell'applicazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="c21f1-321">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="c21f1-322">Ad esempio, è possibile impostarlo per avviare una procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="c21f1-322">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="c21f1-323">Dati</span><span class="sxs-lookup"><span data-stu-id="c21f1-323">Data</span></span>                  | <span data-ttu-id="c21f1-324">Crea un file contenente i dati specificati.</span><span class="sxs-lookup"><span data-stu-id="c21f1-324">Creates a file containing specified data.</span></span> <span data-ttu-id="c21f1-325">Questo **valore \_ binario REG** specifica i dati del file.</span><span class="sxs-lookup"><span data-stu-id="c21f1-325">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="c21f1-326">Se è specificato **NullFile** o **filename** , **i dati** vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="c21f1-326">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="c21f1-327">FileName</span><span class="sxs-lookup"><span data-stu-id="c21f1-327">FileName</span></span>              | <span data-ttu-id="c21f1-328">Crea un file che è una copia di un file specificato.</span><span class="sxs-lookup"><span data-stu-id="c21f1-328">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="c21f1-329">Questo valore **reg \_ SZ** specifica il percorso completo del file da copiare.</span><span class="sxs-lookup"><span data-stu-id="c21f1-329">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="c21f1-330">NullFile</span><span class="sxs-lookup"><span data-stu-id="c21f1-330">NullFile</span></span>              | <span data-ttu-id="c21f1-331">Crea un file vuoto.</span><span class="sxs-lookup"><span data-stu-id="c21f1-331">Creates an empty file.</span></span> <span data-ttu-id="c21f1-332">A **NullFile** non è stato assegnato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="c21f1-332">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="c21f1-333">Se viene specificato **NullFile** , i valori del registro di sistema **Data** e **filename** verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="c21f1-333">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="c21f1-334">Il seguente esempio di chiave del registro di sistema e screenshot illustrano il **nuovo** sottomenu per il tipo di file. MYP-ms.</span><span class="sxs-lookup"><span data-stu-id="c21f1-334">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="c21f1-335">Dispone di un comando, **applicazione programmi**.</span><span class="sxs-lookup"><span data-stu-id="c21f1-335">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="c21f1-336">Lo screenshot illustra il **nuovo** sottomenu.</span><span class="sxs-lookup"><span data-stu-id="c21f1-336">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="c21f1-337">Quando un utente seleziona l' **applicazione di programma** dal **nuovo** sottomenu, la shell crea un file denominato **nuovo programma Application. MYP-ms** e lo passa a **MyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="c21f1-337">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![Screenshot di Esplora risorse che mostra un nuovo comando "programma applicazione" nel sottomenu "nuovo"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="c21f1-339">Creazione di gestori di trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="c21f1-339">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="c21f1-340">La procedura di base per l'implementazione di un gestore di trascinamento della selezione è identica a quella dei gestori di menu di scelta rapida convenzionali.</span><span class="sxs-lookup"><span data-stu-id="c21f1-340">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="c21f1-341">Tuttavia, i gestori dei menu di scelta rapida usano in genere solo il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passato al metodo [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del gestore per estrarre il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c21f1-341">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="c21f1-342">Un gestore di trascinamento della selezione può implementare un gestore dati più sofisticato per modificare il comportamento dell'oggetto trascinato.</span><span class="sxs-lookup"><span data-stu-id="c21f1-342">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="c21f1-343">Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell per trascinare un oggetto, viene visualizzato un menu di scelta rapida quando l'utente tenta di eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c21f1-343">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="c21f1-344">Lo screenshot seguente illustra un tipico menu di scelta rapida con trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="c21f1-344">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![screenshot del menu di scelta rapida del trascinamento della selezione](images/context-menu/context-dragdrop.png)

<span data-ttu-id="c21f1-346">Un gestore di trascinamento della selezione è un gestore di menu di scelta rapida che consente di aggiungere elementi a questo menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="c21f1-346">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="c21f1-347">I gestori di trascinamento della selezione vengono in genere registrati nella sottochiave seguente.</span><span class="sxs-lookup"><span data-stu-id="c21f1-347">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="c21f1-348">Aggiungere una sottochiave nella sottochiave **DragDropHandlers** denominata per il gestore di trascinamento della selezione e impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe del gestore (CLSID).</span><span class="sxs-lookup"><span data-stu-id="c21f1-348">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="c21f1-349">Nell'esempio seguente viene abilitato il gestore di trascinamento della selezione **MyDD** .</span><span class="sxs-lookup"><span data-stu-id="c21f1-349">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="c21f1-350">Eliminazione di verbi e controllo della visibilità</span><span class="sxs-lookup"><span data-stu-id="c21f1-350">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="c21f1-351">È possibile utilizzare le impostazioni dei criteri di Windows per controllare la visibilità dei verbi.</span><span class="sxs-lookup"><span data-stu-id="c21f1-351">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="c21f1-352">I verbi possono essere eliminati tramite le impostazioni dei criteri aggiungendo un valore **SuppressionPolicy** o un valore GUID **SuppressionPolicyEx** alla sottochiave del registro di sistema del verbo.</span><span class="sxs-lookup"><span data-stu-id="c21f1-352">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="c21f1-353">Impostare il valore della sottochiave **SuppressionPolicy** sull'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="c21f1-353">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="c21f1-354">Se il criterio è attivato, il verbo e la voce del menu di scelta rapida associato vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="c21f1-354">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="c21f1-355">Per i possibili valori ID dei criteri, vedere l'enumerazione [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="c21f1-355">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="c21f1-356">Uso del modello di selezione dei verbi</span><span class="sxs-lookup"><span data-stu-id="c21f1-356">Employing the Verb Selection Model</span></span>

<span data-ttu-id="c21f1-357">I valori del registro di sistema devono essere impostati per i verbi per gestire le situazioni in cui un utente può selezionare un singolo elemento, più elementi o una selezione da un elemento.</span><span class="sxs-lookup"><span data-stu-id="c21f1-357">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="c21f1-358">Un verbo richiede valori di registro distinti per ognuna di queste tre situazioni supportate dal verbo.</span><span class="sxs-lookup"><span data-stu-id="c21f1-358">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="c21f1-359">I valori possibili per il modello di selezione dei verbi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c21f1-359">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="c21f1-360">Specificare il valore MultiSelectModel per tutti i verbi.</span><span class="sxs-lookup"><span data-stu-id="c21f1-360">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="c21f1-361">Se il valore MultiSelectModel non è specificato, viene dedotto dal tipo di implementazione del verbo scelto.</span><span class="sxs-lookup"><span data-stu-id="c21f1-361">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="c21f1-362">Per i metodi basati su COM, ad esempio DropTarget e ExecuteCommand, viene utilizzato il **lettore** e per gli altri metodi viene utilizzato il **documento** .</span><span class="sxs-lookup"><span data-stu-id="c21f1-362">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="c21f1-363">Specificare **Single** per i verbi che supportano una sola selezione.</span><span class="sxs-lookup"><span data-stu-id="c21f1-363">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="c21f1-364">Specificare il **lettore** per i verbi che supportano un numero qualsiasi di elementi.</span><span class="sxs-lookup"><span data-stu-id="c21f1-364">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="c21f1-365">Specificare il **documento** per i verbi che creano una finestra di primo livello per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="c21f1-365">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="c21f1-366">Questa operazione limita il numero di elementi attivati e consente di evitare l'esaurimento delle risorse di sistema se l'utente apre troppe finestre.</span><span class="sxs-lookup"><span data-stu-id="c21f1-366">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="c21f1-367">Quando il numero di elementi selezionati non corrisponde al modello di selezione dei verbi o è maggiore dei limiti predefiniti indicati nella tabella seguente, il verbo non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="c21f1-367">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="c21f1-368">Tipo di implementazione del verbo</span><span class="sxs-lookup"><span data-stu-id="c21f1-368">Type of verb implementation</span></span> | <span data-ttu-id="c21f1-369">Documento</span><span class="sxs-lookup"><span data-stu-id="c21f1-369">Document</span></span> | <span data-ttu-id="c21f1-370">Lettore</span><span class="sxs-lookup"><span data-stu-id="c21f1-370">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="c21f1-371">Legacy</span><span class="sxs-lookup"><span data-stu-id="c21f1-371">Legacy</span></span>                      | <span data-ttu-id="c21f1-372">15 elementi</span><span class="sxs-lookup"><span data-stu-id="c21f1-372">15 items</span></span> | <span data-ttu-id="c21f1-373">100 elementi</span><span class="sxs-lookup"><span data-stu-id="c21f1-373">100 items</span></span> |
| <span data-ttu-id="c21f1-374">COM</span><span class="sxs-lookup"><span data-stu-id="c21f1-374">COM</span></span>                         | <span data-ttu-id="c21f1-375">15 elementi</span><span class="sxs-lookup"><span data-stu-id="c21f1-375">15 items</span></span> | <span data-ttu-id="c21f1-376">Nessun limite</span><span class="sxs-lookup"><span data-stu-id="c21f1-376">No limit</span></span>  |



 

<span data-ttu-id="c21f1-377">Di seguito sono riportate alcune voci del registro di sistema che usano il valore MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="c21f1-377">The following are example registry entries using the MultiSelectModel value.</span></span>

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

### <a name="using-item-attributes"></a><span data-ttu-id="c21f1-378">Uso degli attributi degli elementi</span><span class="sxs-lookup"><span data-stu-id="c21f1-378">Using Item Attributes</span></span>

<span data-ttu-id="c21f1-379">È possibile testare i valori del flag [**SFGAO**](sfgao.md) degli attributi della Shell per un elemento per determinare se il verbo deve essere abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c21f1-379">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="c21f1-380">Per usare questa funzionalità di attributo, aggiungere i seguenti valori **reg \_ DWORD** sotto il verbo:</span><span class="sxs-lookup"><span data-stu-id="c21f1-380">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="c21f1-381">Il valore AttributeMask specifica il valore [**SFGAO**](sfgao.md) dei valori di bit della maschera con cui eseguire il test.</span><span class="sxs-lookup"><span data-stu-id="c21f1-381">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="c21f1-382">Il valore AttributeValue specifica il valore [**SFGAO**](sfgao.md) dei bit sottoposti a test.</span><span class="sxs-lookup"><span data-stu-id="c21f1-382">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="c21f1-383">ImpliedSelectionModel specifica zero per i verbi di elemento o un valore diverso da zero per i verbi nel menu di scelta rapida in background.</span><span class="sxs-lookup"><span data-stu-id="c21f1-383">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="c21f1-384">Nell'esempio seguente di voce del registro di sistema, AttributeMask è impostato su [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="c21f1-384">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

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

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="c21f1-385">Implementazione di verbi personalizzati per le cartelle tramite Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="c21f1-385">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="c21f1-386">In Windows 7 e versioni successive, è possibile aggiungere verbi a una cartella tramite Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="c21f1-386">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="c21f1-387">Per ulteriori informazioni sui file di Desktop.ini, vedere [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="c21f1-387">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="c21f1-388">I file di Desktop.ini devono essere sempre contrassegnati come nascosti dal **sistema**  +   , in modo che non vengano visualizzati dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="c21f1-388">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="c21f1-389">**Per aggiungere verbi personalizzati per le cartelle tramite un file di Desktop.ini, seguire questa procedura:**</span><span class="sxs-lookup"><span data-stu-id="c21f1-389">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="c21f1-390">Creare una cartella contrassegnata come di sola **lettura** o di **sistema**.</span><span class="sxs-lookup"><span data-stu-id="c21f1-390">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="c21f1-391">Creare un file di Desktop.ini che includa un \[ . ShellClassInfo \] DirectoryClass = cartella ProgID.</span><span class="sxs-lookup"><span data-stu-id="c21f1-391">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="c21f1-392">Nel registro di sistema creare **HKEY \_ classi \_ radice** \\ **ProgID** con un valore CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="c21f1-392">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="c21f1-393">Il valore CanUseForDirectory evita l'utilizzo improprio dei ProgID impostati per non partecipare all'implementazione di verbi personalizzati per le cartelle tramite Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="c21f1-393">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="c21f1-394">Aggiungere i verbi nella sottochiave ProgID della **cartella**, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c21f1-394">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="c21f1-395">Questi verbi possono essere il verbo predefinito, nel qual caso fare doppio clic sulla cartella per attivare il verbo.</span><span class="sxs-lookup"><span data-stu-id="c21f1-395">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c21f1-396">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c21f1-396">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c21f1-397">Procedure consigliate per i gestori di menu di scelta rapida e più verbi di selezione</span><span class="sxs-lookup"><span data-stu-id="c21f1-397">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="c21f1-398">Scelta di un verbo statico o dinamico per il menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="c21f1-398">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="c21f1-399">Personalizzazione di un menu di scelta rapida tramite verbi dinamici</span><span class="sxs-lookup"><span data-stu-id="c21f1-399">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="c21f1-400">Menu di scelta rapida (contesto) e gestori di menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="c21f1-400">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="c21f1-401">Verbi e associazioni di file</span><span class="sxs-lookup"><span data-stu-id="c21f1-401">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="c21f1-402">Riferimento al menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="c21f1-402">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
