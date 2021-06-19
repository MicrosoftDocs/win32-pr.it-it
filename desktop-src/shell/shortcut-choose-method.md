---
description: Scegliere un metodo di menu di scelta rapida statico o dinamico quando si implementa un formato di file personalizzato nella shell di Windows.
title: Scelta di un metodo di menu di scelta rapida statico o dinamico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: dfd73ee052594e1136fe2885ce92b682f229096b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394776"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a><span data-ttu-id="592ee-103">Scelta di un metodo di menu di scelta rapida statico o dinamico</span><span class="sxs-lookup"><span data-stu-id="592ee-103">Choosing a Static or Dynamic Shortcut Menu Method</span></span>

<span data-ttu-id="592ee-104">Questo argomento è organizzato come segue:</span><span class="sxs-lookup"><span data-stu-id="592ee-104">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="592ee-105">Scegliere un metodo verbo</span><span class="sxs-lookup"><span data-stu-id="592ee-105">Choose a Verb Method</span></span>](#choose-a-verb-method)
    -   [<span data-ttu-id="592ee-106">Metodi verbi statici</span><span class="sxs-lookup"><span data-stu-id="592ee-106">Static Verb Methods</span></span>](#static-verb-methods)
    -   [<span data-ttu-id="592ee-107">Metodi verbi dinamici preferiti</span><span class="sxs-lookup"><span data-stu-id="592ee-107">Preferred Dynamic Verb Methods</span></span>](#preferred-dynamic-verb-methods)
    -   [<span data-ttu-id="592ee-108">Metodi verbi dinamici sconsigliati</span><span class="sxs-lookup"><span data-stu-id="592ee-108">Discouraged Dynamic Verb Methods</span></span>](#discouraged-dynamic-verb-methods)
-   [<span data-ttu-id="592ee-109">Estendere un menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="592ee-109">Extend a Shortcut Menu</span></span>](#extend-a-shortcut-menu)
-   [<span data-ttu-id="592ee-110">Supporto per i metodi verbi in base al sistema operativo</span><span class="sxs-lookup"><span data-stu-id="592ee-110">Support for Verb Methods by Operating System</span></span>](#support-for-verb-methods-by-operating-system)
-   [<span data-ttu-id="592ee-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="592ee-111">Related topics</span></span>](#related-topics)

## <a name="choose-a-verb-method"></a><span data-ttu-id="592ee-112">Scegliere un metodo verbo</span><span class="sxs-lookup"><span data-stu-id="592ee-112">Choose a Verb Method</span></span>

<span data-ttu-id="592ee-113">È consigliabile implementare un menu di scelta rapida usando uno dei metodi verbi statici.</span><span class="sxs-lookup"><span data-stu-id="592ee-113">It is strongly encouraged that you implement a shortcut menu using one of the static verb methods.</span></span>

### <a name="static-verb-methods"></a><span data-ttu-id="592ee-114">Metodi verbi statici</span><span class="sxs-lookup"><span data-stu-id="592ee-114">Static Verb Methods</span></span>

<span data-ttu-id="592ee-115">I verbi statici sono i verbi più semplici da implementare, ma forniscono comunque funzionalità avanzate.</span><span class="sxs-lookup"><span data-stu-id="592ee-115">Static verbs are the simplest verbs to implement, but they still provide rich functionality.</span></span> <span data-ttu-id="592ee-116">Scegliere sempre il metodo di menu di scelta rapida più semplice che soddisfi le proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="592ee-116">Always chose the simplest shortcut menu method that meets your needs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="592ee-117">Verbo statico</span><span class="sxs-lookup"><span data-stu-id="592ee-117">Static Verb</span></span></th>
<th><span data-ttu-id="592ee-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="592ee-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="592ee-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess con</strong></a> parametri della riga di comando</span><span class="sxs-lookup"><span data-stu-id="592ee-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> with command line parameters</span></span></td>
<td><span data-ttu-id="592ee-120">Questo è il modo più semplice e familiare per implementare un verbo statico.</span><span class="sxs-lookup"><span data-stu-id="592ee-120">This is the simplest and most familiar means of implementing a static verb.</span></span> <span data-ttu-id="592ee-121">Un processo viene richiamato tramite una chiamata alla <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>funzione CreateProcess</strong></a> con i file selezionati ed eventuali parametri facoltativi passati come riga di comando.</span><span class="sxs-lookup"><span data-stu-id="592ee-121">A process is invoked through a call to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> function with the selected files and any optional parameters passed as the command line.</span></span> <span data-ttu-id="592ee-122">Verrà aperto il file o la cartella.</span><span class="sxs-lookup"><span data-stu-id="592ee-122">This opens the file or folder.</span></span><br/> <span data-ttu-id="592ee-123">Questo metodo presenta le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="592ee-123">This method has the following limitations:</span></span>
<ul>
<li><span data-ttu-id="592ee-124">La lunghezza della riga di comando è limitata a 2000 caratteri, limitando il numero di elementi che il verbo può gestire.</span><span class="sxs-lookup"><span data-stu-id="592ee-124">The command-line length is limited to 2000 characters, which limits the number of items that the verb can handle.</span></span></li>
<li><span data-ttu-id="592ee-125">Può essere usato solo con file system elementi.</span><span class="sxs-lookup"><span data-stu-id="592ee-125">Can only be used with file system items.</span></span></li>
<li><span data-ttu-id="592ee-126">Non consente il nuovo uso di un processo già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="592ee-126">Does not enable re-use of an already running process.</span></span></li>
<li><span data-ttu-id="592ee-127">Richiede l'installazione di un eseguibile per gestire il verbo.</span><span class="sxs-lookup"><span data-stu-id="592ee-127">Requires that an executable be installed to handle the verb.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="592ee-128"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></span><span class="sxs-lookup"><span data-stu-id="592ee-128"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a></span></span></td>
<td><span data-ttu-id="592ee-129">Un'attivazione verbo basata su COM significa che supporta l'attivazione in-process o out-of-process.</span><span class="sxs-lookup"><span data-stu-id="592ee-129">A COM-based verb activation means that supports in-proc or out-of-proc activation.</span></span> <span data-ttu-id="592ee-130"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> supporta anche il nuovo uso di un gestore già in esecuzione quando <strong>l'interfaccia IDropTarget</strong> viene implementata da un server locale.</span><span class="sxs-lookup"><span data-stu-id="592ee-130"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> also supports re-use of an already running handler when the <strong>IDropTarget</strong> interface is implemented by a local server.</span></span> <span data-ttu-id="592ee-131">Esprime inoltre perfettamente gli elementi tramite l'oggetto dati sottoposto a marshalling e fornisce un riferimento alla catena di siti di chiamata in modo che sia possibile interagire con l'invoker tramite <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService.</strong></a></span><span class="sxs-lookup"><span data-stu-id="592ee-131">It also perfectly expresses the items via the marshaled data object and provides a reference to the invoking site chain so that you can interact with the invoker through the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="592ee-132">Windows 7 e versioni successive: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="592ee-132">Windows 7 and later: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a></span></span></td>
<td><span data-ttu-id="592ee-133">Metodo di implementazione più diretto.</span><span class="sxs-lookup"><span data-stu-id="592ee-133">The most direct implementation method.</span></span> <span data-ttu-id="592ee-134">Poiché si tratta di un metodo invoke basato su COM (come DropTarget), questa interfaccia supporta l'attivazione in-process e out-of-process.</span><span class="sxs-lookup"><span data-stu-id="592ee-134">Because this is a COM-based invoke method (like DropTarget) this interface supports in-proc and out-of-proc activation.</span></span> <span data-ttu-id="592ee-135">Il verbo <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>implementa IExecuteCommand</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>e, facoltativamente, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand.</strong></a></span><span class="sxs-lookup"><span data-stu-id="592ee-135">The verb implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>, and optionally <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span></span> <span data-ttu-id="592ee-136">Gli elementi vengono passati direttamente come matrice di elementi della shell e più parametri dell'invoker sono disponibili per l'implementazione del verbo, inclusi il punto di richiamo, lo stato della tastiera e così via.</span><span class="sxs-lookup"><span data-stu-id="592ee-136">The items are passed directly as a Shell item array and more of the parameters from the invoker are available to the verb implementation, including the invoke point, keyboard state, and so forth.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="592ee-137">Windows 7 e versioni successive:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="592ee-137">Windows 7 and later:<strong>ExplorerCommand</strong>/ <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span></span></td>
<td><span data-ttu-id="592ee-138">Consente alle origini dati che forniscono i comandi del modulo comandi tramite <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> di usare tali comandi come verbi in un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="592ee-138">Enables data sources that provide their command module commands through <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="592ee-139">Poiché questa interfaccia supporta solo l'attivazione in-process, è consigliabile usarla dalle origini dati della shell che devono condividere l'implementazione tra comandi e menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="592ee-139">Because this interface supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="592ee-140">[**IExplorerCommand è**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) un ibrido tra un verbo statico e dinamico.</span><span class="sxs-lookup"><span data-stu-id="592ee-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) is a hybrid between a static and dynamic verb.</span></span> <span data-ttu-id="592ee-141">**IExplorerCommand è** stato dichiarato in Windows Vista, ma la possibilità di implementare un verbo in un menu di scelta rapida è una novità di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="592ee-141">**IExplorerCommand** was declared in Windows Vista, but its ability to implement a verb in a shortcut menu is new to Windows 7.</span></span>

 

<span data-ttu-id="592ee-142">Per altre informazioni sulle query [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione di file, vedere [Tipi percepiti e Registrazione dell'applicazione.](fa-perceivedtypes.md)</span><span class="sxs-lookup"><span data-stu-id="592ee-142">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="preferred-dynamic-verb-methods"></a><span data-ttu-id="592ee-143">Metodi verbi dinamici preferiti</span><span class="sxs-lookup"><span data-stu-id="592ee-143">Preferred Dynamic Verb Methods</span></span>

<span data-ttu-id="592ee-144">Sono preferibili i metodi verbi dinamici seguenti:</span><span class="sxs-lookup"><span data-stu-id="592ee-144">The following dynamic verb methods are preferred:</span></span>



| <span data-ttu-id="592ee-145">Tipo di verbo</span><span class="sxs-lookup"><span data-stu-id="592ee-145">Verb Type</span></span>                                                                                 | <span data-ttu-id="592ee-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="592ee-146">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="592ee-147">Verbo statico (elencato nella tabella precedente) + Sintassi di query avanzata (AQS)</span><span class="sxs-lookup"><span data-stu-id="592ee-147">Static verb (listed in the previous table) + Advanced Query Syntax (AQS)</span></span>                  | <span data-ttu-id="592ee-148">Questa scelta ottiene la visibilità dinamica del verbo.</span><span class="sxs-lookup"><span data-stu-id="592ee-148">This choice gets dynamic verb visibility.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="592ee-149">Windows 7 e versioni successive: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span><span class="sxs-lookup"><span data-stu-id="592ee-149">Windows 7 and later: [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span></span>                         | <span data-ttu-id="592ee-150">Questa scelta consente un'implementazione comune di verbi e comandi di esplorazione visualizzati nel modulo di comando in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="592ee-150">This choice enables a common implementation of verbs and explorer commands that are displayed in the command module in Windows Explorer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="592ee-151">Windows 7 e versioni successive: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbo statico</span><span class="sxs-lookup"><span data-stu-id="592ee-151">Windows 7 and later: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + static verb</span></span> | <span data-ttu-id="592ee-152">Questa scelta ottiene anche la visibilità dinamica del verbo.</span><span class="sxs-lookup"><span data-stu-id="592ee-152">This choice also gets dynamic verb visibility.</span></span> <span data-ttu-id="592ee-153">Si tratta di un modello ibrido in cui viene usato un semplice gestore in-process per calcolare se un verbo statico specificato deve essere displyed.</span><span class="sxs-lookup"><span data-stu-id="592ee-153">It is a hybrid model where a simple in-process handler is used to compute if a given static verb should be displyed.</span></span> <span data-ttu-id="592ee-154">Questo può essere applicato a tutti i metodi di implementazione dei verbi statici per ottenere un comportamento dinamico e ridurre al minimo l'esposizione della logica in-process.</span><span class="sxs-lookup"><span data-stu-id="592ee-154">This can be applied to all of the static verb implementation methods to achieve dynamic behavior and minimize the exposure of the in-process logic.</span></span> <span data-ttu-id="592ee-155">[**IExplorerCommandState ha**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) il vantaggio di essere eseguito in un thread in background, evitando così blocchi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="592ee-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) has the advantage of running on a background thread, and thereby avoids UI hangs.</span></span> <span data-ttu-id="592ee-156">È notevolmente più semplice di [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)</span><span class="sxs-lookup"><span data-stu-id="592ee-156">It is considerably simpler than [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> |



 

### <a name="discouraged-dynamic-verb-methods"></a><span data-ttu-id="592ee-157">Metodi verbi dinamici sconsigliati</span><span class="sxs-lookup"><span data-stu-id="592ee-157">Discouraged Dynamic Verb Methods</span></span>

<span data-ttu-id="592ee-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) è il metodo più potente ma anche il metodo più complesso da implementare.</span><span class="sxs-lookup"><span data-stu-id="592ee-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="592ee-159">Si basa su oggetti COM in-process eseguiti sul thread del chiamante, che in genere Esplora risorse ma può essere qualsiasi applicazione che ospita gli elementi.</span><span class="sxs-lookup"><span data-stu-id="592ee-159">It is based on in-process COM objects that run on the thread of the caller, which usually Windows Explorer but can be any application hosting the items.</span></span> <span data-ttu-id="592ee-160">**IContextMenu supporta** la visibilità dei verbi, l'ordinamento e il disegno personalizzato.</span><span class="sxs-lookup"><span data-stu-id="592ee-160">**IContextMenu** supports verb visibility, ordering, and custom drawing.</span></span> <span data-ttu-id="592ee-161">Alcune di queste funzionalità sono state aggiunte alle funzionalità dei verbi statici, ad esempio un'icona da associare a un comando e [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) per gestire la visibilità.</span><span class="sxs-lookup"><span data-stu-id="592ee-161">Some of these features have been added to the static verb features, such as an icon to be associated with a command, and [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) to deal with visibility.</span></span>

<span data-ttu-id="592ee-162">Se è necessario estendere il menu di scelta rapida per un tipo di file registrando un verbo dinamico per il tipo di file, seguire le istruzioni fornite in [Personalizzazione](shortcut-menu-using-dynamic-verbs.md)di un menu di scelta rapida utilizzando verbi dinamici .</span><span class="sxs-lookup"><span data-stu-id="592ee-162">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided in [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

## <a name="extend-a-shortcut-menu"></a><span data-ttu-id="592ee-163">Estendere un menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="592ee-163">Extend a Shortcut Menu</span></span>

<span data-ttu-id="592ee-164">Dopo aver scelto un metodo verbo, è possibile estendere un menu di scelta rapida per un tipo di file registrando un verbo statico per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="592ee-164">After you choose a verb method you can extend a shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="592ee-165">Per altre informazioni, vedere [Creazione di gestori del menu di scelta rapida.](context-menu-handlers.md)</span><span class="sxs-lookup"><span data-stu-id="592ee-165">For more information, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="support-for-verb-methods-by-operating-system"></a><span data-ttu-id="592ee-166">Supporto per i metodi verbi in base al sistema operativo</span><span class="sxs-lookup"><span data-stu-id="592ee-166">Support for Verb Methods by Operating System</span></span>

<span data-ttu-id="592ee-167">Il supporto per i metodi di chiamata dei verbi in base al sistema operativo è elencato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="592ee-167">Support for verb invocation methods by operating system are listed in the following table.</span></span>



| <span data-ttu-id="592ee-168">Metodo Verb</span><span class="sxs-lookup"><span data-stu-id="592ee-168">Verb Method</span></span>          | <span data-ttu-id="592ee-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="592ee-169">Windows XP</span></span> | <span data-ttu-id="592ee-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="592ee-170">Windows Vista</span></span> | <span data-ttu-id="592ee-171">Windows 7 e oltre</span><span class="sxs-lookup"><span data-stu-id="592ee-171">Windows 7 and beyond</span></span> |
|----------------------|------------|---------------|----------------------|
| <span data-ttu-id="592ee-172">CreateProcess</span><span class="sxs-lookup"><span data-stu-id="592ee-172">CreateProcess</span></span>        | <span data-ttu-id="592ee-173">X</span><span class="sxs-lookup"><span data-stu-id="592ee-173">X</span></span>          | <span data-ttu-id="592ee-174">X</span><span class="sxs-lookup"><span data-stu-id="592ee-174">X</span></span>             | <span data-ttu-id="592ee-175">X</span><span class="sxs-lookup"><span data-stu-id="592ee-175">X</span></span>                    |
| <span data-ttu-id="592ee-176">DDE</span><span class="sxs-lookup"><span data-stu-id="592ee-176">DDE</span></span>                  | <span data-ttu-id="592ee-177">X</span><span class="sxs-lookup"><span data-stu-id="592ee-177">X</span></span>          | <span data-ttu-id="592ee-178">X</span><span class="sxs-lookup"><span data-stu-id="592ee-178">X</span></span>             | <span data-ttu-id="592ee-179">X</span><span class="sxs-lookup"><span data-stu-id="592ee-179">X</span></span>                    |
| <span data-ttu-id="592ee-180">DropTarget</span><span class="sxs-lookup"><span data-stu-id="592ee-180">DropTarget</span></span>           | <span data-ttu-id="592ee-181">X</span><span class="sxs-lookup"><span data-stu-id="592ee-181">X</span></span>          | <span data-ttu-id="592ee-182">X</span><span class="sxs-lookup"><span data-stu-id="592ee-182">X</span></span>             | <span data-ttu-id="592ee-183">X</span><span class="sxs-lookup"><span data-stu-id="592ee-183">X</span></span>                    |
| <span data-ttu-id="592ee-184">ExecuteCommand</span><span class="sxs-lookup"><span data-stu-id="592ee-184">ExecuteCommand</span></span>       |            | <span data-ttu-id="592ee-185">X</span><span class="sxs-lookup"><span data-stu-id="592ee-185">X</span></span>             | <span data-ttu-id="592ee-186">X</span><span class="sxs-lookup"><span data-stu-id="592ee-186">X</span></span>                    |
| <span data-ttu-id="592ee-187">ExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="592ee-187">ExplorerCommand</span></span>      |            |               | <span data-ttu-id="592ee-188">X</span><span class="sxs-lookup"><span data-stu-id="592ee-188">X</span></span>                    |
| <span data-ttu-id="592ee-189">ExplorerCommandState</span><span class="sxs-lookup"><span data-stu-id="592ee-189">ExplorerCommandState</span></span> |            |               | <span data-ttu-id="592ee-190">X</span><span class="sxs-lookup"><span data-stu-id="592ee-190">X</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="592ee-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="592ee-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="592ee-192">Procedure consigliate per i gestori del menu di scelta rapida e più verbi di selezione</span><span class="sxs-lookup"><span data-stu-id="592ee-192">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="592ee-193">Creazione di gestori del menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="592ee-193">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="592ee-194">Personalizzazione di un menu di scelta rapida tramite verbi dinamici</span><span class="sxs-lookup"><span data-stu-id="592ee-194">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="592ee-195">Menu di scelta rapida e gestori del menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="592ee-195">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="592ee-196">Riferimento al menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="592ee-196">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> <dt>

[<span data-ttu-id="592ee-197">Verbi e associazioni di file</span><span class="sxs-lookup"><span data-stu-id="592ee-197">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> </dl>

 

 
