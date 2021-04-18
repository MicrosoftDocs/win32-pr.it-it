---
description: L'installazione di un gestore di protocollo comporta la copia delle DLL in una posizione appropriata nella directory programmi e quindi la registrazione del gestore del protocollo tramite il registro di sistema.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Installazione e registrazione di gestori di protocollo (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306180"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a>Installazione e registrazione di gestori di protocollo (Windows Search)

L'installazione di un gestore di protocollo comporta la copia delle DLL in una posizione appropriata nella directory programmi e quindi la registrazione del gestore del protocollo tramite il registro di sistema. L'applicazione di installazione può anche aggiungere una radice di ricerca e regole di ambito per definire un ambito di ricerca per indicizzazione predefinito per l'origine dati della shell.

Questo argomento è organizzato nel modo seguente:

-   [Informazioni sugli URL](#about-urls)
-   [Implementazione delle interfacce del gestore di protocollo](#implementing-protocol-handler-interfaces)
    -   [ISearchProtocol e ISearchProtocol2](#isearchprotocol-and-isearchprotocol2)
    -   [IUrlAccessor, IUrlAccessor2, IUrlAccessor3 e IUrlAccessor4](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [IProtocolHandlerSite](#iprotocolhandlersite)
-   [Implementazione di gestori di filtri per i contenitori](#implementing-filter-handlers-for-containers)
-   [Installazione e registrazione di un gestore di protocollo](#installing-and-registering-a-protocol-handler)
    -   [Linee guida per la registrazione di un gestore di protocollo](#guidelines-for-registering-a-protocol-handler)
    -   [Registrazione di un gestore di protocollo](#installing-and-registering-a-protocol-handler)
    -   [Registrazione del gestore del tipo di file del gestore di protocollo](#registering-the-protocol-handlers-file-type-handler)
-   [Verifica dell'indicizzazione degli elementi](#ensuring-that-your-items-are-indexed)
-   [Argomenti correlati](#related-topics)

## <a name="about-urls"></a>Informazioni sugli URL

Windows Search USA gli URL per identificare in modo univoco gli elementi nella gerarchia dell'origine dati della shell. L'URL che rappresenta il primo nodo della gerarchia è denominato radice di [ricerca](-search-3x-wds-extidx-csm-searchroots.md); Windows Search inizierà l'indicizzazione alla radice di ricerca, richiedendo che il gestore di protocollo enumera i collegamenti figlio per ogni URL.

La struttura di URL tipica è la seguente:


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



La sintassi dell'URL è descritta nella tabella seguente.



| Sintassi           | Descrizione                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | Identifica il gestore di protocollo da richiamare per l'URL.                                                                                                                                                           |
| {SID utente}       | Identifica il contesto di sicurezza dell'utente in cui viene chiamato il gestore di protocollo. Se non viene identificato alcun ID di sicurezza utente (SID), il gestore di protocollo viene chiamato nel contesto di sicurezza del servizio di sistema. |
| <path>     | Definisce la gerarchia dell'archivio in cui ogni barra ('/') è un separatore tra i nomi delle cartelle.                                                                                                            |
| <ItemID>   | Rappresenta una stringa univoca che identifica l'elemento figlio, ad esempio il nome del file.                                                                                                                            |



 

L'indicizzatore di ricerca di Windows taglia la barra finale dagli URL. Di conseguenza, non è possibile fare affidamento sulla presenza di una barra finale per identificare una directory rispetto a un elemento. Il gestore di protocollo deve essere in grado di gestire questa sintassi dell'URL. Verificare che il nome del protocollo selezionato per identificare l'origine dati della shell non sia in conflitto con quelli correnti. Questa convenzione di denominazione è consigliata: `companyName.scheme` .

Per ulteriori informazioni sulla creazione di un'origine dati della shell, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="implementing-protocol-handler-interfaces"></a>Implementazione delle interfacce del gestore di protocollo

Per la creazione di un gestore di protocollo è necessaria l'implementazione delle tre interfacce seguenti:

-   [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) per la gestione di oggetti UrlAccessor.
-   [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) per esporre le proprietà e identificare i filtri appropriati per gli elementi nell'origine dati della shell.
-   [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) per filtrare i file proprietari o per enumerare e filtrare i file archiviati in modo gerarchico.

Oltre alle tre interfacce obbligatorie elencate, le altre interfacce sono facoltative ed è possibile implementare qualsiasi interfaccia facoltativa più appropriata per l'attività.

### <a name="isearchprotocol-and-isearchprotocol2"></a>ISearchProtocol e ISearchProtocol2

Le interfacce SearchProtocol inizializzano e gestiscono gli oggetti UrlAccessor del gestore del protocollo. L'interfaccia [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) è un'estensione facoltativa di [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)e include un metodo aggiuntivo per specificare altre informazioni sull'utente e sull'elemento.

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a>IUrlAccessor, IUrlAccessor2, IUrlAccessor3 e IUrlAccessor4

Le interfacce [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) sono descritte nella tabella seguente.



| Interfaccia                                                 | Descrizione                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | Per un URL specificato, l'interfaccia [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) fornisce l'accesso alle proprietà dell'elemento esposto nell'URL. Può inoltre associare tali proprietà a un filtro specifico del gestore di protocollo, ovvero un filtro diverso da quello associato al nome del file. |
| [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (facoltativo) | L'interfaccia [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) estende [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) con metodi che ottengono una tabella codici per le proprietà dell'elemento e il relativo URL di visualizzazione e che ottengono il tipo di elemento nell'URL (documento o directory).                                    |
| [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (facoltativo) | L'interfaccia [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) estende [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) con un metodo che ottiene una matrice di SID utente, consentendo all'host del protocollo di ricerca di rappresentare questi utenti per indicizzare l'elemento.                                                      |
| [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (facoltativo) | L'interfaccia [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) estende la funzionalità dell'interfaccia [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) con un metodo che identifica se il contenuto dell'elemento deve essere indicizzato.                                                                 |



 

Viene creata un'istanza dell'oggetto UrlAccessor che viene inizializzato da un oggetto SearchProtocol. Le interfacce [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) forniscono l'accesso a informazioni importanti tramite i metodi descritti nella tabella seguente.



| Metodo                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor:: GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | Restituisce l'ora dell'Ultima modifica apportata all'URL. Se questa volta è più recente dell'ultima volta in cui l'indicizzatore ha elaborato questo URL, vengono chiamati i gestori di filtro (implementazioni dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) per estrarre i dati modificati (possibilmente) per tale elemento. Gli orari modificati per le directory vengono ignorati. |
| [**IUrlAccessor:: directory**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | Indica se l'URL rappresenta una cartella contenente un URL figlio.                                                                                                                                                                                                                                                            |
| [**IUrlAccessor::BindToStream**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | Esegue l'associazione a un' [interfaccia IStream](/windows/win32/api/objidl/nn-objidl-istream) che rappresenta i dati di un file in un archivio dati personalizzato.                                                                                                                                                                           |
| [**IUrlAccessor::BindToFilter**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | Esegue l'associazione a un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)specifico del gestore di protocollo, che può esporre le proprietà per l'elemento.                                                                                                                                                                                                                 |
| [**IUrlAccessor4::ShouldIndexItemContent**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | Indica se il contenuto dell'elemento deve essere indicizzato.                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a>IProtocolHandlerSite

L'interfaccia [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) viene utilizzata per creare un'istanza di un gestore di filtro, che è ospitato in un processo isolato. Il gestore di filtri appropriato viene ottenuto per un identificatore di classe persistente (CLSID), una classe di archiviazione di documenti o un'estensione di file specificati. Il vantaggio di chiedere al processo host di eseguire l'associazione a [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è che il processo host è in grado di gestire il processo di individuazione di un gestore di filtri appropriato e di controllare la sicurezza richiesta per la chiamata al gestore.

## <a name="implementing-filter-handlers-for-containers"></a>Implementazione di gestori di filtri per i contenitori

Se si implementa un gestore di protocollo gerarchico, è necessario implementare un gestore di filtri per un contenitore che enumera gli URL figlio. Un gestore di filtro è un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Il processo di enumerazione è un ciclo attraverso i metodi [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) e [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) dell'interfaccia **IFilter** . ogni URL figlio viene esposto come valore della proprietà.

[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) restituisce le proprietà del contenitore. Per enumerare gli URL figlio, **IFilter:: GetChunk** restituisce uno dei valori seguenti:

-   [Pkey \_ \_UrlToIndex di ricerca](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):

    URL dell'elemento senza l'ora dell'Ultima modifica. [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) restituisce un PROPVARIANT contenente l'URL figlio.

-   [Pkey \_ \_UrlToIndexWithModificationTime di ricerca](../properties/props-system-search-urltoindexwithmodificationtime.md):

    L'URL e l'ora dell'Ultima modifica. [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) restituisce un PROPVARIANT contenente un vettore dell'URL figlio e l'ora dell'Ultima modifica.

La restituzione di [pkey \_ Search \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) è più efficiente perché l'indicizzatore può determinare immediatamente se l'elemento deve essere indicizzato senza chiamare i metodi [**ISearchProtocol:: CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) e [**IUrlAccessor:: GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) .

Nell'esempio di codice seguente viene illustrato come restituire la proprietà [ \_ \_ UrlToIndexWithModificationTime di ricerca pkey](../properties/props-system-search-urltoindexwithmodificationtime.md) .

> [!IMPORTANT]
>
> Copyright (c) Microsoft Corporation. Tutti i diritti sono riservati.

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> Un componente [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) del contenitore deve sempre enumerare tutti gli URL figlio anche se gli URL figlio non sono stati modificati, perché l'indicizzatore rileva le eliminazioni tramite il processo di enumerazione. Se l'output della data in [un \_ \_ UrlToIndexWithModificationTime di ricerca pkey](../properties/props-system-search-urltoindexwithmodificationtime.md) indica che i dati non sono stati modificati, l'indicizzatore non aggiorna i dati per tale URL.

 

## <a name="installing-and-registering-a-protocol-handler"></a>Installazione e registrazione di un gestore di protocollo

L'installazione dei gestori di protocollo comporta la copia delle DLL in un percorso appropriato nella directory programmi e la successiva registrazione delle DLL. I gestori di protocollo devono implementare la registrazione automatica per l'installazione. L'applicazione di installazione può anche aggiungere una radice di ricerca e regole di ambito per definire un ambito di ricerca per indicizzazione predefinito per l'origine dati della shell, che viene illustrato in [assicurandosi che gli elementi siano indicizzati](#ensuring-that-your-items-are-indexed) alla fine di questo argomento.

### <a name="guidelines-for-registering-a-protocol-handler"></a>Linee guida per la registrazione di un gestore di protocollo

Quando si registra un gestore di protocollo, attenersi alle linee guida seguenti:

-   Il programma di installazione deve usare il programma di installazione EXE o MSI.
-   È necessario fornire le note sulla versione.
-   È necessario creare una voce di installazione applicazioni per ogni componente aggiuntivo installato.
-   Il programma di installazione deve assumere tutte le impostazioni del registro di sistema per il tipo di file o l'archivio specifico che il componente aggiuntivo corrente riconosce.
-   Se un componente aggiuntivo precedente viene sovrascritto, il programma di installazione deve inviare una notifica all'utente.
-   Se un componente aggiuntivo più recente ha sovrascritto il componente aggiuntivo precedente, dovrebbe essere possibile ripristinare la funzionalità del componente aggiuntivo precedente e impostarlo di nuovo come componente aggiuntivo predefinito per quel tipo di file.
-   Il programma di installazione deve definire un ambito di ricerca per indicizzazione predefinito per l'indicizzatore mediante l'aggiunta di una radice di ricerca e le regole dell'ambito mediante Gestione ambito ricerca per indicizzazione.

### <a name="registering-a-protocol-handler"></a>Registrazione di un gestore di protocollo

È necessario creare quattordici voci nel registro di sistema per registrare il componente gestore di protocollo, dove:

-   *Ver \_ IND \_ ProgID* è il ProgID indipendente dalla versione dell'implementazione del gestore del protocollo.
-   *Ver \_ DEP \_ ProgID* è il ProgID dipendente dalla versione dell'implementazione del gestore del protocollo.
-   *CLSID \_ 1* è il CLSID dell'implementazione del gestore di protocollo.

**Per registrare un gestore di protocollo:**

1.  Registrare la versione Independent ProgID con le chiavi e i valori seguenti:

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  Registrare il ProgID dipendente dalla versione con le chiavi e i valori seguenti:

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  Registrare il CLSID del gestore di protocollo con le chiavi e i valori seguenti:

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  Registrare il gestore di protocollo con Windows Search. Nell'esempio seguente <Protocol Name> è il nome del protocollo stesso, ad esempio file, MAPI e così via:

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    Prima di Windows Vista:

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a>Registrazione del gestore del tipo di file del gestore di protocollo

È necessario creare due voci nel registro di sistema per registrare il gestore del tipo di file del gestore di protocollo (noto anche come estensione della Shell).

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a>Verifica dell'indicizzazione degli elementi

Dopo aver implementato il gestore di protocollo, è necessario specificare gli elementi della shell da indicizzare nel gestore del protocollo. È possibile utilizzare Gestione catalogo per avviare la reindicizzazione (per ulteriori informazioni, vedere Utilizzo di [gestione catalogo](-search-3x-wds-mngidx-catalog-manager.md)). In alternativa, è possibile usare anche il gestore della ricerca per indicizzazione (CSM) per configurare le regole predefinite che indicano gli URL di cui l'indicizzatore vuole eseguire la ricerca per indicizzazione. per ulteriori informazioni, vedere [utilizzo di gestione ambito indicizzazione](-search-3x-wds-extidx-csm.md) e [gestione delle regole dell'ambito](-search-3x-wds-extidx-csm-scoperules.md). È anche possibile aggiungere una radice di ricerca (per altre informazioni, vedere [Managing Search Roots](-search-3x-wds-extidx-csm-searchroots.md)). Un'altra opzione disponibile per l'utente consiste nel seguire la procedura descritta nell'esempio REINDEX negli [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

L'interfaccia [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) fornisce metodi che inviano una notifica al motore di ricerca dei contenitori per eseguire la ricerca per indicizzazione e/o guardare e gli elementi sottoposti a tali contenitori da includere o escludere durante la ricerca per indicizzazione In Windows 7 e versioni successive, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) estende **ISearchCrawlScopeManager** con il metodo [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) che ottiene la versione, che informa i client se lo stato del CSM è stato modificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui gestori di protocollo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Sviluppo di gestori di protocollo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Notifica dell'indice delle modifiche](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Aggiunta di icone e menu di scelta rapida](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Esempio di codice: estensioni della Shell per i gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Creazione di un connettore di ricerca per un gestore di protocollo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Debug di gestori di protocollo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
