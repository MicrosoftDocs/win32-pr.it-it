---
description: In questo argomento viene illustrato come creare e registrare gestori di proprietà per utilizzare il sistema di proprietà di Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Inizializzazione di gestori di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8eb11bc44217e508313bfb477c65925b44216e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231764"
---
# <a name="initializing-property-handlers"></a>Inizializzazione di gestori di proprietà

In questo argomento viene illustrato come creare e registrare gestori di proprietà per utilizzare il sistema di proprietà di Windows.

Questo argomento è organizzato nel modo seguente:

-   [Gestori di proprietà](#property-handlers)
-   [Prima di iniziare](#before-you-begin)
-   [Inizializzazione di gestori di proprietà](#initializing-property-handlers)
-   [Archivio delle proprietà in memoria](#in-memory-property-store)
-   [Gestione dei valori di PROPVARIANT-Based](#dealing-with-propvariant-based-values)
-   [Supporto dei metadati aperti](#supporting-open-metadata)
-   [Contenuto full-text](#full-text-contents)
-   [Fornire valori per le proprietà](#providing-values-for-properties)
-   [Scrittura di valori indietro](#writing-back-values)
-   [Implementazione di IPropertyStoreCapabilities](#implementing-ipropertystorecapabilities)
-   [Registrazione e distribuzione di gestori di proprietà](#registering-and-distributing-property-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="property-handlers"></a>Gestori di proprietà

I gestori di proprietà sono una parte essenziale del sistema di proprietà. Vengono richiamati in-process dall'indicizzatore per leggere e indicizzare i valori delle proprietà e vengono richiamati anche da Esplora risorse in-process per leggere e scrivere i valori delle proprietà direttamente nei file. Questi gestori devono essere accuratamente scritti e testati per evitare prestazioni ridotte o la perdita di dati nei file interessati. Per altre informazioni sulle considerazioni specifiche dell'indicizzatore che influiscono sull'implementazione del gestore di proprietà, vedere [sviluppo di gestori di proprietà per la ricerca di Windows](../search/-search-3x-wds-extidx-propertyhandlers.md).

In questo argomento viene illustrato un formato di file basato su XML di esempio che descrive una ricetta con l'estensione del nome di file recipe. L'estensione del nome file. Recipe è registrata come formato di file distinto anziché basarsi sul formato di file XML più generico, il cui gestore usa un flusso secondario per archiviare le proprietà. Si consiglia di registrare estensioni di file univoche per i tipi di file.

## <a name="before-you-begin"></a>Prima di iniziare

I gestori di proprietà sono oggetti COM che creano l'astrazione [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per un formato di file specifico. Leggono (analizzano) e scrivono questo formato di file in modo conforme alla specifica. Alcuni gestori di proprietà eseguono il proprio lavoro in base alle API che astraggono l'accesso a un formato di file specifico. Prima di sviluppare un gestore di proprietà per il formato di file, è necessario comprendere in che modo il formato di file archivia le proprietà e come vengono mappate le proprietà (nomi e valori) nell'astrazione dell'archivio delle proprietà.

Quando si pianifica l'implementazione, tenere presente che i gestori di proprietà sono componenti di basso livello caricati nel contesto di processi quali Esplora risorse, l'indicizzatore di ricerca di Windows e applicazioni di terze parti che usano il modello di programmazione degli elementi della shell. Di conseguenza, i gestori di proprietà non possono essere implementati nel codice gestito e devono essere implementati in C++. Se il gestore USA API o servizi per svolgere il proprio lavoro, è necessario assicurarsi che tali servizi possano funzionare correttamente negli ambienti in cui viene caricato il gestore della proprietà.

> [!Note]  
> I gestori di proprietà sono sempre associati a tipi di file specifici; Pertanto, se il formato di file contiene proprietà che richiedono un gestore di proprietà personalizzato, è necessario registrare sempre un'estensione di file univoca per ogni formato di file.

 

## <a name="initializing-property-handlers"></a>Inizializzazione di gestori di proprietà

Prima che una proprietà venga utilizzata dal sistema, viene inizializzata chiamando un'implementazione di [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream). Il gestore della proprietà deve essere inizializzato con il sistema che lo assegna all'implementazione del gestore. Questo metodo di inizializzazione assicura gli elementi seguenti:

-   Il gestore delle proprietà può essere eseguito in un processo con restrizioni (una funzionalità di sicurezza importante) senza disporre dei diritti di accesso per la lettura o la scrittura diretta dei file, bensì per accedere al contenuto attraverso il flusso.
-   Il sistema può essere considerato attendibile per gestire correttamente il file oplock, che è un'importante misura di affidabilità.
-   Il sistema di proprietà fornisce un servizio di salvataggio automatico sicuro senza alcuna funzionalità aggiuntiva richiesta dall'implementazione del gestore di proprietà. Per ulteriori informazioni sui flussi, vedere la sezione [scrittura dei valori indietro](#writing-back-values) .
-   L'uso di [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) astrae l'implementazione da file System dettagli. Ciò consente al gestore di supportare l'inizializzazione tramite archivi alternativi, ad esempio una cartella File Transfer Protocol (FTP) o un file compresso con estensione zip.

In alcuni casi non è possibile inizializzare con i flussi. In tali situazioni sono disponibili altre due interfacce che i gestori di proprietà possono implementare: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) e [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem). Se un gestore di proprietà non implementa [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), deve rifiutare esplicitamente l'esecuzione nel processo isolato in cui l'indicizzatore di sistema lo inserirebbe per impostazione predefinita in caso di modifica del flusso. Per rifiutare esplicitamente questa funzionalità, impostare il valore del registro di sistema seguente.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

Tuttavia, è preferibile implementare [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) ed eseguire un'inizializzazione basata sul flusso. Di conseguenza, il gestore delle proprietà sarà più sicuro e affidabile. La disabilitazione dell'isolamento dei processi è in genere destinata solo ai gestori di proprietà legacy e deve essere evitata con qualsiasi nuovo codice.

Per esaminare in dettaglio l'implementazione di un gestore di proprietà, esaminare l'esempio di codice seguente, che è un'implementazione di [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize). Il gestore viene inizializzato caricando un documento della ricetta basato su XML tramite un puntatore a tale istanza di [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) associata del documento. La variabile **\_ spDocEle** utilizzata in prossimità della fine dell'esempio di codice viene definita in precedenza nell'esempio come file Msxml2:: IXMLDOMElementPtr.

> [!Note]  
> Gli esempi di codice seguenti e tutti i successivi sono ricavati dall'esempio di gestore della ricetta incluso in Windows Software Development Kit (SDK). .

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



Â 

Dopo il caricamento del documento, le proprietà da visualizzare in Esplora risorse vengono caricate chiamando il metodo **\_ LoadProperties** protetto, come illustrato nell'esempio di codice seguente. Questo processo viene esaminato in dettaglio nella sezione successiva.


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



Se il flusso è di sola lettura, ma il parametro *grfMode* contiene il \_ flag STGM ReadWrite, l'inizializzazione dovrebbe avere esito negativo e restituire STG \_ e \_ AccessDenied. Senza questo controllo, Esplora risorse Mostra i valori delle proprietà come scrivibili anche se non lo sono, causando una confusione nell'esperienza dell'utente finale.

Il gestore proprietà viene inizializzato solo una volta nel corso della sua durata. Se viene richiesta una seconda inizializzazione, il gestore deve restituire `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .

## <a name="in-memory-property-store"></a>In-Memory archivio delle proprietà

Prima di esaminare l'implementazione di **\_ LoadProperties**, è necessario comprendere la matrice **PropertyMap** utilizzata nell'esempio per eseguire il mapping delle proprietà nel documento XML alle proprietà esistenti nel sistema di proprietà tramite i relativi valori pkey.

Non esporre ogni elemento e attributo nel file XML come proprietà. Selezionare invece solo quelli che si ritiene possano essere utili per gli utenti finali nell'organizzazione dei propri documenti (in questo caso, le ricette). Si tratta di un concetto importante da tenere presente quando si sviluppano i gestori delle proprietà, ovvero la differenza tra le informazioni realmente utili per gli scenari aziendali e le informazioni che appartengono ai dettagli del file e possono essere visualizzate aprendo il file stesso. Le proprietà non sono destinate a una duplicazione completa di un file XML.


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



Di seguito è illustrata l'implementazione completa del metodo **\_ LoadProperties** chiamato da [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



Il metodo **\_ LoadProperties** chiama la funzione helper della shell [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) per creare un archivio delle proprietà in memoria (cache) per le proprietà gestite. Utilizzando una cache, le modifiche vengono rilevate. In questo modo non è possibile verificare se un valore della proprietà è stato modificato nella cache, ma non ancora salvato in un archivio permanente. Consente inoltre di liberare in modo permanente i valori delle proprietà che non sono stati modificati.

Il metodo **\_ LoadProperties** chiama anche **\_ LoadProperty** la cui implementazione è illustrata nel codice seguente, una volta per ogni proprietà mappata. **\_ LoadProperty** ottiene il valore della proprietà come specificato nell'elemento **PropertyMap** nel flusso XML e lo assegna alla cache in memoria tramite una chiamata a [**IPropertyStoreCache:: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate). Il \_ flag Normal PSC nella chiamata a **IPropertyStoreCache:: SetValueAndState** indica che il valore della proprietà non è stato modificato dall'ora di immissione della cache.


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a>Gestione dei valori di PROPVARIANT-Based

Nell'implementazione di **\_ LoadProperty**, un valore della proprietà viene fornito sotto forma di [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Viene fornito un set di API nel Software Development Kit (SDK) per eseguire la conversione da tipi primitivi, ad esempio **PWSTR** o **int** , a o da tipi **PROPVARIANT** . Queste API si trovano in Propvarutil. h.

Ad esempio, per convertire un [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in una stringa, è possibile usare [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) come illustrato di seguito.


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



Per inizializzare un PROPVARIANT da una stringa, è possibile usare [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



Come si può notare in uno qualsiasi dei file Recipe inclusi nell'esempio, può essere presente più di una parola chiave in ogni file. Per tenere conto di questo problema, il sistema di proprietà supporta stringhe multivalore rappresentate come vettore di stringhe (ad esempio "VT \_ vector \| VT \_ LPWSTR"). Il metodo **\_ LoadVectorProperty** nell'esempio usa valori basati su vettori.


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



Se non esiste un valore nel file, non viene restituito alcun errore. Impostare invece il valore su VT \_ vuoto e restituire **S \_ OK**. VT \_ vuoto indica che il valore della proprietà non esiste.

## <a name="supporting-open-metadata"></a>Supporto dei metadati aperti

In questo esempio viene utilizzato un formato di file basato su XML. È possibile estendere lo schema per supportare proprietà che non sono state considerate durante pronto sviluppo, ad esempio. Questo sistema è noto come metadati aperti. Questo esempio estende il sistema di proprietà creando un nodo sotto l'elemento **Recipe** denominato **ExtendedProperties**, come illustrato nell'esempio di codice seguente.


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



Per caricare le proprietà estese mantenute durante l'inizializzazione, implementare il metodo **\_ LoadExtendedProperties** , come illustrato nell'esempio di codice seguente.


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



Le API di serializzazione dichiarate in propsys. h vengono usate per serializzare e deserializzare i tipi [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in BLOB di dati, quindi viene usata la codifica Base64 per serializzare tali BLOB in stringhe che è possibile salvare in XML. Queste stringhe vengono archiviate nell'attributo **valore** dell'elemento **ExtendedProperties** . Il metodo di utilità seguente, implementato nel file util. cpp dell'esempio, esegue la serializzazione. Inizia con una chiamata alla funzione [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) per eseguire la serializzazione binaria, come illustrato nell'esempio di codice seguente.


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



Successivamente, la funzione [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â, dichiarata in WinCrypt. h, esegue la conversione Base64.


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



La funzione **DeserializePropVariantFromString** , disponibile anche in util. cpp, inverte l'operazione, deserializzando i valori dal file XML.

Per informazioni sul supporto per i metadati aperti, vedere la sezione relativa ai tipi di file che supportano i metadati aperti in [tipi di file](../shell/fa-file-types.md).

## <a name="full-text-contents"></a>Contenuto Full-Text

I gestori di proprietà possono inoltre facilitare una ricerca full-text del contenuto dei file e rappresentano un modo semplice per fornire tale funzionalità se il formato di file non è eccessivamente complesso. Esiste un modo alternativo, più potente per fornire il testo completo del file tramite l'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

Nella tabella seguente vengono riepilogati i vantaggi di ogni approccio utilizzando [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) o [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).



| Funzionalità                                   | IFilter                      | IPropertyStore |
|----------------------------------------------|------------------------------|----------------|
| Consente di eseguire il writeback dei file?                  | No                           | Sì            |
| Viene fornita una combinazione di contenuto e proprietà?      | Sì                          | Sì            |
| Multilingue?                                | Sì                          | No             |
| MIME/Embedded?                               | Sì                          | No             |
| Confini del testo?                             | Frase, paragrafo, capitolo | nessuno           |
| Implementazione supportata per SPS/SQL Server? | Sì                          | No             |
| Implementazione                               | Complex                      | Semplice         |



 

Nell'esempio di gestore della ricetta, il formato del file Recipe non presenta requisiti complessi, pertanto è stato implementato solo [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per il supporto full-text. La ricerca full-text è implementata per i nodi XML denominati nella matrice seguente.


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



Il sistema di proprietà contiene la `System.Search.Contents` \_ Proprietà ( \_ contenuto di ricerca pkey), che è stata creata per fornire il contenuto full-text all'indicizzatore. Il valore di questa proprietà non viene mai visualizzato direttamente nell'interfaccia utente; il testo di tutti i nodi XML denominati nella matrice precedente viene concatenato in una singola stringa. Tale stringa viene quindi fornita all'indicizzatore come contenuto full-text del file Recipe tramite una chiamata a [**IPropertyStoreCache:: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) , come illustrato nell'esempio di codice seguente.


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a>Fornire valori per le proprietà

Quando vengono usati per leggere i valori, i gestori delle proprietà vengono in genere richiamati per uno dei seguenti motivi:

-   Per enumerare tutti i valori delle proprietà.
-   Per ottenere il valore di una proprietà specifica.

Per l'enumerazione, viene richiesto a un gestore di proprietà di enumerarne le proprietà durante l'indicizzazione o quando la finestra di dialogo Proprietà richiede la visualizzazione delle proprietà nell' **altro** gruppo. L'indicizzazione viene eseguita costantemente come operazione in background. Ogni volta che un file viene modificato, l'indicizzatore riceve una notifica e indicizza nuovamente il file chiedendo al gestore proprietà di enumerarne le proprietà. È pertanto fondamentale che i gestori di proprietà siano implementati in modo efficiente e restituiscano i valori delle proprietà il più rapidamente possibile. Enumerare tutte le proprietà per cui si dispone di valori, come per qualsiasi raccolta, ma non enumerare le proprietà che coinvolgono calcoli a elevato utilizzo di memoria o richieste di rete che potrebbero renderle lente per il recupero.

Quando si scrive un gestore di proprietà, in genere è necessario considerare i due set di proprietà seguenti.

-   Proprietà primarie: proprietà supportate dal tipo di file in modo nativo. Ad esempio, un gestore delle proprietà foto per i metadati del file di immagine scambiabile (EXIF) supporta in modo nativo `System.Photo.FNumber` .
-   Proprietà estese: proprietà supportate dal tipo di file come parte dei metadati aperti.

Poiché nell'esempio viene utilizzata la cache in memoria, l'implementazione di metodi [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) è solo una questione di delega a tale cache, come illustrato nell'esempio di codice seguente.


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



Se si sceglie di non delegare la cache in memoria, è necessario implementare i metodi per fornire> il comportamento previsto seguente:

-   [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): se non sono presenti proprietà, questo metodo restituisce **S \_ OK**.
-   [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): se *iProp* è maggiore o uguale a *CProps*, questo metodo restituisce e \_ INVALIDARG e la struttura a cui punta il parametro *pkey* viene riempita con zeri.
-   [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) riflettono lo stato corrente del gestore della proprietà. Se un [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) viene aggiunto o rimosso dal file tramite [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), questi due metodi devono riflettere tale modifica la volta successiva che vengono chiamati.
-   [**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): se viene richiesto un valore inesistente per questo metodo, viene restituito **S \_ OK** con il valore indicato come VT \_ Empty.

## <a name="writing-back-values"></a>Scrittura di valori indietro

Quando il gestore delle proprietà scrive il valore di una proprietà usando [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), non scrive il valore nel file fino a quando non viene chiamato il metodo [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) . La cache in memoria può essere utile per implementare questo schema. Nel codice di esempio, l'implementazione di **IPropertyStore:: SetValue** imposta semplicemente il nuovo valore nella cache in memoria e imposta lo stato di tale proprietà su PSC \_ Dirty.


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



In qualsiasi implementazione di [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , è previsto il comportamento seguente da [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):

-   Se la proprietà esiste già, viene impostato il valore della proprietà.
-   Se la proprietà non esiste, viene aggiunta la nuova proprietà e il relativo valore impostato.
-   Se il valore della proprietà non può essere reso permanente con la stessa accuratezza specificata (ad esempio, il troncamento a causa di limitazioni delle dimensioni nel formato del file), il valore viene impostato per quanto possibile e viene restituito il valore inplace \_ S \_ troncato.
-   Se la proprietà non è supportata dal gestore della proprietà, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` viene restituito.
-   Se c'è un altro motivo per cui non è possibile impostare il valore della proprietà, ad esempio il file bloccato o la mancanza di diritti per la modifica tramite gli elenchi di controllo di accesso (ACL), \_ \_ viene restituito STG E AccessDenied.

Uno dei principali vantaggi dell'uso dei flussi, come l'esempio, è l'affidabilità. I gestori di proprietà devono sempre considerare che non è possibile lasciare un file in uno stato incoerente in caso di errore irreversibile. Il danneggiamento dei file di un utente ovviamente dovrebbe essere evitato e il modo migliore per eseguire questa operazione è il meccanismo "copy-on-write". Se il gestore delle proprietà usa un flusso per accedere a un file, si ottiene automaticamente questo comportamento. il sistema scrive tutte le modifiche apportate al flusso, sostituendo il file con la nuova copia solo durante l'operazione di commit.

Per eseguire l'override di questo comportamento e controllare manualmente il processo di salvataggio dei file, è possibile rifiutare esplicitamente il comportamento di salvataggio sicuro impostando il valore ManualSafeSave nella voce del registro di sistema del gestore, come illustrato qui.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

Quando un gestore specifica il valore ManualSafeSave, il flusso con cui viene inizializzato non è un flusso transazionale (STGM \_ transazionale). Il gestore stesso deve implementare la funzione di salvataggio sicuro per garantire che il file non sia danneggiato se l'operazione di salvataggio viene interrotta. Se il gestore implementa la scrittura sul posto, viene scritto nel flusso specificato. Se il gestore non supporta questa funzionalità, deve recuperare un flusso con il quale scrivere la copia aggiornata del file usando [**IDestinationStreamFactory:: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream). Al termine della scrittura del gestore, deve chiamare [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) nel flusso originale per completare l'operazione e sostituire il contenuto del flusso originale con la nuova copia del file.

ManualSafeSave è anche la situazione predefinita se non si inizializza il gestore con un flusso. Senza un flusso originale per ricevere il contenuto del flusso temporaneo, è necessario usare [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) per eseguire una sostituzione atomica del file di origine.

I formati di file di grandi dimensioni che verranno usati in modo da produrre file di dimensioni superiori a 1 MB devono implementare il supporto per la scrittura di proprietà sul posto; in caso contrario, il comportamento delle prestazioni non soddisfa le aspettative dei client del sistema di proprietà. In questo scenario, il tempo necessario per scrivere le proprietà non deve essere influenzato dalle dimensioni del file.

Per file di grandi dimensioni, ad esempio un file video di almeno 1 GB, è necessaria una soluzione diversa. Se il file non dispone di spazio sufficiente per eseguire la scrittura sul posto, il gestore potrebbe non riuscire a eseguire l'aggiornamento della proprietà se la quantità di spazio riservata per la scrittura di proprietà sul posto è stata esaurita. Questo errore si verifica per evitare scarse prestazioni derivanti da 2 GB di IO (1 a lettura, 1 per la scrittura). A causa di questo potenziale errore, questi formati di file devono riservare spazio sufficiente per la scrittura di proprietà sul posto.

Se il file dispone di spazio sufficiente nell'intestazione per la scrittura dei metadati e se la scrittura di tali metadati non comporta l'aumento o la riduzione del file, è possibile che la scrittura sul posto sia sicura. Si consiglia 64 KB come punto di partenza. La scrittura sul posto è equivalente al gestore che richiede ManualSafeSave e chiama [**IStream:: commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) nell'implementazione di [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))e offre prestazioni decisamente migliori rispetto a copy-on-Write. Se le dimensioni del file sono cambiate a causa di modifiche al valore della proprietà, la scrittura sul posto non deve essere tentata a causa del rischio di un file danneggiato in caso di interruzione anomala.

> [!Note]  
> Per motivi di prestazioni, è consigliabile usare l'opzione ManualSafeSave con i gestori di proprietà che lavorano con file di 100 KB o più grandi.

 

Come illustrato nell'implementazione di esempio seguente di [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), il gestore per ManualSafeSave è registrato per illustrare l'opzione di salvataggio sicuro manuale. Il metodo **\_ SaveCacheToDom** scrive i valori delle proprietà archiviati nella cache in memoria nell'oggetto XMLdocument.


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



Quindi, chiedersi se il pecificato supporta [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



Eseguire quindi il commit del flusso originale, che scrive i dati nel file originale in modo sicuro.


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



Esaminare quindi l'implementazione di **\_ SaveCacheToDom** .


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



Ottenere quindi il numero di proprietà archiviate nella cache in memoria.


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



Scorrere ora le proprietà per determinare se il valore di una proprietà è stato modificato dopo che è stato caricato in memoria.


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



Il metodo [**IPropertyStoreCache:: GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) ottiene lo stato della proprietà nella cache. Il \_ flag PSC Dirty, che è stato impostato nell'implementazione di [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) , contrassegna una proprietà come modificata.


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



Eseguire il mapping della proprietà al nodo XML come specificato nella **matrice \_ rgPropertyMap, ad esempio** .


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



Se una proprietà non è presente nella mappa, è una nuova proprietà impostata da Esplora risorse. Poiché i metadati aperti sono supportati, salvare la nuova proprietà nella sezione **ExtendedProperties** del codice XML.


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a>Implementazione di IPropertyStoreCapabilities

[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informa l'interfaccia utente della shell se una particolare proprietà può essere modificata nell'interfaccia utente della shell. È importante notare che questo si riferisce solo alla possibilità di modificare la proprietà nell'interfaccia utente, non se è possibile chiamare correttamente [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) sulla proprietà. Una proprietà che provoca un valore restituito di S \_ false da [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) può comunque essere in grado di essere impostata tramite un'applicazione.


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) restituisce **\_ OK** per indicare che agli utenti finali deve essere consentito modificare direttamente la proprietà; S \_ false indica che non dovrebbero. S \_ false può indicare che le applicazioni sono responsabili della scrittura della proprietà, non degli utenti. La shell Disabilita i controlli di modifica nel modo appropriato in base ai risultati delle chiamate a questo metodo. Si presuppone che un gestore che non implementa [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) supporti i metadati aperti attraverso il supporto per la scrittura di qualsiasi proprietà.

Se si compila un gestore che gestisce solo le proprietà di sola lettura, è necessario implementare il metodo **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)o [**IINITIALIZEWITHFILE**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) in modo che restituisca STG \_ E \_ AccessDenied quando viene chiamato con il flag STGM \_ ReadWrite.

Per alcune proprietà l'attributo [innate](./propdesc-schema-typeinfo.md) è impostato su **true**. Le proprietà innate hanno le caratteristiche seguenti:

-   La proprietà viene in genere calcolata in qualche modo. Ad esempio, `System.Image.BitDepth` viene calcolato dall'immagine stessa.
-   La modifica della proprietà non avrebbe senso senza modificare il file. Ad esempio, la modifica di `System.Image.Dimensions` non consente di ridimensionare l'immagine, quindi non ha senso consentire all'utente di modificarla.
-   In alcuni casi, queste proprietà vengono fornite automaticamente dal sistema. Gli esempi includono `System.DateModified` , che viene fornito dal file System, e `System.SharedWith` , che si basa sull'identità con cui l'utente condivide il file.

A causa di queste caratteristiche, le proprietà contrassegnate come *innate* vengono fornite all'utente nell'interfaccia utente della Shell solo come proprietà di sola lettura. Se una proprietà è contrassegnata come *innata*, il sistema di proprietà non archivia tale proprietà nel gestore della proprietà. Per questo motivo, i gestori di proprietà non necessitano di codice speciale per tenere conto di queste proprietà nelle rispettive implementazioni. Se il valore dell'attributo *innate* non viene dichiarato in modo esplicito per una proprietà specifica, il valore predefinito è **false**.

## <a name="registering-and-distributing-property-handlers"></a>Registrazione e distribuzione di gestori di proprietà

Con il gestore di proprietà implementato, deve essere registrato e la relativa estensione del nome file associata al gestore. Per altre informazioni, vedere [registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui gestori delle proprietà](./building-property-handlers-properties.md)
</dt> <dt>

[Uso dei nomi dei tipi](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
</dt> <dt>

[Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
</dt> <dt>

[Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
