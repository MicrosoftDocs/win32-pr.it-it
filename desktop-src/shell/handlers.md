---
description: Le funzionalità della shell possono essere estese con le voci del registro di sistema e i file ini.
ms.assetid: 74a81e4f-7357-4901-a118-ba44e8892f25
title: Creazione di gestori di estensione della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f3c1684b7491e2ad29fae29f48164ffdd47cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994701"
---
# <a name="creating-shell-extension-handlers"></a>Creazione di gestori di estensione della shell

Le funzionalità della shell possono essere estese con le voci del registro di sistema e i file ini. Sebbene questo approccio per estendere la shell sia semplice e appropriato per molti scopi, è limitato. Se ad esempio si usa il registro di sistema per specificare un'icona personalizzata per un tipo di file, verrà visualizzata la stessa icona per ogni file di quel tipo. L'estensione della shell con il registro di sistema non consente di variare l'icona per file diversi dello stesso tipo. Altri aspetti della shell, ad esempio la finestra delle proprietà **delle proprietà che** può essere visualizzata quando si fa clic con il pulsante destro del mouse su un file, non possono essere modificati nel registro di sistema.

Un approccio più potente e flessibile per estendere la Shell consiste nell'implementare i *gestori di estensioni della shell*. Questi gestori possono essere implementati per un'ampia gamma di azioni che possono essere eseguite dalla Shell. Prima di eseguire l'azione, la shell esegue una query sul gestore dell'estensione, offrendo la possibilità di modificare l'azione. Un esempio comune è un gestore di estensione del menu di scelta rapida. Se ne viene implementato uno per un tipo di file, verrà eseguita una query ogni volta che viene fatto clic con il pulsante destro del mouse su uno dei file. Il gestore può quindi specificare voci di menu aggiuntive in base al file, anziché avere lo stesso set per l'intero tipo di file.

In questo documento viene illustrato come implementare i gestori di estensione che consentono di modificare un'ampia gamma di azioni della shell. I gestori seguenti sono associati a un tipo di file specifico e consentono di specificare in base al file:



| Gestore                                               | Descrizione                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestore del menu di scelta rapida](context-menu-handlers.md)    | Chiamato prima che venga visualizzato il menu di scelta rapida di un file. Consente di aggiungere elementi al menu di scelta rapida in base al file.                                               |
| [Gestore dati](how-to-create-data-handlers.md)       | Chiamato quando viene eseguita un'operazione di trascinamento e rilascio sugli oggetti dragShell. Consente di fornire altri formati degli Appunti all'obiettivo di rilascio.                        |
| [Gestore di trascinamento](how-to-create-drop-handlers.md)       | Chiamato quando un oggetto dati viene trascinato o rilasciato in un file. Consente di creare un file in un obiettivo di rilascio.                                                          |
| [Gestore icone](how-to-create-icon-handlers.md)       | Chiamato prima che venga visualizzata l'icona di un file. Consente di sostituire l'icona predefinita del file con un'icona personalizzata in base al file.                                    |
| [Gestore della finestra delle proprietà](propsheet-handlers.md)      | Chiamato prima della visualizzazione della finestra delle proprietà **delle proprietà di** un oggetto. Consente di aggiungere o sostituire pagine.                                                              |
| [**Gestore immagini di anteprima**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Fornisce un'immagine per rappresentare l'elemento.                                                                                                                                   |
| [**Gestore della finestra popup**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Fornisce il testo popup quando l'utente posiziona il puntatore del mouse sull'oggetto.                                                                                               |
| [**Gestore di metadati**](/windows/win32/api/propsys/nn-propsys-ipropertystore)     | Fornisce l'accesso in lettura e scrittura ai metadati (proprietà) archiviati in un file. Questa operazione può essere utilizzata per estendere la visualizzazione dettagli, infotip, la pagina delle proprietà e le funzionalità di raggruppamento. |



 

Altri gestori non sono associati a un tipo di file specifico, ma vengono chiamati prima di alcune operazioni della shell:



| Gestore                                                            | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestore delle colonne](../lwef/column-handlers.md)                             | Chiamato da Esplora risorse prima di visualizzare la visualizzazione dettagli di una cartella. Consente di aggiungere colonne personalizzate alla visualizzazione dettagli.        |
| [Gestore hook di copia](how-to-create-copy-hook-handlers.md)          | Chiamato quando un oggetto Folder o Printer sta per essere spostato, copiato, eliminato o rinominato. Consente di approvare o porre il veto sull'operazione.   |
| [Gestore di trascinamento della selezione](context-menu-handlers.md)                 | Chiamato quando un file viene trascinato con il pulsante destro del mouse. Consente di modificare il menu di scelta rapida visualizzato.                     |
| [Gestore sovrimpressione icone](how-to-implement-icon-overlay-handlers.md) | Chiamato prima che venga visualizzata l'icona di un file. Consente di specificare una sovrapposizione per l'icona del file.                                          |
| [Gestore ricerche](../lwef/search-handlers.md)                             | Chiamato per avviare un motore di ricerca. Consente di implementare un motore di ricerca personalizzato accessibile dal menu **Start** o da Esplora risorse. |



 

I dettagli relativi all'implementazione di gestori di estensioni specifici sono descritti nelle sezioni elencate in precedenza. Nella parte restante di questo documento vengono illustrati alcuni problemi di implementazione comuni a tutti i gestori di estensioni della shell.

-   [Implementazione di gestori di estensioni della shell](#implementing-shell-extension-handlers)
    -   [Implementazione di IPersistFile](#implementing-ipersistfile)
    -   [Implementazione di IShellExtInit](#implementing-ishellextinit)
    -   [Personalizzazione di infotip](#infotip-customization)
-   [Miglioramento della ricerca di Windows con gestori di estensioni della shell](#enhancing-windows-search-with-shell-extension-handlers)
-   [Registrazione di gestori estensioni della shell](#registering-shell-extension-handlers)
    -   [Nomi dei gestori](#handler-names)
    -   [Oggetti shell predefiniti](#predefined-shell-objects)
    -   [Esempio di registrazione di un gestore estensioni](#example-of-an-extension-handler-registration)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-shell-extension-handlers"></a>Implementazione di gestori di estensioni della shell

Gran parte dell'implementazione di un oggetto gestore dell'estensione della shell dipende dal tipo. Esistono, tuttavia, alcuni elementi comuni. Questa sezione illustra gli aspetti dell'implementazione condivisi da tutti i gestori di estensioni della shell.

Molti gestori di estensioni della shell sono oggetti Component Object Model (COM) in-process. È necessario assegnare un GUID e registrarlo come descritto in Registering Shell Extension Handler. Vengono implementate come dll ed è necessario esportare le funzioni standard seguenti:

-   [**DllMain**](../dlls/dllmain.md). Il punto di ingresso standard della DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Espone la class factory dell'oggetto.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM chiama questa funzione per determinare se l'oggetto serve qualsiasi client. In caso contrario, il sistema può scaricare la DLL e liberare la memoria associata.

Come tutti gli oggetti COM, i gestori di estensioni della shell devono implementare un'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e un [class factory](../com/implementing-iclassfactory.md). La maggior parte dei gestori di estensione deve implementare anche un'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**ISHELLEXTINIT**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) in Windows XP o versioni precedenti. Questi sono stati sostituiti da [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) e [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista. La shell usa queste interfacce per inizializzare il gestore.

L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) deve essere implementata dai seguenti elementi:

-   Gestori di dati
-   Gestori di rilascio

In passato, i gestori delle icone erano necessari anche per implementare [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), ma questo non è più vero. Per i gestori di icone, **IPersistFile** è ora facoltativo e sono preferibili altre interfacce, ad esempio [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) .

L'interfaccia [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) deve essere implementata dai seguenti elementi:

-   Gestori dei menu di scelta rapida
-   Gestori di trascinamento della selezione
-   Gestori della finestra delle proprietà

### <a name="implementing-ipersistfile"></a>Implementazione di IPersistFile

L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è destinata a consentire il caricamento o il salvataggio di un oggetto in un file su disco. Sono disponibili sei metodi, oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinque dei propri e il metodo [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) che eredita da [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist). Con le estensioni della shell, **IPersist** viene usato solo per inizializzare un oggetto gestore dell'estensione della shell. Poiché in genere non è necessario leggere o scrivere sul disco, solo i metodi **GetClassID** e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) richiedono un'implementazione non token.

La shell chiama prima [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e la funzione restituisce l'identificatore di classe (CLSID) dell'oggetto gestore di estensione. La shell chiama quindi [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) e passa due valori. Il primo, *pszFileName*, è una stringa Unicode con il nome del file o della cartella su cui la Shell sta per operare. Il secondo è *dwMode*, che indica la modalità di accesso ai file. Poiché in genere non è necessario accedere ai file, *dwMode* è in genere pari a zero. Il metodo archivia questi valori in base alle esigenze per un riferimento successivo.

Nel frammento di codice seguente viene illustrato il modo in cui un tipico gestore dell'estensione della shell implementa i metodi [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) . È progettato per gestire ANSI o Unicode. CLSID \_ SampleExtHandler è il GUID dell'oggetto gestore dell'estensione e CSampleExtHandler è il nome della classe utilizzata per implementare l'interfaccia. Le variabili **m \_ szFileName** e **m \_ dwMode** sono variabili private utilizzate per archiviare i flag di accesso e il nome del file.


```C++
wchar_t m_szFileName[MAX_PATH];    // The file name
DWORD m_dwMode;                  // The file access mode

CSampleExtHandler::GetClassID(CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

CSampleExtHandler::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(_szFileName, ARRAYSIZE(m_szFileName), pszFile);
}
```

### <a name="implementing-ishellextinit"></a>Implementazione di IShellExtInit

L'interfaccia [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) ha un solo metodo, [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Il metodo dispone di tre parametri che la shell può usare per passare vari tipi di informazioni. I valori passati dipendono dal tipo di gestore e altri possono essere impostati su **null**.

-   *pIDFolder* include il puntatore di una cartella a un elenco di identificatori di elemento (PIDL). Per le estensioni della finestra delle proprietà, è **null**. Per le estensioni del menu di scelta rapida, è il PIDL della cartella che contiene l'elemento di cui viene visualizzato il menu di scelta rapida. Per i gestori di trascinamento della selezione non predefiniti, è il PIDL della cartella di destinazione.
-   *pDataObject* include un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) di un oggetto dati. L'oggetto dati include uno o più nomi di file nel formato [CF \_ HDROP](dragdrop.md) .
-   *hRegKey* include una chiave del registro di sistema per l'oggetto file o il tipo di cartella.

Il metodo [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) archivia il nome file, il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) e la chiave del registro di sistema in base alle esigenze per un uso successivo. Nel frammento di codice seguente viene illustrata un'implementazione di **IShellExtInit:: Initialize**. Per semplicità, in questo esempio si presuppone che l'oggetto dati contenga un solo file. In generale, potrebbe contenere più file che dovranno essere estratti.


```C++
LPCITEMIDLIST  m_pIDFolder;           //The folder's PIDL
wchar_t        m_szFile[MAX_PATH];    //The file name
IDataObject   *m_pDataObj;            //The IDataObject pointer
HKEY           m_hRegKey;             //The file or folder's registry key

STDMETHODIMP CShellExt::Initialize(LPCITEMIDLIST pIDFolder, 
                                   IDataObject *pDataObj, 
                                   HKEY hRegKey) 
{ 
    // If Initialize has already been called, release the old PIDL
    ILFree(m_pIDFolder);
    m_pIDFolder = nullptr;

    // Store the new PIDL.
    if (pIDFolder)
    {
        m_pIDFolder = ILClone(pIDFolder);
    }
    
    // If Initialize has already been called, release the old
    // IDataObject pointer.
    if (m_pDataObj)
    { 
        m_pDataObj->Release(); 
    }
     
    // If a data object pointer was passed in, save it and
    // extract the file name. 
    if (pDataObj) 
    { 
        m_pDataObj = pDataObj; 
        pDataObj->AddRef(); 
      
        STGMEDIUM   medium;
        FORMATETC   fe = {CF_HDROP, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};
        UINT        uCount;

        if (SUCCEEDED(m_pDataObj->GetData(&fe, &medium)))
        {
            // Get the count of files dropped.
            uCount = DragQueryFile((HDROP)medium.hGlobal, (UINT)-1, NULL, 0);

            // Get the first file name from the CF_HDROP.
            if (uCount)
                DragQueryFile((HDROP)medium.hGlobal, 0, m_szFile, 
                              sizeof(m_szFile)/sizeof(TCHAR));

            ReleaseStgMedium(&medium);
        }
    }

    // Duplicate the registry handle. 
    if (hRegKey) 
        RegOpenKeyEx(hRegKey, nullptr, 0L, MAXIMUM_ALLOWED, &m_hRegKey); 
    return S_OK; 
}
```

CSampleExtHandler è il nome della classe utilizzata per implementare l'interfaccia. Le **variabili \_ m pIDFolder**, **m \_ pDataObject**, **m \_ szFileName** e **m \_ hRegKey** sono variabili private usate per archiviare le informazioni passate. Per semplicità, in questo esempio si presuppone che l'oggetto dati conterrà un solo nome file. Una volta recuperata la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) dall'oggetto dati, [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) viene utilizzato per estrarre il nome file dal membro **Media. hGlobal** della struttura **FORMATETC** . Se viene passata una chiave del registro di sistema, il metodo usa [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) per aprire la chiave e assegna l'handle a **m \_ hRegKey**.

### <a name="infotip-customization"></a>Personalizzazione di infotip

Esistono due modi per personalizzare infotip:

-   Implementare un oggetto che supporta [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) e quindi registrare l'oggetto sotto la sottochiave corretta nel registro di sistema. vedere la sezione relativa alla [registrazione dei gestori estensioni della shell](#registering-shell-extension-handlers) .
-   Specificare una stringa fissa o un elenco di proprietà di file specifiche da visualizzare.

Per visualizzare una stringa fissa per un'estensione dello spazio dei nomi, creare una voce denominata `InfoTip` nella chiave *{CLSID}* dell'estensione dello spazio dei nomi. Impostare il valore di tale voce su una stringa letterale che si vuole visualizzare, come illustrato in questo esempio, o una stringa indiretta che specifica una risorsa e un indice all'interno di tale risorsa (per finalità di localizzazione).

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Per visualizzare una stringa fissa per un tipo di file, creare una voce denominata `InfoTip` nella chiave *ProgID* del tipo di file. Impostare il valore di tale voce su una stringa letterale che si desidera visualizzare o su una stringa indiretta che specifichi una risorsa e un indice all'interno di tale risorsa (per finalità di localizzazione), come illustrato in questo esempio.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = Resource.dll, 3
```

Se si vuole che la shell visualizzi proprietà specifiche del file in infotip per un tipo di file specifico, creare una voce denominata `InfoTip` nella chiave *ProgID* per quel tipo di file. Impostare il valore di tale voce come elenco delimitato da punti e virgola di nomi di proprietà canoniche, coppie di identificatori di formato (FMTID)/Property Identifier (PID) o entrambi. Questo valore deve iniziare con "prop:" per identificarlo come stringa di elenco delle proprietà. Se si omette "prop:", il valore viene considerato come stringa letterale e visualizzato come tale.

Nell'esempio seguente, *propName* è un nome di proprietà canonico (ad esempio System. date) e *{fmtid}, PID* è una coppia [**fmtid/PID**](./objects.md) .

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = prop:propname;propname;{fmtid},pid;{fmtid},pid
```

È possibile utilizzare i nomi di proprietà seguenti:



| Nome proprietà    | Descrizione                   | Recuperato da                                                                             |
|------------------|-------------------------------|--------------------------------------------------------------------------------------------|
| Autore           | Autore del documento        | [**autore di PIDSI \_**](../stg/the-summary-information-property-set.md)                              |
| Titolo            | Titolo del documento         | [**\_titolo PIDSI**](../stg/the-summary-information-property-set.md)                               |
| Oggetto          | Riepilogo oggetto               | [**\_oggetto PIDSI**](../stg/the-summary-information-property-set.md)                             |
| Commento          | Commenti del documento             | [**PIDSI \_ Proprietà commento**](../stg/the-summary-information-property-set.md) o cartella/driver |
| PageCount        | Numero di pagine               | [**\_PageCount PIDSI**](../stg/the-summary-information-property-set.md)                           |
| Nome             | Nome descrittivo                 | Visualizzazione cartelle standard                                                                       |
| OriginalLocation | Percorso del file originale     | Cartella valigetta e cartella Cestino                                                    |
| DateDeleted      | Il file di data è stato eliminato         | Cartella Cestino                                                                         |
| Tipo             | Tipo di file                  | Visualizzazione Dettagli cartella standard                                                               |
| Dimensione             | Dimensioni del file                  | Visualizzazione Dettagli cartella standard                                                               |
| SyncCopyIn       | Uguale a OriginalLocation      | Uguale a OriginalLocation                                                                   |
| Ultima modifica         | Data ultima modifica            | Visualizzazione Dettagli cartella standard                                                               |
| Data di creazione          | Data creazione                  | Visualizzazione Dettagli cartella standard                                                               |
| Accedere         | Data ultimo accesso            | Visualizzazione Dettagli cartella standard                                                               |
| InCartella         | Directory che contiene il file | Risultati della ricerca nei documenti                                                                    |
| Classifica             | Qualità della corrispondenza di ricerca       | Risultati della ricerca nei documenti                                                                    |
| FreeSpace        | Spazio di archiviazione disponibile       | Unità disco                                                                                |
| NumberOfVisits   | Numero di visite              | Cartella Preferiti                                                                           |
| Attributi       | Attributi file               | Visualizzazione Dettagli cartella standard                                                               |
| Company          | Nome azienda                  | [**\_società PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)    |
| Category         | Categoria documento             | [**\_categoria PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Copyright        | Copyright del supporto               | [**\_Copyright PIDMSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| HTMLInfoTipFile  | File InfoTip HTML             | File Desktop.ini per la cartella                                                                |



 

## <a name="enhancing-windows-search-with-shell-extension-handlers"></a>Miglioramento della ricerca di Windows con gestori di estensioni della shell

I gestori di estensioni della shell possono essere usati per migliorare l'esperienza utente fornita da un gestore di protocollo di ricerca di Windows. Per abilitare tali miglioramenti, il gestore dell'estensione della shell di supporto deve essere progettato per l'integrazione con il gestore di protocollo di ricerca come origine dati. Per informazioni su come migliorare un gestore del protocollo di ricerca di Windows tramite l'integrazione con un gestore dell'estensione della shell, vedere [aggiunta di icone, anteprime e menu di scelta rapida](../search/-search-3x-wds-ph-ui-extensions.md). Per ulteriori informazioni sui gestori del protocollo di ricerca di Windows, vedere [sviluppo di gestori di protocollo](../search/-search-3x-wds-phaddins.md).

## <a name="registering-shell-extension-handlers"></a>Registrazione di gestori estensioni della shell

Un oggetto gestore dell'estensione della shell deve essere registrato prima che la shell possa usarlo. Questa sezione è una descrizione generale di come registrare un gestore dell'estensione della shell.

Ogni volta che si crea o si modifica un gestore dell'estensione della shell, è importante notificare al sistema che è stata apportata una modifica a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specificando l'evento **SHCNE \_ ASSOCCHANGED** . Se non si chiama **SHChangeNotify**, è possibile che la modifica non venga riconosciuta fino al riavvio del sistema.

Come per tutti gli oggetti COM, è necessario creare un GUID per il gestore usando uno strumento come UUIDGEN.exe. Creare una chiave in **HKEY \_ classi \_ radice** \\ **CLSID** il cui nome è il formato stringa del GUID. Poiché i gestori di estensioni della shell sono server in-process, è necessario creare una chiave **InprocServer32** sotto la chiave GUID con il valore predefinito impostato sul percorso della dll del gestore. Utilizzare il modello di threading dell'Apartment.

Ogni volta che la shell esegue un'azione che può coinvolgere un gestore dell'estensione della shell, verifica la chiave del registro di sistema appropriata. La chiave in cui viene registrato un gestore di estensione controlla quindi quando verrà chiamato. Ad esempio, è pratica comune avere un gestore di menu di scelta rapida chiamato quando la shell Visualizza un menu di scelta rapida per un membro di un [tipo di file](fa-file-types.md). In questo caso, il gestore deve essere registrato sotto la chiave **ProgID** del tipo di file.

### <a name="handler-names"></a>Nomi dei gestori

Per abilitare un gestore dell'estensione della shell, creare una sottochiave con il nome della sottochiave del gestore (vedere di seguito) nella sottochiave **ShellEx** del **ProgID** (per i tipi di file) o il nome del tipo di oggetto della shell (per [gli oggetti shell predefiniti](#predefined-shell-objects)).

Ad esempio, se si desidera registrare un gestore dell'estensione del menu di scelta rapida per il programma. 1, iniziare creando la sottochiave seguente:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Per i gestori seguenti, creare una sottochiave sotto la chiave "Handler nome sottochiave", il cui nome è la versione in formato stringa del CLSID dell'estensione della shell. È possibile registrare più estensioni con la chiave del nome della sottochiave del gestore creando più sottochiavi.



| Gestore                                               | Interfaccia          | Nome sottochiave gestore       |
|-------------------------------------------------------|--------------------|---------------------------|
| Gestore del menu di scelta rapida                                 | IContextMenu       | **ContextMenuHandlers**   |
| Gestore CopyHook                                      | ICopyHook          | **CopyHookHandlers**      |
| Gestore di trascinamento della selezione                                 | IContextMenu       | **DragDropHandlers**      |
| Gestore della finestra delle proprietà                                | IShellPropSheetExt | **PropertySheetHandlers** |
| Gestore del provider di colonne (deprecato in Windows Vista) | IColumnProvider    | **ColumnHandlers**        |



 

Per i gestori seguenti, il valore predefinito della chiave del nome della sottochiave del gestore è la versione in formato stringa del CLSID dell'estensione della shell. Per questi gestori è possibile registrare solo un'estensione.



| Gestore                 | Interfaccia                                         | Nome sottochiave gestore                        |
|-------------------------|---------------------------------------------------|--------------------------------------------|
| Gestore dati            | IDataObject                                       | **DataHandler**                            |
| Gestore di trascinamento            | IDropTarget                                       | **DropHandler**                            |
| Gestore icone            | IExtractIconA/W                                   | **IconHandler**                            |
| Gestore immagini           | IExtractImage                                     | **{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}** |
| Gestore immagini di anteprima | IThumbnailProvider                                | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Gestore della finestra popup         | IQueryInfo                                        | **{00021500-0000-0000-C000-000000000046}** |
| Collegamento della shell (ANSI)      | IShellLinkA                                       | **{000214EE-0000-0000-C000-000000000046}** |
| Collegamento Shell (UNICODE)    | IShellLinkW                                       | **{000214F9-0000-0000-C000-000000000046}** |
| Archiviazione strutturata      | IStorage                                          | **{0000000B-0000-0000-C000-000000000046}** |
| Metadati                | IPropertyStore                                    | **Gestoreproprietà**                        |
| Metadati                | IPropertySetStorage (deprecato in Windows Vista) | **Gestoreproprietà**                        |
| Aggiungi a menu Start       | IStartMenuPinnedList                              | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Aggiungere alla barra delle applicazioni          |                                                   | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Le sottochiavi specificate per aggiungere **pin al menu Start** e aggiungere **alla barra delle applicazioni** al menu di scelta rapida di un elemento sono necessarie solo per i tipi di file che includono la voce di [collegamento](./links.md) .

Il supporto per i gestori del provider di colonne è stato rimosso in Windows Vista. Inoltre, a partire da Windows Vista, [**IPropertySetStorage**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) è stato deprecato a favore di [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

Sebbene [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) rimanga supportato, è preferibile [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) per Windows Vista e versioni successive.

### <a name="predefined-shell-objects"></a>Oggetti shell predefiniti

La shell definisce oggetti aggiuntivi sotto **la \_ \_ radice delle classi HKEY** che possono essere estese in modo analogo ai tipi di file. Per aggiungere un gestore della finestra delle proprietà per tutti i file, ad esempio, è possibile eseguire la registrazione con la chiave **PropertySheetHandlers** .

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

La tabella seguente fornisce le varie sottochiavi della **\_ \_ radice delle classi HKEY** in cui è possibile registrare i gestori di estensione. Si noti che molti gestori di estensioni non possono essere registrati in tutte le sottochiavi elencate. Per ulteriori informazioni, vedere la documentazione del gestore specifico.



| Sottochiave                    | Descrizione                                                          | Possibili gestori                                | Versione |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|---------|
| **\** _                    | Tutti i file                                                            | Menu di scelta rapida, finestra delle proprietà, verbi (vedere di seguito) | Tutti     |
| _ *AllFileSystemObjects**  | Tutti i file e le cartelle di file                                           | Menu di scelta rapida, finestra delle proprietà, verbi             | 4,71    |
| **Cartella**                | Tutte le cartelle                                                          | Menu di scelta rapida, finestra delle proprietà, verbi             | Tutti     |
| **Directory**             | Cartelle di file                                                         | Menu di scelta rapida, finestra delle proprietà, verbi             | Tutti     |
| **\\Sfondo directory** | Sfondo cartella file                                               | Solo menu di scelta rapida                               | 4,71    |
| **Unità**                 | Tutte le unità in computer, ad esempio "C: \\ "                             | Menu di scelta rapida, finestra delle proprietà, verbi             | Tutti     |
| **Network**               | Intera rete (in risorse di rete)                             | Menu di scelta rapida, finestra delle proprietà, verbi             | Tutti     |
| **Tipo di rete \\\\\#**     | Tutti gli oggetti di tipo \# (vedere di seguito)                                   | Menu di scelta rapida, finestra delle proprietà, verbi             | 4,71    |
| **NetShare**              | Tutte le condivisioni di rete                                                   | Menu di scelta rapida, finestra delle proprietà, verbi             | 4,71    |
| **NetServer**             | Tutti i server di rete                                                  | Menu di scelta rapida, finestra delle proprietà, verbi             | 4,71    |
| *\_Nome provider di rete \_* | Tutti gli oggetti forniti dal provider di rete "*Network \_ provider \_ Name*" | Menu di scelta rapida, finestra delle proprietà, verbi             | Tutti     |
| **Stampanti**              | Tutte le stampanti                                                         | Menu di scelta rapida, finestra delle proprietà                    | Tutti     |
| **AudioCD**               | CD audio nell'unità CD                                                 | Solo verbi                                       | Tutti     |
| **DVD**                   | Unità DVD (Windows 2000)                                             | Menu di scelta rapida, finestra delle proprietà, verbi             | 4,71    |



 

Note:

-   Per accedere al menu di scelta rapida dello sfondo della cartella file, fare clic con il pulsante destro del mouse all'interno di una cartella di file, ma non su uno dei contenuti della cartella.
-   I "verbi" sono comandi speciali registrati nel verbo della shell della sottochiave **\_ \_ radice delle classi HKEY** \\  \\  \\  .
-   Per il tipo di **rete** \\  \\ **\#** , " \# " è un codice del tipo di provider di rete in decimale. Il codice del tipo di provider di rete è la parola più elevata di un tipo di rete. L'elenco dei tipi di rete viene specificato nel file di intestazione Winnetwk. h (WNNC \_ net \_ \* Values). Ad esempio, WNNC \_ net \_ Shiva è 0x00330000, quindi la chiave del tipo corrispondente sarà **HKEY \_ classi \_ radice** tipo di \\ **rete** \\  \\ **51** .
-   "*Network \_ provider \_ Name*" è un nome di provider di rete come specificato da [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), con gli spazi convertiti in caratteri di sottolineatura. Ad esempio, se è installato il provider rete Microsoft Networking, il nome del provider è "rete Microsoft Windows" e il *nome del \_ provider \_ di rete* corrispondente è **\_ \_ rete Microsoft Windows**.

### <a name="example-of-an-extension-handler-registration"></a>Esempio di registrazione di un gestore estensioni

Per abilitare un particolare gestore, creare una sottochiave nella chiave del tipo di gestore dell'estensione con il nome del gestore. La shell non usa il nome del gestore, ma deve essere diverso da tutti gli altri nomi sotto tale sottochiave di tipo. Impostare il valore predefinito della sottochiave Name sul formato stringa del GUID del gestore.

Nell'esempio seguente vengono illustrate le voci del registro di sistema che consentono il menu di scelta rapida e i gestori dell'estensione della finestra delle proprietà, utilizzando un esempio di file MYP:

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

La procedura di registrazione descritta in questa sezione deve essere seguita per tutti i sistemi Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per l'implementazione di estensioni In-Process](shell-and-managed-code.md)
</dt> </dl>

 

 
