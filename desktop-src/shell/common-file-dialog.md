---
description: A partire da Windows Vista, la finestra di dialogo elemento comune sostituisce la finestra di dialogo file comune precedente quando viene usata per aprire o salvare un file.
title: Finestra di dialogo elemento comune
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 896514779b2ba3d11d3db0551f82e21f1d4120b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342846"
---
# <a name="common-item-dialog"></a><span data-ttu-id="35d3b-103">Finestra di dialogo elemento comune</span><span class="sxs-lookup"><span data-stu-id="35d3b-103">Common Item Dialog</span></span>

<span data-ttu-id="35d3b-104">A partire da Windows Vista, la finestra di dialogo elemento comune sostituisce la finestra di dialogo file comune precedente quando viene usata per aprire o salvare un file.</span><span class="sxs-lookup"><span data-stu-id="35d3b-104">Starting with Windows Vista, the Common Item Dialog supersedes the older Common File Dialog when used to open or save a file.</span></span> <span data-ttu-id="35d3b-105">La finestra di dialogo elemento comune viene utilizzata in due varianti: la finestra di dialogo **Apri** e la finestra di dialogo **Salva** .</span><span class="sxs-lookup"><span data-stu-id="35d3b-105">The Common Item Dialog is used in two variations: the **Open** dialog and the **Save** dialog.</span></span> <span data-ttu-id="35d3b-106">Queste due finestre di dialogo condividono la maggior parte delle funzionalità, ma ognuna ha i propri metodi univoci.</span><span class="sxs-lookup"><span data-stu-id="35d3b-106">These two dialogs share most of their functionality, but each has its own unique methods.</span></span>

<span data-ttu-id="35d3b-107">Sebbene la versione più recente venga denominata finestra di dialogo elemento comune, la maggior parte della documentazione continua a essere denominata finestra di dialogo file comune.</span><span class="sxs-lookup"><span data-stu-id="35d3b-107">While this newer version is named the Common Item Dialog, it continues to be called the Common File Dialog in most documentation.</span></span> <span data-ttu-id="35d3b-108">A meno che non si occupi specificamente di una versione precedente di Windows, è necessario presupporre che qualsiasi menzione della finestra di dialogo file comune faccia riferimento a questa finestra di dialogo elemento comune.</span><span class="sxs-lookup"><span data-stu-id="35d3b-108">Unless you are dealing specifically with an older version of Windows, you should assume that any mention of the Common File Dialog refers to this Common Item Dialog.</span></span>

<span data-ttu-id="35d3b-109">Gli argomenti seguenti sono descritti di seguito:</span><span class="sxs-lookup"><span data-stu-id="35d3b-109">The following topics are discussed here:</span></span>

-   [<span data-ttu-id="35d3b-110">IFileDialog, IFileOpenDialog e IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="35d3b-110">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [<span data-ttu-id="35d3b-111">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="35d3b-111">Sample Usage</span></span>](#sample-usage)
-   [<span data-ttu-id="35d3b-112">Ascolto degli eventi dalla finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="35d3b-112">Listening to Events from the Dialog</span></span>](#listening-to-events-from-the-dialog)
    -   [<span data-ttu-id="35d3b-113">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="35d3b-113">OnFileOk</span></span>](#onfileok)
    -   [<span data-ttu-id="35d3b-114">OnShareViolation e OnWrite</span><span class="sxs-lookup"><span data-stu-id="35d3b-114">OnShareViolation and OnOverwrite</span></span>](#onshareviolation-and-onoverwrite)
-   [<span data-ttu-id="35d3b-115">Personalizzazione della finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="35d3b-115">Customizing the Dialog</span></span>](#customizing-the-dialog)
    -   [<span data-ttu-id="35d3b-116">Aggiunta di opzioni al pulsante OK</span><span class="sxs-lookup"><span data-stu-id="35d3b-116">Adding Options to the OK Button</span></span>](#adding-options-to-the-ok-button)
    -   [<span data-ttu-id="35d3b-117">Risposta agli eventi nei controlli aggiunti</span><span class="sxs-lookup"><span data-stu-id="35d3b-117">Responding to Events in Added Controls</span></span>](#responding-to-events-in-added-controls)
-   [<span data-ttu-id="35d3b-118">Esempi completi</span><span class="sxs-lookup"><span data-stu-id="35d3b-118">Full Samples</span></span>](#full-samples)
-   [<span data-ttu-id="35d3b-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35d3b-119">Related topics</span></span>](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a><span data-ttu-id="35d3b-120">IFileDialog, IFileOpenDialog e IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="35d3b-120">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>

<span data-ttu-id="35d3b-121">Windows Vista fornisce le implementazioni delle finestre di dialogo **Apri** e **Salva** : CLSID \_ FileOpenDialog e \_ CLSID FileSaveDialog.</span><span class="sxs-lookup"><span data-stu-id="35d3b-121">Windows Vista provides implementations of the **Open** and **Save** dialogs: CLSID\_FileOpenDialog and CLSID\_FileSaveDialog.</span></span> <span data-ttu-id="35d3b-122">Queste finestre di dialogo sono mostrate qui.</span><span class="sxs-lookup"><span data-stu-id="35d3b-122">Those dialog boxes are shown here.</span></span>

![screenshot della finestra di dialogo Apri](images/cid/openfiledialog.png)

![screenshot della finestra di dialogo Salva con nome](images/cid/savefiledialog.png)

<span data-ttu-id="35d3b-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) e [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) ereditano da [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) e condividono gran parte delle relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="35d3b-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) and [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) inherit from [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and share much of their functionality.</span></span> <span data-ttu-id="35d3b-126">Inoltre, la finestra di dialogo **Apri** supporta **IFileOpenDialog** e la finestra di dialogo **Salva** supporta **IFileSaveDialog**.</span><span class="sxs-lookup"><span data-stu-id="35d3b-126">In addition, the **Open** dialog supports **IFileOpenDialog**, and the **Save** dialog supports **IFileSaveDialog**.</span></span>

<span data-ttu-id="35d3b-127">L'implementazione della finestra di dialogo elemento comune presente in Windows Vista offre diversi vantaggi rispetto all'implementazione fornita nelle versioni precedenti:</span><span class="sxs-lookup"><span data-stu-id="35d3b-127">The Common Item Dialog implementation found in Windows Vista provides several advantages over the implementation provided in earlier versions:</span></span>

-   <span data-ttu-id="35d3b-128">Supporta l'uso diretto dello spazio dei nomi della shell tramite [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) invece di usare percorsi di file System.</span><span class="sxs-lookup"><span data-stu-id="35d3b-128">Supports direct use of the Shell namespace through [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) instead of using file system paths.</span></span>
-   <span data-ttu-id="35d3b-129">Consente la personalizzazione semplice della finestra di dialogo, ad esempio l'impostazione dell'etichetta sul pulsante **OK** , senza richiedere una procedura di hook.</span><span class="sxs-lookup"><span data-stu-id="35d3b-129">Enables simple customization of the dialog, such as setting the label on the **OK** button, without requiring a hook procedure.</span></span>
-   <span data-ttu-id="35d3b-130">Supporta una personalizzazione più completa della finestra di dialogo mediante l'aggiunta di un set di controlli basati sui dati che operano senza un modello di finestra di dialogo Win32.</span><span class="sxs-lookup"><span data-stu-id="35d3b-130">Supports more extensive customization of the dialog by the addition of a set of data-driven controls that operate without a Win32 dialog template.</span></span> <span data-ttu-id="35d3b-131">Questo schema di personalizzazione libera il processo chiamante dal layout dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="35d3b-131">This customization scheme frees the calling process from UI layout.</span></span> <span data-ttu-id="35d3b-132">Poiché le modifiche apportate alla progettazione della finestra di dialogo continuano a utilizzare questo modello di dati, l'implementazione della finestra di dialogo non è associata alla versione corrente specifica della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-132">Since any changes to the dialog design continue to use this data model, the dialog implementation is not tied to the specific current version of the dialog.</span></span>
-   <span data-ttu-id="35d3b-133">Supporta la notifica del chiamante degli eventi all'interno della finestra di dialogo, ad esempio la modifica della selezione o il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="35d3b-133">Supports caller notification of events within the dialog, such as selection change or file type change.</span></span> <span data-ttu-id="35d3b-134">Consente inoltre al processo chiamante di associare determinati eventi nella finestra di dialogo, ad esempio l'analisi.</span><span class="sxs-lookup"><span data-stu-id="35d3b-134">Also enables the calling process to hook certain events in the dialog, such as the parsing.</span></span>
-   <span data-ttu-id="35d3b-135">Introduce nuove funzionalità della finestra di dialogo, ad esempio l'aggiunta di posizioni specificate dal chiamante alla barra dei **punti** .</span><span class="sxs-lookup"><span data-stu-id="35d3b-135">Introduces new dialog features such as adding caller-specified places to the **Places** bar.</span></span>
-   <span data-ttu-id="35d3b-136">Nella finestra di dialogo **Salva** gli sviluppatori possono sfruttare le nuove funzionalità dei metadati della shell di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="35d3b-136">In the **Save** dialog, developers can take advantage of new metadata features of the Windows Vista Shell.</span></span>

<span data-ttu-id="35d3b-137">Inoltre, gli sviluppatori possono scegliere di implementare le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="35d3b-137">Additionally, developers can choose to implement the following interfaces:</span></span>

-   <span data-ttu-id="35d3b-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) per ricevere le notifiche degli eventi all'interno della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) to receive notifications of events within the dialog.</span></span>
-   <span data-ttu-id="35d3b-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) per aggiungere controlli alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) to add controls to the dialog.</span></span>
-   <span data-ttu-id="35d3b-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) a ricevere notifiche relative agli eventi nei controlli aggiunti.</span><span class="sxs-lookup"><span data-stu-id="35d3b-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) to be notified of events in those added controls.</span></span>

<span data-ttu-id="35d3b-141">La finestra di dialogo **Apri** o **Salva** restituisce un oggetto [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) o [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) al processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="35d3b-141">The **Open** or **Save** dialog returns an [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) or [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) object to the calling process.</span></span> <span data-ttu-id="35d3b-142">Il chiamante può quindi usare un singolo oggetto **IShellItem** per ottenere un percorso di file System o per aprire un flusso sull'elemento per leggere o scrivere informazioni.</span><span class="sxs-lookup"><span data-stu-id="35d3b-142">The caller can then use an individual **IShellItem** object to get a file system path or to open a stream on the item to read or write information.</span></span>

<span data-ttu-id="35d3b-143">I flag e le opzioni disponibili per i nuovi metodi di finestra di dialogo sono molto simili ai flag **OFN** precedenti trovati nella struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e usati in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="35d3b-143">Flags and options available to the new dialog methods are very similar to the older **OFN** flags found in the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure and used in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="35d3b-144">Molti di essi sono esattamente uguali, ad eccezione del fatto che iniziano con un prefisso FOS.</span><span class="sxs-lookup"><span data-stu-id="35d3b-144">Many of them are exactly the same, except that they begin with an FOS prefix.</span></span> <span data-ttu-id="35d3b-145">L'elenco completo si trova negli argomenti [**IFileDialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) e [**IFileDialog:: SetOption**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) .</span><span class="sxs-lookup"><span data-stu-id="35d3b-145">The complete list can be found in the [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) and [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) topics.</span></span> <span data-ttu-id="35d3b-146">Per impostazione predefinita, le finestre di dialogo **Apri** e **Salva** vengono create con i flag più comuni.</span><span class="sxs-lookup"><span data-stu-id="35d3b-146">**Open** and **Save** dialogs are created by default with the most common flags.</span></span> <span data-ttu-id="35d3b-147">Per la finestra di dialogo **Apri** , questo è (FOS \_ PATHMUSTEXIST \| Fos \_ FILEMUSTEXIST \| Fos \_ NOCHANGEDIR) e per la finestra di dialogo **Salva** è (FOS OVERWRITEPROMPT Fos NOREADONLYRETURN Fos PATHMUSTEXIST \_ \| \_ \| \_ \| Fos \_ NOCHANGEDIR).</span><span class="sxs-lookup"><span data-stu-id="35d3b-147">For the **Open** dialog, this is (FOS\_PATHMUSTEXIST \| FOS\_FILEMUSTEXIST \| FOS\_NOCHANGEDIR) and for the **Save** dialog this is (FOS\_OVERWRITEPROMPT \| FOS\_NOREADONLYRETURN \| FOS\_PATHMUSTEXIST \| FOS\_NOCHANGEDIR).</span></span>

<span data-ttu-id="35d3b-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) e le relative interfacce discendenti ereditano da ed estendono [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span><span class="sxs-lookup"><span data-stu-id="35d3b-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and its descendant interfaces inherit from and extend [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span></span> <span data-ttu-id="35d3b-149">[**Mostra**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) accetta come unico parametro l'handle della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="35d3b-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) takes as its only parameter the handle of the parent window.</span></span> <span data-ttu-id="35d3b-150">Se il valore di **show** viene restituito correttamente, il risultato è valido.</span><span class="sxs-lookup"><span data-stu-id="35d3b-150">If **Show** returns successfully, there is a valid result.</span></span> <span data-ttu-id="35d3b-151">Se restituisce `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , significa che l'utente ha annullato la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-151">If it returns `HRESULT_FROM_WIN32(ERROR_CANCELLED)`, it means the user canceled the dialog.</span></span> <span data-ttu-id="35d3b-152">Potrebbe inoltre restituire legittimamente un altro codice di errore, ad esempio **E \_ OutOfMemory**.</span><span class="sxs-lookup"><span data-stu-id="35d3b-152">It might also legitimately return another error code such as **E\_OUTOFMEMORY**.</span></span>

### <a name="sample-usage"></a><span data-ttu-id="35d3b-153">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="35d3b-153">Sample Usage</span></span>

<span data-ttu-id="35d3b-154">Nelle sezioni seguenti viene illustrato il codice di esempio per un'ampia gamma di attività di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-154">The following sections show example code for a variety of dialog tasks.</span></span>

-   [<span data-ttu-id="35d3b-155">Utilizzo di base</span><span class="sxs-lookup"><span data-stu-id="35d3b-155">Basic Usage</span></span>](#basic-usage)
-   [<span data-ttu-id="35d3b-156">Limitazione dei risultati agli elementi del file System</span><span class="sxs-lookup"><span data-stu-id="35d3b-156">Limiting Results to File System Items</span></span>](#limiting-results-to-file-system-items)
-   [<span data-ttu-id="35d3b-157">Specifica dei tipi di file per una finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="35d3b-157">Specifying File Types for a Dialog</span></span>](#specifying-file-types-for-a-dialog)
-   [<span data-ttu-id="35d3b-158">Controllo della cartella predefinita</span><span class="sxs-lookup"><span data-stu-id="35d3b-158">Controlling the Default Folder</span></span>](#controlling-the-default-folder)
-   [<span data-ttu-id="35d3b-159">Aggiunta di elementi alla barra dei punti</span><span class="sxs-lookup"><span data-stu-id="35d3b-159">Adding Items to the Places Bar</span></span>](#adding-items-to-the-places-bar)
-   [<span data-ttu-id="35d3b-160">Persistenza dello stato</span><span class="sxs-lookup"><span data-stu-id="35d3b-160">State Persistence</span></span>](#state-persistence)
-   [<span data-ttu-id="35d3b-161">Funzionalità MultiSelect</span><span class="sxs-lookup"><span data-stu-id="35d3b-161">Multiselect Capabilities</span></span>](#multiselect-capabilities)

<span data-ttu-id="35d3b-162">La maggior parte del codice di esempio è disponibile nell' [esempio Windows SDK finestra di dialogo file comune](samples-commonfiledialog.md).</span><span class="sxs-lookup"><span data-stu-id="35d3b-162">Most of the sample code can be found in the Windows SDK [Common File Dialog Sample](samples-commonfiledialog.md).</span></span>

### <a name="basic-usage"></a><span data-ttu-id="35d3b-163">Utilizzo di base</span><span class="sxs-lookup"><span data-stu-id="35d3b-163">Basic Usage</span></span>

<span data-ttu-id="35d3b-164">Nell'esempio seguente viene illustrato come avviare una finestra di dialogo **aperta** .</span><span class="sxs-lookup"><span data-stu-id="35d3b-164">The following example illustrates how to launch an **Open** dialog.</span></span> <span data-ttu-id="35d3b-165">In questo esempio è limitato ai documenti di Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="35d3b-165">In this example, it is restricted to Microsoft Word documents.</span></span>

> [!Note]  
> <span data-ttu-id="35d3b-166">Molti esempi in questo argomento usano la `CDialogEventHandler_CreateInstance` funzione helper per creare un'istanza dell'implementazione di [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) .</span><span class="sxs-lookup"><span data-stu-id="35d3b-166">Several examples in this topic use the `CDialogEventHandler_CreateInstance` helper function to create an instance of the [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) implementation.</span></span> <span data-ttu-id="35d3b-167">Per usare questa funzione nel codice, copiare il codice sorgente per la `CDialogEventHandler_CreateInstance` funzione dall' [esempio di finestra di dialogo file comune](samples-commonfiledialog.md), da cui vengono presi tutti gli esempi in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="35d3b-167">To use this function in your own code, copy the source code for the `CDialogEventHandler_CreateInstance` function from the [Common File Dialog Sample](samples-commonfiledialog.md), from which all of the examples in this topic are taken.</span></span>

 


```C++
HRESULT BasicFileOpen()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
                    if (SUCCEEDED(hr))
                    {
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
                                if (SUCCEEDED(hr))
                                {
                                    // Show the dialog
                                    hr = pfd->Show(NULL);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Obtain the result once the user clicks 
                                        // the 'Open' button.
                                        // The result is an IShellItem object.
                                        IShellItem *psiResult;
                                        hr = pfd->GetResult(&psiResult);
                                        if (SUCCEEDED(hr))
                                        {
                                            // We are just going to print out the 
                                            // name of the file for sample sake.
                                            PWSTR pszFilePath = NULL;
                                            hr = psiResult->GetDisplayName(SIGDN_FILESYSPATH, 
                                                               &pszFilePath);
                                            if (SUCCEEDED(hr))
                                            {
                                                TaskDialog(NULL,
                                                           NULL,
                                                           L"CommonFileDialogApp",
                                                           pszFilePath,
                                                           NULL,
                                                           TDCBF_OK_BUTTON,
                                                           TD_INFORMATION_ICON,
                                                           NULL);
                                                CoTaskMemFree(pszFilePath);
                                            }
                                            psiResult->Release();
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="limiting-results-to-file-system-items"></a><span data-ttu-id="35d3b-168">Limitazione dei risultati agli elementi del file System</span><span class="sxs-lookup"><span data-stu-id="35d3b-168">Limiting Results to File System Items</span></span>

<span data-ttu-id="35d3b-169">Nell'esempio seguente, tratto dalla precedente, viene illustrato come limitare i risultati agli elementi file system.</span><span class="sxs-lookup"><span data-stu-id="35d3b-169">The following example, taken from above, demonstrates how to restrict results to file system items.</span></span> <span data-ttu-id="35d3b-170">Si noti che [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) aggiunge il nuovo flag a un valore ottenuto tramite [**IFileDialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span><span class="sxs-lookup"><span data-stu-id="35d3b-170">Note that [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) adds the new flag to a value obtained through [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span></span> <span data-ttu-id="35d3b-171">Questo è il metodo consigliato.</span><span class="sxs-lookup"><span data-stu-id="35d3b-171">This is the recommended method.</span></span>


```C++
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
```



### <a name="specifying-file-types-for-a-dialog"></a><span data-ttu-id="35d3b-172">Specifica dei tipi di file per una finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="35d3b-172">Specifying File Types for a Dialog</span></span>

<span data-ttu-id="35d3b-173">Per impostare tipi di file specifici che la finestra di dialogo è in grado di gestire, usare il metodo [**IFileDialog:: Setypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) .</span><span class="sxs-lookup"><span data-stu-id="35d3b-173">To set specific file types that the dialog can handle, use the [**IFileDialog::SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) method.</span></span> <span data-ttu-id="35d3b-174">Tale metodo accetta una matrice di [**strutture \_ FILTERSPEC di COMDLG**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) , ognuna delle quali rappresenta un tipo di file.</span><span class="sxs-lookup"><span data-stu-id="35d3b-174">That method accepts an array of [**COMDLG\_FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) structures, each of which represents a file type.</span></span>

<span data-ttu-id="35d3b-175">Il meccanismo di estensione predefinito in una finestra di dialogo è invariato da [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="35d3b-175">The default extension mechanism in a dialog is unchanged from [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="35d3b-176">L'estensione del nome file aggiunta al testo che l'utente digita nella casella di modifica nome file viene inizializzata all'apertura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-176">The file name extension that is appended to the text the user types in the file name edit box is initialized when the dialog opens.</span></span> <span data-ttu-id="35d3b-177">Deve corrispondere al tipo di file predefinito (selezionato quando viene visualizzata la finestra di dialogo).</span><span class="sxs-lookup"><span data-stu-id="35d3b-177">It should match the default file type (that selected as the dialog opens).</span></span> <span data-ttu-id="35d3b-178">Se il tipo di file predefinito è " \* . \* " (tutti i file), il file può essere un'estensione di propria scelta.</span><span class="sxs-lookup"><span data-stu-id="35d3b-178">If the default file type is "\*.\*" (all files), the file can be an extension of your choice.</span></span> <span data-ttu-id="35d3b-179">Se l'utente sceglie un tipo di file diverso, l'estensione viene aggiornata automaticamente alla prima estensione del nome file associata al tipo di file.</span><span class="sxs-lookup"><span data-stu-id="35d3b-179">If the user chooses a different file type, the extension automatically updates to the first file name extension associated with that file type.</span></span> <span data-ttu-id="35d3b-180">Se l'utente sceglie " \* . \* " (tutti i file), quindi l'estensione ripristina il valore originale.</span><span class="sxs-lookup"><span data-stu-id="35d3b-180">If the user chooses "\*.\*" (all files), then the extension reverts to its original value.</span></span>

<span data-ttu-id="35d3b-181">L'esempio seguente illustra come questa operazione è stata eseguita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="35d3b-181">The following example illustrates how this was done above.</span></span>


```C++
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
```



### <a name="controlling-the-default-folder"></a><span data-ttu-id="35d3b-182">Controllo della cartella predefinita</span><span class="sxs-lookup"><span data-stu-id="35d3b-182">Controlling the Default Folder</span></span>

<span data-ttu-id="35d3b-183">È possibile usare quasi tutte le cartelle dello spazio dei nomi della shell come cartella predefinita per la finestra di dialogo (la cartella visualizzata quando l'utente sceglie di aprire o salvare un file).</span><span class="sxs-lookup"><span data-stu-id="35d3b-183">Almost any folder in the Shell namespace can be used as the default folder for the dialog (the folder presented when the user chooses to open or save a file).</span></span> <span data-ttu-id="35d3b-184">Chiamare [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) prima di chiamare [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-184">Call [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) to do so.</span></span>

<span data-ttu-id="35d3b-185">La cartella predefinita è la cartella in cui viene avviata la finestra di dialogo la prima volta che l'utente apre l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35d3b-185">The default folder is the folder in which the dialog starts the first time a user opens it from your application.</span></span> <span data-ttu-id="35d3b-186">Successivamente, la finestra di dialogo si aprirà nell'ultima cartella aperta da un utente o nell'ultima cartella utilizzata per salvare un elemento.</span><span class="sxs-lookup"><span data-stu-id="35d3b-186">After that, the dialog will open in the last folder a user opened or the last folder they used to save an item.</span></span> <span data-ttu-id="35d3b-187">Per ulteriori informazioni, vedere [persistenza dello stato](#state-persistence) .</span><span class="sxs-lookup"><span data-stu-id="35d3b-187">See [State Persistence](#state-persistence) for more details.</span></span>

<span data-ttu-id="35d3b-188">È possibile forzare la visualizzazione della finestra di dialogo per visualizzare sempre la stessa cartella quando si apre, indipendentemente dall'azione dell'utente precedente, chiamando [**IFileDialog:: fileFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span><span class="sxs-lookup"><span data-stu-id="35d3b-188">You can force the dialog to always show the same folder when it opens, regardless of previous user action, by calling [**IFileDialog::SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span></span> <span data-ttu-id="35d3b-189">Tuttavia, questa operazione non è consigliata.</span><span class="sxs-lookup"><span data-stu-id="35d3b-189">However, we do not recommended doing this.</span></span> <span data-ttu-id="35d3b-190">Se si chiama la **cartella fileFolder** prima di visualizzare la finestra di dialogo, non viene visualizzata la posizione più recente da cui l'utente ha salvato o aperto.</span><span class="sxs-lookup"><span data-stu-id="35d3b-190">If you call **SetFolder** before you display the dialog box, the most recent location that the user saved to or opened from is not shown.</span></span> <span data-ttu-id="35d3b-191">A meno che non esista un motivo molto specifico per questo comportamento, non si tratta di un'esperienza utente buona o prevista e deve essere evitata.</span><span class="sxs-lookup"><span data-stu-id="35d3b-191">Unless there is a very specific reason for this behavior, it is not a good or expected user experience and should be avoided.</span></span> <span data-ttu-id="35d3b-192">In quasi tutte le istanze, [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) è il metodo migliore.</span><span class="sxs-lookup"><span data-stu-id="35d3b-192">In almost all instances, [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) is the better method.</span></span>

<span data-ttu-id="35d3b-193">Quando si salva un documento per la prima volta nella finestra di dialogo **Salva** , è necessario seguire le stesse linee guida per determinare la cartella iniziale come è stato fatto nella finestra di dialogo **Apri** .</span><span class="sxs-lookup"><span data-stu-id="35d3b-193">When saving a document for the first time in the **Save** dialog, you should follow the same guidelines in determining the initial folder as you did in the **Open** dialog.</span></span> <span data-ttu-id="35d3b-194">Se l'utente sta modificando un documento esistente in precedenza, aprire la finestra di dialogo nella cartella in cui è archiviato il documento e popolare la casella di modifica con il nome del documento.</span><span class="sxs-lookup"><span data-stu-id="35d3b-194">If the user is editing a previously existing document, open the dialog in the folder where that document is stored, and populate the edit box with that document's name.</span></span> <span data-ttu-id="35d3b-195">Chiamare [**IFileSaveDialog:: SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) con l'elemento corrente prima di chiamare [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span><span class="sxs-lookup"><span data-stu-id="35d3b-195">Call [**IFileSaveDialog::SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) with the current item prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span></span>

### <a name="adding-items-to-the-places-bar"></a><span data-ttu-id="35d3b-196">Aggiunta di elementi alla barra dei punti</span><span class="sxs-lookup"><span data-stu-id="35d3b-196">Adding Items to the Places Bar</span></span>

<span data-ttu-id="35d3b-197">Nell'esempio seguente viene illustrata l'aggiunta di elementi alla barra dei **punti** :</span><span class="sxs-lookup"><span data-stu-id="35d3b-197">The following example demonstrates the addition of items to the **Places** bar:</span></span>


```C++
HRESULT AddItemsToCommonPlaces()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Always use known folders instead of hard-coding physical file paths.
        // In this case we are using Public Music KnownFolder.
        IKnownFolderManager *pkfm = NULL;
        hr = CoCreateInstance(CLSID_KnownFolderManager, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pkfm));
        if (SUCCEEDED(hr))
        {
            // Get the known folder.
            IKnownFolder *pKnownFolder = NULL;
            hr = pkfm->GetFolder(FOLDERID_PublicMusic, &pKnownFolder);
            if (SUCCEEDED(hr))
            {
                // File Dialog APIs need an IShellItem that represents the location.
                IShellItem *psi = NULL;
                hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                if (SUCCEEDED(hr))
                {
                    // Add the place to the bottom of default list in Common File Dialog.
                    hr = pfd->AddPlace(psi, FDAP_BOTTOM);
                    if (SUCCEEDED(hr))
                    {
                        // Show the File Dialog.
                        hr = pfd->Show(NULL);
                        if (SUCCEEDED(hr))
                        {
                            //
                            // You can add your own code here to handle the results.
                            //
                        }
                    }
                    psi->Release();
                }
                pKnownFolder->Release();
            }
            pkfm->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="state-persistence"></a><span data-ttu-id="35d3b-198">Persistenza dello stato</span><span class="sxs-lookup"><span data-stu-id="35d3b-198">State Persistence</span></span>

<span data-ttu-id="35d3b-199">Prima di Windows Vista, uno stato, ad esempio l'ultima cartella visitata, veniva salvato in base ai singoli processi.</span><span class="sxs-lookup"><span data-stu-id="35d3b-199">Prior to Windows Vista, a state, such as the last visited folder, was saved on a per-process basis.</span></span> <span data-ttu-id="35d3b-200">Tuttavia, tali informazioni venivano utilizzate indipendentemente dall'azione specifica.</span><span class="sxs-lookup"><span data-stu-id="35d3b-200">However, that information was used regardless of the particular action.</span></span> <span data-ttu-id="35d3b-201">Ad esempio, un'applicazione di modifica video presenta la stessa cartella nella finestra di dialogo **Render As** come si farebbe nella finestra di dialogo **Importa supporti** .</span><span class="sxs-lookup"><span data-stu-id="35d3b-201">For example, a video editing application would present the same folder in the **Render As** dialog as is would in the **Import Media** dialog.</span></span> <span data-ttu-id="35d3b-202">In Windows Vista è possibile essere più specifici tramite l'uso di GUID.</span><span class="sxs-lookup"><span data-stu-id="35d3b-202">In Windows Vista you can be more specific through the use of GUIDs.</span></span> <span data-ttu-id="35d3b-203">Per assegnare un **GUID** alla finestra di dialogo, chiamare [**IFileDialog:: SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span><span class="sxs-lookup"><span data-stu-id="35d3b-203">To assign a **GUID** to the dialog, call [**iFileDialog::SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span></span>

### <a name="multiselect-capabilities"></a><span data-ttu-id="35d3b-204">Funzionalità MultiSelect</span><span class="sxs-lookup"><span data-stu-id="35d3b-204">Multiselect Capabilities</span></span>

<span data-ttu-id="35d3b-205">La funzionalità MultiSelect è disponibile nella finestra di dialogo **Apri** usando il metodo [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="35d3b-205">Multiselect functionality is available in the **Open** dialog using the [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) method as shown here.</span></span>


```C++
HRESULT MultiselectInvoke()
{
    IFileOpenDialog *pfd;
    
    // CoCreate the dialog object.
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));

    if (SUCCEEDED(hr))
    {
        DWORD dwOptions;
        // Specify multiselect.
        hr = pfd->GetOptions(&dwOptions);
        
        if (SUCCEEDED(hr))
        {
            hr = pfd->SetOptions(dwOptions | FOS_ALLOWMULTISELECT);
        }

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog.
            hr = pfd->Show(NULL);

            if (SUCCEEDED(hr))
            {
                // Obtain the result of the user interaction.
                IShellItemArray *psiaResults;
                hr = pfd->GetResults(&psiaResults);
                
                if (SUCCEEDED(hr))
                {
                    //
                    // You can add your own code here to handle the results.
                    //
                    psiaResults->Release();
                }
            }
        }
        pfd->Release();
    }
    return hr;
}
```



## <a name="listening-to-events-from-the-dialog"></a><span data-ttu-id="35d3b-206">Ascolto degli eventi dalla finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="35d3b-206">Listening to Events from the Dialog</span></span>

<span data-ttu-id="35d3b-207">Un processo chiamante può registrare un'interfaccia [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) con la finestra di dialogo usando i metodi [**IFileDialog:: Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) e [**IFileDialog:: Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) , come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="35d3b-207">A calling process can register an [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) interface with the dialog by using the [**IFileDialog::Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) and [**IFileDialog::Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) methods as shown here.</span></span>

<span data-ttu-id="35d3b-208">Questa operazione è ricavata dall'esempio di [utilizzo di base](#basic-usage) .</span><span class="sxs-lookup"><span data-stu-id="35d3b-208">This is taken from the [Basic Usage](#basic-usage) sample.</span></span>


```C++
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
```



<span data-ttu-id="35d3b-209">La maggior parte dell'elaborazione del dialogo viene effettuata qui.</span><span class="sxs-lookup"><span data-stu-id="35d3b-209">The bulk of the dialog processing would be placed here.</span></span>


```C++
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



<span data-ttu-id="35d3b-210">Il processo chiamante può utilizzare gli eventi per la notifica quando l'utente modifica la cartella, il tipo di file o la selezione.</span><span class="sxs-lookup"><span data-stu-id="35d3b-210">The calling process can use events for notification when the user changes the folder, file type, or selection.</span></span> <span data-ttu-id="35d3b-211">Questi eventi sono particolarmente utili quando il processo chiamante ha aggiunto controlli alla finestra di dialogo (vedere [personalizzazione della finestra di dialogo](#customizing-the-dialog)) e deve modificare lo stato di tali controlli in risposta a questi eventi.</span><span class="sxs-lookup"><span data-stu-id="35d3b-211">These events are particularly useful when the calling process has added controls to the dialog (see [Customizing the Dialog](#customizing-the-dialog)) and must change the state of those controls in reaction to these events.</span></span> <span data-ttu-id="35d3b-212">Utile in tutti i casi è la capacità del processo chiamante di fornire codice personalizzato per gestire situazioni quali la condivisione di violazioni, la sovrascrittura dei file o la determinazione di un file valido prima della chiusura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-212">Useful in all cases is the ability of the calling process to provide custom code to deal with situations such as sharing violations, overwriting files, or determining if a file is valid before the dialog closes.</span></span> <span data-ttu-id="35d3b-213">Alcuni di questi casi sono descritti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="35d3b-213">Some of those cases are described in this section.</span></span>

### <a name="onfileok"></a><span data-ttu-id="35d3b-214">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="35d3b-214">OnFileOk</span></span>

<span data-ttu-id="35d3b-215">Questo metodo viene chiamato dopo che l'utente sceglie un elemento, immediatamente prima della chiusura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-215">This method is called after the user chooses an item, just before the dialog closes.</span></span> <span data-ttu-id="35d3b-216">L'applicazione può quindi chiamare [**IFileDialog:: GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) o [**IFileOpenDialog:: GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) come verrebbe eseguita dopo la chiusura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-216">The application can then call [**IFileDialog::GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) or [**IFileOpenDialog::GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) as would be done once the dialog had closed.</span></span> <span data-ttu-id="35d3b-217">Se l'elemento scelto è accettabile, può restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35d3b-217">If the item chosen is acceptable, they can return S\_OK.</span></span> <span data-ttu-id="35d3b-218">In caso contrario, restituiscono S \_ false e visualizzano l'interfaccia utente che indica all'utente il motivo per cui l'elemento scelto non è valido.</span><span class="sxs-lookup"><span data-stu-id="35d3b-218">Otherwise, they return S\_FALSE and display UI that tells the user why the chosen item is not valid.</span></span> <span data-ttu-id="35d3b-219">Se \_ viene restituito S false, la finestra di dialogo non viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="35d3b-219">If S\_FALSE is returned, the dialog does not close.</span></span>

<span data-ttu-id="35d3b-220">Il processo chiamante può utilizzare l'handle di finestra del dialogo stesso come elemento padre dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="35d3b-220">The calling process can use the window handle of the dialog itself as the parent of the UI.</span></span> <span data-ttu-id="35d3b-221">Tale handle può essere ottenuto chiamando prima [**IOleWindow:: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) e chiamando [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) con l'handle, come illustrato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="35d3b-221">That handle can be obtained by first calling [**IOleWindow::QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) and then calling [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) with the handle as shown in this example.</span></span>


```C++
HRESULT CDialogEventHandler::OnFileOk(IFileDialog *pfd) 
{ 
    IShellItem *psiResult;
    HRESULT hr = pfd->GetResult(&psiResult);
    
    if (SUCCEEDED(hr))
    {
        SFGAOF attributes;
        hr = psiResult->GetAttributes(SFGAO_COMPRESSED, &attributes);
    
        if (SUCCEEDED(hr))
        {
            if (attributes & SFGAO_COMPRESSED)
            {
                // Accept the file.
                hr = S_OK;
            }
            else
            {
                // Refuse the file.
                hr = S_FALSE;
                
                _DisplayMessage(pfd, L"Not a compressed file.");
            }
        }
        psiResult->Release();
    }
    return hr;
};

HRESULT CDialogEventHandler::_DisplayMessage(IFileDialog *pfd, PCWSTR pszMessage)
{
    IOleWindow *pWindow;
    HRESULT hr = pfd->QueryInterface(IID_PPV_ARGS(&pWindow));
    
    if (SUCCEEDED(hr))
    {
        HWND hwndDialog;
        hr = pWindow->GetWindow(&hwndDialog);
    
        if (SUCCEEDED(hr))
        {
            MessageBox(hwndDialog, pszMessage, L"An error has occurred", MB_OK);
        }
        pWindow->Release();
    }
    return hr;
}
```



### <a name="onshareviolation-and-onoverwrite"></a><span data-ttu-id="35d3b-222">OnShareViolation e OnWrite</span><span class="sxs-lookup"><span data-stu-id="35d3b-222">OnShareViolation and OnOverwrite</span></span>

<span data-ttu-id="35d3b-223">Se l'utente sceglie di sovrascrivere un file nella finestra di dialogo **Salva** o se un file salvato o sostituito è in uso e non può essere scritto in una violazione di condivisione, l'applicazione può fornire funzionalità personalizzate per ignorare il comportamento predefinito della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-223">If the user chooses to overwrite a file in the **Save** dialog, or if a file being saved or replaced is in use and cannot be written to (a sharing violation), the application can provide custom functionality to override the default behavior of the dialog.</span></span> <span data-ttu-id="35d3b-224">Per impostazione predefinita, quando si sovrascrive un file, nella finestra di dialogo viene visualizzato un prompt che consente all'utente di verificare l'azione.</span><span class="sxs-lookup"><span data-stu-id="35d3b-224">By default, when overwriting a file, the dialog displays a prompt allowing the user to verify this action.</span></span> <span data-ttu-id="35d3b-225">Per le violazioni di condivisione, per impostazione predefinita nella finestra di dialogo viene visualizzato un messaggio di errore, non viene chiuso e l'utente deve effettuare un'altra scelta.</span><span class="sxs-lookup"><span data-stu-id="35d3b-225">For sharing violations, by default the dialog displays an error message, it does not close, and the user is required to make another choice.</span></span> <span data-ttu-id="35d3b-226">Il processo chiamante può eseguire l'override di queste impostazioni predefinite e visualizzare la propria interfaccia utente, se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="35d3b-226">The calling process can override these defaults and display its own UI if desired.</span></span> <span data-ttu-id="35d3b-227">È possibile indicare alla finestra di dialogo di rifiutare il file e rimanere aperti o accettare il file e chiuderlo correttamente.</span><span class="sxs-lookup"><span data-stu-id="35d3b-227">The dialog can be instructed to refuse the file and remain open or accept the file and close successfully.</span></span>

## <a name="customizing-the-dialog"></a><span data-ttu-id="35d3b-228">Personalizzazione della finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="35d3b-228">Customizing the Dialog</span></span>

<span data-ttu-id="35d3b-229">È possibile aggiungere una serie di controlli alla finestra di dialogo senza specificare un modello di finestra di dialogo Win32.</span><span class="sxs-lookup"><span data-stu-id="35d3b-229">A variety of controls can be added to the dialog without supplying a Win32 dialog template.</span></span> <span data-ttu-id="35d3b-230">Questi controlli includono pulsanti, ComboBox, casella, CheckButton, elenchi di RadioButton, gruppi, separatori e controlli di testo statici.</span><span class="sxs-lookup"><span data-stu-id="35d3b-230">These controls include PushButton, ComboBox, EditBox, CheckButton, RadioButton lists, Groups, Separators, and Static Text controls.</span></span> <span data-ttu-id="35d3b-231">Chiamare **QueryInterface** sull'oggetto finestra di dialogo ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)o [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) per ottenere un puntatore [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) .</span><span class="sxs-lookup"><span data-stu-id="35d3b-231">Call **QueryInterface** on the dialog object ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), or [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) to obtain an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer.</span></span> <span data-ttu-id="35d3b-232">Usare tale interfaccia per aggiungere controlli.</span><span class="sxs-lookup"><span data-stu-id="35d3b-232">Use that interface to add controls.</span></span> <span data-ttu-id="35d3b-233">A ogni controllo è associato un ID fornito dal chiamante, nonché uno stato *visibile* e *abilitato* che può essere impostato dal processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="35d3b-233">Each control has an associated caller-supplied ID as well as a *visible* and *enabled* state that can be set by the calling process.</span></span> <span data-ttu-id="35d3b-234">Alcuni controlli, ad esempio il pulsante, hanno anche testo associato.</span><span class="sxs-lookup"><span data-stu-id="35d3b-234">Some controls, such as PushButton, also have text associated with them.</span></span>

<span data-ttu-id="35d3b-235">È possibile aggiungere più controlli in un "gruppo visivo" che si sposta come una singola unità nel layout della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-235">Multiple controls can be added into a "visual group" that moves as a single unit in the layout of the dialog.</span></span> <span data-ttu-id="35d3b-236">Ai gruppi può essere associata un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="35d3b-236">Groups can have a label associated with them.</span></span>

<span data-ttu-id="35d3b-237">I controlli possono essere aggiunti solo prima che venga visualizzata la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-237">Controls can be added only before the dialog is shown.</span></span> <span data-ttu-id="35d3b-238">Tuttavia, una volta visualizzata la finestra di dialogo, i controlli possono essere nascosti o visualizzati in base alle esigenze, forse in risposta all'azione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="35d3b-238">However, once the dialog is displayed, controls can be hidden or shown as desired, perhaps in response to user action.</span></span> <span data-ttu-id="35d3b-239">Gli esempi seguenti illustrano come aggiungere un elenco di pulsanti di opzione alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-239">The following examples show how to add a radio button list to the dialog.</span></span>


```C++
// Controls
#define CONTROL_GROUP           2000
#define CONTROL_RADIOBUTTONLIST 2
#define CONTROL_RADIOBUTTON1    1
#define CONTROL_RADIOBUTTON2    2       // It is OK for this to have the same ID
                    // as CONTROL_RADIOBUTTONLIST, because it 
                    // is a child control under CONTROL_RADIOBUTTONLIST


// This code snippet demonstrates how to add custom controls in the Common File Dialog.
HRESULT AddCustomControls()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    // Create a Visual Group.
                    hr = pfdc->StartVisualGroup(CONTROL_GROUP, L&quot;Sample Group&quot;);
                    if (SUCCEEDED(hr))
                    {
                        // Add a radio-button list.
                        hr = pfdc->AddRadioButtonList(CONTROL_RADIOBUTTONLIST);
                        if (SUCCEEDED(hr))
                        {
                            // Set the state of the added radio-button list.
                            hr = pfdc->SetControlState(CONTROL_RADIOBUTTONLIST, 
                                               CDCS_VISIBLE | CDCS_ENABLED);
                            if (SUCCEEDED(hr))
                            {
                                // Add individual buttons to the radio-button list.
                                hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                          CONTROL_RADIOBUTTON1,
                                                          L&quot;Change Title to ABC&quot;);
                                if (SUCCEEDED(hr))
                                {
                                    hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                              CONTROL_RADIOBUTTON2,
                                                              L&quot;Change Title to XYZ&quot;);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Set the default selection to option 1.
                                        hr = pfdc->SetSelectedControlItem(CONTROL_RADIOBUTTONLIST,
                                                                          CONTROL_RADIOBUTTON1);
                                    }
                                }
                            }
                        }
                        // End the visual group.
                        pfdc->EndVisualGroup();
                    }
                    pfdc->Release();
                }

                if (FAILED(hr))
                {
                    // Unadvise here in case we encounter failures 
                    // before we get a chance to show the dialog.
                    pfd->Unadvise(dwCookie);
                }
            }
            pfde->Release();
        }

        if (SUCCEEDED(hr))
        {
            // Now show the dialog.
            hr = pfd->Show(NULL);
            if (SUCCEEDED(hr))
            {
                //
                // You can add your own code here to handle the results.
                //
            }
            // Unhook the event handler.
            pfd->Unadvise(dwCookie);
        }
        pfd->Release();
    }
    return hr;
}
```





### <a name="adding-options-to-the-ok-button"></a><span data-ttu-id="35d3b-240">Aggiunta di opzioni al pulsante OK</span><span class="sxs-lookup"><span data-stu-id="35d3b-240">Adding Options to the OK Button</span></span>

<span data-ttu-id="35d3b-241">Analogamente, è possibile aggiungere scelte ai pulsanti **Apri** o **Salva** , che corrispondono al pulsante **OK** per i rispettivi tipi di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-241">Similarly, choices can be added to the **Open** or **Save** buttons, which are the **OK** button for their respective dialog types.</span></span> <span data-ttu-id="35d3b-242">Le opzioni sono accessibili tramite una casella di riepilogo a discesa collegata al pulsante.</span><span class="sxs-lookup"><span data-stu-id="35d3b-242">The options are accessible through a drop-down list box attached to the button.</span></span> <span data-ttu-id="35d3b-243">Il primo elemento dell'elenco diventa il testo per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="35d3b-243">The first item in the list becomes the text for the button.</span></span> <span data-ttu-id="35d3b-244">Nell'esempio seguente viene illustrato come fornire un pulsante **Apri** con due possibilità: "Apri" e "Apri come di sola lettura".</span><span class="sxs-lookup"><span data-stu-id="35d3b-244">The following example shows how to provide an **Open** button with two possibilities: "Open" and "Open as read-only".</span></span>


```C++
// OpenChoices options
#define OPENCHOICES 0
#define OPEN 0
#define OPEN_AS_READONLY 1


HRESULT AddOpenChoices()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    hr = pfdc->EnableOpenDropDown(OPENCHOICES);
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, OPEN, L&quot;&Open&quot;);
                    }                    
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, 
                                                OPEN_AS_READONLY, 
                                                L&quot;Open as &read-only&quot;);
                    }
                    if (SUCCEEDED(hr))
                    {
                        pfd->Show(NULL);
                    }
                }
                pfdc->Release();
            }
            pfd->Unadvise(dwCookie);
        }
        pfde->Release();
    }
    pfd->Release();
    return hr;
}
```





<span data-ttu-id="35d3b-245">La scelta dell'utente può essere verificata dopo che la finestra di dialogo viene restituita dal metodo [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) come per una casella combinata oppure può essere verificata come parte della gestione di [**IFileDialogEvents:: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span><span class="sxs-lookup"><span data-stu-id="35d3b-245">The user's choice can be verified after the dialog returns from the [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) method as you would for a ComboBox, or it can verified as part of the handling by [**IFileDialogEvents::OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span></span>

### <a name="responding-to-events-in-added-controls"></a><span data-ttu-id="35d3b-246">Risposta agli eventi nei controlli aggiunti</span><span class="sxs-lookup"><span data-stu-id="35d3b-246">Responding to Events in Added Controls</span></span>

<span data-ttu-id="35d3b-247">Il gestore eventi fornito dal processo chiamante può implementare [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) oltre a [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span><span class="sxs-lookup"><span data-stu-id="35d3b-247">The events handler provided by the calling process can implement [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) in addition to [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span></span> <span data-ttu-id="35d3b-248">**IFileDialogControlEvents** consente al processo chiamante di rispondere a questi eventi:</span><span class="sxs-lookup"><span data-stu-id="35d3b-248">**IFileDialogControlEvents** enables the calling process to react to these events:</span></span>

-   <span data-ttu-id="35d3b-249">Pulsante selezionato</span><span class="sxs-lookup"><span data-stu-id="35d3b-249">PushButton clicked</span></span>
-   <span data-ttu-id="35d3b-250">Stato CheckButton modificato</span><span class="sxs-lookup"><span data-stu-id="35d3b-250">CheckButton state changed</span></span>
-   <span data-ttu-id="35d3b-251">Elemento selezionato da un menu, una casella combinata o un elenco di RadioButton</span><span class="sxs-lookup"><span data-stu-id="35d3b-251">Item selected from a menu, ComboBox, or RadioButton list</span></span>
-   <span data-ttu-id="35d3b-252">Attivazione del controllo.</span><span class="sxs-lookup"><span data-stu-id="35d3b-252">Control activating.</span></span> <span data-ttu-id="35d3b-253">Viene inviato quando un menu sta per visualizzare un elenco a discesa, nel caso in cui il processo chiamante voglia modificare gli elementi dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="35d3b-253">This is sent when a menu is about to display a drop-down list, in case the calling process wants to change the items in the list.</span></span>

## <a name="full-samples"></a><span data-ttu-id="35d3b-254">Esempi completi</span><span class="sxs-lookup"><span data-stu-id="35d3b-254">Full Samples</span></span>

<span data-ttu-id="35d3b-255">Di seguito sono riportati esempi di C++ completi e scaricabili dal Windows Software Development Kit (SDK) che illustrano l'utilizzo e l'interazione con la finestra di dialogo elemento comune.</span><span class="sxs-lookup"><span data-stu-id="35d3b-255">The following are complete, downloadable C++ samples from the Windows Software Development Kit (SDK) which demonstrate the use of and interaction with the Common Item Dialog.</span></span>

-   [<span data-ttu-id="35d3b-256">Esempio di finestre di dialogo comuni di file</span><span class="sxs-lookup"><span data-stu-id="35d3b-256">Common File Dialog Sample</span></span>](samples-commonfiledialog.md)
-   [<span data-ttu-id="35d3b-257">Esempio di modalità di finestre di dialogo comuni di file</span><span class="sxs-lookup"><span data-stu-id="35d3b-257">Common File Dialog Modes Sample</span></span>](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a><span data-ttu-id="35d3b-258">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35d3b-258">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35d3b-259">**argomenti di IID \_ PPV \_**</span><span class="sxs-lookup"><span data-stu-id="35d3b-259">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
