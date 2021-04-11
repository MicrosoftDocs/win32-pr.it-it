---
description: In questo argomento vengono introdotti i requisiti per la creazione di gestori di metadati personalizzati per il componente di imaging Windows (WIC), inclusi i reader di metadati e i writer.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Panoramica dell'estendibilità dei metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232323"
---
# <a name="metadata-extensibility-overview"></a>Panoramica dell'estendibilità dei metadati

In questo argomento vengono introdotti i requisiti per la creazione di gestori di metadati personalizzati per il componente di imaging Windows (WIC), inclusi i reader di metadati e i writer. Vengono inoltre illustrati i requisiti per estendere l'individuazione dei componenti in fase di esecuzione di WIC per includere i gestori di metadati personalizzati.

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
    -   [Chiavi del registro di sistema del gestore dei metadati](#metadata-handler-registry-keys)
    -   [Lettori di metadati](#metadata-readers)
    -   [Writer di metadati](#metadata-writers)
    -   [Firma di un gestore di metadati](#signing-a-metadata-handler)
-   [Considerazioni speciali](#special-considerations)
    -   [PROPVARIANTS](#propvariants)
    -   [Gestori 8BIM](#8bim-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere una conoscenza approfondita di WIC, dei relativi componenti e dei metadati per le immagini. Per ulteriori informazioni sui metadati WIC, vedere [Cenni preliminari sui metadati WIC](-wic-about-metadata.md). Per ulteriori informazioni sui componenti WIC, vedere [Cenni preliminari sul componente Windows Imaging](-wic-about-windows-imaging-codec.md).

## <a name="introduction"></a>Introduzione

Come illustrato nella [Panoramica dei metadati di WIC](-wic-about-metadata.md), spesso sono presenti più blocchi di metadati all'interno di un'immagine, ognuno dei quali espone tipi diversi di informazioni in formati di metadati diversi. Per interagire con un formato di metadati incorporato in un'immagine, un'applicazione deve usare un gestore di metadati appropriato. WIC fornisce diversi gestori di metadati (Reader di metadati e writer) che consentono di leggere e scrivere tipi specifici di metadati, ad esempio EXIF o XMP.

Oltre ai gestori nativi forniti, WIC fornisce le API che consentono di creare nuovi gestori di metadati che fanno parte dell'individuazione del componente runtime di WIC. Ciò consente alle applicazioni che utilizzano WIC di leggere e scrivere formati di metadati personalizzati.

I passaggi seguenti consentono ai gestori di metadati di partecipare all'individuazione dei metadati di run-time di WIC.

-   Implementare una classe del gestore di lettura dei metadati ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) che espone le interfacce WIC necessarie per la lettura del formato di metadati personalizzato. Ciò consente alle applicazioni basate su WIC di leggere il formato dei metadati nello stesso modo in cui leggono i formati di metadati nativi.
-   Implementare una classe di gestori di writer di metadati ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) che espone le interfacce WIC necessarie per la codifica del formato di metadati personalizzato. Ciò consente alle applicazioni basate su WIC di serializzare il formato dei metadati in formati di immagine supportati.
-   Firmare digitalmente e registrare i gestori di metadati. In questo modo i gestori dei metadati possono essere individuati in fase di esecuzione associando il modello di identificazione nel registro di sistema al modello incorporato nel file di immagine.

## <a name="creating-a-metadata-reader"></a>Creazione di un lettore di metadati

L'accesso principale ai blocchi di metadati all'interno di un codec è tramite l'interfaccia [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementata da ciascun codec WIC. Questa interfaccia enumera tutti i blocchi di metadati incorporati in un formato di immagine in modo che sia possibile individuare e creare un'istanza del gestore di metadati appropriato per ogni blocco. I blocchi di metadati non riconosciuti da WIC sono considerati sconosciuti e sono definiti come CLSID GUID \_ WICUnknownMetadataReader. Per fare in modo che il formato dei metadati venga riconosciuto da WIC, è necessario creare una classe che implementi tre interfacce: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Se il formato dei metadati presenta restrizioni che eseguono il rendering di alcuni metodi delle interfacce richieste inappropriate, tali metodi devono restituire WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatareader-interface"></a>Interfaccia IWICMetadataReader

L'interfaccia [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) deve essere implementata quando si crea un lettore di metadati. Questa interfaccia fornisce l'accesso agli elementi di metadati sottoposti all'interno del flusso di dati di un formato di metadati.

Nel codice seguente viene illustrata la definizione dell'interfaccia del lettore di metadati come definito nel file wincodecsdk. idl.

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

Il metodo **GetMetadataFormat** restituisce il GUID del formato dei metadati.

Il metodo **GetMetadataHandlerInfo** restituisce un'interfaccia [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) che fornisce informazioni sul gestore di metadati. Sono incluse informazioni quali i formati di immagine che supportano il formato dei metadati e il fatto che il lettore di metadati debba accedere al flusso di metadati completo.

Il metodo **GetCount** restituisce il numero di singoli elementi di metadati (compresi i blocchi di metadati incorporati) trovati all'interno del flusso di metadati.

Il metodo **GetValueByIndex** restituisce un elemento di metadati in base a un valore di indice. Questo metodo consente alle applicazioni di scorrere in ciclo ogni elemento di metadati in un blocco di metadati. Nel codice seguente viene illustrato come un'applicazione può utilizzare questo metodo per recuperare ogni elemento di metadati in un blocco di metadati.


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



Il metodo **GetValue** recupera un elemento di metadati specifico per schema e/o ID. Questo metodo è simile al metodo **GetValueByIndex** , con la differenza che recupera un elemento di metadati con uno schema o un ID specifico.

Il metodo **GetEnumerator** restituisce un enumeratore di ogni elemento di metadati nel blocco di metadati. Ciò consente alle applicazioni di utilizzare un enumeratore per esplorare il formato dei metadati.

Se il formato dei metadati non ha una nozione di schemi per gli elementi di metadati, GetValue... i metodi devono ignorare questa proprietà. Se, tuttavia, il formato supporta la denominazione dello schema, è necessario prevedere un valore **null** .

Se un elemento dei metadati è un blocco di metadati incorporato, creare un gestore di metadati dal sottoflusso del contenuto incorporato e restituire il nuovo gestore di metadati. Se non è disponibile alcun lettore di metadati per il blocco annidato, creare un'istanza di e restituire un lettore di metadati sconosciuto. Per creare un nuovo lettore di metadati per il blocco incorporato, chiamare i metodi **CreateMetadataReaderFromContainer** o **CreateMetadataReader** della factory del componente oppure chiamare la funzione [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) .

Se il flusso di metadati contiene contenuto big endian, il lettore di metadati è responsabile dello scambio di tutti i valori di dati elaborati. È anche responsabile di informare i lettori di metadati annidati che lavorano con il flusso di dati big-endian. Tuttavia, tutti i valori devono essere restituiti in formato little-endian.

Implementare il supporto per la navigazione dello spazio dei nomi supportando le query in cui l'ID elemento dei metadati è un `VT_CLSID` (Guid) corrispondente a un formato di metadati. Se un lettore di metadati annidati per tale formato viene identificato durante l'analisi, deve essere restituito. Ciò consente alle applicazioni di utilizzare un lettore di query di metadati per eseguire ricerche nel formato dei metadati.

Quando si recupera un elemento di metadati in base all'ID, è necessario utilizzare la [funzione PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) per assegnare l'ID al tipo previsto. Il lettore IFD, ad esempio, forza l'assegnazione di un ID al tipo `VT_UI2` in concomitanza con il tipo di dati di un ID di tag IFD UShort. Per eseguire questa operazione, è necessario che il tipo di input e il tipo previsto siano [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Questa operazione non è necessaria, ma questa coercizione semplifica il codice che chiama il Reader per eseguire una query per gli elementi di metadati.

### <a name="iwicpersiststream-interface"></a>Interfaccia IWICPersistStream

L'interfaccia [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) eredita da **IPersistStream** e fornisce metodi aggiuntivi per il salvataggio e il caricamento di oggetti tramite l'enumerazione [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

Nel codice seguente viene illustrata la definizione dell'interfaccia [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) come definito nel file wincodecsdk. idl.

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

Il metodo **LoadEx** fornisce al lettore di metadati un flusso di dati contenente il blocco di metadati. Il lettore analizza questo flusso per accedere agli elementi di metadati sottostanti. Il lettore di metadati viene inizializzato con un sottoflusso posizionato all'inizio del contenuto dei metadati non elaborati. Se il lettore non richiede il flusso completo, il sottoflusso è limitato nell'intervallo al solo contenuto del blocco di metadati. in caso contrario, il flusso di metadati completo viene fornito con la posizione impostata all'inizio del blocco di metadati.

Il metodo **SaveEx** viene utilizzato dai writer di metadati per serializzare il blocco di metadati. Quando **SaveEx** viene utilizzato in un lettore di metadati, deve restituire WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

### <a name="iwicstreamprovider-interface"></a>Interfaccia IWICStreamProvider

L'interfaccia [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) consente al lettore di metadati di fornire riferimenti al relativo flusso di contenuto, fornire informazioni sul flusso e aggiornare le versioni memorizzate nella cache del flusso.

Nel codice seguente viene illustrata la definizione dell'interfaccia [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) come definito nel file wincodecsdk. idl.

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

Il metodo **GetStream** recupera un riferimento al flusso di metadati. Il flusso restituito deve avere il puntatore del flusso reimpostato sulla posizione iniziale. Se il formato dei metadati richiede l'accesso completo al flusso, la posizione iniziale deve essere l'inizio del blocco di metadati.

Il metodo **GetPersistOptions** restituisce le opzioni correnti del flusso dall'enumerazione [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

Il metodo **GetPreferredVendorGUID** restituisce il GUID del fornitore del lettore di metadati.

Il metodo **RefreshStream** aggiorna il flusso di metadati. Questo metodo deve chiamare **LoadEx** con un flusso **null** per qualsiasi blocco di metadati annidato. Questa operazione è necessaria perché i blocchi di metadati annidati e i relativi elementi potrebbero non esistere più, a causa della modifica sul posto.

## <a name="creating-a-metadata-writer"></a>Creazione di un writer di metadati

Un writer di metadati è un tipo di gestore di metadati che fornisce un modo per serializzare un blocco di metadati in un frame immagine o all'esterno di un singolo frame se il formato dell'immagine lo supporta. L'accesso principale ai writer di metadati all'interno di un codec è tramite l'interfaccia [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) implementata da ciascun codificatore WIC. Questa interfaccia consente alle applicazioni di enumerare ogni blocco di metadati incorporato in un'immagine in modo che il writer di metadati appropriato possa essere individuato e di cui è stata creata un'istanza per ogni blocco di metadati. I blocchi di metadati che non dispongono di un writer di metadati corrispondente sono considerati sconosciuti e sono definiti come CLSID GUID \_ WICUnknownMetadataReader. Per abilitare le applicazioni abilitate per WIC per la serializzazione e la scrittura del formato dei metadati, è necessario creare una classe che implementi le interfacce seguenti: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Se il formato dei metadati presenta restrizioni che eseguono il rendering di alcuni metodi delle interfacce richieste inappropriate, tali metodi devono restituire WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatawriter-interface"></a>Interfaccia IWICMetadataWriter

L'interfaccia [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) deve essere implementata dal writer di metadati. Poiché **IWICMetadataWriter** eredita da [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), è inoltre necessario implementare tutti i metodi di **IWICMetadataReader**. Poiché entrambi i tipi di gestori richiedono la stessa ereditarietà dell'interfaccia, potrebbe essere necessario creare una singola classe che fornisca la funzionalità di lettura e scrittura.

Nel codice seguente viene illustrata la definizione dell'interfaccia del writer dei metadati come definito nel file wincodecsdk. idl.

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

Il metodo **SetValue** scrive l'elemento dei metadati specificato nel flusso di metadati.

Il metodo **SetValueByIndex** scrive l'elemento dei metadati specificato nell'indice specificato nel flusso di metadati. L'indice non fa riferimento all'ID ma alla posizione dell'elemento all'interno del blocco di metadati.

Il metodo **RemoveValue** rimuove l'elemento di metadati specificato dal flusso di metadati.

Il metodo **RemoveValueByIndex** rimuove l'elemento di metadati in corrispondenza dell'indice specificato dal flusso di metadati. Dopo la rimozione di un elemento, è previsto che gli elementi dei metadati rimanenti occupino l'indice sgomberato se l'indice non è l'ultimo indice. Si prevede anche che il conteggio cambierà dopo la rimozione dell'elemento.

È responsabilità del writer dei metadati convertire gli elementi [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) nella struttura sottostante richiesta dal formato. Tuttavia, a differenza del lettore di metadati, i tipi VARIANT non devono essere in genere assegnati a tipi diversi perché il chiamante indica in modo specifico il tipo di dati da usare.

Il writer di metadati deve eseguire il commit di tutti gli elementi di metadati nel flusso dell'immagine, inclusi i valori nascosti o non riconosciuti. Sono inclusi i blocchi di metadati annidati sconosciuti. Tuttavia, è responsabilità del codificatore impostare gli elementi di metadati critici prima di avviare l'operazione di salvataggio.

Se il flusso di metadati contiene contenuto big endian, il writer dei metadati è responsabile dello scambio di tutti i valori di dati elaborati. È anche responsabile di informare eventuali writer di metadati annidati che utilizzano un flusso di dati Big-Endian quando vengono salvati.

Implementare il supporto per la creazione e la rimozione dello spazio dei nomi supportando operazioni set e Remove sugli elementi di metadati con un tipo di `VT_CLSID` (Guid) corrispondente a un formato di metadati. Il writer di metadati chiama la funzione [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) per incorporare correttamente il contenuto del writer di metadati annidato nel writer di metadati padre.

Se il formato dei metadati supporta la codifica sul posto, si è responsabili della gestione della spaziatura interna necessaria. Per ulteriori informazioni sulla codifica sul posto, vedere [Cenni preliminari sui metadati WIC](-wic-about-metadata.md) e [Cenni preliminari sulla lettura e scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md).

### <a name="iwicpersiststream-interface"></a>Interfaccia IWICPersistStream

L'interfaccia [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) eredita da **IPersistStream** e fornisce metodi aggiuntivi per il salvataggio e il caricamento di oggetti tramite l'enumerazione [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

Nel codice seguente viene illustrata la definizione dell'interfaccia [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) come definito nel file wincodecsdk. idl.

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

Il metodo **LoadEx** fornisce al gestore di metadati un flusso di dati contenente il blocco di metadati.

Il metodo **SaveEx** serializza i metadati in un flusso. Se il flusso specificato è uguale al flusso di inizializzazione, è consigliabile eseguire la codifica sul posto. Se è supportata la codifica sul posto, questo metodo deve restituire WINCODEC \_ Err \_ TOOMUCHMETADATA quando la spaziatura interna non è sufficiente per eseguire la codifica sul posto. Se la codifica sul posto non è supportata, questo metodo deve restituire WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

Il metodo **IPersistStream:: GetSizeMax** deve essere implementato e deve restituire la dimensione esatta del contenuto dei metadati che verrà scritto nel salvataggio successivo.

È necessario implementare il metodo **IPersistStream:: IsDirty** se il writer dei metadati viene inizializzato tramite un flusso, in modo che un'immagine possa determinare in modo affidabile se il relativo contenuto è stato modificato.

Se il formato dei metadati supporta i blocchi di metadati annidati, il writer di metadati deve delegare ai writer di metadati annidati la serializzazione del contenuto durante il salvataggio in un flusso.

### <a name="iwicstreamprovider-interface"></a>Interfaccia IWICStreamProvider

L'implementazione dell'interfaccia [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) per un writer di metadati è identica a quella di un lettore di metadati. Per ulteriori informazioni, vedere la sezione Creazione di un lettore di metadati in questo documento.

## <a name="installing-and-registering-a-metadata-handler"></a>Installazione e registrazione di un gestore di metadati

Per installare un gestore di metadati, è necessario fornire l'assembly del gestore e registrarlo nel registro di sistema. È possibile decidere come e quando vengono popolate le chiavi del registro di sistema.

> [!Note]  
> Per migliorare la leggibilità, i GUID esadecimali effettivi non vengono visualizzati nelle chiavi del registro di sistema illustrate nelle sezioni seguenti di questo documento. Per trovare il valore esadecimale per un nome descrittivo specificato, vedere i file wincodec. idl e wincodecsdk. idl.

 

### <a name="metadata-handler-registry-keys"></a>Chiavi del registro di sistema del gestore dei metadati

Ogni gestore di metadati è identificato da un CLSID univoco e ogni gestore è necessario per registrare il relativo CLSID sotto il GUID dell'ID di categoria del gestore di metadati. Ogni ID di categoria del tipo di gestore è definito in wincodec. idl; il nome dell'ID categoria per i lettori è CATId \_ WICMetadataReader e il nome ID categoria per Writers è CATID \_ WICMetadataWriter.

Ogni gestore di metadati è identificato da un CLSID univoco e ogni gestore è necessario per registrare il relativo CLSID sotto il GUID dell'ID di categoria del gestore di metadati. Ogni ID di categoria del tipo di gestore è definito in wincodec. idl; il nome dell'ID categoria per i lettori è CATId \_ WICMetadataReader e il nome ID categoria per Writers è CATID \_ WICMetadataWriter.

> [!Note]  
> Negli elenchi di chiavi del registro di sistema seguenti, {Reader CLSID} fa riferimento al CLSID univoco fornito per il lettore di metadati. {Writer CLSID} fa riferimento al CLSID univoco fornito per il writer di metadati. {Handler CLSID} fa riferimento al CLSID del Reader, al CLSID del writer o a entrambi, a seconda dei gestori che vengono fornite. {Container GUID} fa riferimento all'oggetto contenitore (formato di immagine o formato dei metadati) che può contenere il blocco di metadati.

 

Le chiavi del registro di sistema seguenti registrano il gestore di metadati con gli altri gestori di metadati disponibili:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

Oltre a registrare i gestori nelle rispettive categorie, è necessario registrare anche chiavi aggiuntive che forniscono informazioni specifiche per il gestore. I lettori e i writer condividono requisiti di chiave del registro di sistema simili. Nella sintassi seguente viene illustrato come registrare un gestore. Il gestore del lettore e il gestore del writer devono essere registrati in questo modo, usando i rispettivi CLSID:

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

La registrazione del lettore di metadati include anche chiavi che descrivono come è possibile incorporare il Reader in un formato di contenitore. Un formato di contenitore può essere un formato di immagine, ad esempio TIFF o JPEG. può anche essere un altro formato di metadati, ad esempio un blocco di metadati IFD. I formati di contenitori di immagini supportati in modo nativo sono elencati in wincodec. idl; ogni formato di contenitore di immagini viene definito come GUID con un nome che inizia con GUID \_ containerFormat. I formati di contenitori di metadati supportati in modo nativo sono elencati in wincodecsdk. idl; ogni formato di contenitore di metadati viene definito come GUID con un nome che inizia con GUID \_ MetadataFormat.

Le chiavi seguenti registrano un contenitore supportato dal lettore di metadati e i dati necessari per la lettura da tale contenitore. Ogni contenitore supportato dal reader deve essere registrato in questo modo.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

La chiave del modello descrive il modello binario utilizzato per associare il blocco di metadati al lettore. Quando si definisce un modello per il lettore di metadati, è consigliabile che il lettore dei metadati possa comprendere i metadati nel blocco di metadati in fase di elaborazione.

La chiave dataOffset descrive l'offset fisso dei metadati dall'intestazione del blocco. Questa chiave è facoltativa e, se non specificata, significa che i metadati effettivi non possono essere individuati usando un offset fisso dall'intestazione del blocco.

### <a name="metadata-writers"></a>Writer di metadati

La registrazione del writer dei metadati include anche chiavi che descrivono come scrivere l'intestazione che precede il contenuto dei metadati incorporato in un formato di contenitore. Come nel lettore, un formato di contenitore può essere un formato di immagine o un altro blocco di metadati.

Le chiavi seguenti registrano un contenitore supportato dal writer di metadati e i dati necessari per scrivere l'intestazione e i metadati. Ogni contenitore supportato dal writer deve essere registrato in questo modo.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

La chiave WriteHeader descrive il modello binario dell'intestazione del blocco di metadati da scrivere. Questo schema binario coincide con la chiave del pattern Reader del formato dei metadati.

La chiave WriteOffset descrive l'offset fisso dall'intestazione del blocco in cui devono essere scritti i metadati. Questa chiave è facoltativa e, se non specificata, significa che i metadati effettivi non devono essere scritti con l'intestazione.

### <a name="signing-a-metadata-handler"></a>Firma di un gestore di metadati

Tutti i gestori di metadati devono essere firmati digitalmente per partecipare al processo di individuazione WIC. Per WIC non verrà caricato alcun gestore non firmato da un'autorità di certificazione attendibile. Per ulteriori informazioni sulla firma digitale, vedere [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).

## <a name="special-considerations"></a>Considerazioni speciali

Le sezioni seguenti includono informazioni aggiuntive che è necessario prendere in considerazione durante la creazione di gestori di metadati personalizzati.

### <a name="propvariants"></a>PROPVARIANTS

WIC usa un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) per rappresentare un elemento di metadati sia per la lettura che per la scrittura. Un PROPVARIANT fornisce un tipo di dati e un valore di dati per un elemento di metadati utilizzato in un formato di metadati. In qualità di writer di un gestore di metadati, è possibile avere una grande flessibilità sulla modalità di archiviazione dei dati nel formato dei metadati e sulla modalità di rappresentazione dei dati all'interno di un blocco di metadati. Nella tabella seguente vengono fornite le linee guida che consentono di scegliere il tipo di PROPVARIANT appropriato da utilizzare in situazioni diverse.



| Il tipo di metadati è...          | USA tipo PROPVARIANT      | Proprietà PROPVARIANT                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vuoto o inesistente.       | VT \_ vuoto                 | Non applicabile.                                                                                                                                                                                                                                                                |
| Non definito.                   | \_BLOB VT                  | Usare la proprietà BLOB per impostare le dimensioni e il puntatore all'oggetto BLOB allocato usando CoTaskMemAlloc.                                                                                                                                                                           |
| Un blocco di metadati.            | VT \_ sconosciuto               | Questo tipo usa la proprietà punkVal.                                                                                                                                                                                                                                           |
| Matrice di tipi.           | VT \_ vettore \| VT \_ {Type}  | Usare la proprietà CA {Type} per impostare il conteggio e il puntatore sulla matrice allocata usando CoTaskMemAlloc.                                                                                                                                                                            |
| Matrice di blocchi di metadati. | \_ \| variante VT vector \_ VT | Utilizzare la proprietà capropvar per impostare la matrice di varianti.                                                                                                                                                                                                                       |
| Valore razionale con segno.     | \_I8 VT                    | Utilizzare la proprietà hVal per impostare il valore. Impostare la parola alta sul denominatore e la parola bassa sul numeratore.                                                                                                                                                                |
| Valore razionale.            | \_UI8 VT                   | Utilizzare la proprietà uhVal per impostare il valore. Impostare HighPart sul denominatore e LowPart sul numeratore. Si noti che LowPart è un int senza segno. Il numeratore deve essere convertito da un int senza segno a un int per garantire che il bit di segno venga mantenuto se presente. |



 

Per evitare la ridondanza nella rappresentazione di elementi di matrice, non usare matrici sicure; usare solo matrici semplici. In questo modo si riduce il lavoro che un'applicazione deve eseguire quando si interpretano i tipi [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Evitare `VT_BYREF` di usare e archiviare i valori in linea laddove possibile. `VT_BYREF` è inefficiente per i tipi piccoli (comuni per gli elementi di metadati) e non fornisce informazioni sulle dimensioni.

Prima di usare un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), chiamare sempre **PropVariantInit** per inizializzare il valore. Al termine del PROPVARIANT, chiamare sempre **PropVariantClear** per rilasciare la memoria allocata per la variabile.

### <a name="8bim-handlers"></a>Gestori 8BIM

Quando si scrive un gestore di metadati per un blocco di metadati 8BIM, è necessario usare una firma che incapsula sia la firma 8BIM che l'ID. Il lettore di metadati 8BIMIPTC nativo, ad esempio, fornisce le seguenti informazioni del registro di sistema per l'individuazione dei Reader:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

Il lettore 8BIMIPTC ha un modello registrato di 0x38, 0x42, 0x49, irreversibile 0x4D, 0x04, 0x04. I primi quattro byte (0x38, 0x42, 0x49, irreversibile 0x4D) sono la firma 8BIM e gli ultimi due byte (0x04, 0x04) sono l'ID del record IPTC.

Quindi, per scrivere un lettore di metadati 8BIM per le informazioni di risoluzione, è necessario un modello registrato di 0x38, 0x42, 0x49, irreversibile 0x4D, 0x03, 0xED. Anche in questo caso i primi quattro byte (0x38, 0x42, 0x49, irreversibile 0x4D) sono la firma 8BIM. Gli ultimi due byte (0x03, 0xED), tuttavia, sono l'ID delle informazioni di risoluzione definito dal formato PSD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Cenni preliminari sui metadati WIC](-wic-about-metadata.md)
</dt> <dt>

[Cenni preliminari sul linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Panoramica della lettura e della scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Procedura: ricodificare un'immagine JPEG con i metadati](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
