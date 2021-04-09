---
title: Implementazione di un gestore di protocollo per WDS
description: La creazione di un gestore di protocollo comporta l'implementazione di ISearchProtocol per la gestione di oggetti UrlAccessor, IUrlAccessor per la generazione di metadati relativi e per identificare i filtri appropriati per gli elementi nell'archivio dati, IProtocolHandlerSite per creare un'istanza di un oggetto SearchProtocol e identificare i filtri appropriati e IFilterto filtrare i file proprietari o enumerare e filtrare i file archiviati gerarchicamente.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117647"
---
# <a name="implementing-a-protocol-handler-for-wds"></a>Implementazione di un gestore di protocollo per WDS

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

La creazione di un gestore di protocollo comporta l'implementazione di [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) per la gestione di oggetti UrlAccessor, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) per la generazione di metadati relativi e per identificare i filtri appropriati per gli elementi nell'archivio dati, IProtocolHandlerSite per creare un'istanza di un oggetto SearchProtocol e identificare i filtri appropriati e [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per filtrare i file proprietari o per enumerare e filtrare i file archiviati gerarchicamente. Il gestore di protocollo deve essere multithreading.

In questa sezione sono inclusi gli argomenti seguenti:

-   [Nota sugli URL](#note-on-urls)
-   [Interfacce del gestore di protocollo](#protocol-handler-interfaces)
-   [IFilters per i contenitori](#ifilters-for-containers)
-   [Aggiunta della funzionalità opzioni gestore di protocollo](#adding-protocol-handler-options-functionality)
    -   [ISearchProtocolOptions](#isearchprotocoloptions)
-   [Argomenti correlati](#related-topics)

## <a name="note-on-urls"></a>Nota sugli URL

Microsoft Windows Desktop Search (WDS) USA gli URL per identificare in modo univoco gli elementi in un file system, all'interno di un archivio di tipo database o sul Web. Un URL che definisce un nodo di immissione è denominato pagina iniziale; WDS inizia da tale pagina iniziale e ricerca in modo ricorsivo l'archivio dati. La struttura di URL tipica è la seguente:

`protocol://host/path/name.extension`

> [!Note]
>
> Quando si vuole aggiungere un nuovo archivio dati, è necessario selezionare un nome per identificarlo che non sia in conflitto con quelli correnti. Questa convenzione di denominazione è consigliata: companyName. Scheme.

 

## <a name="protocol-handler-interfaces"></a>Interfacce del gestore di protocollo

**ISearchProtocol**

L'interfaccia [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) richiama, Inizializza e gestisce gli oggetti UrlAccessor. Per ulteriori informazioni sull'implementazione dell'interfaccia ISearchProtocol, vedere **riferimento all'interfaccia ISearchProtocol**.

**IUrlAccessor**

Per un URL specificato, l'interfaccia [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) genera i metadati sulla struttura del percorso e sugli elementi contenuti e associa tali elementi a un filtro. Viene creata un'istanza dell'oggetto **IUrlAccessor** che viene inizializzato da un oggetto SearchProtocol. Tuttavia, è anche possibile implementare un metodo di inizializzazione interna, in modo che l'oggetto **IUrlAccessor** possa eseguire attività di inizializzazione specifiche del gestore di protocollo, ad esempio la convalida dell'URL per un elemento a cui si accede o il controllo dell'ora dell'Ultima modifica per determinare se un file deve essere elaborato nella ricerca corrente.

> [!Note]
>
> Gli orari modificati per le directory vengono ignorati. L'oggetto [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) deve enumerare gli oggetti figlio per determinare se sono state apportate modifiche o eliminazioni.

 

Gran parte della progettazione dell'oggetto **UrlAccessor** dipende dal fatto che la struttura sia gerarchica o basata sul collegamento. Per gli archivi dati gerarchici, l'oggetto **UrlAccessor** deve trovare un filtro in grado di enumerarne il contenuto. Un'altra distinzione tra i gestori di protocollo gerarchici e basati sui collegamenti è l'utilizzo del metodo di directory. Nei gestori di protocollo basati sul collegamento, questo metodo deve restituire S \_ false. I gestori di protocollo gerarchico devono restituire S \_ OK per i contenitori.

Per altre istruzioni sull'implementazione di un'interfaccia [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) , vedere informazioni di riferimento sull' [**interfaccia IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) .

**IProtocolHandlerSite**

Questa interfaccia viene utilizzata per creare un'istanza di un oggetto **SearchProtocol** e fornisce anche l'oggetto **UrlAccessor** con un filtro appropriato per un ID di classe specificato (CLSID).

## <a name="ifilters-for-containers"></a>IFilters per i contenitori

Se si implementa un gestore di protocollo gerarchico, è necessario implementare un componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)del contenitore che enumera gli URL che rappresentano i contenitori o le cartelle. Il processo di enumerazione è un ciclo attraverso i metodi **GetChunk** e **GetValue** dell'interfaccia IFilter che restituiscono un elenco di URL che rappresentano ogni elemento nel contenitore.

In primo luogo, **GetChunk** restituisce un FULLPROSPEC con il set di proprietà gather \_ propset e uno dei seguenti:

-   PID \_ gthr \_ DIRLINK, l'URL dell'elemento senza l'ora dell'Ultima modifica o
-   PID \_ gthr \_ DIRLINK \_ con il \_ tempo, l'URL e l'ora dell'Ultima modifica

Il GUID del set di proprietà per GATHER \_ propset è 0B63E343-9CCC-11D0-Bcdb-00805FCCCE04. La proprietà Campo PROPSPEC è PID \_ gthr \_ DIRLINK = 2 o PID \_ gthr \_ DIRLINK \_ with \_ Time = 12 Decimal.

La restituzione \_ di PID gthr \_ DIRLINK \_ con \_ l'ora è più efficiente perché l'indicizzatore può determinare immediatamente se l'elemento deve essere indicizzato senza chiamare i metodi ISearchProtocol->CreateUrlAccessor () e IUrlAccessor->GetLastModified ().

Quindi **GetValue** restituisce un PROPVARIANT per l'URL (e l'ora dell'Ultima modifica, se usato), come:

-   VT \_ LPWSTR, URL dell'elemento figlio oppure
-   Vettore dell'URL seguito da un FILETIME

Il codice di esempio seguente illustra come compilare il PID \_ gthr \_ DIRLINK appropriato \_ con il \_ tempo.

> [!Note]
>
> **QUESTO CODICE E LE INFORMAZIONI VENGONO FORNITE "COSÌ COME SONO" SENZA GARANZIA DI ALCUN TIPO, ESPRESSA O IMPLICITA, INCLUSE, A TITOLO ESEMPLIFICATIVO, LE GARANZIE IMPLICITE DI COMMERCIABILITÀ E/O IDONEITÀ PER UNO SCOPO SPECIFICO.**
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
> Un componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)del contenitore deve sempre enumerare tutti gli URL figlio anche se gli URL figlio non sono stati modificati, perché l'indicizzatore rileva le eliminazioni tramite il processo di enumerazione. Se l'output della data in un \_ collegamento dir \_ con l' \_ ora indica che i dati non sono stati modificati, l'indicizzatore non aggiorna i dati per tale URL.

 

L'URL fisico è l'URL elaborato dall'oggetto **UrlAccessor** . Se il filtro non genera un DisplayUrl intuitivo, WDS Visualizza l'URL fisico all'utente come parte dei risultati della ricerca. Lo schema WDS contiene due proprietà che consentono di controllare ciò che viene visualizzato all'utente finale, come illustrato nella tabella seguente.



| GUID                                 | Campo PROPSPEC      | Descrizione                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | DisplayFolder | Percorso della cartella visualizzato all'utente nei risultati della ricerca |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | FolderName    | Nome visualizzato della cartella padre                   |



 

Se il codice non genera DisplayFolder o FolderName, questi valori vengono calcolati da DisplayUrl. Le barre nell'URL indicano i contenitori all'interno dell'archivio o file system.

## <a name="adding-protocol-handler-options-functionality"></a>Aggiunta della funzionalità opzioni gestore di protocollo

Affinché il gestore di protocollo disponga di una pagina iniziale predefinita e di un URL del nodo di ingresso, è necessario implementare l'interfaccia **ISearchProtocolOptions** . Nelle versioni future di WDS questa interfaccia fornirà Hook alla finestra di dialogo Opzioni per un'esperienza utente migliorata. Questa interfaccia offre le funzionalità seguenti:

-   Determina se i requisiti per il gestore di protocollo sono soddisfatti. Ad esempio, l'archivio del gestore di protocollo potrebbe richiedere l'accesso a una determinata applicazione per indicizzare correttamente i dati dell'applicazione, ma l'applicazione non è disponibile.
-   Identifica i requisiti minimi necessari al gestore di protocollo per elaborare un elemento. I requisiti possono essere espressi in una descrizione intuitiva e localizzata, ad esempio "Microsoft Outlook 2000 o versione successiva".
-   Definisce gli URL che devono essere elaborati dal gestore di protocollo per impostazione predefinita.

### <a name="isearchprotocoloptions"></a>ISearchProtocolOptions

Nella tabella seguente vengono descritti i metodi che è necessario implementare per l'interfaccia **ISearchProtocolOptions** .



| Metodo               | Descrizione                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| CheckRequirements    | Determina se vengono soddisfatti i requisiti minimi di un gestore di protocollo personalizzato                             |
| GetDefaultCrawlScope | Restituisce un elenco di URL predefiniti all'interno di un archivio specificato per un gestore di protocollo personalizzato                   |
| Getrequirements      | Identifica una descrizione intuitiva e localizzata dei requisiti minimi per un gestore di protocollo personalizzato |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Notifica dell'indice delle modifiche](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Aggiunta di icone, anteprime e menu di scelta rapida con le estensioni della shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 