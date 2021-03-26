---
description: È possibile registrare un elenco di proprietà di visualizzazione contenuto univoco e il modello di layout per il tipo di file o l'elemento.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Registrare un set di visualizzazioni contenuto di proprietà e pattern di layout per un tipo di file o un elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104350801"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a><span data-ttu-id="12075-103">Come registrare un set di visualizzazioni di contenuto univoco di proprietà e pattern di layout per il tipo di file o l'elemento</span><span class="sxs-lookup"><span data-stu-id="12075-103">How to Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item</span></span>

<span data-ttu-id="12075-104">È possibile registrare un elenco di proprietà di visualizzazione contenuto univoco e il modello di layout per il tipo di file o l'elemento.</span><span class="sxs-lookup"><span data-stu-id="12075-104">You can register a unique Content view property list and layout pattern for the file type or item.</span></span> <span data-ttu-id="12075-105">Se il tipo di file o l'elemento è associato anche a un tipo, la registrazione della visualizzazione contenuto specifica del tipo di file o dell'elemento eseguirà l'override della registrazione del tipo.</span><span class="sxs-lookup"><span data-stu-id="12075-105">If your file type or item is also associated with a Kind, the specific Content view registration of the file type or item will override the Kind registration.</span></span> <span data-ttu-id="12075-106">Questo può essere utile se le proprietà più importanti di questo elemento sono diverse da quelle di altri elementi dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="12075-106">This might be useful if the most important properties for this item are different from other items of the same Kind.</span></span> <span data-ttu-id="12075-107">Se non si associa il tipo di file o l'elemento a un tipo di elemento o si registra direttamente la visualizzazione contenuto, il sistema utilizza le informazioni di visualizzazione del contenuto predefinite (archiviate in una chiave del registro di sistema a cui fa riferimento l'ultimo elemento di tutti gli elementi ' array di associazione, HKEY \_ classi \_ radice \\ \* )</span><span class="sxs-lookup"><span data-stu-id="12075-107">If you do not associate your file type or item with an item Kind or directly register the Content view, the system uses the default Content view information (stored in a registry key referenced by the last element in all items' association array, HKEY\_CLASSES\_ROOT\\\*)</span></span>

<span data-ttu-id="12075-108">Prima di registrare un elenco di proprietà personalizzato per il tipo di file, è necessario comprendere la modalità di ricerca e la modalità di visualizzazione dei risultati e i modelli di layout disponibili.</span><span class="sxs-lookup"><span data-stu-id="12075-108">Before registering a custom property list for your file type, you should understand the Search Result mode and Browse mode, and the layout patterns that are available to you.</span></span>

## <a name="instructions"></a><span data-ttu-id="12075-109">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="12075-109">Instructions</span></span>

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a><span data-ttu-id="12075-110">Passaggio 1: informazioni sulla modalità di visualizzazione e visualizzazione dei risultati della ricerca</span><span class="sxs-lookup"><span data-stu-id="12075-110">Step 1: Understanding the Search Result Mode and Browse Mode</span></span>

<span data-ttu-id="12075-111">Per la visualizzazione contenuto è necessario definire un modello di layout e un set di elenchi di proprietà per un elemento in un set di risultati di ricerca (modalità risultato ricerca) e quando si passa a una posizione della shell (modalità Browse).</span><span class="sxs-lookup"><span data-stu-id="12075-111">Content view requires defining a layout pattern and set of property lists for an item in a set of search results (Search result mode), and when browsing to a Shell location (Browse mode).</span></span> <span data-ttu-id="12075-112">È possibile usare gli stessi valori per i risultati della ricerca e l'esplorazione, così come sono `Kind.Music` .</span><span class="sxs-lookup"><span data-stu-id="12075-112">You can use the same values for Search result and Browse, as `Kind.Music` does.</span></span> <span data-ttu-id="12075-113">In alternativa, è possibile definire un elenco di proprietà e/o un modello di layout diverso `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="12075-113">Alternatively, you can define a different property list and/or layout pattern as `Kind.Document` does.</span></span>

<span data-ttu-id="12075-114">Nel caso di `Kind.Document` , gli utenti spesso cercano parole nel testo del documento.</span><span class="sxs-lookup"><span data-stu-id="12075-114">In the case of `Kind.Document`, users often search for words in the text of the document.</span></span> <span data-ttu-id="12075-115">Pertanto, l'inclusione di più testo di esempio nel risultato della ricerca potrebbe essere la scelta migliore.</span><span class="sxs-lookup"><span data-stu-id="12075-115">Therefore, including more sample text in the search result might be the best choice.</span></span> <span data-ttu-id="12075-116">Nell'esempio seguente viene illustrata la visualizzazione contenuto di Esplora `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="12075-116">The following example illustrates the Browse Content view of `Kind.Document`.</span></span>

![sfogliare la visualizzazione contenuto di kind.document](images/content-view/browsecontentviewkinddocument.png)

<span data-ttu-id="12075-118">Poiché gli utenti cercano raramente un particolare testo quando si esplorano i documenti, l'ottimizzazione della scelta delle proprietà e del layout per adattare più risultati della ricerca sullo schermo potrebbe essere la scelta migliore.</span><span class="sxs-lookup"><span data-stu-id="12075-118">Because users are rarely looking for particular text when browsing for documents, optimizing your choice of properties and layout to fit more search results on the screen might be the best choice.</span></span> <span data-ttu-id="12075-119">Lo screenshot seguente illustra la visualizzazione del contenuto di ricerca di `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="12075-119">The following screen shot illustrates the Search Content view of `Kind.Document`.</span></span>

### <a name="step-2-understanding-layout-patterns"></a><span data-ttu-id="12075-120">Passaggio 2: informazioni sui modelli di layout</span><span class="sxs-lookup"><span data-stu-id="12075-120">Step 2: Understanding Layout Patterns</span></span>

<span data-ttu-id="12075-121">Sono disponibili quattro modelli di layout: Alpha, beta, gamma e Delta.</span><span class="sxs-lookup"><span data-stu-id="12075-121">There are four layout patterns: Alpha, Beta, Gamma, and Delta.</span></span>

<span data-ttu-id="12075-122">**Layout alfa**</span><span class="sxs-lookup"><span data-stu-id="12075-122">**Alpha layout**</span></span>

<span data-ttu-id="12075-123">Il modello di layout alfa è ottimizzato per i risultati della ricerca di documenti che contengono estratti.</span><span class="sxs-lookup"><span data-stu-id="12075-123">The Alpha layout pattern is optimized for document search results that contain excerpts.</span></span> <span data-ttu-id="12075-124">Include le specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="12075-124">It has the following specifications:</span></span>

-   <span data-ttu-id="12075-125">Righe: 4</span><span class="sxs-lookup"><span data-stu-id="12075-125">Rows: 4</span></span>
-   <span data-ttu-id="12075-126">Proprietà: 7</span><span class="sxs-lookup"><span data-stu-id="12075-126">Properties: 7</span></span>
-   <span data-ttu-id="12075-127">Layout alfa quando l'elemento ha 350 pixel o più di spazio orizzontale, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="12075-127">Alpha layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![schema di layout Alpha](images/content-view/layout1.png)

-   <span data-ttu-id="12075-129">Nella figura seguente viene illustrato il layout alfa quando l'elemento ha 350 pixel o più di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-129">The following illustration shows the Alpha layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Diagramma che mostra un esempio di layout alfa](images/content-view/alphaviewmore.png)

-   <span data-ttu-id="12075-131">Nella figura seguente viene illustrato il layout alfa quando l'elemento ha meno di 350 pixel di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-131">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Screenshot che mostra un esempio di layout alfa in Microsoft Word.](images/content-view/layout2.png)

-   <span data-ttu-id="12075-133">Nella figura seguente viene illustrato il layout alfa quando l'elemento ha meno di 350 pixel di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-133">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![esempio di layout alfa](images/content-view/alphaviewless.png)

<span data-ttu-id="12075-135">**Layout beta**</span><span class="sxs-lookup"><span data-stu-id="12075-135">**Beta Layout**</span></span>

<span data-ttu-id="12075-136">Il modello di layout beta è ottimizzato per i risultati della ricerca dei documenti di posta elettronica che contengono estratti.</span><span class="sxs-lookup"><span data-stu-id="12075-136">The Beta layout pattern is optimized for email document search results that contain excerpts.</span></span> <span data-ttu-id="12075-137">Include le specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="12075-137">It has the following specifications:</span></span>

-   <span data-ttu-id="12075-138">Righe: 4</span><span class="sxs-lookup"><span data-stu-id="12075-138">Rows: 4</span></span>
-   <span data-ttu-id="12075-139">Proprietà: 5</span><span class="sxs-lookup"><span data-stu-id="12075-139">Properties: 5</span></span>
-   <span data-ttu-id="12075-140">Layout beta quando l'elemento ha 350 pixel o più di spazio orizzontale, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="12075-140">Beta layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Diagramma che mostra un esempio di layout beta.](images/content-view/layout3.png)

-   <span data-ttu-id="12075-142">Nella figura seguente viene illustrato il layout beta quando l'elemento ha 350 pixel o più di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-142">The following illustration shows the beta layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Screenshot che mostra un esempio di layout beta per la posta elettronica.](images/content-view/betaviewmore.png)

-   <span data-ttu-id="12075-144">Nella figura seguente viene illustrato il layout beta quando l'elemento ha meno di 350 pixel di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-144">The following illustration shows the Beta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Diagramma che mostra un esempio di layout beta con meno di 350 pixel di spazio orizzontale.](images/content-view/layout4.png)

-   <span data-ttu-id="12075-146">La figura seguente mostra il layout beta quando l'elemento ha meno di 350 pixel di spazio orizzontale:</span><span class="sxs-lookup"><span data-stu-id="12075-146">The following illustration shows the beta layout when the item has less than 350 pixels of horizontal space:</span></span>

    ![esempio di layout beta](images/content-view/betaviewless.png)

<span data-ttu-id="12075-148">**Layout gamma**</span><span class="sxs-lookup"><span data-stu-id="12075-148">**Gamma Layout**</span></span>

<span data-ttu-id="12075-149">Il modello di layout gamma è simile a alfa ma usa un layout a due righe anziché quattro.</span><span class="sxs-lookup"><span data-stu-id="12075-149">The Gamma layout pattern is similar to Alpha but uses a two-line layout instead of four.</span></span> <span data-ttu-id="12075-150">Questo layout è ideale per gli scenari in cui si desidera visualizzare un frammento, ma si desidera inserire più elementi sullo schermo o per i tipi di file che richiedono meno spazio per visualizzare le informazioni più importanti.</span><span class="sxs-lookup"><span data-stu-id="12075-150">This layout is ideal for scenarios in which you want to see a snippet but want to fit more items on the screen, or for file types that require less space to show the most critical information.</span></span> <span data-ttu-id="12075-151">Il layout gamma presenta le specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="12075-151">The Gamma layout has the following specifications:</span></span>

-   <span data-ttu-id="12075-152">Righe: 2</span><span class="sxs-lookup"><span data-stu-id="12075-152">Rows: 2</span></span>
-   <span data-ttu-id="12075-153">Proprietà: 4</span><span class="sxs-lookup"><span data-stu-id="12075-153">Properties: 4</span></span>
-   <span data-ttu-id="12075-154">La figura seguente mostra il layout gamma quando l'elemento ha 350 pixel o più di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-154">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Diagramma che mostra un esempio di layout gamma.](images/content-view/layout5.png)

-   <span data-ttu-id="12075-156">La figura seguente mostra il layout gamma quando l'elemento ha 350 pixel o più di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-156">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Screenshot che mostra un esempio di layout gamma per un elemento dell'elenco di controllo.](images/content-view/gammaviewmore.png)

-   <span data-ttu-id="12075-158">La figura seguente mostra il layout gamma quando l'elemento ha meno di 350 pixel di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-158">The following illustration shows the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Diagramma che mostra un esempio di layout gamma con meno di 350 pixel di spazio orizzontale.](images/content-view/layout6.png)

-   <span data-ttu-id="12075-160">Esempio di layout gamma quando l'elemento ha meno di 350 pixel di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-160">Example of the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![esempio di layout gamma](images/content-view/gammaviewless.png)

<span data-ttu-id="12075-162">**Layout Delta**</span><span class="sxs-lookup"><span data-stu-id="12075-162">**Delta Layout**</span></span>

<span data-ttu-id="12075-163">Il modello di layout Delta è ottimizzato per la visualizzazione di molte proprietà più brevi, ad esempio per musica e immagini.</span><span class="sxs-lookup"><span data-stu-id="12075-163">The Delta layout pattern is optimized for displaying many shorter properties such as for music and pictures.</span></span> <span data-ttu-id="12075-164">Include le specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="12075-164">It has the following specifications:</span></span>

-   <span data-ttu-id="12075-165">Righe: 2</span><span class="sxs-lookup"><span data-stu-id="12075-165">Rows: 2</span></span>
-   <span data-ttu-id="12075-166">Proprietà: 6</span><span class="sxs-lookup"><span data-stu-id="12075-166">Properties: 6</span></span>
-   <span data-ttu-id="12075-167">Layout Delta quando l'elemento ha 700 pixel o più di spazio orizzontale, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="12075-167">Delta layout when the item has 700 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Diagramma che mostra un esempio di layout Delta.](images/content-view/layout7.png)

-   <span data-ttu-id="12075-169">Esempio di layout Delta quando l'elemento ha 700 pixel o più di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-169">Example of the delta layout when the item has 700 pixels or more of horizontal space.</span></span>

    ![Screenshot che mostra un esempio di layout Delta per un file musicale.](images/content-view/deltalayoutmore.png)

-   <span data-ttu-id="12075-171">Layout Delta quando l'elemento ha una lunghezza compresa tra 350 e 700 pixel di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-171">Delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![Diagramma che mostra un esempio di layout Delta con una lunghezza compresa tra 350 e 700 pixel di spazio orizzontale.](images/content-view/layout8.png)

-   <span data-ttu-id="12075-173">Esempio di layout Delta quando l'elemento ha una lunghezza compresa tra 350 e 700 pixel di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-173">Example of the delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![esempio di layout Delta](images/content-view/deltaviewbetween.png)

-   <span data-ttu-id="12075-175">Layout Delta quando l'elemento ha meno di 350 pixel di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-175">Delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![esempio di layout](images/content-view/layout9.png)

-   <span data-ttu-id="12075-177">Esempio di layout Delta quando l'elemento ha meno di 350 pixel di spazio orizzontale.</span><span class="sxs-lookup"><span data-stu-id="12075-177">Example of the delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Screenshot che mostra un esempio di layout Delta per un file musicale con meno di 350 pixel di spazio orizzontale.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="12075-179">Passaggio 3: registrazione delle proprietà personalizzate e del layout per il tipo di file</span><span class="sxs-lookup"><span data-stu-id="12075-179">Step 3: Registering Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="12075-180">Dopo aver compreso la modalità dei risultati della ricerca, la modalità browse e i modelli di layout, è possibile registrare un elenco di proprietà personalizzato per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="12075-180">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="12075-181">**Per registrare un elenco di proprietà e un modello di layout personalizzati per il tipo di file.**</span><span class="sxs-lookup"><span data-stu-id="12075-181">**To register a custom property list and layout pattern for your file type.**</span></span>

1.  <span data-ttu-id="12075-182">Scegliere tra i quattro modelli di layout: Alpha, beta, gamma o Delta.</span><span class="sxs-lookup"><span data-stu-id="12075-182">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>
2.  <span data-ttu-id="12075-183">Prendere in considerazione le seguenti regole di formattazione che si applicano ugualmente a tutti e quattro i modelli di layout:</span><span class="sxs-lookup"><span data-stu-id="12075-183">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>
    -   <span data-ttu-id="12075-184">La proprietà 1 viene sempre visualizzata in dimensioni maggiori.</span><span class="sxs-lookup"><span data-stu-id="12075-184">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="12075-185">Dimensioni del carattere di grandi dimensioni generalmente utilizzate per il nome dell'elemento, ma possono essere utilizzate anche per la proprietà ancoraggio o altro elemento.</span><span class="sxs-lookup"><span data-stu-id="12075-185">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
    -   <span data-ttu-id="12075-186">La proprietà 4 è destinata agli estratti nei modelli di layout Alpha, beta e gamma.</span><span class="sxs-lookup"><span data-stu-id="12075-186">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="12075-187">Questa proprietà è assegnata più spazio in tali modelli e viene visualizzata in un colore grigio, invece che in nero come le altre proprietà, per consentirne l'emergere.</span><span class="sxs-lookup"><span data-stu-id="12075-187">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
    -   <span data-ttu-id="12075-188">Le misurazioni dei pixel indicate di seguito si trovano in pixel relativi e le dimensioni includono l'icona o l'anteprima a sinistra delle proprietà e lo spazio tra l'icona e l'anteprima e il rettangolo di selezione.</span><span class="sxs-lookup"><span data-stu-id="12075-188">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
    -   <span data-ttu-id="12075-189">La maggior parte delle proprietà ha una dimensione di visualizzazione minima.</span><span class="sxs-lookup"><span data-stu-id="12075-189">Most properties have a minimum display size.</span></span> <span data-ttu-id="12075-190">Pertanto, non verranno visualizzati se lo spazio disponibile non è sufficiente a una determinata dimensione di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="12075-190">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="12075-191">La dimensione minima è in genere di 100 pixel.</span><span class="sxs-lookup"><span data-stu-id="12075-191">The minimum size is usually 100 pixels wide.</span></span>
    -   <span data-ttu-id="12075-192">Ogni schema di layout definisce il numero di righe e il numero di proprietà in ogni riga.</span><span class="sxs-lookup"><span data-stu-id="12075-192">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>
3.  <span data-ttu-id="12075-193">Decidere quali proprietà si desidera visualizzare nel layout e quale proprietà si desidera visualizzare in ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="12075-193">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="12075-194">Quando si decide quale proprietà visualizzare in ogni posizione nel layout, prendere in considerazione la lunghezza tipica della proprietà, la sua importanza per l'utente e se deve essere eliminata quando la dimensione della finestra è troppo piccola per contenere tutte le proprietà.</span><span class="sxs-lookup"><span data-stu-id="12075-194">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>
4.  <span data-ttu-id="12075-195">Registrare un modello di layout e un elenco di proprietà per il tipo di file o per il tipo di elemento aggiungendo le seguenti chiavi sotto la chiave del registro di sistema ProgID per il tipo di file o l'elemento (in questo esempio, per il tipo di file xyz).</span><span class="sxs-lookup"><span data-stu-id="12075-195">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  <span data-ttu-id="12075-196">Osservare le linee guida di formattazione seguenti per la registrazione delle proprietà:</span><span class="sxs-lookup"><span data-stu-id="12075-196">Observe the following formatting guidelines for registering properties:</span></span>

    -   <span data-ttu-id="12075-197">Ogni registrazione inizia con `prop:`</span><span class="sxs-lookup"><span data-stu-id="12075-197">Each registration starts with `prop:`</span></span>
    -   <span data-ttu-id="12075-198">Ogni proprietà richiede il nome completo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="12075-198">Each property requires the full property name.</span></span>
    -   <span data-ttu-id="12075-199">Le proprietà sono separate da un punto e virgola senza spazio.</span><span class="sxs-lookup"><span data-stu-id="12075-199">Properties are separated by a semicolon with no space.</span></span>
    -   <span data-ttu-id="12075-200">Le proprietà vengono visualizzate nell'ordine definito dal modello di layout selezionato.</span><span class="sxs-lookup"><span data-stu-id="12075-200">Properties are displayed in the order defined by the selected layout pattern.</span></span>
    -   <span data-ttu-id="12075-201">`~` indica che l'etichetta della proprietà non deve essere visualizzata.</span><span class="sxs-lookup"><span data-stu-id="12075-201">`~` indicates that the property label should not be displayed.</span></span>
    -   <span data-ttu-id="12075-202">`~System.LayoutPattern.PlaceHolder` usare se si vuole lasciare vuota una proprietà specificata nel modello di layout.</span><span class="sxs-lookup"><span data-stu-id="12075-202">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

    <span data-ttu-id="12075-203">La chiave del registro di sistema di esempio seguente illustra queste linee guida per la formattazione.</span><span class="sxs-lookup"><span data-stu-id="12075-203">The following sample registry key illustrates these formatting guidelines.</span></span>

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    <span data-ttu-id="12075-204">I valori possibili per (ContentViewModeForBrowse) includono i seguenti: prop: ~ System. ItemNameDisplay; System. Author; System. LayoutPattern. segnaposto; System. Keywords; System. DateModified; ~ System. size</span><span class="sxs-lookup"><span data-stu-id="12075-204">Possible values for (ContentViewModeForBrowse) include the following: prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified; ~System.Size</span></span>

## <a name="remarks"></a><span data-ttu-id="12075-205">Commenti</span><span class="sxs-lookup"><span data-stu-id="12075-205">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="12075-206">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12075-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12075-207">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="12075-207">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="12075-208">Nomi dei tipi</span><span class="sxs-lookup"><span data-stu-id="12075-208">Kind Names</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="12075-209">System. Propin. ContentViewModeForBrowse</span><span class="sxs-lookup"><span data-stu-id="12075-209">System.PropList.ContentViewModeForBrowse</span></span>](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[<span data-ttu-id="12075-210">System. Propin. ContentViewModeForSearch</span><span class="sxs-lookup"><span data-stu-id="12075-210">System.PropList.ContentViewModeForSearch</span></span>](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
