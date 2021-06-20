---
description: Questo articolo illustra come inizializzare i gestori delle proprietà per l'uso con il sistema di proprietà di Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Inizializzazione dei gestori di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d7626f92b3d81a6764e635c10302747f82a383
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406994"
---
# <a name="initializing-property-handlers"></a>Inizializzazione dei gestori di proprietà

Questo argomento illustra come creare e registrare gestori di proprietà per l'uso con il sistema di proprietà di Windows.

Questo argomento è organizzato come segue:

-   [Gestori delle proprietà](#property-handlers)
-   [Prima di iniziare](#before-you-begin)
-   [Inizializzazione dei gestori di proprietà](#initializing-property-handlers)
-   [In memoria Archivio proprietà](#in-memory-property-store)
-   [Gestione dei PROPVARIANT-Based predefiniti](#dealing-with-propvariant-based-values)
-   [Supporto dei metadati aperti](#supporting-open-metadata)
-   [Contenuto full-text](#full-text-contents)
-   [Fornire valori per le proprietà](#providing-values-for-properties)
-   [Scrittura di valori](#writing-back-values)
-   [Implementazione di IPropertyStoreCapabilities](#implementing-ipropertystorecapabilities)
-   [Registrazione e distribuzione di gestori di proprietà](#registering-and-distributing-property-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="property-handlers"></a>Gestori delle proprietà

I gestori delle proprietà sono una parte fondamentale del sistema di proprietà. Vengono richiamati in-process dall'indicizzatore per leggere e indicizzare i valori delle proprietà e vengono richiamati anche da Esplora risorse in-process per leggere e scrivere i valori delle proprietà direttamente nei file. Questi gestori devono essere scritti e testati con attenzione per evitare prestazioni ridotte o la perdita di dati nei file interessati. Per altre informazioni sulle considerazioni specifiche dell'indicizzatore che influiscono sull'implementazione del gestore delle proprietà, vedere Sviluppo di gestori di proprietà [per Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

Questo argomento illustra un formato di file basato su XML di esempio che descrive una ricetta con estensione recipe. L'estensione di file con estensione recipe viene registrata come formato di file distinto anziché basarsi sul formato di file .xml più generico, il cui gestore usa un flusso secondario per archiviare le proprietà. È consigliabile registrare estensioni di file univoche per i tipi di file.

## <a name="before-you-begin"></a>Prima di iniziare

I gestori di proprietà sono oggetti COM che creano [**l'astrazione IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per un formato di file specifico. Leggono (analizzano) e scrivono questo formato di file in modo conforme alle specifiche. Alcuni gestori di proprietà esereranno il proprio lavoro in base alle API che astrarranno l'accesso a un formato di file specifico. Prima di sviluppare un gestore delle proprietà per il formato di file, è necessario comprendere in che modo il formato di file archivia le proprietà e come tali proprietà (nomi e valori) vengono mappate nell'astrazione dell'archivio proprietà.

Quando si pianifica l'implementazione, tenere presente che i gestori delle proprietà sono componenti di basso livello caricati nel contesto di processi come Esplora risorse, l'indicizzatore Windows Search e applicazioni di terze parti che usano il modello di programmazione dell'elemento Shell. Di conseguenza, i gestori di proprietà non possono essere implementati nel codice gestito e devono essere implementati in C++. Se il gestore usa api o servizi per eseguire il proprio lavoro, è necessario assicurarsi che tali servizi possano funzionare correttamente negli ambienti in cui viene caricato il gestore delle proprietà.

> [!Note]  
> I gestori di proprietà sono sempre associati a tipi di file specifici. Pertanto, se il formato di file contiene proprietà che richiedono un gestore delle proprietà personalizzate, è necessario registrare sempre un'estensione di file univoca per ogni formato di file.

 

## <a name="initializing-property-handlers"></a>Inizializzazione dei gestori di proprietà

Prima che una proprietà venga usata dal sistema, viene inizializzata chiamando un'implementazione di [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream). Il gestore della proprietà deve essere inizializzato facendo in modo che il sistema gli assegni un flusso anziché lasciare tale assegnazione all'implementazione del gestore. Questo metodo di inizializzazione garantisce quanto segue:

-   Il gestore delle proprietà può essere eseguito in un processo con restrizioni (una funzionalità di sicurezza importante) senza avere diritti di accesso per leggere o scrivere direttamente i file, anziché accedere al contenuto tramite il flusso.
-   Il sistema può essere considerato attendibile per gestire correttamente gli oplock dei file, che è una misura di affidabilità importante.
-   Il sistema di proprietà fornisce un servizio di salvataggio sicuro automatico senza alcuna funzionalità aggiuntiva richiesta dall'implementazione del gestore delle proprietà. Per altre [informazioni sui flussi,](#writing-back-values) vedere la sezione Writing Back Values (Scrittura di valori).
-   L'uso di [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) astrae l'implementazione file system dettagli. In questo modo il gestore può supportare l'inizializzazione tramite archivi alternativi, ad esempio una cartella File Transfer Protocol (FTP) o un file compresso con un'estensione .zip file.

In alcuni casi l'inizializzazione con i flussi non è possibile. In queste situazioni, sono disponibili altre due interfacce che i gestori delle proprietà possono implementare: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) e [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem). Se un gestore delle proprietà non implementa [**IInitializeWithStream,**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)deve rifiutare esplicitamente l'esecuzione nel processo isolato in cui l'indicizzatore di sistema lo insererebbe per impostazione predefinita in caso di modifica al flusso. Per rifiutare esplicitamente questa funzionalità, impostare il valore del Registro di sistema seguente.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

Tuttavia, è molto meglio implementare [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) ed eseguire un'inizializzazione basata su flusso. Di conseguenza, il gestore della proprietà sarà più sicuro e affidabile. La disabilitazione dell'isolamento dei processi è in genere destinata solo ai gestori di proprietà legacy e deve essere evitata in modo faticoso da qualsiasi nuovo codice.

Per esaminare in dettaglio l'implementazione di un gestore di proprietà, esaminare l'esempio di codice seguente, ovvero un'implementazione di [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize). Il gestore viene inizializzato caricando un documento recipe basato su XML tramite un puntatore all'istanza [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) associata del documento. La **\_ variabile spDocEle** usata vicino alla fine dell'esempio di codice è definita in precedenza nell'esempio come MSXML2::IXMLDOMElementPtr.

> [!Note]  
> Gli esempi di codice seguenti e di tutti i successivi sono tratto dall'esempio di gestore di ricette incluso nel Windows Software Development Kit (Windows SDK) (SDK). .

 


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

Dopo il caricamento del documento stesso, le proprietà da visualizzare nel Esplora risorse vengono caricate chiamando il metodo **\_ LoadProperties** protetto, come illustrato nell'esempio di codice seguente. Questo processo viene esaminato in dettaglio nella sezione successiva.


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



Se il flusso è di sola lettura ma il *parametro grfMode* contiene il flag STGM READWRITE, l'inizializzazione avrà esito negativo e restituirà \_ STG \_ E \_ ACCESSDENIED. Senza questo controllo, Esplora risorse i valori delle proprietà come scrivibili anche se non lo sono, con un'esperienza utente finale confusa.

Il gestore della proprietà viene inizializzato una sola volta nella relativa durata. Se viene richiesta una seconda inizializzazione, il gestore deve restituire `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .

## <a name="in-memory-property-store"></a>In-Memory Archivio proprietà

Prima di vedere l'implementazione di **\_ LoadProperties,** è necessario comprendere la matrice **PropertyMap** usata nell'esempio per eseguire il mapping delle proprietà nel documento XML alle proprietà esistenti nel sistema di proprietà tramite i relativi valori PKEY.

Non esporre ogni elemento e attributo nel file XML come proprietà. Selezionare invece solo quelli che si ritiene siano utili per gli utenti finali nell'organizzazione dei documenti (in questo caso, le ricette). Si tratta di un concetto importante da tenere presente quando si sviluppano i gestori delle proprietà: la differenza tra le informazioni realmente utili per gli scenari aziendali e le informazioni che appartengono ai dettagli del file e possono essere visualizzate aprendo il file stesso. Le proprietà non devono essere una duplicazione completa di un file XML.


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



Ecco l'implementazione completa **\_ del metodo LoadProperties** chiamato da [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).


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



Il **\_ metodo LoadProperties** chiama la funzione helper Shell [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) per creare un archivio delle proprietà in memoria (cache) per le proprietà gestite. Usando una cache, le modifiche vengono rilevate per l'utente. In questo modo è possibile verificare se un valore di proprietà è stato modificato nella cache ma non è stato ancora salvato nell'archiviazione persistente. Consente inoltre di rendere inutili persistenti i valori delle proprietà che non sono stati modificati.

Il **\_ metodo LoadProperties** chiama anche **\_ LoadProperty** la cui implementazione è illustrata nel codice seguente) una volta per ogni proprietà mappata. **\_ LoadProperty** ottiene il valore della proprietà come specificato nell'elemento **PropertyMap** nel flusso XML e lo assegna alla cache in memoria tramite una chiamata a [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate). Il flag PSC NORMAL nella chiamata \_ a **IPropertyStoreCache::SetValueAndState** indica che il valore della proprietà non è stato modificato dopo l'immissione nella cache.


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



## <a name="dealing-with-propvariant-based-values"></a>Gestione dei PROPVARIANT-Based predefiniti

Nell'implementazione **\_ di LoadProperty** viene fornito un valore della proprietà sotto forma di [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Viene fornito un set di API nel Software Development Kit (SDK) per la conversione da tipi primitivi come **PWSTR** o **int** a o da tipi **PROPVARIANT.** Queste API sono disponibili in Propvarutil.h.

Ad esempio, per convertire [**un oggetto PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in una stringa, è possibile usare [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) come illustrato di seguito.


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



Per inizializzare un oggetto PROPVARIANT da una stringa, è possibile usare [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



Come si può vedere in uno dei file di ricette inclusi nell'esempio, può essere presente più di una parola chiave in ogni file. A tale scopo, il sistema di proprietà supporta stringhe multivalore rappresentate come vettore di stringhe ,ad esempio "VT \_ VECTOR \| VT \_ LPWSTR". Il **\_ metodo LoadVectorProperty** nell'esempio usa valori basati su vettori.


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



Se non esiste un valore nel file, non restituire un errore. Impostare invece il valore su VT \_ EMPTY e restituire S **\_ OK**. VT \_ EMPTY indica che il valore della proprietà non esiste.

## <a name="supporting-open-metadata"></a>Supporto dei metadati aperti

In questo esempio viene utilizzato un formato di file basato su XML. Il relativo schema può essere esteso per supportare le proprietà che non sono state pensate durante lo sviluppo, ad esempio. Questo sistema è noto come metadati aperti. Questo esempio estende il sistema di proprietà creando un nodo nell'elemento **Recipe** denominato **ExtendedProperties**, come illustrato nell'esempio di codice seguente.


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



Per caricare le proprietà estese persistenti durante l'inizializzazione, implementare il **\_ metodo LoadExtendedProperties,** come illustrato nell'esempio di codice seguente.


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



Le API di serializzazione dichiarate in Propsys.h vengono usate per serializzare e deserializzare i tipi [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in BLOB di dati e quindi viene usata la codifica Base64 per serializzare tali BLOB in stringhe che possono essere salvate nel codice XML. Queste stringhe vengono archiviate **nell'attributo EncodedValue** dell'elemento **ExtendedProperties.** Il metodo di utilità seguente, implementato nel file Util.cpp dell'esempio, esegue la serializzazione. Inizia con una chiamata alla [**funzione StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) per eseguire la serializzazione binaria, come illustrato nell'esempio di codice seguente.


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



Successivamente, la [**funzione CryptBinaryToString,**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)dichiarata in Wincrypt.h, esegue la conversione Base64.


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



La **funzione DeserializePropVariantFromString,** disponibile anche in Util.cpp, inverte l'operazione, deserializzando i valori dal file XML.

Per informazioni sul supporto per i metadati aperti, vedere "Tipi di file che supportano metadati aperti" in [Tipi di file.](../shell/fa-file-types.md)

## <a name="full-text-contents"></a>Full-Text contenuto

I gestori di proprietà possono anche semplificare una ricerca full-text del contenuto del file e sono un modo semplice per fornire tale funzionalità se il formato di file non è troppo complicato. Esiste un modo alternativo e più potente per fornire il testo completo del file tramite [**l'implementazione dell'interfaccia IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)

La tabella seguente riepiloga i vantaggi di ogni approccio usando [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) o [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)



| Funzionalità                                   | Ifilter                      | Ipropertystore |
|----------------------------------------------|------------------------------|----------------|
| Consente il write back nei file?                  | No                           | Sì            |
| Fornisce una combinazione di contenuto e proprietà?      | Sì                          | Sì            |
| Multilingue?                                | Sì                          | No             |
| MIME/Embedded?                               | Sì                          | No             |
| Limiti di testo?                             | Frase, paragrafo, capitolo | Nessuno           |
| Implementazione supportata per SPS/SQL Server? | Sì                          | No             |
| Implementazione                               | Complex                      | Semplice         |



 

Nell'esempio del gestore di recipe il formato del file recipe non presenta requisiti complessi, quindi è stato implementato solo [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per il supporto full-text. La ricerca full-text viene implementata per i nodi XML denominati nella matrice seguente.


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



Il sistema di proprietà contiene la proprietà (PKEY Search Contents), creata per fornire `System.Search.Contents` \_ contenuto \_ full-text all'indicizzatore. Il valore di questa proprietà non viene mai visualizzato direttamente nell'interfaccia utente. Il testo di tutti i nodi XML denominati nella matrice precedente viene concatenato in un'unica stringa. Tale stringa viene quindi fornita all'indicizzatore come contenuto full-text del file recipe tramite una chiamata a [**IPropertyStoreCache::SetValueAndState,**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) come illustrato nell'esempio di codice seguente.


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



## <a name="providing-values-for-properties"></a>Specifica di valori per le proprietà

Quando vengono usati per leggere i valori, i gestori delle proprietà vengono in genere richiamati per uno dei motivi seguenti:

-   Per enumerare tutti i valori delle proprietà.
-   Per ottenere il valore di una proprietà specifica.

Per l'enumerazione, a un gestore delle proprietà viene richiesto di enumerarne le proprietà durante l'indicizzazione o quando la finestra di dialogo delle proprietà richiede la visualizzazione delle proprietà nel **gruppo Altro** . L'indicizzazione continua come operazione in background. Ogni volta che un file viene modificato, l'indicizzatore viene informato e indicizza nuovamente il file richiedendo al gestore delle proprietà di enumerarne le proprietà. È quindi fondamentale che i gestori delle proprietà siano implementati in modo efficiente e restituiranno i valori delle proprietà il più rapidamente possibile. Enumerare tutte le proprietà per le quali si dispone di valori, come si farebbe per qualsiasi raccolta, ma non enumerare le proprietà che comportano calcoli a elevato utilizzo di memoria o richieste di rete che potrebbero renderle lente per il recupero.

Quando si scrive un gestore di proprietà, in genere è necessario considerare i due set di proprietà seguenti.

-   Proprietà primarie: proprietà supportate dal tipo di file in modo nativo. Ad esempio, un gestore della proprietà photo per i metadati EXIF (Exchangeable Image File) supporta in modo nativo `System.Photo.FNumber` .
-   Proprietà estese: proprietà supportate dal tipo di file come parte dei metadati aperti.

Poiché l'esempio usa la cache in memoria, l'implementazione dei metodi [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) è solo una questione di delega a tale cache, come illustrato nell'esempio di codice seguente.


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



Se si sceglie di non delegare alla cache in memoria, è necessario implementare i metodi> il comportamento previsto seguente:

-   [**IPropertyStore::GetCount:**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85))se non sono presenti proprietà, questo metodo restituisce **S \_ OK.**
-   [**IPropertyStore::GetAt:**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85))se *iProp* è maggiore o uguale a *cProps,* questo metodo restituisce E INVALIDARG e la struttura a cui punta il parametro pkey viene riempita con \_ zeri. 
-   [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) riflettono lo stato corrente del gestore della proprietà. Se [**propertyKEY viene**](/windows/win32/api/wtypes/ns-wtypes-propertykey) aggiunto o rimosso dal file tramite [**IPropertyStore::SetValue,**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))questi due metodi devono riflettere tale modifica alla successiva chiamata.
-   [**IPropertyStore::GetValue:**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85))se a questo metodo viene richiesto un valore che non esiste, restituisce **S \_ OK** con il valore segnalato come VT \_ EMPTY.

## <a name="writing-back-values"></a>Scrittura di valori

Quando il gestore delle proprietà scrive il valore di una proprietà usando [**IPropertyStore::SetValue,**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))non scrive il valore nel file fino a quando non viene chiamato [**IPropertyStore::Commit.**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) La cache in memoria può essere utile per implementare questo schema. Nel codice di esempio l'implementazione **di IPropertyStore::SetValue** imposta semplicemente il nuovo valore nella cache in memoria e imposta lo stato di tale proprietà su PSC \_ DIRTY.


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



In qualsiasi [**implementazione di IPropertyStore,**](/windows/win32/api/propsys/nn-propsys-ipropertystore) da [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))è previsto il comportamento seguente:

-   Se la proprietà esiste già, viene impostato il valore della proprietà .
-   Se la proprietà non esiste, viene aggiunta la nuova proprietà e ne viene impostato il valore.
-   Se il valore della proprietà non può essere reso persistente con la stessa accuratezza specificata (ad esempio, il troncamento a causa di limitazioni delle dimensioni nel formato di file), il valore viene impostato per quanto possibile e viene restituito INPLACE \_ S \_ TRUNCATED.
-   Se la proprietà non è supportata dal gestore della proprietà, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` viene restituito .
-   Se esiste un altro motivo per cui non è possibile impostare il valore della proprietà, ad esempio il file bloccato o la mancanza di diritti di modifica tramite elenchi di controllo di accesso (ACL), viene restituito STG \_ E \_ ACCESSDENIED.

Uno dei principali vantaggi dell'uso dei flussi, come nell'esempio, è l'affidabilità. I gestori di proprietà devono sempre considerare che non possono lasciare un file in uno stato incoerente in caso di errore irreversibile. È ovviamente consigliabile evitare di danneggiare i file di un utente e il modo migliore per eseguire questa operazione è con un meccanismo di copia su scrittura. Se il gestore delle proprietà usa un flusso per accedere a un file, si ottiene automaticamente questo comportamento. il sistema scrive tutte le modifiche nel flusso, sostituendo il file con la nuova copia solo durante l'operazione di commit.

Per eseguire l'override di questo comportamento e controllare manualmente il processo di salvataggio dei file, è possibile rifiutare esplicitamente il comportamento di salvataggio sicuro impostando il valore ManualSafeSave nella voce del Registro di sistema del gestore, come illustrato di seguito.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

Quando un gestore specifica il valore ManualSafeSave, il flusso con cui viene inizializzato non è un flusso transazionato (STGM \_ TRANSACTED). Il gestore stesso deve implementare la funzione di salvataggio sicuro per garantire che il file non sia danneggiato se l'operazione di salvataggio viene interrotta. Se il gestore implementa la scrittura sul posto, scriverà nel flusso specificato. Se il gestore non supporta questa funzionalità, deve recuperare un flusso con cui scrivere la copia aggiornata del file usando [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream). Al termine della scrittura, il gestore deve chiamare [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) nel flusso originale per completare l'operazione e sostituire il contenuto del flusso originale con la nuova copia del file.

ManualSafeSave è anche la situazione predefinita se non si inizializza il gestore con un flusso. Senza un flusso originale per ricevere il contenuto del flusso temporaneo, è necessario usare [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) per eseguire una sostituzione atomica del file di origine.

I formati di file di grandi dimensioni che verranno usati in modo da produrre file superiori a 1 MB devono implementare il supporto per la scrittura di proprietà sul posto; In caso contrario, il comportamento delle prestazioni non soddisfa le aspettative dei client del sistema di proprietà. In questo scenario, il tempo necessario per scrivere le proprietà non deve essere influenzato dalle dimensioni del file.

Per i file di dimensioni molto grandi, ad esempio un file video di almeno 1 GB, è necessaria una soluzione diversa. Se lo spazio nel file non è sufficiente per eseguire la scrittura sul posto, il gestore potrebbe non riuscire a eseguire l'aggiornamento della proprietà se la quantità di spazio riservata per la scrittura delle proprietà sul posto è stata esaurita. Questo errore si verifica per evitare prestazioni scarse derivanti da 2 GB di I/O (da 1 a lettura, 1 da scrivere). A causa di questo potenziale errore, questi formati di file devono riservare spazio sufficiente per la scrittura delle proprietà sul posto.

Se il file ha spazio sufficiente nell'intestazione per scrivere i metadati e se la scrittura di questi metadati non causa l'aumentare o la riduzione del file, potrebbe essere sicuro scrivere sul posto. Come punto di partenza è consigliabile usare 64 KB. La scrittura sul posto equivale al gestore che richiede ManualSafeSave e chiama [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) nell'implementazione di [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))e ha prestazioni molto migliori rispetto alla copia in scrittura. Se le dimensioni del file cambiano a causa di modifiche al valore della proprietà, non è consigliabile eseguire la scrittura sul posto a causa del potenziale danneggiamento di un file in caso di terminazione anomala.

> [!Note]  
> Per motivi di prestazioni, è consigliabile usare l'opzione ManualSafeSave con gestori di proprietà che funzionano con file di dimensioni maggiori o superiori a 100 KB.

 

Come illustrato nell'implementazione di esempio seguente di [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), il gestore per ManualSafeSave viene registrato per illustrare l'opzione di salvataggio sicuro manuale. Il **\_ metodo SaveCacheToDom** scrive i valori delle proprietà archiviati nella cache in memoria nell'oggetto XMLdocument.


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



Chiedere quindi se il pecified supporta [**IDestinationStreamFactory.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory)


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



Eseguire quindi il commit del flusso originale, che scrive di nuovo i dati nel file originale in modo sicuro.


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



Esaminare quindi **\_ l'implementazione di SaveCacheToDom.**


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



Scorrere ora le proprietà per determinare se il valore di una proprietà è stato modificato dopo il caricamento in memoria.


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



Il [**metodo IPropertyStoreCache::GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) ottiene lo stato della proprietà nella cache. Il flag DIRTY di PSC, impostato nell'implementazione \_ di [**IPropertyStore::SetValue,**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) contrassegna una proprietà come modificata.


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



Eseguire il mapping della proprietà al nodo XML come specificato nella **matrice \_ rgPropertyMap.**


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



Se una proprietà non è presente nella mappa, è una nuova proprietà impostata da Esplora risorse. Poiché i metadati aperti sono supportati, salvare la nuova proprietà nella **sezione ExtendedProperties** del codice XML.


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

[**IPropertyStoreCapabilities informa**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) l'interfaccia utente della shell se una determinata proprietà può essere modificata nell'interfaccia utente della shell. È importante notare che ciò riguarda solo la possibilità di modificare la proprietà nell'interfaccia utente, non se è possibile chiamare [**correttamente IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) sulla proprietà. Una proprietà che provoca un valore restituito S FALSE da \_ [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) potrebbe comunque essere impostata tramite un'applicazione.


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**IsPropertyWritable restituisce**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) **S \_ OK** per indicare che agli utenti finali deve essere consentito modificare direttamente la proprietà. S \_ FALSE indica che non dovrebbero. S \_ FALSE può significare che le applicazioni sono responsabili della scrittura della proprietà, non degli utenti. Shell disabilita la modifica dei controlli in base ai risultati delle chiamate a questo metodo. Si presuppone che un gestore che non [**implementa IPropertyStoreCapabilities supporti**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) i metadati aperti tramite il supporto per la scrittura di qualsiasi proprietà.

Se si compila un gestore che gestisce solo proprietà di sola lettura, è necessario implementare il metodo **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)o [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) in modo che restituisca STG E ACCESSDENIED quando viene chiamato con il \_ flag \_ STGM \_ READWRITE.

Per alcune proprietà [l'attributo isInnate](./propdesc-schema-typeinfo.md) è impostato su **true.** Le proprietà innate hanno le caratteristiche seguenti:

-   La proprietà viene in genere calcolata in qualche modo. Ad esempio, `System.Image.BitDepth` viene calcolato dall'immagine stessa.
-   La modifica della proprietà non avrebbe senso senza modificare il file. Ad esempio, la modifica non ridimensiona l'immagine, quindi non ha senso consentire `System.Image.Dimensions` all'utente di modificarla.
-   In alcuni casi, queste proprietà vengono fornite automaticamente dal sistema. Ad esempio, , fornito dal file system, e , che si basa sull'utente con cui `System.DateModified` `System.SharedWith` condivide il file.

A causa di queste caratteristiche, le proprietà contrassegnate come *IsInnate* vengono fornite all'utente nell'interfaccia utente della shell solo come proprietà di sola lettura. Se una proprietà è contrassegnata come *IsInnate,* il sistema di proprietà non archivia tale proprietà nel gestore delle proprietà. Pertanto, i gestori delle proprietà non necessitano di codice speciale per la gestione di queste proprietà nelle rispettive implementazioni. Se il valore *dell'attributo IsInnate* non viene dichiarato in modo esplicito per una determinata proprietà, il valore predefinito è **false**.

## <a name="registering-and-distributing-property-handlers"></a>Registrazione e distribuzione di gestori di proprietà

Con il gestore della proprietà implementato, deve essere registrato e la relativa estensione di file associata al gestore. Per altre informazioni, vedere [Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md).

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

 

 
