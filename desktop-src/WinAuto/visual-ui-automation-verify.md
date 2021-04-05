---
title: Verifica automazione interfaccia utente visiva
description: Verifica di automazione interfaccia utente visuale (Visual UIA Verify) è una finestra \ 32; Driver GUI per la libreria di test di UIA progettata per il test manuale dell'automazione dell'interfaccia utente.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e224a52d243427af86c6cd27a3add3be03d9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713771"
---
# <a name="visual-ui-automation-verify"></a><span data-ttu-id="ee40e-103">Verifica automazione interfaccia utente visiva</span><span class="sxs-lookup"><span data-stu-id="ee40e-103">Visual UI Automation Verify</span></span>

<span data-ttu-id="ee40e-104">Visual UI Automation Verify (Visual UIA Verify) è un driver GUI Windows per la libreria di test di UIA progettata per il test manuale dell'automazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-104">Visual UI Automation Verify (Visual UIA Verify) is a Windows GUI driver for the UIA Test Library that is designed for manual testing of UI automation.</span></span> <span data-ttu-id="ee40e-105">Fornisce un'interfaccia per la funzionalità della libreria di test UIA che elimina l'overhead di codifica di uno strumento da riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ee40e-105">It provides an interface to UIA Test Library functionality that eliminates the coding overhead of a command-line tool.</span></span>

-   [<span data-ttu-id="ee40e-106">Comandi di menu</span><span class="sxs-lookup"><span data-stu-id="ee40e-106">Menu Commands</span></span>](#menu-commands)
-   [<span data-ttu-id="ee40e-107">Riquadri funzionali</span><span class="sxs-lookup"><span data-stu-id="ee40e-107">Functional Panes</span></span>](#functional-panes)
    -   [<span data-ttu-id="ee40e-108">Riquadro dell'albero elementi di automazione</span><span class="sxs-lookup"><span data-stu-id="ee40e-108">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
    -   [<span data-ttu-id="ee40e-109">Riquadro test</span><span class="sxs-lookup"><span data-stu-id="ee40e-109">Tests Pane</span></span>](#tests-pane)
    -   [<span data-ttu-id="ee40e-110">Riquadro Risultati test</span><span class="sxs-lookup"><span data-stu-id="ee40e-110">Test Results Pane</span></span>](#test-results-pane)
    -   [<span data-ttu-id="ee40e-111">Riquadro proprietà</span><span class="sxs-lookup"><span data-stu-id="ee40e-111">Properties Pane</span></span>](#properties-pane)

<span data-ttu-id="ee40e-112">Visual UIA Verify supporta solo il logger di verifica di UIA (WUIALoggerXml.dll) in modo nativo.</span><span class="sxs-lookup"><span data-stu-id="ee40e-112">Visual UIA Verify supports only the UIA Verify XML logger (WUIALoggerXml.dll) natively.</span></span> <span data-ttu-id="ee40e-113">Le trasformazioni XML selezionabili dall'utente sono incorporate in Visual UIA Verify per presentare diverse visualizzazioni del report del logger XML nel riquadro **risultati test** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-113">User-selectable XML transformations are incorporated into Visual UIA Verify to present various views of the XML logger report in the **Test Results** pane.</span></span>

<span data-ttu-id="ee40e-114">Per impostazione predefinita, Visual UIA Verify carica il provider del lato client di automazione interfaccia utente fornito con la versione originale di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-114">By default, Visual UIA Verify loads the UI Automation client-side provider that shipped with the original release of UI Automation.</span></span> <span data-ttu-id="ee40e-115">È possibile scegliere di non caricare il provider aggiungendo **/NOCLIENTSIDEPROVIDER** nell'opzione della riga di comando di VisualUIVerifyNative.exe.</span><span class="sxs-lookup"><span data-stu-id="ee40e-115">You can choose not to load this provider by adding **/NOCLIENTSIDEPROVIDER** in the command-line option of VisualUIVerifyNative.exe.</span></span>

<span data-ttu-id="ee40e-116">Lo screenshot seguente mostra le principali aree funzionali dell'interfaccia utente di verifica di Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="ee40e-116">The following screen shot shows the main functional areas of the Visual UIA Verify user interface.</span></span>

![principali aree funzionali dell'interfaccia utente di verifica di Visual UIA](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a><span data-ttu-id="ee40e-118">Comandi di menu</span><span class="sxs-lookup"><span data-stu-id="ee40e-118">Menu Commands</span></span>

<span data-ttu-id="ee40e-119">Nella tabella seguente vengono descritti i comandi del menu di verifica di visuali.</span><span class="sxs-lookup"><span data-stu-id="ee40e-119">The following table describes the commands in the Visual UIA Verify menu.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee40e-120">Menu</span><span class="sxs-lookup"><span data-stu-id="ee40e-120">Menu</span></span></th>
<th><span data-ttu-id="ee40e-121">Comando</span><span class="sxs-lookup"><span data-stu-id="ee40e-121">Command</span></span></th>
<th><span data-ttu-id="ee40e-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee40e-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee40e-123"><strong>File</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-123"><strong>File</strong></span></span></td>
<td><span data-ttu-id="ee40e-124"><strong>Esci</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-124"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="ee40e-125">Uscire da Visual UIA Verify.</span><span class="sxs-lookup"><span data-stu-id="ee40e-125">Exit Visual UIA Verify.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee40e-126"><strong>Visualizzazione</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-126"><strong>View</strong></span></span></td>
<td><span data-ttu-id="ee40e-127"><strong>Evidenziazione</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-127"><strong>Highlighting</strong></span></span></td>
<td><span data-ttu-id="ee40e-128">Evidenziare il rettangolo delimitatore dell'elemento selezionato nel riquadro <strong>dell'albero degli elementi di automazione</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee40e-128">Highlight the bounding rectangle of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="ee40e-129">Sono disponibili le seguenti opzioni.</span><span class="sxs-lookup"><span data-stu-id="ee40e-129">The following options are available.</span></span>
<ul>
<li><span data-ttu-id="ee40e-130"><strong>Rettangolo</strong>: linea rossa continua.</span><span class="sxs-lookup"><span data-stu-id="ee40e-130"><strong>Rectangle</strong>—A solid red line.</span></span></li>
<li><span data-ttu-id="ee40e-131"><strong>Rettangolo di dissolvenza</strong>: una linea rossa continua che scompare dopo pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="ee40e-131"><strong>Fading Rectangle</strong>—A solid red line that disappears after a few seconds.</span></span></li>
<li><span data-ttu-id="ee40e-132"><strong>Rays e rettangolo</strong>, una linea rossa continua con linee di evidenziazione blu aggiuntive che si irradiano da ogni angolo del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="ee40e-132"><strong>Rays and Rectangle</strong>—A solid red line with additional blue highlight lines that radiate from each corner of the bounding rectangle.</span></span></li>
<li><span data-ttu-id="ee40e-133"><strong>None</strong>: Nessuna evidenziazione visibile.</span><span class="sxs-lookup"><span data-stu-id="ee40e-133"><strong>None</strong>—No visible highlight.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="ee40e-134"><strong>Albero degli elementi di automazione</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ee40e-134"><strong>Automation Elements Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ee40e-135"><strong>Aggiorna elemento selezionato</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-135"><strong>Refresh Selected Element</strong></span></span></td>
<td><span data-ttu-id="ee40e-136">Aggiornare gli elementi figlio dell'elemento selezionato nel riquadro <strong>dell'albero degli elementi di automazione</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee40e-136">Refresh the children of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="ee40e-137">L'elenco di elementi è statico e non viene aggiornato dinamicamente (automaticamente) se l'albero degli elementi viene modificato.</span><span class="sxs-lookup"><span data-stu-id="ee40e-137">The list of elements is static and does not refresh dynamically (automatically) if the element tree changes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee40e-138"><strong>Spostamento</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-138"><strong>Navigation</strong></span></span></td>
<td><span data-ttu-id="ee40e-139">Spostarsi nella gerarchia della struttura ad albero degli elementi in uno dei seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="ee40e-139">Navigate through the element tree hierarchy to one of the following elements.</span></span>
<ul>
<li><span data-ttu-id="ee40e-140"><strong>Parent</strong>: passa all'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="ee40e-140"><strong>Parent</strong>—Go to parent element.</span></span></li>
<li><span data-ttu-id="ee40e-141"><strong>Primo elemento figlio</strong>— passa al primo elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="ee40e-141"><strong>First Child</strong>—Go to first child element.</span></span></li>
<li><span data-ttu-id="ee40e-142"><strong>Fratello di pari livello successivo</strong>-Vai al primo elemento di pari livello.</span><span class="sxs-lookup"><span data-stu-id="ee40e-142"><strong>Next Sibling</strong>—Go to first sibling element.</span></span></li>
<li><span data-ttu-id="ee40e-143"><strong>Precedente elemento di pari livello</strong>-passa a elemento di pari livello precedente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-143"><strong>Previous Sibling</strong>—Go to previous sibling element.</span></span></li>
<li><span data-ttu-id="ee40e-144"><strong>Ultimo elemento figlio</strong>: passa all'ultimo elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="ee40e-144"><strong>Last Child</strong>—Go to last child element.</span></span></li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="ee40e-145"><strong>Modalità</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ee40e-145"><strong>Mode</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ee40e-146"><strong>Always On Top</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-146"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="ee40e-147">La finestra di verifica di visuale UIA rimane nella parte superiore dell'ordine z del desktop.</span><span class="sxs-lookup"><span data-stu-id="ee40e-147">The Visual UIA Verify window remains at the top of the desktop z-order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee40e-148"><strong>Modalità hover (usare Ctrl)</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-148"><strong>Hover Mode (Use Ctrl)</strong></span></span></td>
<td><span data-ttu-id="ee40e-149">Quando si preme il tasto CTRL, l'elemento sotto il cursore del mouse viene identificato come elemento di interesse.</span><span class="sxs-lookup"><span data-stu-id="ee40e-149">When the Ctrl key is pressed, the element under the mouse cursor is identified as the element of interest.</span></span> <span data-ttu-id="ee40e-150">Il riquadro dell' <strong>albero degli elementi di automazione</strong> viene aggiornato e viene evidenziato l'elemento corrispondente nell'elenco di elementi.</span><span class="sxs-lookup"><span data-stu-id="ee40e-150">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ee40e-151"><strong>Rilevamento dello stato attivo</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-151"><strong>Focus Tracking</strong></span></span></td>
<td><span data-ttu-id="ee40e-152">Quando viene modificato lo stato attivo, l'elemento con lo stato attivo viene identificato come elemento di interesse.</span><span class="sxs-lookup"><span data-stu-id="ee40e-152">As the focus changes, the element with the focus is identified as the element of interest.</span></span> <span data-ttu-id="ee40e-153">Il riquadro dell' <strong>albero degli elementi di automazione</strong> viene aggiornato e viene evidenziato l'elemento corrispondente nell'elenco di elementi.</span><span class="sxs-lookup"><span data-stu-id="ee40e-153">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="ee40e-154"><strong>Test</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ee40e-154"><strong>Tests</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ee40e-155"><strong>Vai a sinistra</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-155"><strong>Go Left</strong></span></span></td>
<td><span data-ttu-id="ee40e-156">Spostare un nodo a sinistra nell'albero dei <strong>test</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee40e-156">Move one node left in the <strong>Tests</strong> tree.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee40e-157"><strong>Vai su</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-157"><strong>Go Up</strong></span></span></td>
<td><span data-ttu-id="ee40e-158">Spostare un nodo verso l'alto nell'albero dei <strong>test</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee40e-158">Move one node up in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ee40e-159"><strong>Vai giù</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-159"><strong>Go Down</strong></span></span></td>
<td><span data-ttu-id="ee40e-160">Spostare un nodo verso il basso nell'albero dei <strong>test</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee40e-160">Move one node down in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ee40e-161"><strong>Vai a destra</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-161"><strong>Go Right</strong></span></span></td>
<td><span data-ttu-id="ee40e-162">Spostare un nodo direttamente nell'albero dei <strong>test</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee40e-162">Move one node right in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ee40e-163"><strong>Esegui i test selezionati sull'elemento selezionato</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-163"><strong>Run Selected Test(s) On Selected Element</strong></span></span></td>
<td><span data-ttu-id="ee40e-164">Esegue i test selezionati dall'albero dei <strong>test</strong> nell'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="ee40e-164">Run the selected tests from the <strong>Tests</strong> tree on the selected element.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ee40e-165"><strong>Filtra problemi noti</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-165"><strong>Filter Known Problems</strong></span></span></td>
<td><span data-ttu-id="ee40e-166">Filtrare i bug noti di automazione interfaccia utente dai risultati del test.</span><span class="sxs-lookup"><span data-stu-id="ee40e-166">Filter known UI Automation bugs from the test results.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ee40e-167"><strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-167"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="ee40e-168"><strong>Informazioni sulle verifiche di automazione interfaccia utente visiva</strong></span><span class="sxs-lookup"><span data-stu-id="ee40e-168"><strong>About Visual UI Automation Verify</strong></span></span></td>
<td><span data-ttu-id="ee40e-169">Visualizza la versione del software e le informazioni sul copyright per la verifica di Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="ee40e-169">Display the software version and copyright information for Visual UIA Verify.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a><span data-ttu-id="ee40e-170">Riquadri funzionali</span><span class="sxs-lookup"><span data-stu-id="ee40e-170">Functional Panes</span></span>

<span data-ttu-id="ee40e-171">Questa sezione descrive i riquadri funzionali nell'interfaccia utente di verifica di Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="ee40e-171">This section describes the functional panes in the Visual UIA Verify user interface.</span></span>

-   [<span data-ttu-id="ee40e-172">Riquadro dell'albero elementi di automazione</span><span class="sxs-lookup"><span data-stu-id="ee40e-172">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
-   [<span data-ttu-id="ee40e-173">Riquadro test</span><span class="sxs-lookup"><span data-stu-id="ee40e-173">Tests Pane</span></span>](#tests-pane)
-   [<span data-ttu-id="ee40e-174">Riquadro Risultati test</span><span class="sxs-lookup"><span data-stu-id="ee40e-174">Test Results Pane</span></span>](#test-results-pane)
-   [<span data-ttu-id="ee40e-175">Riquadro proprietà</span><span class="sxs-lookup"><span data-stu-id="ee40e-175">Properties Pane</span></span>](#properties-pane)

### <a name="automation-elements-tree-pane"></a><span data-ttu-id="ee40e-176">Riquadro dell'albero elementi di automazione</span><span class="sxs-lookup"><span data-stu-id="ee40e-176">Automation Elements Tree Pane</span></span>

<span data-ttu-id="ee40e-177">Il riquadro dell' **albero degli elementi di automazione** contiene uno snapshot gerarchico di oggetti elemento di automazione disponibili per il test.</span><span class="sxs-lookup"><span data-stu-id="ee40e-177">The **Automation Elements Tree** pane contains a hierarchical snapshot of automation element objects that are available for testing.</span></span> <span data-ttu-id="ee40e-178">Il primo elemento della struttura ad albero rappresenta il desktop.</span><span class="sxs-lookup"><span data-stu-id="ee40e-178">The top element in the tree represents the desktop.</span></span>

<span data-ttu-id="ee40e-179">Questa vista è una raccolta statica compilata al momento dell'avvio di Visual UIA Verify.</span><span class="sxs-lookup"><span data-stu-id="ee40e-179">This view is a static collection that is compiled when Visual UIA Verify starts.</span></span> <span data-ttu-id="ee40e-180">Per aggiornare la visualizzazione nel nodo selezionato, utilizzare il comando di menu **Aggiorna elemento selezionato** o il pulsante della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="ee40e-180">To refresh the view at the selected node, use the **Refresh Selected Element** menu command or toolbar button.</span></span>

<span data-ttu-id="ee40e-181">Lo screenshot seguente mostra il riquadro dell' **albero degli elementi di automazione** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-181">The following screen shot shows the **Automation Elements Tree** pane.</span></span>

![riquadro dell'albero degli elementi di automazione della verifica di Visual UIA](images/automation-elements-tree-pane.png)

<span data-ttu-id="ee40e-183">Un nodo grigio (non disponibile) nell' **albero degli elementi di automazione** indica che l'elemento è un membro della visualizzazione non elaborata di automazione interfaccia utente, ma non soddisfa le condizioni necessarie per essere considerato un membro della visualizzazione contenuto o della visualizzazione controlli.</span><span class="sxs-lookup"><span data-stu-id="ee40e-183">A dimmed (unavailable) node in the **Automation Elements Tree** indicates that the element is a member of the UI Automation raw view, but does not meet the conditions necessary to be considered a member of the content view or control view.</span></span> <span data-ttu-id="ee40e-184">Tuttavia, l'elemento può comunque essere testato dalla verifica di automazione interfaccia utente visuale.</span><span class="sxs-lookup"><span data-stu-id="ee40e-184">However, the element can still be tested from Visual UI Automation Verify.</span></span> <span data-ttu-id="ee40e-185">Per altre informazioni, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ee40e-185">For more information, see the [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="ee40e-186">I comandi disponibili dalla barra degli strumenti dell' **albero degli elementi di automazione** includono:</span><span class="sxs-lookup"><span data-stu-id="ee40e-186">Commands available from the **Automation Elements Tree** toolbar include:</span></span>

-   <span data-ttu-id="ee40e-187">**Aggiorna**: consente di aggiornare il nodo selezionato e i relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="ee40e-187">**Refresh**—Refresh the selected node and its children.</span></span> <span data-ttu-id="ee40e-188">Questo comando non aggiorna l'intero albero degli elementi a meno che non sia selezionato il nodo radice.</span><span class="sxs-lookup"><span data-stu-id="ee40e-188">This command does not refresh the entire element tree unless the root node is selected.</span></span>
-   <span data-ttu-id="ee40e-189">**Padre (CTRL + MAIUSC + F6)**: consente di passare all'elemento padre del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-189">**Parent (Ctrl+Shift+F6)**—Go to parent of the current node.</span></span>
-   <span data-ttu-id="ee40e-190">**Primo elemento figlio (CTRL + MAIUSC + F7)**: passa al primo elemento figlio del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-190">**First Child (Ctrl+Shift+F7)**—Go to first child of the current node..</span></span>
-   <span data-ttu-id="ee40e-191">Elemento di **pari livello successivo (CTRL + MAIUSC + F8)**: passa al figlio di pari livello successivo del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-191">**Next Sibling (Ctrl+Shift+F8)**—Go to next sibling child of the current node.</span></span>
-   <span data-ttu-id="ee40e-192">Elemento di **pari livello precedente (CTRL + MAIUSC + F9)**: consente di passare all'elemento di pari livello precedente del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-192">**Previous Sibling (Ctrl+Shift+F9)**—Go to previous sibling of the current node.</span></span>
-   <span data-ttu-id="ee40e-193">**Ultimo elemento figlio (CTRL + MAIUSC + F10)**: passa all'ultimo elemento figlio del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-193">**Last Child (Ctrl+Shift+F10)**—Go to last child of the current node.</span></span>
-   <span data-ttu-id="ee40e-194">**Rilevamento dello stato attivo**: attiva o disattiva la selezione dei nodi in base al rilevamento dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="ee40e-194">**Focus Tracking**—Toggle node selection on or off based on focus tracking.</span></span>

### <a name="tests-pane"></a><span data-ttu-id="ee40e-195">Riquadro test</span><span class="sxs-lookup"><span data-stu-id="ee40e-195">Tests Pane</span></span>

<span data-ttu-id="ee40e-196">Il riquadro **test** contiene un elenco di test di automazione interfaccia utente organizzati per tipo di test (**elemento di automazione**, **controllo** e **modello**) e priorità (**Verifica della compilazione**, **priorità 0**, **priorità 1**, **priorità 2** e **priorità 3**).</span><span class="sxs-lookup"><span data-stu-id="ee40e-196">The **Tests** pane contains a list of UI Automation tests organized by test type (**Automation Element**, **Control**, and **Pattern**) and priority (**Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, and **Priority 3**).</span></span> <span data-ttu-id="ee40e-197">Questo elenco viene generato in base al tipo di controllo dell'elemento selezionato nel riquadro **dell'albero degli elementi di automazione** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-197">This list is generated based on the control type of the selected element in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="ee40e-198">Per altre informazioni, vedere [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ee40e-198">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="ee40e-199">Lo screenshot seguente mostra il riquadro **test** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-199">The following screen shot shows the **Tests** pane.</span></span>

![riquadro test](images/test-pane.png)

<span data-ttu-id="ee40e-201">I comandi disponibili dalla barra degli strumenti **test** includono:</span><span class="sxs-lookup"><span data-stu-id="ee40e-201">Commands available from the **Tests** toolbar include:</span></span>

-   <span data-ttu-id="ee40e-202">**Mostra**: specifica i test di automazione interfaccia utente da visualizzare; ovvero visualizzare tutti i test o solo i test adatti al tipo di controllo dell'elemento selezionato nell' **albero degli elementi di automazione** (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="ee40e-202">**Show**—Specifies the UI Automation tests to display; that is, display all tests or only tests suited to the control type of the selected element in the **Automation Elements Tree** (default).</span></span>
-   <span data-ttu-id="ee40e-203">**Tipo**: specifica i tipi di test da visualizzare: **elemento di automazione**, **modello** o **controllo**.</span><span class="sxs-lookup"><span data-stu-id="ee40e-203">**Type**—Specifies the test types to display: **Automation Element**, **Pattern**, or **Control**.</span></span>
-   <span data-ttu-id="ee40e-204">**Priorità**— specifica le priorità di test da visualizzare **: verifica della compilazione**, **priorità 0**, **priorità 1**, **priorità 2** o **priorità 3**.</span><span class="sxs-lookup"><span data-stu-id="ee40e-204">**Priorities**—Specifies the test priorities to display: **Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, or **Priority 3**.</span></span>
-   <span data-ttu-id="ee40e-205">**Vai a sinistra**: consente di passare all'elemento padre del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-205">**Go Left**—Go to the parent of the current node.</span></span>
-   <span data-ttu-id="ee40e-206">**Go up**: passare all'elemento di pari livello precedente del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-206">**Go Up**—Go to the previous sibling of the current node.</span></span>
-   <span data-ttu-id="ee40e-207">**Vai giù**— passa all'elemento di pari livello successivo del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-207">**Go Down**—Go to the next sibling of the current node.</span></span>
-   <span data-ttu-id="ee40e-208">**Vai a destra**: passa al primo elemento figlio del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-208">**Go Right**—Go to the first child of the current node.</span></span>
-   <span data-ttu-id="ee40e-209">**Esegui test selezionati**: esegue i test sull'elemento selezionato nell' **albero degli elementi di automazione**.</span><span class="sxs-lookup"><span data-stu-id="ee40e-209">**Run Selected Test(s)**—Runs the tests on the element selected in the **Automation Elements Tree**.</span></span>

### <a name="test-results-pane"></a><span data-ttu-id="ee40e-210">Riquadro Risultati test</span><span class="sxs-lookup"><span data-stu-id="ee40e-210">Test Results Pane</span></span>

<span data-ttu-id="ee40e-211">Il riquadro **risultati test** contiene la funzionalità di registrazione per la verifica degli oggetti visivi.</span><span class="sxs-lookup"><span data-stu-id="ee40e-211">The **Test Results** pane contains the Visual UIA Verify logging functionality.</span></span> <span data-ttu-id="ee40e-212">Lo screenshot seguente mostra il riquadro **risultati test** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-212">The following screen shot shows the **Test Results** pane.</span></span>

![riquadro risultati test](images/test-results-pane.png)

<span data-ttu-id="ee40e-214">I comandi disponibili dalla barra degli strumenti **risultati test** includono:</span><span class="sxs-lookup"><span data-stu-id="ee40e-214">Commands available from the **Tests Results** toolbar include:</span></span>

-   <span data-ttu-id="ee40e-215">**Back**-pagina precedente nella cronologia di visualizzazione del report.</span><span class="sxs-lookup"><span data-stu-id="ee40e-215">**Back**—Page backward in report viewing history.</span></span>
-   <span data-ttu-id="ee40e-216">In **diretta**: pagina in futuro nella cronologia di visualizzazione del report.</span><span class="sxs-lookup"><span data-stu-id="ee40e-216">**Forward**—Page forward in report viewing history.</span></span>
-   <span data-ttu-id="ee40e-217">**Complessiva**— Visualizza un riepilogo dei risultati del test (errore **passato**, **non riuscito** e **imprevisto**).</span><span class="sxs-lookup"><span data-stu-id="ee40e-217">**Overall**—Displays a summary of the test results (**Passed**, **Failed**, and **Unexpected Error**).</span></span> <span data-ttu-id="ee40e-218">Il risultato del test è collegato alla visualizzazione **tutti i risultati** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-218">The test result is linked to the **All Results** view.</span></span> <span data-ttu-id="ee40e-219">Il comando **generale** Visualizza una tabella come quella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="ee40e-219">The **Overall** command displays a table like the following one.</span></span>

    ![tabella dei risultati del test complessiva](images/overall-test-results.png)

-   <span data-ttu-id="ee40e-221">**Tutti i risultati**: Visualizza un log dettagliato per ogni risultato del test, come illustrato nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="ee40e-221">**All Results**— Displays a detailed log for each test result, as shown in the following tables.</span></span>

    ![Dettagli risultati log di esempio dalla vista tutti i risultati](images/all-results-log.png)

    <span data-ttu-id="ee40e-223">Il nome del test nella tabella **tutti i risultati** è collegato a una descrizione test case per l'elemento, come nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-223">The test name in the **All Results** table is linked to a test case description for the element, as in the following table.</span></span>

    ![test case dettagli](images/test-case-detail.png)

-   <span data-ttu-id="ee40e-225">**Log completo**— Visualizza una visualizzazione alternativa del log dettagliato per ogni risultato del test, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-225">**Full Log**—Displays an alternate view of the detailed log for each test result, as shown in the following screen shot.</span></span>

    ![visualizzazione alternativa di un test case dettaglio](images/alt-view-of-test-case-detail.png)

-   <span data-ttu-id="ee40e-227">**XML**-Visualizza il codice XML non elaborato generato dal logger XML.</span><span class="sxs-lookup"><span data-stu-id="ee40e-227">**XML**—Displays the raw XML generated by the XML logger.</span></span>
-   <span data-ttu-id="ee40e-228">Ricerca **veloce**: ricerca di testo semplice della visualizzazione corrente nel riquadro **risultati test** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-228">**Quick Find**—Simple text search of the current view in the **Test Results** pane.</span></span>
-   <span data-ttu-id="ee40e-229">**Apri in una nuova finestra**— apre la visualizzazione corrente in una nuova istanza di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ee40e-229">**Open in New Window**—Opens the current view in a new instance of Internet Explorer.</span></span>

### <a name="properties-pane"></a><span data-ttu-id="ee40e-230">Riquadro delle proprietà</span><span class="sxs-lookup"><span data-stu-id="ee40e-230">Properties Pane</span></span>

<span data-ttu-id="ee40e-231">Il riquadro **Proprietà** contiene un elenco di proprietà di automazione interfaccia utente e i valori di proprietà organizzati per tipo di proprietà: **accessibilità generale**, **Identificazione**, **modelli** (pattern di controllo), **stato** e **visibilità**.</span><span class="sxs-lookup"><span data-stu-id="ee40e-231">The **Properties** pane contains a list of UI Automation properties and property values organized by property type: **General Accessibility**, **Identification**, **Patterns** (control patterns), **State**, and **Visibility**.</span></span> <span data-ttu-id="ee40e-232">I valori delle proprietà vengono popolati dinamicamente in base al tipo di controllo dell'oggetto selezionato nel riquadro **dell'albero degli elementi di automazione** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-232">The property values are dynamically populated based on the control type of the object selected in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="ee40e-233">Lo screenshot seguente mostra il riquadro **Proprietà** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-233">The following screen shot shows the **Properties** pane.</span></span>

![riquadro proprietà](images/properties-pane.png)

<span data-ttu-id="ee40e-235">Se il controllo selezionato supporta un pattern di controllo specifico, Visual UIA Verify fornisce la possibilità di chiamare metodi supportati da tale pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="ee40e-235">If the selected control supports a specific control pattern, Visual UIA Verify provides the ability to call methods that are supported by that control pattern.</span></span> <span data-ttu-id="ee40e-236">Ad esempio, il [tipo di controllo Window](uiauto-supportwindowcontroltype.md) supporta il [pattern di controllo Window](uiauto-implementingwindow.md), che dispone di un metodo [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) che può essere richiamato dal riquadro **Proprietà** , come illustrato nello screenshot seguente.</span><span class="sxs-lookup"><span data-stu-id="ee40e-236">For example, the [Window control type](uiauto-supportwindowcontroltype.md) supports the [Window control pattern](uiauto-implementingwindow.md), which has a [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) method that can be invoked from the **Properties** pane, as shown in the following screen shot.</span></span> <span data-ttu-id="ee40e-237">Per altre informazioni, vedere [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ee40e-237">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

![Metodo Close del pattern di controllo Window richiamato dal riquadro proprietà](images/close-invoked-from-properties-pane.png)

<span data-ttu-id="ee40e-239">I comandi disponibili nella barra degli strumenti **Proprietà** includono:</span><span class="sxs-lookup"><span data-stu-id="ee40e-239">Commands available from the **Properties** toolbar include:</span></span>

-   <span data-ttu-id="ee40e-240">**Aggiorna**: consente di aggiornare l'albero delle **Proprietà** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-240">**Refresh**—Refresh the **Properties** tree.</span></span>
-   <span data-ttu-id="ee40e-241">**Espandi tutto**— espande tutti i nodi nella struttura ad albero delle **Proprietà** .</span><span class="sxs-lookup"><span data-stu-id="ee40e-241">**Expand All**—Expands all nodes in the **Properties** tree.</span></span>

 

 




