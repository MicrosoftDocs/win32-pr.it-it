---
description: In questo argomento vengono presentati i requisiti per la creazione di gestori di metadati personalizzati per Windows Imaging Component (WIC), inclusi i lettori e i writer di metadati.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Panoramica dell'estendibilità dei metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d38206fb02c47edbe9744deb6ceb0093277d8354f8717aa89c3f1976bdeb51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088173"
---
# <a name="metadata-extensibility-overview"></a>Panoramica dell'estendibilità dei metadati

In questo argomento vengono presentati i requisiti per la creazione di gestori di metadati personalizzati per Windows Imaging Component (WIC), inclusi i lettori e i writer di metadati. Vengono inoltre illustrati i requisiti per l'estensione dell'individuazione dei componenti di run-time wic per includere i gestori di metadati personalizzati.

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Introduzione](#introduction)
-   [Creazione di un lettore di metadati](#creating-a-metadata-reader)
    -   [Interfaccia IWICMetadataReader](#iwicmetadatareader-interface)
    -   [Interfaccia IWICPersistStream](#iwicpersiststream-interface)
    -   [Interfaccia IWICStreamProvider](#iwicstreamprovider-interface)
-   [Creazione di un writer di metadati](#creating-a-metadata-writer)
    -   [Interfaccia IWICMetadataWriter](#iwicmetadatawriter-interface)
    -   [Interfaccia IWICPersistStream](#iwicpersiststream-interface)
    -   [Interfaccia IWICStreamProvider](#iwicstreamprovider-interface)
-   [Installazione e registrazione di un gestore di metadati](#installing-and-registering-a-metadata-handler)
    -   [Chiavi del Registro di sistema del gestore dei metadati](#metadata-handler-registry-keys)
    -   [Lettori di metadati](#metadata-readers)
    -   [Writer di metadati](#metadata-writers)
    -   [Firma di un gestore di metadati](#signing-a-metadata-handler)
-   [Considerazioni speciali](#special-considerations)
    -   [PROPVARIANTS](#propvariants)
    -   [Gestori 8BIM](#8bim-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere una conoscenza approfondita di WIC, dei relativi componenti e dei metadati per le immagini. Per altre informazioni sui metadati WIC, vedere Panoramica [dei metadati WIC.](-wic-about-metadata.md) Per altre informazioni sui componenti WIC, vedere panoramica del [Windows imaging.](-wic-about-windows-imaging-codec.md)

## <a name="introduction"></a>Introduzione

Come illustrato nella panoramica [dei metadati WIC,](-wic-about-metadata.md)spesso sono presenti più blocchi di metadati all'interno di un'immagine, ognuno dei quali espone tipi diversi di informazioni in formati di metadati diversi. Per interagire con un formato di metadati incorporato in un'immagine, un'applicazione deve usare un gestore di metadati appropriato. WIC offre diversi gestori di metadati (lettori e writer di metadati) che consentono di leggere e scrivere tipi specifici di metadati, ad esempio Exif o XMP.

Oltre ai gestori nativi forniti, WIC fornisce API che consentono di creare nuovi gestori di metadati che partecipano all'individuazione dei componenti di run-time di WIC. In questo modo le applicazioni che usano WIC possono leggere e scrivere i formati di metadati personalizzati.

La procedura seguente consente ai gestori di metadati di partecipare all'individuazione dei metadati di run-time del WiC.

-   Implementare una classe del gestore del lettore di metadati ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) che espone le interfacce WIC necessarie per la lettura del formato dei metadati personalizzato. In questo modo le applicazioni basate su WIC possono leggere il formato dei metadati nello stesso modo in cui leggono i formati di metadati nativi.
-   Implementare una classe del gestore del writer di metadati ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) che espone le interfacce WIC necessarie per la codifica del formato dei metadati personalizzato. Ciò consente alle applicazioni basate su WIC di serializzare il formato dei metadati nei formati di immagine supportati.
-   Firmare e registrare digitalmente i gestori di metadati. Ciò consente di individuare i gestori di metadati in fase di esecuzione abbinando il modello di identificazione nel Registro di sistema con il modello incorporato nel file di immagine.

## <a name="creating-a-metadata-reader"></a>Creazione di un lettore di metadati

L'accesso principale ai blocchi di metadati all'interno di un codec è tramite [**l'interfaccia IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementata da ogni codec WIC. Questa interfaccia enumera ogni blocco di metadati incorporato in un formato immagine in modo che sia possibile individuare e creare un'istanza del gestore di metadati appropriato per ogni blocco. I blocchi di metadati non riconosciuti da WIC sono considerati sconosciuti e sono definiti come CLSID GUID \_ WICUnknownMetadataReader. Per fare in modo che il formato dei metadati sia riconosciuto da WIC, è necessario creare una classe che implementa tre interfacce: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Se il formato dei metadati presenta restrizioni che rendono inappropriati alcuni metodi delle interfacce richieste, tali metodi devono restituire WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatareader-interface"></a>Interfaccia IWICMetadataReader

[**L'interfaccia IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) deve essere implementata durante la creazione di un lettore di metadati. Questa interfaccia consente di accedere agli elementi di metadati sottostante all'interno del flusso di dati di un formato di metadati.

Il codice seguente illustra la definizione dell'interfaccia del lettore di metadati come definito nel file wincodecsdk.idl.

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

Il **metodo GetMetadataFormat** restituisce il GUID del formato dei metadati.

Il **metodo GetMetadataHandlerInfo** restituisce [**un'interfaccia IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) che fornisce informazioni sul gestore dei metadati. Sono incluse informazioni quali quali i formati di immagine che supportano il formato dei metadati e se il lettore di metadati richiede l'accesso al flusso di metadati completo.

Il **metodo GetCount** restituisce il numero di singoli elementi di metadati (inclusi i blocchi di metadati incorporati) trovati all'interno del flusso di metadati.

Il **metodo GetValueByIndex** restituisce un elemento di metadati in base a un valore di indice. Questo metodo consente alle applicazioni di scorrere in ciclo ogni elemento di metadati in un blocco di metadati. Il codice seguente illustra come un'applicazione può usare questo metodo per recuperare ogni elemento di metadati in un blocco di metadati.


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



Il **metodo GetValue** recupera un elemento di metadati specifico in base allo schema e/o all'ID. Questo metodo è simile al **metodo GetValueByIndex,** ad eccezione del fatto che recupera un elemento di metadati con uno schema o un ID specifico.

Il **metodo GetEnumerator** restituisce un enumeratore di ogni elemento di metadati nel blocco di metadati. In questo modo le applicazioni possono usare un enumeratore per spostarsi nel formato dei metadati.

Se il formato dei metadati non ha una nozione di schemi per gli elementi di metadati, getValue... I metodi devono ignorare questa proprietà. Se, tuttavia, il formato supporta la denominazione dello schema, è consigliabile prevedere un **valore NULL.**

Se un elemento di metadati è un blocco di metadati incorporato, creare un gestore di metadati dal flusso secondario del contenuto incorporato e restituire il nuovo gestore di metadati. Se non è disponibile alcun lettore di metadati per il blocco annidato, creare un'istanza di e restituire un lettore di metadati sconosciuto. Per creare un nuovo lettore di metadati per il blocco incorporato, chiamare i metodi **CreateMetadataReaderFromContainer** o **CreateMetadataReader** della factory del componente oppure chiamare la [**funzione WICMatchMetadataContent.**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)

Se il flusso di metadati contiene contenuto big-endian, il lettore di metadati è responsabile dello scambio dei valori dei dati che elabora. È anche responsabile di informare tutti i lettori di metadati annidati che stanno lavorando con il flusso di dati big-endian. Tuttavia, tutti i valori devono essere restituiti in formato little endian.

Implementare il supporto per l'esplorazione dello spazio dei nomi supportando le query in cui l'ID dell'elemento dei metadati è `VT_CLSID` un (GUID) corrispondente a un formato di metadati. Se durante l'analisi viene identificato un lettore di metadati annidati per tale formato, deve essere restituito . In questo modo le applicazioni possono usare un lettore di query di metadati per eseguire ricerche nel formato dei metadati.

Quando si riceve un elemento di metadati in base all'ID, è consigliabile usare la funzione [PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) per forzare l'ID nel tipo previsto. Ad esempio, il lettore IFD forza un ID a digitare in modo che coincida con il tipo di dati di un `VT_UI2` ID di tag IFD USHORT. A tale scopo, il tipo di input e il tipo previsto devono essere [entrambi PROPVARIANT.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Questa operazione non è necessaria, ma questa coercizione semplifica il codice che chiama il lettore per eseguire query per gli elementi di metadati.

### <a name="iwicpersiststream-interface"></a>Interfaccia IWICPersistStream

[**L'interfaccia IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) eredita da **IPersistStream** e fornisce metodi aggiuntivi per salvare e caricare oggetti usando l'enumerazione [**WICPersistOptions.**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)

Il codice seguente illustra la definizione [**dell'interfaccia IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) come definito nel file wincodecsdk.idl.

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

Il **metodo LoadEx** fornisce al lettore di metadati un flusso di dati contenente il blocco di metadati. Il lettore analizza questo flusso per accedere agli elementi di metadati sottostanti. Il lettore di metadati viene inizializzato con un flusso secondario posizionato all'inizio del contenuto dei metadati non elaborati. Se il lettore non richiede il flusso completo, l'intervallo del flusso secondario è limitato al solo contenuto del blocco di metadati. In caso contrario, il flusso di metadati completo viene fornito con la posizione impostata all'inizio del blocco di metadati.

Il **metodo SaveEx** viene usato dai writer di metadati per serializzare il blocco di metadati. Quando **SaveEx viene** usato in un lettore di metadati, deve restituire WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION.

### <a name="iwicstreamprovider-interface"></a>Interfaccia IWICStreamProvider

[**L'interfaccia IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) consente al lettore di metadati di fornire riferimenti al relativo flusso di contenuto, fornire informazioni sul flusso e aggiornare le versioni memorizzate nella cache del flusso.

Il codice seguente illustra la definizione [**dell'interfaccia IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) come definito nel file wincodecsdk.idl.

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

Il **metodo GetStream** recupera un riferimento al flusso di metadati. Il flusso restituito deve avere il puntatore del flusso reimpostato sulla posizione iniziale. Se il formato dei metadati richiede l'accesso completo al flusso, la posizione iniziale deve essere l'inizio del blocco di metadati.

Il **metodo GetPersistOptions** restituisce le opzioni correnti del flusso dall'enumerazione [**WICPersistOptions.**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)

Il **metodo GetPreferredVendorGUID** restituisce il GUID del fornitore del lettore di metadati.

Il **metodo RefreshStream** aggiorna il flusso di metadati. Questo metodo deve chiamare **LoadEx con** un flusso **NULL** per tutti i blocchi di metadati annidati. Ciò è necessario perché i blocchi di metadati annidati e i relativi elementi potrebbero non esistere più a causa della modifica sul posto.

## <a name="creating-a-metadata-writer"></a>Creazione di un writer di metadati

Un writer di metadati è un tipo di gestore di metadati che consente di serializzare un blocco di metadati in un frame di immagine o all'esterno di un singolo frame, se supportato dal formato di immagine. L'accesso principale ai writer di metadati all'interno di un codec è tramite [**l'interfaccia IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) implementata da ogni codificatore WIC. Questa interfaccia consente alle applicazioni di enumerare ognuno dei blocchi di metadati incorporati in un'immagine in modo che sia possibile individuare e creare un'istanza del writer di metadati appropriato per ogni blocco di metadati. I blocchi di metadati che non dispongono di un writer di metadati corrispondente sono considerati sconosciuti e sono definiti come CLSID GUID \_ WICUnknownMetadataReader. Per consentire alle applicazioni abilitate per WIC di serializzare e scrivere il formato dei metadati, è necessario creare una classe che implementa le interfacce [**seguenti: IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Se il formato dei metadati presenta restrizioni che rendono inappropriati alcuni metodi delle interfacce richieste, tali metodi devono restituire WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatawriter-interface"></a>Interfaccia IWICMetadataWriter

[**L'interfaccia IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) deve essere implementata dal writer di metadati. Inoltre, poiché **IWICMetadataWriter** eredita da [**IWICMetadataReader,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)è necessario implementare anche tutti i metodi di **IWICMetadataReader.** Poiché entrambi i tipi di gestore richiedono la stessa ereditarietà dell'interfaccia, è possibile creare una singola classe che fornisce funzionalità di lettura e scrittura.

Il codice seguente illustra la definizione dell'interfaccia del writer di metadati come definito nel file wincodecsdk.idl.

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

Il **metodo SetValue** scrive l'elemento di metadati specificato nel flusso di metadati.

Il **metodo SetValueByIndex** scrive l'elemento di metadati specificato nell'indice specificato nel flusso di metadati. L'indice non fa riferimento all'ID, ma alla posizione dell'elemento all'interno del blocco di metadati.

Il **metodo RemoveValue** rimuove l'elemento di metadati specificato dal flusso di metadati.

Il **metodo RemoveValueByIndex** rimuove dal flusso di metadati l'elemento di metadati in corrispondenza dell'indice specificato. Dopo la rimozione di un elemento, è previsto che gli elementi di metadati rimanenti occupino l'indice liberato se l'indice non è l'ultimo indice. È anche previsto che il conteggio cambi dopo la rimozione dell'elemento.

È responsabilità del writer di metadati convertire gli [elementi PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) nella struttura sottostante richiesta dal formato. Tuttavia, a differenza del lettore di metadati, i tipi VARIANT in genere non devono essere forzati a tipi diversi perché il chiamante indica in modo specifico il tipo di dati da usare.

Il writer di metadati deve eseguire il commit di tutti gli elementi di metadati nel flusso dell'immagine, inclusi i valori nascosti o non riconosciuti. Sono inclusi blocchi di metadati annidati sconosciuti. Tuttavia, è responsabilità del codificatore impostare eventuali elementi di metadati critici prima di avviare l'operazione di salvataggio.

Se il flusso di metadati contiene contenuto big-endian, il writer di metadati è responsabile dello scambio dei valori dei dati che elabora. È anche responsabile di informare gli eventuali writer di metadati annidati che stanno lavorando con un flusso di dati big-endian durante il salvataggio.

Implementare il supporto per la creazione e la rimozione dello spazio dei nomi supportando le operazioni di impostazione e rimozione sugli elementi di metadati con un tipo `VT_CLSID` (GUID) corrispondente a un formato di metadati. Il writer di metadati chiama la [**funzione WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) per incorporare correttamente il contenuto del writer di metadati annidato nel writer di metadati padre.

Se il formato dei metadati supporta la codifica sul posto, l'utente è responsabile della gestione della spaziatura interna richiesta. Per altre informazioni sulla codifica sul posto, vedere WiC Metadata Overview (Panoramica dei metadati [WIC)](-wic-about-metadata.md) e Overview of Reading and Writing Image Metadata (Panoramica della lettura e della [scrittura di metadati di immagini).](-wic-codec-readingwritingmetadata.md)

### <a name="iwicpersiststream-interface"></a>Interfaccia IWICPersistStream

[**L'interfaccia IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) eredita da **IPersistStream** e fornisce metodi aggiuntivi per salvare e caricare oggetti usando l'enumerazione [**WICPersistOptions.**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)

Il codice seguente illustra la definizione [**dell'interfaccia IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) come definito nel file wincodecsdk.idl.

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

Il **metodo LoadEx** fornisce al gestore dei metadati un flusso di dati contenente il blocco di metadati.

Il **metodo SaveEx** serializza i metadati in un flusso. Se il flusso fornito è uguale al flusso di inizializzazione, è necessario eseguire la codifica sul posto. Se la codifica sul posto è supportata, questo metodo deve restituire WINCODEC \_ ERR TOOMUCHMETADATA quando il riempimento non è sufficiente per eseguire \_ la codifica sul posto. Se la codifica sul posto non è supportata, questo metodo deve restituire WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION.

Il **metodo IPersistStream::GetSizeMax** deve essere implementato e deve restituire la dimensione esatta del contenuto dei metadati che verrebbe scritto nel salvataggio successivo.

Il **metodo IPersistStream::IsDirty** deve essere implementato se il writer di metadati viene inizializzato tramite un flusso, in modo che un'immagine possa determinare in modo affidabile se il relativo contenuto è stato modificato.

Se il formato dei metadati supporta blocchi di metadati annidati, il writer di metadati deve delegare ai writer di metadati annidati la serializzazione del contenuto durante il salvataggio in un flusso.

### <a name="iwicstreamprovider-interface"></a>Interfaccia IWICStreamProvider

L'implementazione [**dell'interfaccia IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) per un writer di metadati è la stessa di un lettore di metadati. Per altre informazioni, vedere la sezione Creazione di un lettore di metadati in questo documento.

## <a name="installing-and-registering-a-metadata-handler"></a>Installazione e registrazione di un gestore di metadati

Per installare un gestore di metadati, è necessario fornire l'assembly del gestore e registrarlo nel Registro di sistema. È possibile decidere come e quando vengono popolate le chiavi del Registro di sistema.

> [!Note]  
> Per una leggibilità, i GUID esadecimali effettivi non vengono visualizzati nelle chiavi del Registro di sistema illustrate nelle sezioni seguenti di questo documento. Per trovare il valore esadecimale per un nome descrittivo specificato, vedere i file wincodec.idl e wincodecsdk.idl.

 

### <a name="metadata-handler-registry-keys"></a>Chiavi del Registro di sistema del gestore dei metadati

Ogni gestore di metadati è identificato da un CLSID univoco e ogni gestore deve registrare il proprio CLSID nel GUID id di categoria del gestore di metadati. L'ID categoria di ogni tipo di gestore è definito in wincodec.idl; Il nome dell'ID di categoria per i lettori è CATID WICMetadataReader e il nome dell'ID di categoria per \_ i writer è CATID \_ WICMetadataWriter.

Ogni gestore di metadati è identificato da un CLSID univoco e ogni gestore deve registrare il proprio CLSID nel GUID id di categoria del gestore di metadati. L'ID categoria di ogni tipo di gestore è definito in wincodec.idl; Il nome dell'ID di categoria per i lettori è CATID WICMetadataReader e il nome dell'ID di categoria per \_ i writer è CATID \_ WICMetadataWriter.

> [!Note]  
> Nei seguenti elenchi di chiavi del Registro di sistema, {CLSID lettore} fa riferimento al CLSID univoco fornito per il lettore di metadati. {WRITER CLSID} fa riferimento al CLSID univoco fornito per il writer di metadati. {HANDLER CLSID} fa riferimento al CLSID del lettore, al CLSID del writer o a entrambi, a seconda dei gestori da fornire. {GUID contenitore} fa riferimento all'oggetto contenitore (formato immagine o formato di metadati) che può contenere il blocco di metadati.

 

Le chiavi del Registro di sistema seguenti registrano il gestore dei metadati con gli altri gestori di metadati disponibili:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

Oltre a registrare i gestori nelle rispettive categorie, è necessario registrare anche chiavi aggiuntive che forniscono informazioni specifiche per il gestore. Lettori e writer condividono requisiti simili per le chiavi del Registro di sistema. La sintassi seguente illustra come registrare un gestore. Sia il gestore del reader che il gestore del writer devono essere registrati in questo modo, usando i rispettivi CLSID:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a>Lettori di metadati

La registrazione del lettore di metadati include anche chiavi che descrivono come il lettore può essere incorporato in un formato contenitore. Un formato di contenitore può essere un formato di immagine, ad esempio TIFF o JPEG. può anche essere un altro formato di metadati, ad esempio un blocco di metadati IFD. I formati dei contenitori di immagini supportati in modo nativo sono elencati in wincodec.idl; ogni formato del contenitore di immagini è definito come GUID con un nome che inizia con GUID \_ ContainerFormat. I formati dei contenitori di metadati supportati in modo nativo sono elencati in wincodecsdk.idl; Ogni formato del contenitore di metadati è definito come GUID con un nome che inizia con \_ GUID MetadataFormat.

Le chiavi seguenti registrano un contenitore che il lettore di metadati supporta e i dati necessari per leggere da tale contenitore. Ogni contenitore supportato dal lettore deve essere registrato in questo modo.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

La chiave Pattern descrive il modello binario usato per associare il blocco di metadati al lettore. Quando si definisce un modello per il lettore di metadati, deve essere sufficientemente affidabile che una corrispondenza positiva significa che il lettore di metadati è in grado di comprendere i metadati nel blocco di metadati in fase di elaborazione.

La chiave DataOffset descrive l'offset fisso dei metadati dall'intestazione del blocco. Questa chiave è facoltativa e, se non specificata, significa che i metadati effettivi non possono essere individuati usando un offset fisso dall'intestazione del blocco.

### <a name="metadata-writers"></a>Writer di metadati

La registrazione del writer di metadati include anche chiavi che descrivono come scrivere l'intestazione che precede il contenuto dei metadati incorporato in un formato contenitore. Come per il lettore, un formato del contenitore può essere un formato di immagine o un altro blocco di metadati.

Le chiavi seguenti registrano un contenitore che il writer di metadati supporta e i dati necessari per scrivere l'intestazione e i metadati. Ogni contenitore supportato dal writer deve essere registrato in questo modo.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

La chiave WriteHeader descrive il modello binario dell'intestazione del blocco di metadati da scrivere. Questo modello binario coincide con la chiave pattern reader del formato dei metadati.

La chiave WriteOffset descrive l'offset fisso dall'intestazione del blocco in cui devono essere scritti i metadati. Questa chiave è facoltativa e, se non specificata, significa che i metadati effettivi non devono essere scritti con l'intestazione .

### <a name="signing-a-metadata-handler"></a>Firma di un gestore di metadati

Tutti i gestori di metadati devono essere firmati digitalmente per partecipare al processo di individuazione WIC. WiC non carica alcun gestore non firmato da un'autorità di certificazione attendibile. Per altre informazioni sulla firma digitale, vedere [Introduzione alla firma del codice.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))

## <a name="special-considerations"></a>Considerazioni speciali

Le sezioni seguenti includono informazioni aggiuntive da considerare quando si creano gestori di metadati personalizzati.

### <a name="propvariants"></a>PROPVARIANTS

WIC usa una [proprietà PROPVARIANT per](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) rappresentare un elemento di metadati sia per la lettura che per la scrittura. Un oggetto PROPVARIANT fornisce un tipo di dati e un valore di dati per un elemento di metadati utilizzato all'interno di un formato di metadati. Il writer di un gestore di metadati offre una notevole flessibilità sulla modalità di archiviazione dei dati nel formato dei metadati e sul modo in cui i dati vengono rappresentati all'interno di un blocco di metadati. Nella tabella seguente vengono fornite linee guida che consentono di decidere il tipo PROPVARIANT appropriato da usare in situazioni diverse.



| Il tipo di metadati è...          | Usare il tipo PROPVARIANT      | Proprietà PROPVARIANT                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vuoto o inesistente.       | VT \_ EMPTY                 | Non applicabile.                                                                                                                                                                                                                                                                |
| Non definito.                   | VT \_ BLOB                  | Usare la proprietà BLOB per impostare le dimensioni e il puntatore all'oggetto BLOB allocato tramite CoTaskMemAlloc.                                                                                                                                                                           |
| Blocco di metadati.            | VT \_ UNKNOWN               | Questo tipo usa la proprietà punkVal.                                                                                                                                                                                                                                           |
| Matrice di tipi.           | VT \_ VECTOR \| VT \_ {type}  | Usare la proprietà ca{type} per impostare il conteggio e il puntatore alla matrice allocata tramite CoTaskMemAlloc.                                                                                                                                                                            |
| Matrice di blocchi di metadati. | VARIANTE \_ VT VECTOR \| VT \_ | Usare la proprietà capropvar per impostare la matrice di varianti.                                                                                                                                                                                                                       |
| Valore razionale con segno.     | VT \_ I8                    | Usare la proprietà hVal per impostare il valore. Impostare la parola alta sul denominatore e la parola bassa sul numeratore.                                                                                                                                                                |
| Valore razionale.            | Interfaccia utente \_ VT8                   | Usare la proprietà uhVal per impostare il valore. Impostare HighPart sul denominatore e LowPart sul numeratore. Si noti che LowPart è unsigned int. Il numeratore deve essere convertito da un unsigned int a int per garantire che il bit di segno sia mantenuto, se presente. |



 

Per evitare ridondanza nella rappresentazione di elementi di matrice, non usare matrici sicure. usare solo matrici semplici. In questo modo si riduce il lavoro che un'applicazione deve eseguire durante l'interpretazione dei [tipi PROPVARIANT.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Evitare di usare `VT_BYREF` e archiviare i valori inline quando possibile. `VT_BYREF` è inefficiente per i tipi di piccole dimensioni (comuni per gli elementi di metadati) e non fornisce informazioni sulle dimensioni.

Prima di usare [propVARIANT,](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)chiamare sempre **PropVariantInit** per inizializzare il valore. Al termine dell'esecuzione di PROPVARIANT, chiamare sempre **PropVariantClear** per rilasciare la memoria allocata per la variabile.

### <a name="8bim-handlers"></a>8BIM Handlers (Gestori 8BIM)

Quando si scrive un gestore di metadati per un blocco di metadati 8BIM, è necessario usare una firma che incapsula sia la firma 8BIM che l'ID. Ad esempio, il lettore di metadati 8BIMIPTC nativo fornisce le informazioni del Registro di sistema seguenti per l'individuazione del lettore:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

Il lettore 8BIMIPTC ha un modello registrato di 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04. I primi quattro byte (0x38, 0x42, 0x49, 0x4D) sono la firma 8BIM e gli ultimi due byte (0x04, 0x04) sono l'ID per il record IPTC.

Pertanto, per scrivere un lettore di metadati 8BIM per le informazioni di risoluzione, è necessario un modello registrato di 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED. Anche in questo caso, i primi quattro byte (0x38, 0x42, 0x49, 0x4D) sono la firma 8BIM. Gli ultimi due byte (0x03, 0xED), tuttavia, sono l'ID delle informazioni di risoluzione come definito dal formato PSD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Panoramica dei metadati WIC](-wic-about-metadata.md)
</dt> <dt>

[Panoramica del linguaggio di query sui metadati](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Panoramica della lettura e della scrittura di metadati dell'immagine](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Procedura: Codificare nuovamente un'immagine JPEG con metadati](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
