---
description: A partire Windows Vista, la finestra di dialogo Elemento comune sostituisce la finestra di dialogo File comune precedente quando viene usata per aprire o salvare un file.
title: Finestra di dialogo elemento comune
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2956bf7329ff9c92b777199d040d1275aa827cfa9ea9c8bfbec175d234b204f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943521"
---
# <a name="common-item-dialog"></a>Finestra di dialogo elemento comune

A partire Windows Vista, la finestra di dialogo Elemento comune sostituisce la finestra di dialogo File comune precedente quando viene usata per aprire o salvare un file. La finestra di dialogo Elemento comune viene usata in due varianti: la **finestra di** dialogo Apri e la finestra **di dialogo** Salva. Questi due dialoghe condividono la maggior parte delle funzionalità, ma ognuno ha metodi univoci.

Anche se questa versione più recente è denominata Finestra di dialogo elementi comuni, nella maggior parte della documentazione continua a essere chiamata finestra di dialogo file comune. A meno che non si tratti specificamente di una versione precedente di Windows, è necessario presupporre che qualsiasi menzione della finestra di dialogo file comune faccia riferimento a questo dialogo elemento comune.

Di seguito sono descritti gli argomenti seguenti:

-   [IFileDialog, IFileOpenDialog e IFileSaveDialog](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [Utilizzo di esempio](#sample-usage)
-   [Ascolto di eventi dal dialogo](#listening-to-events-from-the-dialog)
    -   [OnFileOk](#onfileok)
    -   [OnShareViolation e OnOverwrite](#onshareviolation-and-onoverwrite)
-   [Personalizzazione della finestra di dialogo](#customizing-the-dialog)
    -   [Aggiunta di opzioni al pulsante OK](#adding-options-to-the-ok-button)
    -   [Risposta agli eventi nei controlli aggiunti](#responding-to-events-in-added-controls)
-   [Esempi completi](#full-samples)
-   [Argomenti correlati](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a>IFileDialog, IFileOpenDialog e IFileSaveDialog

Windows Vista offre implementazioni delle finestre **di** **dialogo** Apri e Salva: CLSID \_ FileOpenDialog e \_ CLSID FileSaveDialog. Queste finestre di dialogo sono visualizzate qui.

![Screenshot della finestra di dialogo apri](images/cid/openfiledialog.png)

![Screenshot della finestra di dialogo Salva con nome](images/cid/savefiledialog.png)

[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) e [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) ereditano da [**IFileDialog e**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) condividono gran parte delle funzionalità. Inoltre, la **finestra di dialogo** Apri supporta **IFileOpenDialog** e la finestra **di** dialogo Salva supporta **IFileSaveDialog.**

L'implementazione common item dialog disponibile in Windows Vista offre diversi vantaggi rispetto all'implementazione fornita nelle versioni precedenti:

-   Supporta l'uso diretto dello spazio dei nomi shell tramite [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) anziché file system percorsi.
-   Consente la personalizzazione semplice della finestra di dialogo, ad esempio l'impostazione dell'etichetta sul **pulsante OK,** senza richiedere una procedura hook.
-   Supporta una personalizzazione più estesa della finestra di dialogo con l'aggiunta di un set di controlli guidati dai dati che funzionano senza un modello di finestra di dialogo Win32. Questo schema di personalizzazione libera il processo chiamante dal layout dell'interfaccia utente. Poiché le modifiche apportate alla progettazione della finestra di dialogo continuano a usare questo modello di dati, l'implementazione del dialogo non è associata alla versione corrente specifica del dialogo.
-   Supporta la notifica del chiamante degli eventi all'interno della finestra di dialogo, ad esempio la modifica della selezione o la modifica del tipo di file. Consente inoltre al processo chiamante di associare determinati eventi nella finestra di dialogo, ad esempio l'analisi.
-   Introduce nuove funzionalità del dialogo, ad esempio l'aggiunta di posizioni specificate dal chiamante alla **barra** Posizioni.
-   Nella finestra **di** dialogo Salva gli sviluppatori possono sfruttare le nuove funzionalità dei metadati di Windows Vista Shell.

Inoltre, gli sviluppatori possono scegliere di implementare le interfacce seguenti:

-   [**IFileDialogEvents per ricevere**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) notifiche degli eventi all'interno del dialogo.
-   [**IFileDialogCustomize per**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) aggiungere controlli alla finestra di dialogo.
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) per ricevere una notifica degli eventi nei controlli aggiunti.

La **finestra di** dialogo **Apri** o Salva restituisce un [**oggetto IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) o [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) al processo chiamante. Il chiamante può quindi usare un singolo oggetto **IShellItem** per ottenere un percorso file system o per aprire un flusso sull'elemento per leggere o scrivere informazioni.

I flag e le opzioni disponibili per i nuovi metodi di finestra di dialogo sono molto simili ai flag **OFN** precedenti presenti nella struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e usati in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName.**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea) Molte di esse sono esattamente uguali, ad eccezione del fatto che iniziano con un prefisso FOS. L'elenco completo è disponibile negli argomenti [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) e [**IFileDialog::SetOptions.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) **Le** finestre **di dialogo** Apri e Salva vengono create per impostazione predefinita con i flag più comuni. Per  la finestra di dialogo Apri, si tratta di (FOS PATHMUSTEXIST FOS FILEMUSTEXIST FOS NOCHANGEDIR) e per la finestra di dialogo Salva si tratta \_ di \| \_ \| \_ (FOS  \_ OVERWRITEPROMPT \| FOS \_ NOREADONLYRETURN \| FOS \_ PATHMUSTEXIST \| FOS \_ NOCHANGEDIR).

[**IFileDialog e**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) le relative interfacce discendenti ereditano da ed estendono [**IModalWindow.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow) [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) accetta come unico parametro l'handle della finestra padre. Se **Show** restituisce correttamente, è presente un risultato valido. Se restituisce `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , significa che l'utente ha annullato il dialogo. Potrebbe anche restituire in modo legittimo un altro codice di errore, ad **esempio E \_ OUTOFMEMORY.**

### <a name="sample-usage"></a>Esempio di utilizzo

Le sezioni seguenti illustrano il codice di esempio per un'ampia gamma di attività di dialogo.

-   [Utilizzo di base](#basic-usage)
-   [Limitazione dei risultati agli elementi del file system](#limiting-results-to-file-system-items)
-   [Specifica dei tipi di file per una finestra di dialogo](#specifying-file-types-for-a-dialog)
-   [Controllo della cartella predefinita](#controlling-the-default-folder)
-   [Aggiunta di elementi alla barra Delle posizioni](#adding-items-to-the-places-bar)
-   [Persistenza dello stato](#state-persistence)
-   [Funzionalità di selezione multipla](#multiselect-capabilities)

La maggior parte del codice di esempio è disponibile nell'esempio di Windows di dialogo [file comuni dell'SDK.](samples-commonfiledialog.md)

### <a name="basic-usage"></a>Utilizzo di base

L'esempio seguente illustra come avviare una finestra **di dialogo** Apri. In questo esempio è limitato ai documenti Microsoft Word documenti.

> [!Note]  
> Diversi esempi in questo argomento usano la `CDialogEventHandler_CreateInstance` funzione helper per creare un'istanza dell'implementazione di [**IFileDialogEvents.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) Per usare questa funzione nel proprio codice, copiare il codice sorgente per la funzione dall'esempio di finestra di dialogo File comune , da cui vengono presi tutti gli esempi `CDialogEventHandler_CreateInstance` in questo argomento. [](samples-commonfiledialog.md)

 


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



### <a name="limiting-results-to-file-system-items"></a>Limitazione dei risultati agli elementi del file system

L'esempio seguente, tratto dall'esempio precedente, illustra come limitare i risultati file system elementi. Si noti [**che IFileDialog::SetOptions aggiunge**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) il nuovo flag a un valore ottenuto tramite [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions). Questo è il metodo consigliato.


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

Per impostare tipi di file specifici che il dialogo può gestire, usare il [**metodo IFileDialog::SetFileTypes.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) Tale metodo accetta una matrice di [**strutture \_ COMDLG FILTERSPEC,**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) ognuna delle quali rappresenta un tipo di file.

Il meccanismo di estensione predefinito in una finestra di dialogo rimane invariato rispetto a [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) [**e GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). L'estensione del nome file aggiunta al testo che l'utente digitare nella casella di modifica del nome file viene inizializzata all'apertura della finestra di dialogo. Deve corrispondere al tipo di file predefinito (selezionato all'apertura della finestra di dialogo). Se il tipo di file predefinito è " \* . \* (tutti i file), il file può essere un'estensione di propria scelta. Se l'utente sceglie un tipo di file diverso, l'estensione viene aggiornata automaticamente alla prima estensione di file associata a tale tipo di file. Se l'utente sceglie " \* . \* " (tutti i file), viene ripristinato il valore originale dell'estensione.

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

Quasi tutte le cartelle nello spazio dei nomi Shell possono essere usate come cartella predefinita per la finestra di dialogo (la cartella visualizzata quando l'utente sceglie di aprire o salvare un file). Chiamare [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) prima di [**chiamare Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) a tale scopo.

La cartella predefinita è la cartella in cui viene avviata la finestra di dialogo la prima volta che un utente la apre dall'applicazione. Successivamente, la finestra di dialogo verrà aperta nell'ultima cartella aperta da un utente o nell'ultima cartella usata per salvare un elemento. Per [altri dettagli, vedere Persistenza](#state-persistence) dello stato.

È possibile forzare la visualizzazione sempre della stessa cartella all'apertura della finestra di dialogo, indipendentemente dall'azione dell'utente precedente, chiamando [**IFileDialog::SetFolder.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder) Tuttavia, non è consigliabile eseguire questa operazione. Se si chiama **SetFolder prima** di visualizzare la finestra di dialogo, il percorso più recente in cui l'utente ha salvato o aperto non viene visualizzato. A meno che non vi sia un motivo molto specifico per questo comportamento, non si tratta di un'esperienza utente buona o prevista e deve essere evitata. In quasi tutti i [**casi, IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) è il metodo migliore.

Quando si salva un documento  per la prima volta nella finestra di dialogo Salva, è necessario seguire le stesse linee guida per determinare la cartella iniziale, come è stato fatto nella **finestra di dialogo** Apri. Se l'utente sta modificando un documento esistente in precedenza, aprire la finestra di dialogo nella cartella in cui è archiviato il documento e popolare la casella di modifica con il nome del documento. Chiamare [**IFileSaveDialog::SetSaveAsItem con**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) l'elemento corrente prima di chiamare [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).

### <a name="adding-items-to-the-places-bar"></a>Aggiunta di elementi alla barra Delle posizioni

L'esempio seguente illustra l'aggiunta di elementi alla **barra** Places:


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

Prima di Windows Vista, uno stato, ad esempio l'ultima cartella visitata, è stato salvato in base al processo. Tuttavia, tali informazioni sono stati usati indipendentemente dall'azione specifica. Ad esempio, un'applicazione di modifica video presenterà la stessa cartella nella finestra di dialogo **Esegui** rendering come nella finestra di **dialogo Importa file** multimediali. In Windows Vista è possibile essere più specifici tramite l'uso di GUID. Per assegnare **un GUID** alla finestra di dialogo, chiamare [**iFileDialog::SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).

### <a name="multiselect-capabilities"></a>Funzionalità di selezione multipla

La funzionalità di selezione multipla è disponibile nella **finestra di** dialogo Apri usando il [**metodo GetResults,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) come illustrato di seguito.


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



## <a name="listening-to-events-from-the-dialog"></a>Ascolto di eventi dal dialogo

Un processo chiamante può registrare un'interfaccia [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) con la finestra di dialogo usando i metodi [**IFileDialog::Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) e [**IFileDialog::Unadvise,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) come illustrato di seguito.

Questo è tratto [dall'esempio di utilizzo di](#basic-usage) base.


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



La maggior parte dell'elaborazione del dialogo verrà inserita qui.


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



Il processo chiamante può usare gli eventi per la notifica quando l'utente modifica la cartella, il tipo di file o la selezione. Questi eventi sono particolarmente utili quando il processo chiamante ha aggiunto controlli alla finestra di dialogo (vedere [Personalizzazione](#customizing-the-dialog)della finestra di dialogo) e deve modificare lo stato di tali controlli in risposta a questi eventi. Utile in tutti i casi è la capacità del processo chiamante di fornire codice personalizzato per gestire situazioni come la condivisione di violazioni, la sovrascrittura di file o la determinazione della validità di un file prima della chiusura della finestra di dialogo. Alcuni di questi casi sono descritti in questa sezione.

### <a name="onfileok"></a>OnFileOk

Questo metodo viene chiamato dopo che l'utente ha scelto un elemento, subito prima della chiusura del dialogo. L'applicazione può quindi chiamare [**IFileDialog::GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) o [**IFileOpenDialog::GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) come si farebbe dopo la chiusura del dialogo. Se l'elemento scelto è accettabile, possono restituire S \_ OK. In caso contrario, restituiscono S \_ FALSE e visualizzano l'interfaccia utente che indica all'utente il motivo per cui l'elemento scelto non è valido. Se viene restituito S \_ FALSE, la finestra di dialogo non viene chiusa.

Il processo chiamante può usare l'handle di finestra della finestra di dialogo stessa come elemento padre dell'interfaccia utente. Tale handle può essere ottenuto chiamando [**prima IOleWindow::QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) e quindi [**chiamando IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) con l'handle come illustrato in questo esempio.


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



### <a name="onshareviolation-and-onoverwrite"></a>OnShareViolation e OnOverwrite

Se l'utente sceglie di sovrascrivere un file nella finestra di dialogo Salva o se un file salvato o sostituito è in uso e non può essere scritto in (una violazione di condivisione), l'applicazione può fornire funzionalità personalizzate per eseguire l'override del comportamento predefinito della finestra di dialogo.  Per impostazione predefinita, quando si sovrascrive un file, nella finestra di dialogo viene visualizzato un prompt che consente all'utente di verificare questa azione. Per le violazioni di condivisione, per impostazione predefinita la finestra di dialogo visualizza un messaggio di errore, non si chiude e l'utente deve effettuare un'altra scelta. Il processo chiamante può eseguire l'override di queste impostazioni predefinite e visualizzare la propria interfaccia utente, se necessario. È possibile indicare alla finestra di dialogo di rifiutare il file e rimanere aperto o accettare il file e chiuderlo correttamente.

## <a name="customizing-the-dialog"></a>Personalizzazione della finestra di dialogo

È possibile aggiungere un'ampia gamma di controlli alla finestra di dialogo senza fornire un modello di finestra di dialogo Win32. Questi controlli includono Controlli PushButton, ComboBox, EditBox, CheckButton, RadioButton, Groups, Separators e Static Text. Chiamare **QueryInterface sull'oggetto** finestra di dialogo ([**IFileDialog,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)o [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) per ottenere un [**puntatore IFileDialogCustomize.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) Usare tale interfaccia per aggiungere controlli. A ogni controllo è associato un ID fornito  dal chiamante, nonché *uno* stato visibile e abilitato che può essere impostato dal processo chiamante. Ad alcuni controlli, ad esempio PushButton, è associato anche testo.

È possibile aggiungere più controlli in un "gruppo visivo" che si sposta come singola unità nel layout della finestra di dialogo. Ai gruppi può essere associata un'etichetta.

I controlli possono essere aggiunti solo prima che venga visualizzata la finestra di dialogo. Tuttavia, una volta visualizzata la finestra di dialogo, i controlli possono essere nascosti o visualizzati come desiderato, ad esempio in risposta all'azione dell'utente. Gli esempi seguenti illustrano come aggiungere un elenco di pulsanti di opzione alla finestra di dialogo.


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

Analogamente, è possibile aggiungere opzioni ai pulsanti **Apri** o **Salva,** che sono il **pulsante OK** per i rispettivi tipi di finestra di dialogo. Le opzioni sono accessibili tramite una casella di riepilogo a discesa associata al pulsante. Il primo elemento dell'elenco diventa il testo per il pulsante. L'esempio seguente illustra come fornire un **pulsante** Apri con due possibilità: "Apri" e "Apri come di sola lettura".


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





La scelta dell'utente può essere verificata dopo che la finestra di dialogo viene restituita dal metodo [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) come per un controllo ComboBox oppure può essere verificata come parte della gestione da [**IFileDialogEvents::OnFileOk.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok)

### <a name="responding-to-events-in-added-controls"></a>Risposta agli eventi nei controlli aggiunti

Il gestore eventi fornito dal processo chiamante può implementare [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) oltre a [**IFileDialogEvents.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) **IFileDialogControlEvents** consente al processo chiamante di reagire a questi eventi:

-   PushButton su cui è stato fatto clic
-   Stato checkButton modificato
-   Elemento selezionato da un elenco di menu, ComboBox o RadioButton
-   Controllare l'attivazione. Viene inviato quando un menu sta per visualizzare un elenco a discesa, nel caso in cui il processo chiamante voglia modificare gli elementi nell'elenco.

## <a name="full-samples"></a>Esempi completi

Di seguito sono riportati esempi di C++ completi e scaricabili da Windows Software Development Kit (SDK) che illustrano l'uso e l'interazione con la finestra di dialogo elemento comune.

-   [Esempio di finestre di dialogo comuni di file](samples-commonfiledialog.md)
-   [Esempio di modalità di finestre di dialogo comuni di file](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ARGOMENTI \_ PPV \_ IID**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
