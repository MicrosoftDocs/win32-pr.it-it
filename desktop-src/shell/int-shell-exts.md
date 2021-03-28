---
description: Gran parte dell'implementazione di un oggetto gestore dell'estensione della shell è determinata dal tipo. Esistono, tuttavia, alcuni elementi comuni. Questo argomento descrive gli aspetti dell'implementazione condivisi da tutti i gestori di estensioni della shell.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Inizializzazione di gestori estensioni della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980778"
---
# <a name="initializing-shell-extension-handlers"></a>Inizializzazione di gestori estensioni della shell

Gran parte dell'implementazione di un oggetto gestore dell'estensione della shell è determinata dal tipo. Esistono, tuttavia, alcuni elementi comuni. Questo argomento descrive gli aspetti dell'implementazione condivisi da tutti i gestori di estensioni della shell.

Tutti i gestori di estensioni della shell sono oggetti Component Object Model (COM) in-process. È necessario assegnare un GUID e registrarlo come descritto in [Registering Shell Extension Handler](handlers.md). Vengono implementate come dll ed è necessario esportare le funzioni standard seguenti:

-   [**DllMain**](../dlls/dllmain.md). Il punto di ingresso standard della DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Espone la class factory dell'oggetto.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM chiama questa funzione per determinare se l'oggetto serve qualsiasi client. In caso contrario, il sistema può scaricare la DLL e liberare la memoria associata.

Come tutti gli oggetti COM, i gestori di estensioni della shell devono implementare un'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e un [class factory](../com/implementing-iclassfactory.md). La maggior parte deve implementare anche un'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**ISHELLEXTINIT**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) in Windows XP o versioni precedenti. Questi sono stati sostituiti da [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) e [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista. La shell usa queste interfacce per inizializzare il gestore.

L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) deve essere implementata dai seguenti elementi:

-   Gestori di icone
-   Gestori di dati
-   Gestori di rilascio

L'interfaccia [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) deve essere implementata dai seguenti elementi:

-   Gestori dei menu di scelta rapida
-   Gestori di trascinamento della selezione
-   Gestori della finestra delle proprietà

Gli argomenti seguenti sono descritti nella parte restante di questo argomento:

-   [Implementazione di IPersistFile](#implementing-ipersistfile)
-   [Implementazione di IShellExtInit](#implementing-ishellextinit)
-   [Personalizzazione di infotip](#infotip-customization)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-ipersistfile"></a>Implementazione di IPersistFile

L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è progettata per consentire il caricamento o il salvataggio di un oggetto in un file su disco. Sono disponibili sei metodi, oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinque dei propri e il metodo [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) che eredita da [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist). Con le estensioni della shell, **IPersist** viene usato solo per inizializzare un oggetto gestore dell'estensione della shell. Poiché in genere non è necessario leggere o scrivere sul disco, solo i metodi **GetClassID** e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) richiedono un'implementazione non token.

La shell chiama prima [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e la funzione restituisce l'identificatore di classe (CLSID) dell'oggetto gestore di estensione. La shell chiama quindi [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) e passa due valori. Il primo, *pszFile*, è una stringa Unicode con il nome del file o della cartella su cui la Shell sta per operare. Il secondo è *dwMode*, che indica la modalità di accesso ai file. Poiché in genere non è necessario accedere ai file, *dwMode* è in genere pari a zero. Il metodo archivia questi valori in base alle esigenze per un riferimento successivo.

Nel frammento di codice seguente viene illustrato il modo in cui un tipico gestore dell'estensione della shell implementa i metodi [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) . È progettato per gestire ANSI o Unicode. CLSID \_ SampleExtHandler è il GUID dell'oggetto gestore dell'estensione e CSampleShellExtension è il nome della classe utilizzata per implementare l'interfaccia. Le variabili **m \_ szFileName** e **m \_ dwMode** sono variabili private utilizzate per archiviare i flag di accesso e il nome del file.


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a>Implementazione di IShellExtInit

L'interfaccia [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) ha un solo metodo, [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Il metodo dispone di tre parametri che la shell può usare per passare vari tipi di informazioni. I valori passati dipendono dal tipo di gestore e altri possono essere impostati su **null**.

-   *pidlFolder* include il puntatore di una cartella a un elenco di identificatori di elemento (PIDL). Si tratta di un PIDL assoluto. Per le estensioni della finestra delle proprietà, questo valore è **null**. Per le estensioni del menu di scelta rapida, è il PIDL della cartella che contiene l'elemento di cui viene visualizzato il menu di scelta rapida. Per i gestori di trascinamento della selezione non predefiniti, è il PIDL della cartella di destinazione.
-   *pDataObject* include un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) di un oggetto dati. L'oggetto dati include uno o più nomi di file nel formato [CF \_ HDROP](dragdrop.md) .
-   *hRegKey* include una chiave del registro di sistema per l'oggetto file o il tipo di cartella.

Il metodo [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) archivia il nome file, il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) e la chiave del registro di sistema in base alle esigenze per un uso successivo. Nel frammento di codice seguente viene illustrata un'implementazione di **IShellExtInit:: Initialize**. Per semplicità, in questo esempio si presuppone che l'oggetto dati contenga un solo file. In generale, l'oggetto dati potrebbe contenere più file, ognuno dei quali dovrà essere estratto.


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a>Personalizzazione di infotip

Esistono due modi per personalizzare infotip. Un modo consiste nell'implementare un oggetto che supporta [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) e quindi registrare l'oggetto sotto la sottochiave corretta nel registro di sistema (vedere di seguito). In alternativa, è possibile specificare una stringa fissa o un elenco di determinate proprietà di file da visualizzare.

Per visualizzare una stringa fissa per un'estensione dello spazio dei nomi, creare una sottochiave denominata **infotip** sotto la chiave CLSID dell'estensione dello spazio dei nomi. Impostare i dati della sottochiave in modo che siano la stringa che si desidera visualizzare.

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Per visualizzare una stringa fissa per un tipo di file, creare una sottochiave denominata **infotip** sotto la chiave **ProgID** del tipo di file per cui si vuole specificare infotip. Impostare i dati della sottochiave in modo che siano la stringa che si desidera visualizzare.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

Se si vuole che la shell mostri determinate proprietà del file in infotip per un tipo di file specifico, creare una sottochiave denominata **infotip** sotto la chiave **ProgID** del tipo di file. Impostare i dati di tale sottochiave come un elenco delimitato da punti e virgola di nomi di proprietà canonici o {fmtid}, coppie PID dove *propName* è un nome di proprietà canonico e *{fmtid}, PID* è una [**coppia fmtid/PID**](./objects.md).

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

È possibile utilizzare i nomi di proprietà seguenti.



| Nome proprietà    | Descrizione                   | Recuperato da                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| Autore           | Autore del documento        | [**autore di PIDSI \_**](../stg/the-summary-information-property-set.md)                             |
| Titolo            | Titolo del documento         | [**\_titolo PIDSI**](../stg/the-summary-information-property-set.md)                              |
| Oggetto          | Riepilogo oggetto               | [**\_oggetto PIDSI**](../stg/the-summary-information-property-set.md)                            |
| Commento          | Commenti del documento             | [**PIDSI \_ Proprietà commento**](../stg/the-summary-information-property-set.md) o cartella/unità |
| PageCount        | Numero di pagine               | [**\_PageCount PIDSI**](../stg/the-summary-information-property-set.md)                          |
| Nome             | Nome descrittivo                 | Visualizzazione cartelle standard                                                                      |
| OriginalLocation | Percorso del file originale     | Cartella valigetta e cartella Cestino                                                   |
| DateDeleted      | Il file di data è stato eliminato         | Cartella Cestino                                                                        |
| Tipo             | Tipo di file                  | Visualizzazione Dettagli cartella standard                                                              |
| Dimensione             | Dimensioni del file                  | Visualizzazione Dettagli cartella standard                                                              |
| SyncCopyIn       | Uguale a OriginalLocation      | Uguale a OriginalLocation                                                                  |
| Ultima modifica         | Data ultima modifica            | Visualizzazione Dettagli cartella standard                                                              |
| Data di creazione          | Data creazione                  | Visualizzazione Dettagli cartella standard                                                              |
| Accedere         | Data ultimo accesso            | Visualizzazione Dettagli cartella standard                                                              |
| InCartella         | Directory che contiene il file | Risultati della ricerca nei documenti                                                                   |
| Classifica             | Qualità della corrispondenza di ricerca       | Risultati della ricerca nei documenti                                                                   |
| FreeSpace        | Spazio di archiviazione disponibile       | Unità disco                                                                               |
| NumberOfVisits   | Numero di visite              | Cartella Preferiti                                                                          |
| Attributi       | Attributi file               | Visualizzazione Dettagli cartella standard                                                              |
| Company          | Nome azienda                  | [**\_società PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Category         | Categoria documento             | [**\_categoria PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| Copyright        | Copyright del supporto               | [**\_Copyright PIDMSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| HTMLInfoTipFile  | File InfoTip HTML             | File Desktop.ini per la cartella                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di gestori estensioni della shell](reg-shell-exts.md)
</dt> </dl>

 

 
