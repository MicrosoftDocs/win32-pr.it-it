---
description: Le funzionalità della shell possono essere estese con voci del Registro di sistema e .ini file.
ms.assetid: 74a81e4f-7357-4901-a118-ba44e8892f25
title: Creazione di gestori di estensione della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729fad22eb86e9c32e43c459d7a30b11f68d8d06360b60cee373bb3f74d3749f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032559"
---
# <a name="creating-shell-extension-handlers"></a>Creazione di gestori di estensione della shell

Le funzionalità della shell possono essere estese con voci del Registro di sistema e .ini file. Sebbene questo approccio all'estensione della shell sia semplice e adeguato per molti scopi, è limitato. Ad esempio, se si usa il Registro di sistema per specificare un'icona personalizzata per un tipo di file, verrà visualizzata la stessa icona per ogni file di quel tipo. L'estensione della shell con il Registro di sistema non consente di variare l'icona per file diversi dello stesso tipo. Altri aspetti della shell, ad  esempio la finestra delle proprietà Proprietà che può essere visualizzata quando si fa clic con il pulsante destro del mouse su un file, non possono essere modificati con il Registro di sistema.

Un approccio più potente e flessibile per estendere la shell consiste nell'implementare i *gestori di estensioni della shell*. Questi gestori possono essere implementati per un'ampia gamma di azioni che la shell può eseguire. Prima di eseguire l'azione, la shell esegue una query sul gestore dell'estensione, offrendo la possibilità di modificare l'azione. Un esempio comune è un gestore di estensione del menu di scelta rapida. Se ne viene implementato uno per un tipo di file, verrà eseguita una query ogni volta che si fa clic con il pulsante destro del mouse su uno dei file. Il gestore può quindi specificare voci di menu aggiuntive file per file, anziché avere lo stesso set per l'intero tipo di file.

Questo documento illustra come implementare i gestori di estensioni che consentono di modificare un'ampia gamma di azioni della shell. I gestori seguenti sono associati a un particolare tipo di file e consentono di specificare file per file:



| Gestore                                               | Descrizione                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestore del menu di scelta rapida](context-menu-handlers.md)    | Chiamato prima che venga visualizzato il menu di scelta rapida di un file. Consente di aggiungere voci al menu di scelta rapida file per file.                                               |
| [Gestore dati](how-to-create-data-handlers.md)       | Chiamato quando viene eseguita un'operazione di trascinamento della selezione su oggetti dragShell. Consente di fornire formati di Appunti aggiuntivi all'obiettivo di rilascio.                        |
| [Gestore di eliminazione](how-to-create-drop-handlers.md)       | Chiamato quando un oggetto dati viene trascinato su un file. Consente di convertire un file in un obiettivo di rilascio.                                                          |
| [Gestore dell'icona](how-to-create-icon-handlers.md)       | Chiamato prima che venga visualizzata l'icona di un file. Consente di sostituire l'icona predefinita del file con un'icona personalizzata per ogni file.                                    |
| [Gestore della finestra delle proprietà](propsheet-handlers.md)      | Chiamato prima che venga visualizzata la **finestra delle** proprietà Proprietà di un oggetto. Consente di aggiungere o sostituire pagine.                                                              |
| [**Gestore dell'immagine di anteprima**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Fornisce un'immagine per rappresentare l'elemento.                                                                                                                                   |
| [**Gestore della finestra popup**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Fornisce testo popup quando l'utente passa il puntatore del mouse sull'oggetto .                                                                                               |
| [**Gestore di metadati**](/windows/win32/api/propsys/nn-propsys-ipropertystore)     | Fornisce accesso in lettura e scrittura ai metadati (proprietà) archiviati in un file. Può essere usato per estendere la visualizzazione Dettagli, le descrizioni comandi, la pagina delle proprietà e le funzionalità di raggruppamento. |



 

Altri gestori non sono associati a un particolare tipo di file, ma vengono chiamati prima di alcune operazioni della shell:



| Gestore                                                            | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestore delle colonne](../lwef/column-handlers.md)                             | Chiamato da Windows Explorer prima di visualizzare la visualizzazione Dettagli di una cartella. Consente di aggiungere colonne personalizzate alla visualizzazione Dettagli.        |
| [Gestore hook di copia](how-to-create-copy-hook-handlers.md)          | Chiamato quando una cartella o un oggetto stampante sta per essere spostato, copiato, eliminato o rinominato. Consente di approvare o veto l'operazione.   |
| [Gestore di trascinamento della selezione](context-menu-handlers.md)                 | Chiamato quando un file viene trascinato con il pulsante destro del mouse. Consente di modificare il menu di scelta rapida visualizzato.                     |
| [Gestore di sovrimpressione dell'icona](how-to-implement-icon-overlay-handlers.md) | Chiamato prima che venga visualizzata l'icona di un file. Consente di specificare una sovrimpressione per l'icona del file.                                          |
| [Gestore della ricerca](../lwef/search-handlers.md)                             | Chiamato per avviare un motore di ricerca. Consente di implementare un motore di ricerca personalizzato accessibile dal menu **Start** o Windows Explorer. |



 

I dettagli su come implementare gestori di estensioni specifici sono descritti nelle sezioni elencate in precedenza. Nella parte restante di questo documento vengono illustrati alcuni problemi di implementazione comuni a tutti i gestori di estensioni della shell.

-   [Implementazione di gestori di estensioni della shell](#implementing-shell-extension-handlers)
    -   [Implementazione di IPersistFile](#implementing-ipersistfile)
    -   [Implementazione di IShellExtInit](#implementing-ishellextinit)
    -   [Personalizzazione delle descrizioni comandi](#infotip-customization)
-   [Miglioramento della Windows ricerca con i gestori di estensioni della shell](#enhancing-windows-search-with-shell-extension-handlers)
-   [Registrazione dei gestori di estensioni della shell](#registering-shell-extension-handlers)
    -   [Nomi dei gestori](#handler-names)
    -   [Oggetti shell predefiniti](#predefined-shell-objects)
    -   [Esempio di registrazione di un gestore di estensione](#example-of-an-extension-handler-registration)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-shell-extension-handlers"></a>Implementazione di gestori di estensioni della shell

Gran parte dell'implementazione di un oggetto gestore dell'estensione shell dipende dal tipo. Esistono tuttavia alcuni elementi comuni. Questa sezione illustra gli aspetti dell'implementazione condivisi da tutti i gestori di estensioni della shell.

Molti gestori di estensioni della shell sono oggetti Component Object Model (COM) in-process. È necessario assegnare un GUID e registrarli come descritto in Registrazione dei gestori delle estensioni della shell. Vengono implementati come DLL e devono esportare le funzioni standard seguenti:

-   [**DllMain**](../dlls/dllmain.md). Punto di ingresso standard alla DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Espone l'oggetto class factory.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM chiama questa funzione per determinare se l'oggetto sta servendo client. In caso contrario, il sistema può scaricare la DLL e liberare la memoria associata.

Come tutti gli oggetti COM, i gestori di estensioni della shell devono implementare [**un'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e un [class factory](../com/implementing-iclassfactory.md). La maggior parte dei gestori di estensioni deve implementare anche [**un'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) in Windows XP o versioni precedenti. Sono stati sostituiti [**da IInitializeWithStream,**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) e [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista. La shell usa queste interfacce per inizializzare il gestore.

[**L'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) deve essere implementata nel modo seguente:

-   Gestori di dati
-   Gestori di eliminazione

In passato, i gestori di icone erano necessari anche per implementare [**IPersistFile,**](/windows/win32/api/objidl/nn-objidl-ipersistfile)ma questo non è più vero. Per i gestori di icone, **IPersistFile** è ora facoltativo e sono preferibili altre interfacce, ad esempio [**IInitializeWithItem.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)

[**L'interfaccia IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) deve essere implementata nel modo seguente:

-   Gestori del menu di scelta rapida
-   Gestori di trascinamento della selezione
-   Gestori della finestra delle proprietà

### <a name="implementing-ipersistfile"></a>Implementazione di IPersistFile

[**L'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) consente il caricamento o il salvataggio di un oggetto in un file su disco. Include sei metodi oltre a [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown)cinque dei propri e il metodo [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) che eredita da [**IPersist.**](/windows/win32/api/objidl/nn-objidl-ipersist) Con le estensioni shell, **IPersist** viene usato solo per inizializzare un oggetto gestore dell'estensione shell. Poiché in genere non è necessario leggere o scrivere sul disco, solo i **metodi GetClassID** e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) richiedono un'implementazione nontoken.

Shell chiama [**prima GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e la funzione restituisce l'identificatore di classe (CLSID) dell'oggetto gestore estensioni. Shell chiama quindi [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) e passa due valori. Il primo, *pszFileName*, è una stringa Unicode con il nome del file o della cartella su cui Shell sta per operare. Il secondo è *dwMode*, che indica la modalità di accesso ai file. Poiché in genere non è necessario accedere ai file, *dwMode* è in genere zero. Il metodo archivia questi valori in base alle esigenze per riferimenti successivi.

Il frammento di codice seguente illustra come un tipico gestore di estensioni shell implementa i [**metodi GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) [**e Load.**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) È progettato per gestire ANSI o Unicode. CLSID SampleExtHandler è il GUID dell'oggetto gestore di estensioni e CSampleExtHandler è il nome della classe usata per \_ implementare l'interfaccia. Le **variabili m \_ szFileName** e **m \_ dwMode** sono variabili private usate per archiviare il nome del file e i flag di accesso.


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

[**L'interfaccia IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) ha un solo metodo, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Il metodo dispone di tre parametri che shell può usare per passare vari tipi di informazioni. I valori passati dipendono dal tipo di gestore e alcuni possono essere impostati su **NULL.**

-   *pIDFolder contiene* il puntatore di una cartella a un elenco di identificatori di elemento (PIDL). Per le estensioni della finestra delle proprietà, è **NULL.** Per le estensioni del menu di scelta rapida, è il file PIDL della cartella che contiene l'elemento di cui viene visualizzato il menu di scelta rapida. Per i gestori di trascinamento della selezione non predefiniti, si tratta del FILE PIDL della cartella di destinazione.
-   *pDataObject contiene* un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) di un oggetto dati. L'oggetto dati contiene uno o più nomi di file in [ \_ formato CF HDROP.](dragdrop.md)
-   *hRegKey contiene* una chiave del Registro di sistema per l'oggetto file o il tipo di cartella.

Il [**metodo IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) archivia il nome file, il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) e la chiave del Registro di sistema in base alle esigenze per un uso successivo. Il frammento di codice seguente illustra un'implementazione di **IShellExtInit::Initialize**. Per semplicità, questo esempio presuppone che l'oggetto dati contenga un solo file. In generale, potrebbe contenere più file che dovranno essere estratti.


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

CSampleExtHandler è il nome della classe usata per implementare l'interfaccia . Le **variabili m \_ pIDFolder**, **m \_ pDataObject**, **m \_ szFileName** e **m \_ hRegKey** sono variabili private usate per archiviare le informazioni passate. Per semplicità, questo esempio presuppone che solo un nome file verrà mantenuto dall'oggetto dati. Dopo il [**recupero della struttura FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) dall'oggetto dati, viene usato [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) per estrarre il nome file dal membro **medium.hGlobal** della struttura **FORMATETC.** Se viene passata una chiave del Registro di sistema, il metodo usa [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) per aprire la chiave e assegna l'handle **a m \_ hRegKey**.

### <a name="infotip-customization"></a>Personalizzazione del suggerimento

Esistono due modi per personalizzare le infotip:

-   Implementare un oggetto che [**supporti IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) e quindi registrarlo nella sottochiave appropriata nel Registro di sistema (vedere [Registrazione dei gestori](#registering-shell-extension-handlers) delle estensioni della shell di seguito).
-   Specificare una stringa fissa o un elenco di proprietà di file specifiche da visualizzare.

Per visualizzare una stringa fissa per un'estensione dello spazio dei nomi, creare una voce denominata nella chiave `InfoTip` *{CLSID}* dell'estensione dello spazio dei nomi. Impostare il valore di tale voce in modo che sia la stringa letterale da visualizzare, come illustrato in questo esempio, o una stringa indiretta che specifica una risorsa e un indice all'interno di tale risorsa (a scopo di localizzazione).

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Per visualizzare una stringa fissa per un tipo di file, creare una voce `InfoTip` denominata nella *chiave ProgID* di tale tipo di file. Impostare il valore di tale voce in modo che sia la stringa letterale da visualizzare o una stringa indiretta che specifica una risorsa e un indice all'interno di tale risorsa (a scopo di localizzazione), come illustrato in questo esempio.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = Resource.dll, 3
```

Se si vuole che Shell visualizza proprietà di file specifiche nel suggerimento per un tipo di file specifico, creare una voce denominata nella chiave `InfoTip` *ProgID* per tale tipo di file. Impostare il valore di tale voce su un elenco delimitato da punto e virgola di nomi di proprietà canonici, coppie di identificatori di formato (FMTID)/identificatore di proprietà (PID) o entrambi. Questo valore deve iniziare con "prop:" per identificarlo come stringa dell'elenco delle proprietà. Se si omette "prop:", il valore viene visualizzato come stringa letterale e visualizzato come tale.

Nell'esempio seguente *propname* è un nome di proprietà canonico (ad esempio System.Date) e *{fmtid}, pid* è una coppia [**FMTID/PID.**](./objects.md)

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = prop:propname;propname;{fmtid},pid;{fmtid},pid
```

È possibile usare i nomi di proprietà seguenti:



| Nome proprietà    | Descrizione                   | Recuperato da                                                                             |
|------------------|-------------------------------|--------------------------------------------------------------------------------------------|
| Autore           | Autore del documento        | [**AUTORE \_ PIDSI**](../stg/the-summary-information-property-set.md)                              |
| Titolo            | Titolo del documento         | [**TITOLO \_ PIDSI**](../stg/the-summary-information-property-set.md)                               |
| Oggetto          | Riepilogo dell'oggetto               | [**SOGGETTO \_ PIDSI**](../stg/the-summary-information-property-set.md)                             |
| Commento          | Commenti del documento             | [**PIDSI \_ COMMENT**](../stg/the-summary-information-property-set.md) o proprietà cartella/driver |
| PageCount        | Numero di pagine               | [**PIDSI \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                           |
| Nome             | Nome descrittivo                 | Visualizzazione cartelle standard                                                                       |
| OriginalLocation | Percorso del file originale     | Cartella Briefcase e Cestino cartella                                                    |
| DateDeleted      | Il file di data è stato eliminato         | Cestino cartella                                                                         |
| Tipo             | Tipo di file                  | Visualizzazione dei dettagli della cartella standard                                                               |
| Dimensione             | Dimensioni del file                  | Visualizzazione dei dettagli della cartella standard                                                               |
| SyncCopyIn       | Uguale a OriginalLocation      | Uguale a OriginalLocation                                                                   |
| Ultima modifica         | Data ultima modifica            | Visualizzazione dei dettagli della cartella standard                                                               |
| Data di creazione          | Data creazione                  | Visualizzazione dei dettagli della cartella standard                                                               |
| Accedere         | Data dell'ultimo accesso            | Visualizzazione dei dettagli della cartella standard                                                               |
| InFolder         | Directory contenente il file | Documentare i risultati della ricerca                                                                    |
| Classifica             | Qualità della corrispondenza di ricerca       | Documentare i risultati della ricerca                                                                    |
| FreeSpace        | Spazio di archiviazione disponibile       | Unità disco                                                                                |
| NumberOfVisits   | Numero di visite              | Cartella Preferiti                                                                           |
| Attributi       | Attributi file               | Visualizzazione dei dettagli della cartella standard                                                               |
| Company          | Nome azienda                  | [**SOCIETÀ PIDDSI \_**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)    |
| Category         | Categoria di documenti             | [**CATEGORIA \_ PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Copyright        | Copyright multimediale               | [**PIDMSI \_ COPYRIGHT**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| HTMLInfoTipFile  | File di suggerimento informazioni HTML             | Desktop.ini file per la cartella                                                                |



 

## <a name="enhancing-windows-search-with-shell-extension-handlers"></a>Miglioramento della Windows ricerca con i gestori di estensioni della shell

I gestori di estensioni della shell possono essere usati per migliorare l'esperienza utente fornita da un Windows del protocollo di ricerca. Per abilitare tali miglioramenti, il gestore dell'estensione shell di supporto deve essere progettato per l'integrazione con il gestore del protocollo di ricerca come origine dati. Per informazioni su come migliorare un gestore del protocollo Windows ricerca tramite l'integrazione con un gestore di estensioni della shell, vedere Aggiunta di icone, anteprime e [menu di scelta rapida.](../search/-search-3x-wds-ph-ui-extensions.md) Per altre informazioni sui gestori Windows di protocollo di ricerca, vedere [Sviluppo di gestori di protocollo.](../search/-search-3x-wds-phaddins.md)

## <a name="registering-shell-extension-handlers"></a>Registrazione dei gestori di estensioni della shell

Un oggetto gestore dell'estensione shell deve essere registrato prima che shell possa usarlo. Questa sezione illustra in generale come registrare un gestore dell'estensione della shell.

Ogni volta che si crea o si modifica un gestore dell'estensione shell, è importante notificare al sistema che è stata apportata una modifica con [**SHChangeNotify,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)specificando l'evento **SHCNE \_ ASSOCCHANGED.** Se non si chiama **SHChangeNotify,** la modifica potrebbe non essere riconosciuta fino al riavvio del sistema.

Come per tutti gli oggetti COM, è necessario creare un GUID per il gestore usando uno strumento come UUIDGEN.exe. Creare una chiave in **HKEY \_ CLASSES \_ ROOT** \\ **CLSID** il cui nome è il formato stringa del GUID. Poiché i gestori delle estensioni della shell sono server in-process, è necessario creare una chiave **InProcServer32** sotto la chiave GUID con il valore predefinito impostato sul percorso della DLL del gestore. Usare il modello di threading Apartment.

Ogni volta che la shell esegue un'azione che può coinvolgere un gestore dell'estensione della shell, controlla la chiave del Registro di sistema appropriata. La chiave con cui viene registrato un gestore di estensione controlla quindi quando verrà chiamato. Ad esempio, è pratica comune avere un gestore del menu di scelta rapida chiamato quando nella shell viene visualizzato un menu di scelta rapida per un membro di un [tipo di file](fa-file-types.md). In questo caso, il gestore deve essere registrato nella chiave **ProgID** del tipo di file.

### <a name="handler-names"></a>Nomi dei gestori

Per abilitare un gestore dell'estensione shell, creare una sottochiave con il nome della sottochiave del gestore (vedere di seguito) nella sottochiave **ShellEx** del **ProgID** (per i tipi di file) o del nome del tipo di oggetto shell (per [Oggetti shell](#predefined-shell-objects)predefiniti).

Ad esempio, se si vuole registrare un gestore dell'estensione del menu di scelta rapida per MyProgram.1, creare prima di tutto la sottochiave seguente:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Per i gestori seguenti, creare una sottochiave sotto la chiave "Handler Subkey name" il cui nome è la versione stringa del CLSID dell'estensione shell. È possibile registrare più estensioni nella chiave del nome della sottochiave del gestore creando più sottochiavi.



| Gestore                                               | Interfaccia          | Nome della sottochiave del gestore       |
|-------------------------------------------------------|--------------------|---------------------------|
| Gestore del menu di scelta rapida                                 | IContextMenu       | **ContextMenuHandlers**   |
| Gestore di copyhook                                      | ICopyHook          | **CopyHookHandlers**      |
| Gestore di trascinamento della selezione                                 | IContextMenu       | **DragDropHandlers**      |
| Gestore della finestra delle proprietà                                | IShellPropSheetExt | **PropertySheetHandlers** |
| Gestore del provider di colonne (deprecato in Windows Vista) | IColumnProvider    | **ColumnHandlers**        |



 

Per i gestori seguenti, il valore predefinito della chiave "Handler Subkey Name" è la versione stringa del CLSID dell'estensione shell. Per questi gestori è possibile registrare una sola estensione.



| Gestore                 | Interfaccia                                         | Nome della sottochiave del gestore                        |
|-------------------------|---------------------------------------------------|--------------------------------------------|
| Gestore dati            | Idataobject                                       | **DataHandler**                            |
| Gestore di eliminazione            | Idroptarget                                       | **DropHandler**                            |
| Gestore dell'icona            | IExtractIconA/W                                   | **IconHandler**                            |
| Gestore dell'immagine           | IExtractImage                                     | **{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}** |
| Gestore dell'immagine di anteprima | IThumbnailProvider                                | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Gestore della finestra popup         | IQueryInfo                                        | **{00021500-0000-0000-C000-000000000046}** |
| Collegamento alla shell (ANSI)      | IShellLinkA                                       | **{000214EE-0000-0000-C000-000000000046}** |
| Collegamento alla shell (UNICODE)    | IShellLinkW                                       | **{000214F9-0000-0000-C000-000000000046}** |
| Archiviazione strutturata      | Istorage                                          | **{0000000B-0000-0000-C000-000000000046}** |
| Metadati                | Ipropertystore                                    | **PropertyHandler**                        |
| Metadati                | IPropertySetStorage (deprecato in Windows Vista) | **PropertyHandler**                        |
| Aggiungi al menu Start       | IStartMenuPinnedList                              | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Aggiungere alla barra delle applicazioni          |                                                   | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Le sottochiavi specificate per aggiungere Aggiungi  al **menu Start** e Aggiungi alla barra delle applicazioni al menu di scelta rapida di un elemento sono necessarie solo per i tipi di file che includono la [voce IsShortCut.](./links.md)

Il supporto per i gestori di provider di colonne è stato rimosso in Windows Vista. Inoltre, a Windows Vista, [**IPropertySetStorage**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) è stato deprecato a favore di [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Anche [**se IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) rimane supportato, [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) è preferibile per Windows Vista e versioni successive.

### <a name="predefined-shell-objects"></a>Oggetti shell predefiniti

La shell definisce oggetti aggiuntivi in **HKEY \_ CLASSES \_ ROOT** che possono essere estesi allo stesso modo dei tipi di file. Ad esempio, per aggiungere un gestore della finestra delle proprietà per tutti i file, è possibile eseguire la registrazione sotto la **chiave PropertySheetHandlers.**

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

La tabella seguente fornisce le varie sottochiavi di **HKEY \_ CLASSES \_ ROOT** in cui è possibile registrare i gestori di estensione. Si noti che molti gestori di estensioni non possono essere registrati in tutte le sottochiavi elencate. Per altri dettagli, vedere la documentazione del gestore specifico.



| Sottochiave                    | Descrizione                                                          | Possibili gestori                                | Versione |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|---------|
| **\***                    | Tutti i file                                                            | Menu di scelta rapida, finestra delle proprietà, verbi (vedere di seguito) | Tutti     |
| **AllFileSystemObjects**  | Tutti i file e le cartelle di file                                           | Menu di scelta rapida, finestra delle proprietà, verbi             | 4.71    |
| **Cartella**                | Tutte le cartelle                                                          | Menu di scelta rapida, finestra delle proprietà, verbi             | Tutti     |
| **Directory**             | Cartelle file                                                         | Menu di scelta rapida, finestra delle proprietà, verbi             | Tutti     |
| **Sfondo \\ della directory** | Sfondo della cartella file                                               | Solo menu di scelta rapida                               | 4.71    |
| **Unità**                 | Tutte le unità in MyComputer, ad esempio "C: \\ "                             | Menu di scelta rapida, finestra delle proprietà, verbi             | Tutti     |
| **Network**               | Intera rete (in Risorse di rete)                             | Menu di scelta rapida, finestra delle proprietà, verbi             | Tutti     |
| **Tipo di \\ rete\\\#**     | Tutti gli oggetti di tipo \# (vedere di seguito)                                   | Menu di scelta rapida, Finestra delle proprietà, Verbi             | 4.71    |
| **Netshare**              | Tutte le condivisioni di rete                                                   | Menu di scelta rapida, Finestra delle proprietà, Verbi             | 4.71    |
| **Netserver**             | Tutti i server di rete                                                  | Menu di scelta rapida, Finestra delle proprietà, Verbi             | 4.71    |
| *nome \_ del provider di \_ rete* | Tutti gli oggetti forniti dal provider di rete "*nome \_ provider di \_ rete*" | Menu di scelta rapida, Finestra delle proprietà, Verbi             | Tutti     |
| **Stampanti**              | Tutte le stampanti                                                         | Menu di scelta rapida, finestra delle proprietà                    | Tutti     |
| **AudioCD**               | CD audio nell'unità CD                                                 | Solo verbi                                       | Tutti     |
| **Dvd**                   | Unità DVD (Windows 2000)                                             | Menu di scelta rapida, finestra delle proprietà, verbi             | 4.71    |



 

Note:

-   È possibile accedere al menu di scelta rapida in background della cartella file facendo clic con il pulsante destro del mouse all'interno di una cartella di file, ma non su alcun contenuto della cartella.
-   I "verbi" sono comandi speciali registrati in **HKEY \_ CLASSES ROOT \_ Subkey** \\  \\ **Shell** \\ **Verb** .
-   Per **tipo di** \\ **rete** , " " è un codice di tipo provider di rete in formato \\ **\#** \# decimale. Il codice del tipo di provider di rete è la parola più alta di un tipo di rete. L'elenco dei tipi di rete è specificato nel file di intestazione Winnetwk.h (valori WNNC \_ \_ \* NET). Ad esempio, WNNC NET SHIVA è 0x00330000, quindi la chiave di tipo corrispondente sarà \_ \_ **HKEY \_ CLASSES \_ ROOT** \\ **Network** \\ **Type** \\ **51** .
-   "*network \_ provider \_ name*" è un nome di provider di rete come specificato da [**WNetGetProviderName,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)con gli spazi convertiti in caratteri di sottolineatura. Ad esempio, se è installato il provider di rete Microsoft Networking, il nome del provider è "Microsoft Windows Network" e il nome del *\_ provider \_* di rete corrispondente è **Microsoft Windows \_ \_ Network**.

### <a name="example-of-an-extension-handler-registration"></a>Esempio di registrazione di un gestore di estensione

Per abilitare un gestore specifico, creare una sottochiave sotto la chiave del tipo di gestore di estensione con il nome del gestore. La shell non usa il nome del gestore, ma deve essere diversa da tutti gli altri nomi nella sottochiave del tipo. Impostare il valore predefinito della sottochiave name sul formato stringa del GUID del gestore.

L'esempio seguente illustra le voci del Registro di sistema che abilitano i gestori delle estensioni del menu di scelta rapida e della finestra delle proprietà, usando un tipo di file myp di esempio:

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

La procedura di registrazione descritta in questa sezione deve essere seguita per tutti Windows sistema operativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per l'implementazione In-Process estensioni](shell-and-managed-code.md)
</dt> </dl>

 

 
