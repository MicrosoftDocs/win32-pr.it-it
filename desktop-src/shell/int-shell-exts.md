---
description: Gran parte dell'implementazione di un oggetto gestore dell'estensione Shell è determinata dal tipo. Esistono tuttavia alcuni elementi comuni. Questo argomento illustra gli aspetti dell'implementazione condivisi da tutti i gestori di estensioni shell.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Inizializzazione dei gestori dell'estensione della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f83a47400cff5d0fa4628f6f6f9d9ba74b158947c7843f61831d54f62c7a6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661221"
---
# <a name="initializing-shell-extension-handlers"></a>Inizializzazione dei gestori dell'estensione della shell

Gran parte dell'implementazione di un oggetto gestore dell'estensione Shell è determinata dal tipo. Esistono tuttavia alcuni elementi comuni. Questo argomento illustra gli aspetti dell'implementazione condivisi da tutti i gestori di estensioni shell.

Tutti i gestori dell'estensione shell sono oggetti Component Object Model (COM) in-process. Devono essere assegnati a un GUID e registrati come descritto in [Registrazione dei gestori delle estensioni della shell](handlers.md). Vengono implementate come DLL e devono esportare le funzioni standard seguenti:

-   [**DllMain**](../dlls/dllmain.md). Punto di ingresso standard per la DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Espone l'oggetto class factory.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM chiama questa funzione per determinare se l'oggetto sta servendo client. In caso contrario, il sistema può scaricare la DLL e liberare la memoria associata.

Come tutti gli oggetti COM, i gestori delle estensioni shell devono implementare [**un'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e un [class factory](../com/implementing-iclassfactory.md). La maggior parte deve anche implementare [**un'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) in Windows XP o versioni precedenti. Sono stati sostituiti [**da IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) e [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista. Shell usa queste interfacce per inizializzare il gestore.

[**L'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) deve essere implementata dagli elementi seguenti:

-   Gestori di icone
-   Gestori dati
-   Gestori di eliminazione

[**L'interfaccia IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) deve essere implementata dagli elementi seguenti:

-   Gestori del menu di scelta rapida
-   Gestori di trascinamento della selezione
-   Gestori della finestra delle proprietà

Gli argomenti seguenti sono descritti nella parte restante di questo argomento:

-   [Implementazione di IPersistFile](#implementing-ipersistfile)
-   [Implementazione di IShellExtInit](#implementing-ishellextinit)
-   [Personalizzazione del suggerimento](#infotip-customization)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-ipersistfile"></a>Implementazione di IPersistFile

[**L'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è progettata per consentire il caricamento o il salvataggio di un oggetto in un file su disco. Sono disponibili sei metodi oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinque di per sé e il [**metodo GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) ereditato da [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist). Con le estensioni shell, **IPersist** viene usato solo per inizializzare un oggetto gestore dell'estensione shell. Poiché in genere non è necessario leggere o scrivere sul disco, solo i **metodi GetClassID** e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) richiedono un'implementazione nontoken.

Shell chiama [**prima GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e la funzione restituisce l'identificatore di classe (CLSID) dell'oggetto gestore estensioni. Shell chiama quindi [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) e passa due valori. Il primo, *pszFile*, è una stringa Unicode con il nome del file o della cartella su cui Shell sta per operare. Il secondo è *dwMode*, che indica la modalità di accesso ai file. Poiché in genere non è necessario accedere ai file, *dwMode* è in genere zero. Il metodo archivia questi valori in base alle esigenze per riferimenti successivi.

Il frammento di codice seguente illustra come un tipico gestore di estensioni shell implementa i [**metodi GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) [**e Load.**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) È progettato per gestire ANSI o Unicode. CLSID SampleExtHandler è il GUID dell'oggetto gestore di estensioni e CSampleShellExtension è il nome della classe usata per \_ implementare l'interfaccia. Le **variabili m \_ szFileName** e **m \_ dwMode** sono variabili private usate per archiviare il nome del file e i flag di accesso.


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

[**L'interfaccia IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) ha un solo metodo, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Il metodo dispone di tre parametri che shell può usare per passare vari tipi di informazioni. I valori passati dipendono dal tipo di gestore e alcuni possono essere impostati su **NULL.**

-   *pidlFolder contiene* il puntatore di una cartella a un elenco di identificatori di elemento (PIDL). Si tratta di un FILE PIDL assoluto. Per le estensioni della finestra delle proprietà, questo valore è **NULL.** Per le estensioni del menu di scelta rapida, è il file PIDL della cartella che contiene l'elemento di cui viene visualizzato il menu di scelta rapida. Per i gestori di trascinamento della selezione non predefiniti, si tratta del FILE PIDL della cartella di destinazione.
-   *pDataObject contiene* un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) di un oggetto dati. L'oggetto dati contiene uno o più nomi di file in [ \_ formato CF HDROP.](dragdrop.md)
-   *hRegKey contiene* una chiave del Registro di sistema per l'oggetto file o il tipo di cartella.

Il [**metodo IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) archivia il nome file, il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) e la chiave del Registro di sistema in base alle esigenze per un uso successivo. Il frammento di codice seguente illustra un'implementazione di **IShellExtInit::Initialize**. Per semplicità, questo esempio presuppone che l'oggetto dati contenga un solo file. In generale, l'oggetto dati potrebbe contenere più file, ognuno dei quali dovrà essere estratto.


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



## <a name="infotip-customization"></a>Personalizzazione del suggerimento

Esistono due modi per personalizzare le infotip. Un modo è implementare un oggetto che supporta [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) e quindi registrare l'oggetto nella sottochiave appropriata nel Registro di sistema (vedere di seguito). In alternativa, è possibile specificare una stringa fissa o un elenco di determinate proprietà di file da visualizzare.

Per visualizzare una stringa fissa per un'estensione dello spazio dei nomi, creare una sottochiave denominata **InfoTip** sotto la chiave CLSID dell'estensione dello spazio dei nomi. Impostare i dati di tale sottochiave come stringa da visualizzare.

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Per visualizzare una stringa fissa per un tipo di file, creare una sottochiave denominata **InfoTip** sotto la chiave **ProgID** del tipo di file per cui si vogliono specificare i suggerimenti. Impostare i dati di tale sottochiave come stringa da visualizzare.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

Se si vuole che Shell mostri determinate proprietà del file nel suggerimento per un tipo di file specifico, creare una sottochiave denominata **InfoTip** sotto la chiave **ProgID** di tale tipo di file. Impostare i dati di tale sottochiave come elenco delimitato da punto e virgola di nomi di proprietà canonici o {fmtid}, coppie pid dove *propname* è un nome di proprietà canonico e *{fmtid}, pid* è una coppia [**FMTID/PID**](./objects.md).

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

È possibile usare i nomi di proprietà seguenti.



| Nome proprietà    | Descrizione                   | Recuperato da                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| Autore           | Autore del documento        | [**AUTORE \_ PIDSI**](../stg/the-summary-information-property-set.md)                             |
| Titolo            | Titolo del documento         | [**TITOLO \_ PIDSI**](../stg/the-summary-information-property-set.md)                              |
| Oggetto          | Riepilogo dell'oggetto               | [**SOGGETTO \_ PIDSI**](../stg/the-summary-information-property-set.md)                            |
| Commento          | Commenti del documento             | [**PIDSI \_ PROPRIETÀ COMMENT**](../stg/the-summary-information-property-set.md) o cartella/unità |
| PageCount        | Numero di pagine               | [**PIDSI \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                          |
| Nome             | Nome descrittivo                 | Visualizzazione cartelle standard                                                                      |
| OriginalLocation | Percorso del file originale     | Cartella di valigetta e Cestino cartella                                                   |
| DateDeleted      | Data di eliminazione del file         | Cestino cartella                                                                        |
| Tipo             | Tipo di file                  | Visualizzazione dei dettagli della cartella standard                                                              |
| Dimensione             | Dimensioni del file                  | Visualizzazione dei dettagli della cartella standard                                                              |
| SyncCopyIn       | Uguale a OriginalLocation      | Uguale a OriginalLocation                                                                  |
| Ultima modifica         | Data ultima modifica            | Visualizzazione dei dettagli della cartella standard                                                              |
| Data di creazione          | Data creazione                  | Visualizzazione dei dettagli della cartella standard                                                              |
| Accedere         | Data dell'ultimo accesso            | Visualizzazione dei dettagli della cartella standard                                                              |
| InFolder         | Directory contenente il file | Documentare i risultati della ricerca                                                                   |
| Classifica             | Qualità della corrispondenza di ricerca       | Documentare i risultati della ricerca                                                                   |
| FreeSpace        | Spazio di archiviazione disponibile       | Unità disco                                                                               |
| NumberOfVisits   | Numero di visite              | Cartella Preferiti                                                                          |
| Attributi       | Attributi file               | Visualizzazione dei dettagli della cartella standard                                                              |
| Company          | Nome azienda                  | [**SOCIETÀ PIDDSI \_**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Category         | Categoria di documenti             | [**CATEGORIA \_ PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| Copyright        | Copyright multimediale               | [**PIDMSI \_ COPYRIGHT**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| HTMLInfoTipFile  | File di suggerimento informazioni HTML             | Desktop.ini file per la cartella                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dei gestori di estensioni della shell](reg-shell-exts.md)
</dt> </dl>

 

 
