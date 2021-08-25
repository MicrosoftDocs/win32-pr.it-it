---
title: Implementazione di un gestore di protocollo per WDS
description: La creazione di un gestore di protocollo comporta l'implementazione di ISearchProtocol per gestire gli oggetti UrlAccessor, IUrlAccessor per generare metadati relativi e identificare i filtri appropriati per gli elementi nell'archivio dati, IProtocolHandlerSite per creare un'istanza di un oggetto SearchProtocol e identificare i filtri appropriati e IFilterto filtrare i file proprietari o enumerare e filtrare i file archiviati gerarchicamente.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e33a7ebf6d5f14d0ec4d78031e25b17d59bac5fb99ee7ea6d20046fbe95c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963491"
---
# <a name="implementing-a-protocol-handler-for-wds"></a>Implementazione di un gestore di protocollo per WDS

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows ricerca.](../search/-search-3x-wds-overview.md)

La creazione di un gestore di protocollo comporta l'implementazione di [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) per gestire gli oggetti [**UrlAccessor, IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) per generare metadati relativi e per identificare i filtri appropriati per gli elementi nell'archivio dati, IProtocolHandlerSite per creare un'istanza di un oggetto SearchProtocol e identificare i filtri appropriati e [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per filtrare i file proprietari o per enumerare e filtrare i file archiviati gerarchicamente. Il gestore di protocollo deve essere multithreading.

In questa sezione sono contenuti gli argomenti seguenti:

-   [Nota sugli URL](#note-on-urls)
-   [Interfacce del gestore di protocollo](#protocol-handler-interfaces)
-   [Filtri IFilter per i contenitori](#ifilters-for-containers)
-   [Aggiunta della funzionalità opzioni del gestore di protocollo](#adding-protocol-handler-options-functionality)
    -   [ISearchProtocolOptions](#isearchprotocoloptions)
-   [Argomenti correlati](#related-topics)

## <a name="note-on-urls"></a>Nota sugli URL

Microsoft Windows Desktop Search (WDS) usa gli URL per identificare in modo univoco gli elementi in un file system, all'interno di un archivio simile a un database o sul Web. Un URL che definisce un nodo di immissione è denominato pagina iniziale. WDS inizia dalla pagina iniziale e esegue una ricerca per indicizzazione ricorsiva nell'archivio dati. La struttura tipica dell'URL è:

`protocol://host/path/name.extension`

> [!Note]
>
> Quando si vuole aggiungere un nuovo archivio dati, è necessario selezionare un nome per identificarlo che non sia in conflitto con quello corrente. È consigliabile usare questa convenzione di denominazione: companyName.scheme.

 

## <a name="protocol-handler-interfaces"></a>Interfacce del gestore di protocollo

**ISearchProtocol**

[**L'interfaccia ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) richiama, inizializza e gestisce gli oggetti UrlAccessor. Per altre informazioni sull'implementazione dell'interfaccia ISearchProtocol, vedere **ISearchProtocol Interface reference (Informazioni di riferimento sull'interfaccia ISearchProtocol).**

**IUrlAccessor**

Per un URL specificato, [**l'interfaccia IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) genera metadati sulla struttura del percorso e sugli elementi contenuti e associa tali elementi a un filtro. **L'istanza dell'oggetto IUrlAccessor** viene creata e inizializzata da un oggetto SearchProtocol. Tuttavia, è anche possibile implementare un metodo di inizializzazione interno in modo che l'oggetto **IUrlAccessor** possa eseguire attività di inizializzazione specifiche del gestore di protocollo, ad esempio la convalida dell'URL per un elemento a cui si accede o la verifica dell'ora dell'ultima modifica per determinare se un file deve essere elaborato nella ricerca per indicizzazione corrente.

> [!Note]
>
> Gli orari di modifica per le directory vengono ignorati. [**L'oggetto IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) deve enumerare gli oggetti figlio per determinare se sono state apportate modifiche o eliminazioni.

 

Gran parte della progettazione **dell'oggetto UrlAccessor** dipende dal fatto che la struttura sia gerarchica o basata su collegamento. Per gli archivi dati gerarchici, **l'oggetto UrlAccessor** deve trovare un filtro in grado di enumerarne il contenuto. Un'altra distinzione tra gestori di protocollo gerarchici e basati su collegamento è l'uso del metodo IsDirectory. Nei gestori di protocollo basati su collegamento, questo metodo deve restituire S \_ FALSE. I gestori di protocollo gerarchici devono restituire S \_ OK per i contenitori.

Per altre istruzioni sull'implementazione di [**un'interfaccia IUrlAccessor,**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) vedere le informazioni di [**riferimento sull'interfaccia IUrlAccessor.**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor)

**IProtocolHandlerSite**

Questa interfaccia viene usata per creare un'istanza di un oggetto **SearchProtocol** e fornisce anche all'oggetto **UrlAccessor** un filtro appropriato per un ID di classe (CLSID) specificato.

## <a name="ifilters-for-containers"></a>Filtri IFilter per i contenitori

Se si implementa un gestore di protocollo gerarchico, è necessario implementare un componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)del contenitore che enumera gli URL che rappresentano contenitori o cartelle. Il processo di enumerazione è un ciclo attraverso i metodi **GetChunk** e **GetValue** dell'interfaccia IFilter che restituiscono un elenco di URL che rappresentano ogni elemento nel contenitore.

In primo **luogo, GetChunk** restituisce un oggetto FULLPROSPEC con la proprietà impostata su GATHER \_ PROPSET e su una delle opzioni seguenti:

-   PID \_ GTHR \_ DIRLINK, URL dell'elemento senza l'ora dell'ultima modifica oppure
-   PID \_ GTHR \_ DIRLINK \_ WITH \_ TIME, URL insieme all'ora dell'ultima modifica

Il GUID del set di proprietà per GATHER \_ PROPSET è 0B63E343-9CCC-11D0-BCDB-00805FCCCE04. La proprietà PROPSPEC è PID \_ GTHR \_ DIRLINK=2 o PID \_ GTHR \_ DIRLINK \_ WITH TIME = \_ 12 decimal.

La restituzione di PID GTHR DIRLINK WITH TIME è più efficiente perché l'indicizzatore può determinare immediatamente se l'elemento deve essere indicizzato senza chiamare i metodi \_ \_ \_ \_ ISearchProtocol->CreateUrlAccessor() e IUrlAccessor->GetLastModified().

GetValue **restituisce quindi** un valore PROPVARIANT per l'URL (e l'ora dell'ultima modifica, se usato), come segue:

-   VT \_ LPWSTR, l'URL dell'elemento figlio o
-   Vettore dell'URL seguito da UN FILETIME

Il codice di esempio seguente illustra come compilare il \_ diRLINK PID GTHR \_ \_ WITH TIME \_ corretto.

> [!Note]
>
> **IL CODICE E LE INFORMAZIONI VENGONO FORNITI "COSÌ COME SONO" SENZA GARANZIE DI ALCUN TIPO, ESPRESSE O IMPLICITE, INCLUSE, MA NON LIMITATE, ALLE GARANZIE IMPLICITE DI ESERCENTITÀ E/O IDONEITÀ PER UNO SCOPO SPECIFICO.**
>
> Copyright (C) Microsoft. Tutti i diritti sono riservati.

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
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
>
> Un componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)del contenitore deve sempre enumerare tutti gli URL figlio anche se gli URL figlio non sono stati modificati, perché l'indicizzatore rileva le eliminazioni tramite il processo di enumerazione. Se l'output della data in diR LINKS WITH TIME indica che i dati non sono stati modificati, l'indicizzatore non aggiorna i dati \_ \_ per tale \_ URL.

 

L'URL fisico è l'URL che **l'oggetto UrlAccessor** elabora. Se il filtro non genera un DisplayUrl descrittivo, WDS visualizza l'URL fisico dell'utente come parte dei risultati della ricerca. Lo schema wds contiene due proprietà per controllare ciò che viene visualizzato all'utente finale, come illustrato nella tabella seguente.



| GUID                                 | PROPSPEC      | Descrizione                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | DisplayFolder | Percorso cartella visualizzato all'utente nei risultati della ricerca |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | FolderName    | Nome visualizzato della cartella padre                   |



 

Se il codice non genera displayFolder o FolderName, questi valori vengono calcolati da DisplayUrl. Le barre nell'URL indicano i contenitori all'interno dell'archivio o file system.

## <a name="adding-protocol-handler-options-functionality"></a>Aggiunta della funzionalità opzioni del gestore di protocollo

Perché il gestore di protocollo abbia una pagina iniziale predefinita (e l'URL del nodo di ingresso), è necessario implementare **l'interfaccia ISearchProtocolOptions.** Nelle versioni future di WDS questa interfaccia fornirà hook alla finestra di dialogo Opzioni per un'esperienza utente avanzata. Questa interfaccia fornisce le funzionalità seguenti:

-   Determina se vengono soddisfatti i requisiti per il gestore di protocollo. Ad esempio, l'archivio del gestore di protocollo potrebbe richiedere l'accesso a una determinata applicazione per indicizzare correttamente i dati dell'applicazione, ma tale applicazione non è disponibile.
-   Identifica i requisiti minimi necessari al gestore di protocollo per elaborare un elemento. I requisiti possono essere espressi in una descrizione descrittiva e localizzata, ad esempio "Microsoft Outlook 2000 o versione successiva".
-   Definisce gli URL che il gestore di protocollo deve elaborare per impostazione predefinita.

### <a name="isearchprotocoloptions"></a>ISearchProtocolOptions

La tabella seguente descrive i metodi da implementare per **l'interfaccia ISearchProtocolOptions.**



| Metodo               | Descrizione                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| CheckRequirements    | Determina se vengono soddisfatti i requisiti minimi di un gestore di protocollo personalizzato                             |
| GetDefaultCrawlScope | Restituisce un elenco di URL predefiniti all'interno di un archivio specificato per un gestore di protocollo personalizzato                   |
| GetRequirements      | Identifica una descrizione descrittiva e localizzata dei requisiti minimi per un gestore di protocollo personalizzato |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Notifica delle modifiche all'indice](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Aggiunta di icone, anteprime e menu di scelta rapida con le estensioni della shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 