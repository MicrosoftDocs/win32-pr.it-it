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
# <a name="common-item-dialog"></a>Finestra di dialogo elemento comune

A partire da Windows Vista, la finestra di dialogo elemento comune sostituisce la finestra di dialogo file comune precedente quando viene usata per aprire o salvare un file. La finestra di dialogo elemento comune viene utilizzata in due varianti: la finestra di dialogo **Apri** e la finestra di dialogo **Salva** . Queste due finestre di dialogo condividono la maggior parte delle funzionalità, ma ognuna ha i propri metodi univoci.

Sebbene la versione più recente venga denominata finestra di dialogo elemento comune, la maggior parte della documentazione continua a essere denominata finestra di dialogo file comune. A meno che non si occupi specificamente di una versione precedente di Windows, è necessario presupporre che qualsiasi menzione della finestra di dialogo file comune faccia riferimento a questa finestra di dialogo elemento comune.

Gli argomenti seguenti sono descritti di seguito:

-   [IFileDialog, IFileOpenDialog e IFileSaveDialog](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [Esempio di utilizzo](#sample-usage)
-   [Ascolto degli eventi dalla finestra di dialogo](#listening-to-events-from-the-dialog)
    -   [OnFileOk](#onfileok)
    -   [OnShareViolation e OnWrite](#onshareviolation-and-onoverwrite)
-   [Personalizzazione della finestra di dialogo](#customizing-the-dialog)
    -   [Aggiunta di opzioni al pulsante OK](#adding-options-to-the-ok-button)
    -   [Risposta agli eventi nei controlli aggiunti](#responding-to-events-in-added-controls)
-   [Esempi completi](#full-samples)
-   [Argomenti correlati](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a>IFileDialog, IFileOpenDialog e IFileSaveDialog

Windows Vista fornisce le implementazioni delle finestre di dialogo **Apri** e **Salva** : CLSID \_ FileOpenDialog e \_ CLSID FileSaveDialog. Queste finestre di dialogo sono mostrate qui.

![screenshot della finestra di dialogo Apri](images/cid/openfiledialog.png)

![screenshot della finestra di dialogo Salva con nome](images/cid/savefiledialog.png)

[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) e [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) ereditano da [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) e condividono gran parte delle relative funzionalità. Inoltre, la finestra di dialogo **Apri** supporta **IFileOpenDialog** e la finestra di dialogo **Salva** supporta **IFileSaveDialog**.

L'implementazione della finestra di dialogo elemento comune presente in Windows Vista offre diversi vantaggi rispetto all'implementazione fornita nelle versioni precedenti:

-   Supporta l'uso diretto dello spazio dei nomi della shell tramite [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) invece di usare percorsi di file System.
-   Consente la personalizzazione semplice della finestra di dialogo, ad esempio l'impostazione dell'etichetta sul pulsante **OK** , senza richiedere una procedura di hook.
-   Supporta una personalizzazione più completa della finestra di dialogo mediante l'aggiunta di un set di controlli basati sui dati che operano senza un modello di finestra di dialogo Win32. Questo schema di personalizzazione libera il processo chiamante dal layout dell'interfaccia utente. Poiché le modifiche apportate alla progettazione della finestra di dialogo continuano a utilizzare questo modello di dati, l'implementazione della finestra di dialogo non è associata alla versione corrente specifica della finestra di dialogo.
-   Supporta la notifica del chiamante degli eventi all'interno della finestra di dialogo, ad esempio la modifica della selezione o il tipo di file. Consente inoltre al processo chiamante di associare determinati eventi nella finestra di dialogo, ad esempio l'analisi.
-   Introduce nuove funzionalità della finestra di dialogo, ad esempio l'aggiunta di posizioni specificate dal chiamante alla barra dei **punti** .
-   Nella finestra di dialogo **Salva** gli sviluppatori possono sfruttare le nuove funzionalità dei metadati della shell di Windows Vista.

Inoltre, gli sviluppatori possono scegliere di implementare le interfacce seguenti:

-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) per ricevere le notifiche degli eventi all'interno della finestra di dialogo.
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) per aggiungere controlli alla finestra di dialogo.
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) a ricevere notifiche relative agli eventi nei controlli aggiunti.

La finestra di dialogo **Apri** o **Salva** restituisce un oggetto [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) o [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) al processo chiamante. Il chiamante può quindi usare un singolo oggetto **IShellItem** per ottenere un percorso di file System o per aprire un flusso sull'elemento per leggere o scrivere informazioni.

I flag e le opzioni disponibili per i nuovi metodi di finestra di dialogo sono molto simili ai flag **OFN** precedenti trovati nella struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e usati in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). Molti di essi sono esattamente uguali, ad eccezione del fatto che iniziano con un prefisso FOS. L'elenco completo si trova negli argomenti [**IFileDialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) e [**IFileDialog:: SetOption**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) . Per impostazione predefinita, le finestre di dialogo **Apri** e **Salva** vengono create con i flag più comuni. Per la finestra di dialogo **Apri** , questo è (FOS \_ PATHMUSTEXIST \| Fos \_ FILEMUSTEXIST \| Fos \_ NOCHANGEDIR) e per la finestra di dialogo **Salva** è (FOS OVERWRITEPROMPT Fos NOREADONLYRETURN Fos PATHMUSTEXIST \_ \| \_ \| \_ \| Fos \_ NOCHANGEDIR).

[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) e le relative interfacce discendenti ereditano da ed estendono [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). [**Mostra**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) accetta come unico parametro l'handle della finestra padre. Se il valore di **show** viene restituito correttamente, il risultato è valido. Se restituisce `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , significa che l'utente ha annullato la finestra di dialogo. Potrebbe inoltre restituire legittimamente un altro codice di errore, ad esempio **E \_ OutOfMemory**.

### <a name="sample-usage"></a>Esempio di utilizzo

Nelle sezioni seguenti viene illustrato il codice di esempio per un'ampia gamma di attività di dialogo.

-   [Utilizzo di base](#basic-usage)
-   [Limitazione dei risultati agli elementi del file System](#limiting-results-to-file-system-items)
-   [Specifica dei tipi di file per una finestra di dialogo](#specifying-file-types-for-a-dialog)
-   [Controllo della cartella predefinita](#controlling-the-default-folder)
-   [Aggiunta di elementi alla barra dei punti](#adding-items-to-the-places-bar)
-   [Persistenza dello stato](#state-persistence)
-   [Funzionalità MultiSelect](#multiselect-capabilities)

La maggior parte del codice di esempio è disponibile nell' [esempio Windows SDK finestra di dialogo file comune](samples-commonfiledialog.md).

### <a name="basic-usage"></a>Utilizzo di base

Nell'esempio seguente viene illustrato come avviare una finestra di dialogo **aperta** . In questo esempio è limitato ai documenti di Microsoft Word.

> [!Note]  
> Molti esempi in questo argomento usano la `CDialogEventHandler_CreateInstance` funzione helper per creare un'istanza dell'implementazione di [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) . Per usare questa funzione nel codice, copiare il codice sorgente per la `CDialogEventHandler_CreateInstance` funzione dall' [esempio di finestra di dialogo file comune](samples-commonfiledialog.md), da cui vengono presi tutti gli esempi in questo argomento.

 


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



### <a name="limiting-results-to-file-system-items"></a>Limitazione dei risultati agli elementi del file System

Nell'esempio seguente, tratto dalla precedente, viene illustrato come limitare i risultati agli elementi file system. Si noti che [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) aggiunge il nuovo flag a un valore ottenuto tramite [**IFileDialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions). Questo è il metodo consigliato.


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



### <a name="specifying-file-types-for-a-dialog"></a>Specifica dei tipi di file per una finestra di dialogo

Per impostare tipi di file specifici che la finestra di dialogo è in grado di gestire, usare il metodo [**IFileDialog:: Setypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) . Tale metodo accetta una matrice di [**strutture \_ FILTERSPEC di COMDLG**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) , ognuna delle quali rappresenta un tipo di file.

Il meccanismo di estensione predefinito in una finestra di dialogo è invariato da [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). L'estensione del nome file aggiunta al testo che l'utente digita nella casella di modifica nome file viene inizializzata all'apertura della finestra di dialogo. Deve corrispondere al tipo di file predefinito (selezionato quando viene visualizzata la finestra di dialogo). Se il tipo di file predefinito è " \* . \* " (tutti i file), il file può essere un'estensione di propria scelta. Se l'utente sceglie un tipo di file diverso, l'estensione viene aggiornata automaticamente alla prima estensione del nome file associata al tipo di file. Se l'utente sceglie " \* . \* " (tutti i file), quindi l'estensione ripristina il valore originale.

L'esempio seguente illustra come questa operazione è stata eseguita in precedenza.


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



### <a name="controlling-the-default-folder"></a>Controllo della cartella predefinita

È possibile usare quasi tutte le cartelle dello spazio dei nomi della shell come cartella predefinita per la finestra di dialogo (la cartella visualizzata quando l'utente sceglie di aprire o salvare un file). Chiamare [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) prima di chiamare [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) a tale scopo.

La cartella predefinita è la cartella in cui viene avviata la finestra di dialogo la prima volta che l'utente apre l'applicazione. Successivamente, la finestra di dialogo si aprirà nell'ultima cartella aperta da un utente o nell'ultima cartella utilizzata per salvare un elemento. Per ulteriori informazioni, vedere [persistenza dello stato](#state-persistence) .

È possibile forzare la visualizzazione della finestra di dialogo per visualizzare sempre la stessa cartella quando si apre, indipendentemente dall'azione dell'utente precedente, chiamando [**IFileDialog:: fileFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder). Tuttavia, questa operazione non è consigliata. Se si chiama la **cartella fileFolder** prima di visualizzare la finestra di dialogo, non viene visualizzata la posizione più recente da cui l'utente ha salvato o aperto. A meno che non esista un motivo molto specifico per questo comportamento, non si tratta di un'esperienza utente buona o prevista e deve essere evitata. In quasi tutte le istanze, [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) è il metodo migliore.

Quando si salva un documento per la prima volta nella finestra di dialogo **Salva** , è necessario seguire le stesse linee guida per determinare la cartella iniziale come è stato fatto nella finestra di dialogo **Apri** . Se l'utente sta modificando un documento esistente in precedenza, aprire la finestra di dialogo nella cartella in cui è archiviato il documento e popolare la casella di modifica con il nome del documento. Chiamare [**IFileSaveDialog:: SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) con l'elemento corrente prima di chiamare [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).

### <a name="adding-items-to-the-places-bar"></a>Aggiunta di elementi alla barra dei punti

Nell'esempio seguente viene illustrata l'aggiunta di elementi alla barra dei **punti** :


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



### <a name="state-persistence"></a>Persistenza dello stato

Prima di Windows Vista, uno stato, ad esempio l'ultima cartella visitata, veniva salvato in base ai singoli processi. Tuttavia, tali informazioni venivano utilizzate indipendentemente dall'azione specifica. Ad esempio, un'applicazione di modifica video presenta la stessa cartella nella finestra di dialogo **Render As** come si farebbe nella finestra di dialogo **Importa supporti** . In Windows Vista è possibile essere più specifici tramite l'uso di GUID. Per assegnare un **GUID** alla finestra di dialogo, chiamare [**IFileDialog:: SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).

### <a name="multiselect-capabilities"></a>Funzionalità MultiSelect

La funzionalità MultiSelect è disponibile nella finestra di dialogo **Apri** usando il metodo [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) come illustrato di seguito.


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



## <a name="listening-to-events-from-the-dialog"></a>Ascolto degli eventi dalla finestra di dialogo

Un processo chiamante può registrare un'interfaccia [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) con la finestra di dialogo usando i metodi [**IFileDialog:: Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) e [**IFileDialog:: Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) , come illustrato di seguito.

Questa operazione è ricavata dall'esempio di [utilizzo di base](#basic-usage) .


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



La maggior parte dell'elaborazione del dialogo viene effettuata qui.


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



Il processo chiamante può utilizzare gli eventi per la notifica quando l'utente modifica la cartella, il tipo di file o la selezione. Questi eventi sono particolarmente utili quando il processo chiamante ha aggiunto controlli alla finestra di dialogo (vedere [personalizzazione della finestra di dialogo](#customizing-the-dialog)) e deve modificare lo stato di tali controlli in risposta a questi eventi. Utile in tutti i casi è la capacità del processo chiamante di fornire codice personalizzato per gestire situazioni quali la condivisione di violazioni, la sovrascrittura dei file o la determinazione di un file valido prima della chiusura della finestra di dialogo. Alcuni di questi casi sono descritti in questa sezione.

### <a name="onfileok"></a>OnFileOk

Questo metodo viene chiamato dopo che l'utente sceglie un elemento, immediatamente prima della chiusura della finestra di dialogo. L'applicazione può quindi chiamare [**IFileDialog:: GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) o [**IFileOpenDialog:: GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) come verrebbe eseguita dopo la chiusura della finestra di dialogo. Se l'elemento scelto è accettabile, può restituire S \_ OK. In caso contrario, restituiscono S \_ false e visualizzano l'interfaccia utente che indica all'utente il motivo per cui l'elemento scelto non è valido. Se \_ viene restituito S false, la finestra di dialogo non viene chiusa.

Il processo chiamante può utilizzare l'handle di finestra del dialogo stesso come elemento padre dell'interfaccia utente. Tale handle può essere ottenuto chiamando prima [**IOleWindow:: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) e chiamando [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) con l'handle, come illustrato in questo esempio.


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



### <a name="onshareviolation-and-onoverwrite"></a>OnShareViolation e OnWrite

Se l'utente sceglie di sovrascrivere un file nella finestra di dialogo **Salva** o se un file salvato o sostituito è in uso e non può essere scritto in una violazione di condivisione, l'applicazione può fornire funzionalità personalizzate per ignorare il comportamento predefinito della finestra di dialogo. Per impostazione predefinita, quando si sovrascrive un file, nella finestra di dialogo viene visualizzato un prompt che consente all'utente di verificare l'azione. Per le violazioni di condivisione, per impostazione predefinita nella finestra di dialogo viene visualizzato un messaggio di errore, non viene chiuso e l'utente deve effettuare un'altra scelta. Il processo chiamante può eseguire l'override di queste impostazioni predefinite e visualizzare la propria interfaccia utente, se lo si desidera. È possibile indicare alla finestra di dialogo di rifiutare il file e rimanere aperti o accettare il file e chiuderlo correttamente.

## <a name="customizing-the-dialog"></a>Personalizzazione della finestra di dialogo

È possibile aggiungere una serie di controlli alla finestra di dialogo senza specificare un modello di finestra di dialogo Win32. Questi controlli includono pulsanti, ComboBox, casella, CheckButton, elenchi di RadioButton, gruppi, separatori e controlli di testo statici. Chiamare **QueryInterface** sull'oggetto finestra di dialogo ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)o [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) per ottenere un puntatore [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) . Usare tale interfaccia per aggiungere controlli. A ogni controllo è associato un ID fornito dal chiamante, nonché uno stato *visibile* e *abilitato* che può essere impostato dal processo chiamante. Alcuni controlli, ad esempio il pulsante, hanno anche testo associato.

È possibile aggiungere più controlli in un "gruppo visivo" che si sposta come una singola unità nel layout della finestra di dialogo. Ai gruppi può essere associata un'etichetta.

I controlli possono essere aggiunti solo prima che venga visualizzata la finestra di dialogo. Tuttavia, una volta visualizzata la finestra di dialogo, i controlli possono essere nascosti o visualizzati in base alle esigenze, forse in risposta all'azione dell'utente. Gli esempi seguenti illustrano come aggiungere un elenco di pulsanti di opzione alla finestra di dialogo.


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





### <a name="adding-options-to-the-ok-button"></a>Aggiunta di opzioni al pulsante OK

Analogamente, è possibile aggiungere scelte ai pulsanti **Apri** o **Salva** , che corrispondono al pulsante **OK** per i rispettivi tipi di finestra di dialogo. Le opzioni sono accessibili tramite una casella di riepilogo a discesa collegata al pulsante. Il primo elemento dell'elenco diventa il testo per il pulsante. Nell'esempio seguente viene illustrato come fornire un pulsante **Apri** con due possibilità: "Apri" e "Apri come di sola lettura".


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





La scelta dell'utente può essere verificata dopo che la finestra di dialogo viene restituita dal metodo [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) come per una casella combinata oppure può essere verificata come parte della gestione di [**IFileDialogEvents:: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).

### <a name="responding-to-events-in-added-controls"></a>Risposta agli eventi nei controlli aggiunti

Il gestore eventi fornito dal processo chiamante può implementare [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) oltre a [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents). **IFileDialogControlEvents** consente al processo chiamante di rispondere a questi eventi:

-   Pulsante selezionato
-   Stato CheckButton modificato
-   Elemento selezionato da un menu, una casella combinata o un elenco di RadioButton
-   Attivazione del controllo. Viene inviato quando un menu sta per visualizzare un elenco a discesa, nel caso in cui il processo chiamante voglia modificare gli elementi dell'elenco.

## <a name="full-samples"></a>Esempi completi

Di seguito sono riportati esempi di C++ completi e scaricabili dal Windows Software Development Kit (SDK) che illustrano l'utilizzo e l'interazione con la finestra di dialogo elemento comune.

-   [Esempio di finestre di dialogo comuni di file](samples-commonfiledialog.md)
-   [Esempio di modalità di finestre di dialogo comuni di file](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**argomenti di IID \_ PPV \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
