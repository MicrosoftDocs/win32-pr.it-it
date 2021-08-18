---
description: Questo argomento offre una panoramica dell'uso delle API wic (Windows Imaging Component) per leggere e scrivere metadati incorporati nei file di immagine.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Panoramica della lettura e della scrittura dei metadati delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191ffbe919e09acb153505fd3b43b50453b67708259206bffe66a0322d485a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088143"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a>Panoramica della lettura e della scrittura dei metadati delle immagini

Questo argomento offre una panoramica dell'uso delle API wic (Windows Imaging Component) per leggere e scrivere metadati incorporati nei file di immagine.

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Introduzione](#introduction)
-   [Lettura di metadati tramite un lettore di query](#reading-metadadata-using-a-query-reader)
    -   [Recupero di un lettore di query](#obtaining-a-query-reader)
    -   [Lettura di metadati](#reading-metadata)
    -   [Metodi aggiuntivi per il lettore di query](#additional-query-reader-methods)
-   [Scrittura di metadati tramite un writer di query](#writing-metadata-using-a-query-writer)
    -   [Recupero di un writer di query](#obtaining-a-query-writer)
    -   [Aggiunta di metadati](#adding-metadata)
    -   [Rimozione di metadati](#removing-metadata)
    -   [Copia dei metadati per la ri codifiche](#copying-metadata-for-re-encoding)
-   [Codifica dei metadati veloce](#fast-metadata-encoding)
    -   [Aggiunta di spaziatura interna ai blocchi di metadati](#adding-padding-to-metadata-blocks)
    -   [Recupero di un codificatore di metadati veloce](#obtaining-a-fast-metadata-encoder)
    -   [Uso del codificatore di metadati veloce](#using-the-fast-metadata-encoder)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere familiarità con il sistema di metadati WIC, come descritto in [Panoramica dei metadati WIC.](-wic-about-metadata.md) È anche necessario avere familiarità con il linguaggio di query usato per leggere e scrivere metadati, come descritto in [Panoramica del linguaggio di query sui metadati.](-wic-codec-metadataquerylanguage.md)

## <a name="introduction"></a>Introduzione

WiC offre agli sviluppatori di applicazioni Component Object Model componenti com (com) per leggere e scrivere metadati incorporati nei file di immagine. Esistono due modi per leggere e scrivere metadati:

-   Uso di un lettore/writer di query e di un'espressione di query per eseguire query su blocchi di metadati per blocchi annidati o metadati specifici all'interno di un blocco.
-   Uso di un gestore di metadati (lettore di metadati o writer di metadati) per accedere ai blocchi di metadati annidati o a metadati specifici all'interno dei blocchi di metadati.

Il modo più semplice è usare un lettore/writer di query e un'espressione di query per accedere ai metadati. Un lettore di query ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) viene usato per leggere i metadati, mentre un writer di query ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) viene usato per scrivere metadati. Entrambi usano un'espressione di query per leggere o scrivere i metadati desiderati. In background, un lettore di query (e un writer) usa un gestore di metadati per accedere ai metadati descritti dall'espressione di query.

Il metodo più avanzato è accedere direttamente ai gestori di metadati. Un gestore di metadati viene ottenuto dai singoli fotogrammi usando un lettore di blocchi ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) o un writer di blocchi ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)). I due tipi di gestori di metadati disponibili sono il lettore di metadati ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) e il writer di metadati ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).

Il diagramma seguente del contenuto di un file di immagine JPEG viene usato in tutti gli esempi di questo argomento. L'immagine rappresentata da questo diagramma è stata creata usando Microsoft Paint; I metadati di classificazione sono stati aggiunti usando Raccolta foto funzionalità di Windows Vista.

![illustrazione dell'immagine jpeg con metadati di classificazione](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a>Lettura di metadati tramite un lettore di query

Il modo più semplice per leggere i metadati è usare l'interfaccia del lettore di [**query, IWICMetadataQueryReader.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) Il lettore di query consente di leggere blocchi di metadati ed elementi all'interno di blocchi di metadati usando un'espressione di query.

Esistono tre modi per ottenere un lettore di query: tramite un decodificatore bitmap ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), tramite i singoli fotogrammi ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) o tramite un writer di query ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).

### <a name="obtaining-a-query-reader"></a>Recupero di un lettore di query

Nell'esempio di codice seguente viene illustrato come ottenere un decodificatore bitmap dalla factory di creazione dell'immagine e recuperare un singolo fotogramma bitmap. Questo codice esegue anche le operazioni di configurazione necessarie per ottenere un lettore di query da un frame decodificato.


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



Il decodificatore bitmap per il file test.jpg viene ottenuto usando il **metodo CreateDecoderFromFilename** della factory di creazione dell'immagine. In questo metodo il quarto parametro è impostato sul valore WICDecodeMetadataCacheOnDemand [**dell'enumerazione WICDecodeOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) Indica al decodificatore di memorizzare nella cache i metadati quando sono necessari. ottenere un lettore di query o il lettore di metadati sottostante. L'uso di questa opzione consente di mantenere il flusso ai metadati necessari per la codifica rapida dei metadati e di abilitare la decodifica senza perdita di dati dell'immagine JPEG. In alternativa, è possibile usare l'altro valore **WICDecodeOptions,** WICDecodeMetadataCacheOnLoad, che memorizza nella cache i metadati dell'immagine incorporata non appena l'immagine viene caricata.

Per ottenere il lettore di query del frame, effettuare una semplice chiamata al metodo **GetMetadataQueryReader del** frame. Il codice seguente illustra questa chiamata.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Analogamente, è anche possibile ottenere un lettore di query a livello di decodificatore. Una semplice chiamata al metodo **GetMetadataQueryReader** del decodificatore ottiene il lettore di query del decodificatore. A differenza del lettore di query di un frame, il lettore di query di un decodificatore legge i metadati per un'immagine esterna ai singoli frame. Tuttavia, questo scenario non è comune e i formati di immagine nativi non supportano questa funzionalità. Codec di immagini native forniti da WIC per leggere e scrivere metadati a livello di frame anche per formati a frame singolo, ad esempio JPEG.

### <a name="reading-metadata"></a>Lettura di metadati

Prima di procedere alla lettura effettiva dei metadati, esaminare il diagramma seguente di un file JPEG che include blocchi di metadati incorporati e dati effettivi da recuperare. Questo diagramma fornisce callout a blocchi di metadati ed elementi specifici all'interno dell'immagine che forniscono l'espressione di query dei metadati a ogni blocco o elemento.

![illustrazione dell'immagine jpeg con callout dei metadati](graphics/jpegwithcallouts.png)

Per eseguire una query per trovare blocchi di metadati incorporati o elementi specifici in base al nome, chiamare il **metodo GetMetadataByName.** Questo metodo accetta un'espressione di query e [un oggetto PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in cui viene restituito l'elemento di metadati. Il codice seguente esegue una query per un blocco di metadati annidati e converte il componente [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) fornito dal valore PROPVARIANT in un lettore di query, se trovato.


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



L'espressione di query "/app1/ifd" esegue una query per il blocco IFD annidato nel blocco App1. Il file di immagine JPEG contiene il blocco di metadati annidati IFD, quindi [l'oggetto PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) viene restituito con un tipo di variabile (vt) di e un puntatore a un'interfaccia `VT_UNKNOWN` [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (valVal). Si esegue quindi una query sull'interfaccia IUnknown per un lettore di query.

Nel codice seguente viene illustrata una nuova query basata sul nuovo lettore di query relativo al blocco IFD annidato.


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



L'espressione di query "/{ushort=18249}" esegue una query sul blocco IFD per la classificazione MicrosoftPhoto incorporata nel tag 18249. Il [valore PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) conterrà ora un tipo di valore `VT_UI2` e un valore di dati pari a 50.

Tuttavia, non è necessario ottenere un blocco annidato prima di eseguire una query per valori di dati specifici. Ad esempio, anziché eseguire una query per l'IFD annidato e quindi per la classificazione MicrosoftPhoto, è invece possibile usare il blocco di metadati radice e la query illustrata nel codice seguente per ottenere le stesse informazioni.


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



Oltre a eseguire query per elementi di metadati specifici in un blocco di metadati, è anche possibile enumerare tutti gli elementi di metadati in un blocco di metadati (senza includere gli elementi di metadati nei blocchi di metadati annidati). Per enumerare gli elementi di metadati nel blocco corrente, viene usato il metodo **GetEnumeration** del lettore di query. Questo metodo ottiene **un'interfaccia IEnumString** popolata con gli elementi di metadati nel blocco corrente. Ad esempio, il codice seguente enumera la classificazione XMP e la classificazione MicrosoftPhoto per il blocco IFD annidato ottenuto in precedenza.


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



Per altre informazioni sull'identificazione dei tag appropriati per vari formati di immagine e di metadati, vedere Query sui metadati in [formato immagine nativa.](-wic-native-image-format-metadata-queries.md)

### <a name="additional-query-reader-methods"></a>Metodi aggiuntivi per il lettore di query

Oltre a leggere i metadati, è anche possibile ottenere informazioni aggiuntive sul lettore di query e ottenere metadati tramite altri mezzi. Il lettore di query fornisce due metodi che forniscono informazioni sul lettore di query, **GetContainerFormat** e **GetLocation.**

Con il lettore di query incorporato, è possibile usare **GetContainerFormat** per determinare il tipo di blocco di metadati ed è possibile chiamare **GetLocation** per ottenere il percorso relativo al blocco di metadati radice. Nel codice seguente viene eseguita una query sul lettore di query incorporato per la relativa posizione.


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



La chiamata a **GetContainerFormat per il** lettore di query incorporato restituisce il GUID del formato dei metadati IFD. La chiamata a **GetLocation** restituisce uno spazio dei nomi "/app1/ifd"; fornisce il percorso relativo da cui verranno eseguite le query successive al nuovo lettore di query. Naturalmente, il codice precedente non è molto utile, ma illustra come usare il metodo **GetLocation** per trovare blocchi di metadati annidati.

## <a name="writing-metadata-using-a-query-writer"></a>Scrittura di metadati tramite un writer di query

> [!Note]  
> Alcuni esempi di codice forniti in questa sezione non vengono visualizzati nel contesto dei passaggi effettivi necessari per scrivere i metadati. Per visualizzare gli esempi di codice nel contesto di un esempio funzionante, vedere l'esercitazione Procedura: Codificare nuovamente un'immagine con metadati.

 

Il componente principale per la scrittura di metadati è il writer di query ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). Il writer di query consente di impostare e rimuovere blocchi di metadati ed elementi all'interno di un blocco di metadati.

Analogamente al lettore di query, esistono tre modi per ottenere un writer di query: tramite un codificatore bitmap [**(IWICBitmapEncoder),**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)tramite i singoli fotogrammi [**(IWICBitmapFrameEncode)**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)o tramite un codificatore di metadati veloce [**(IWICFastMetadataEncoder).**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)

### <a name="obtaining-a-query-writer"></a>Recupero di un writer di query

Il writer di query più comune è per un singolo frame di una bitmap. Questo writer di query imposta e rimuove i blocchi di metadati ed elementi di un frame di immagine. Per ottenere il writer di query di un frame di immagine, chiamare il metodo **GetMetadataQueryWriter del** frame. Il codice seguente illustra la semplice chiamata al metodo per ottenere il writer di query di un frame.


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



Analogamente, è possibile ottenere un writer di query anche per il livello del codificatore. Una semplice chiamata al metodo **GetMetadataQueryWriter** del codificatore ottiene il writer di query del codificatore. Il writer di query di un codificatore, a differenza del writer di query di un frame, scrive i metadati per un'immagine all'esterno del singolo frame. Tuttavia, questo scenario non è comune e i formati di immagine nativi non supportano questa funzionalità. I codec di immagini native forniti da WIC leggono e scrivono metadati a livello di frame anche per i formati a frame singolo, ad esempio JPEG.

È anche possibile ottenere un writer di query direttamente dalla factory di creazione dell'immagine ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)). Esistono due metodi factory di creazione dell'immagine che restituiscono un writer di query: **CreateQueryWriter** **e CreateQueryWriterFromReader.**

**CreateQueryWriter crea** un writer di query per il formato di metadati e il fornitore specificati. Questo writer di query consente di scrivere metadati per un formato di metadati specifico e aggiungerli all'immagine. Il codice seguente illustra una **chiamata CreateQueryWriter** per creare un writer di query XMP.


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



In questo esempio il nome `GUID_MetadataFormatXMP` descrittivo viene usato come *parametro guidMetadataFormat.* Rappresenta il GUID del formato di metadati XMP e vendor rappresenta il gestore creato da Microsoft. In alternativa, è possibile passare **NULL** come *parametro pguidVendor* con gli stessi risultati se non esistono altri gestori XMP. Se viene installato un gestore XMP personalizzato insieme al gestore XMP nativo, se si passa **NULL** per il fornitore, il writer di query restituisce il GUID più basso.

**CreateQueryWriterFromReader** è simile al metodo **CreateQueryWriter,** ad eccezione del fatto che prepopola il nuovo writer di query con i dati forniti dal lettore di query. Ciò è utile per ri-codificare un'immagine mantenendo i metadati esistenti o per rimuovere i metadati indesiderati. Il codice seguente illustra una **chiamata CreateQueryWriterFromReader.**


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a>Aggiunta di metadati

Dopo aver ottenuto un writer di query, è possibile usarlo per aggiungere elementi e blocchi di metadati. Per scrivere metadati, usare il metodo **SetMetadataByName** del writer di query. **SetMetadataByName accetta** due parametri: un'espressione di query (*wzName*) e un puntatore a [un oggetto PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*). L'espressione di query definisce il blocco o l'elemento da impostare mentre PROPVARIANT fornisce il valore di dati effettivo da impostare.

L'esempio seguente illustra come aggiungere un titolo usando il writer di query XMP ottenuto in precedenza usando il **metodo CreateQueryWriter.**


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



In questo esempio il tipo di valore (vt) è impostato su , a indicare che verrà usata una stringa `VT_LPWSTR` come valore di dati. Poiché *il* tipo del valore è una stringa, *pwszVal* viene usato per impostare il titolo da usare. **SetMetadataByName viene** quindi chiamato usando l'espressione di query "/dc:title" e l'oggetto [PROPVARIANT appena impostato.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) L'espressione di query usata indica che deve essere impostata la proprietà title nello schema della fotocamera digitale (dc). Si noti che l'espressione non è "/xmp/dc:title"; ciò è dovuto al fatto che il writer di query è già specifico di XMP e non contiene un blocco XMP incorporato, come suggerito da "/xmp/dc:title".

Fino a questo punto non sono stati effettivamente aggiunti metadati a un frame di immagine. È stato semplicemente popolato un writer di query con dati. Per aggiungere a un frame un blocco di metadati rappresentato dal writer di query, chiamare di nuovo **SetMetadataByName** usando il writer di query come valore di [PROPVARIANT.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) In questo modo i metadati nel writer di query vengono copiati nel frame dell'immagine. Il codice seguente illustra come aggiungere i metadati nel writer di query XMP ottenuto in precedenza al blocco di metadati radice di un frame.


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



In questo esempio viene usato un tipo valore (vt) di `VT_UNKOWN` , che indica un tipo di valore dell'interfaccia COM. Il writer di query XMP (piXMPWriter) viene quindi usato come valore di [PROPVARIANT,](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)aggiungendo un riferimento al writer usando il metodo AddRef. Infine, il writer di query XMP viene impostato chiamando il metodo **SetMetadataByName** del frame e passando l'espressione di query "/", che indica il blocco radice, e l'oggetto PROPVARIANT appena impostato.

> [!Note]  
> Se il frame contiene già il blocco di metadati che si sta tentando di aggiungere, i metadati da aggiungere verranno aggiunti e i metadati esistenti verranno sovrascritti.

 

### <a name="removing-metadata"></a>Rimozione di metadati

Un writer di query consente anche di rimuovere i metadati chiamando il **metodo RemoveMetadataByName.** **RemoveMetadataByName accetta** un'espressione di query e rimuove il blocco di metadati o l'elemento, se esistente. Nel codice seguente viene illustrato come rimuovere il titolo aggiunto in precedenza.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



Il codice seguente illustra come rimuovere l'intero blocco di metadati XMP.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a>Copia dei metadati per la ri codifiche

> [!Note]  
> Il codice in questa sezione è valido solo quando i formati di immagine di origine e di destinazione sono uguali. Non è possibile copiare tutti i metadati di un'immagine in una singola operazione durante la codifica in un formato di immagine diverso.

 

Per mantenere i metadati durante la ri codifiche di un'immagine nello stesso formato di immagine, sono disponibili metodi per copiare tutti i metadati in una singola operazione. Ognuna di queste operazioni segue un modello simile. ognuno dei quali imposta i metadati del frame decodificato direttamente nel nuovo frame da codificare.

Il metodo preferito per copiare i metadati è inizializzare il writer di blocchi del nuovo frame con il lettore di blocchi del frame decodificato. Il codice seguente illustra questo metodo.


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



In questo esempio, il lettore di blocchi e il writer di blocco vengono ottenuti rispettivamente dal frame di origine e dal frame di destinazione. Il block writer viene quindi inizializzato dal lettore di blocchi. Inizializza il lettore di blocchi con i metadati precompilato del lettore di blocchi.

Un altro metodo per copiare i metadati è scrivere il blocco di metadati a cui fa riferimento il lettore di query usando il writer di query del codificatore. Il codice seguente illustra questo metodo.


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



In questo caso, un lettore di query viene ottenuto dal frame decodificato e quindi usato come valore della proprietà di [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) con un tipo di valore impostato su VT \_ UNKNOWN. Viene ottenuto il writer di query per il codificatore e viene usata l'espressione di query "/" per impostare i metadati nel percorso di navigazione radice. È anche possibile usare questo metodo quando si impostano blocchi di metadati annidati, modificando l'espressione di query nella posizione desiderata.

Analogamente, è possibile creare un writer di query basato sul lettore di query del frame decodificato usando il metodo **CreateQueryWriterFromReader** della factory di creazione dell'immagine. Il writer di query creato in questa operazione verrà prepopolato con i metadati del lettore di query e potrà quindi essere impostato nel frame. Il codice seguente illustra **l'operazione di copia CreateQueryWriterFromReader.**


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



Questo metodo usa un writer di query separato basato sui dati del lettore di query. Il nuovo writer di query viene quindi impostato nel frame.

Anche in questo caso, queste operazioni per copiare i metadati funzionano solo quando le immagini di origine e di destinazione hanno lo stesso formato. Ciò è dovuto al fatto che formati di immagine diversi archiviano i blocchi di metadati in posizioni diverse. Ad esempio, sia JPEG che TIFF supportano blocchi di metadati XMP. Nelle immagini JPEG il blocco XMP si trova nel blocco di metadati radice, come illustrato nella panoramica [dei metadati WIC.](-wic-about-metadata.md) Tuttavia, in un'immagine TIFF, il blocco XMP è annidato in un blocco IFD radice. Il diagramma seguente illustra le differenze tra un'immagine JPEG e un'immagine TIFF con gli stessi metadati di classificazione.

![Confronto tra jpeg e tiff.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a>Codifica dei metadati veloce

Non è sempre necessario codificare nuovamente un'immagine per scrivere nuovi metadati. I metadati possono essere scritti anche usando un codificatore di metadati veloce. Un codificatore di metadati veloce può scrivere una quantità limitata di metadati in un'immagine senza ri-codificare l'immagine. Questa operazione viene eseguita scrivendo i nuovi metadati all'interno della spaziatura interna vuota fornita da alcuni formati di metadati. I formati di metadati nativi che supportano la spaziatura interna dei metadati sono Exif, IFD, GPS e XMP.

### <a name="adding-padding-to-metadata-blocks"></a>Aggiunta di spaziatura interna ai blocchi di metadati

Prima di poter eseguire la codifica rapida dei metadati, è necessario che vi sia spazio all'interno del blocco di metadati per scrivere altri metadati. Se non c'è spazio sufficiente all'interno della spaziatura interna esistente per scrivere i nuovi metadati, la codifica rapida dei metadati avrà esito negativo. Per aggiungere la spaziatura interna dei metadati a un'immagine, è necessario codificare nuovamente l'immagine. È possibile aggiungere la spaziatura interna nello stesso modo in cui si aggiunge qualsiasi altro elemento di metadati, usando un'espressione di query, se il blocco di metadati in uso lo supporta. L'esempio seguente illustra come aggiungere spaziatura interna a un blocco IFD incorporato in un blocco App1.


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



Per aggiungere la spaziatura interna, creare una proprietà PROPVARIANT di tipo VT UI4 e un valore corrispondente al numero di byte di spaziatura \_ interna da aggiungere. Un valore tipico è 4096 byte. Le query sui metadati per JPEG, TIFF e JPEG-XR sono disponibili in questa tabella.



| Formato dei metadati | Query di metadati JPEG                  | Query sui metadati TIFF, JPEG-XR    |
|-----------------|--------------------------------------|---------------------------------|
| IFD             | /app1/ifd/PaddingSchema:Padding      | /ifd/PaddingSchema:Padding      |
| Exif            | /app1/ifd/exif/PaddingSchema:Padding | /ifd/exif/PaddingSchema:Padding |
| Xmp             | /xmp/PaddingSchema:Padding           | /ifd/xmp/PaddingSchema:Padding  |
| GPS             | /app1/ifd/gps/PaddingSchema:Padding  | /ifd/gps/PaddingSchema:Padding  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a>Recupero di un codificatore di metadati veloce

Quando si dispone di un'immagine con riempimento dei metadati, è possibile ottenere un codificatore di metadati veloce usando i metodi della factory di creazione **dell'immagine CreateFastMetadataEncoderFromDecoder** e **CreateFastMetadataEncoderFromFrameDecode.**

Come suggerisce il nome, **CreateFastMetadataEncoderFromDecoder** crea un codificatore di metadati veloce per i metadati a livello di decodificatore. I formati di immagine nativi forniti da WIC non supportano i metadati a livello di decodificatore, ma questo metodo viene fornito nel caso in cui tale formato di immagine verrà sviluppato in futuro.

Lo scenario più comune consiste nell'ottenere un codificatore di metadati veloce da un frame di immagine usando **CreateFastMetadataEncoderFromFrameDecode.** Il codice seguente ottiene il codificatore di metadati veloce di un frame decodificato e modifica il valore di classificazione nel blocco App1.


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a>Uso del codificatore di metadati veloce

Dal codificatore di metadati veloce è possibile ottenere un writer di query. In questo modo è possibile scrivere metadati usando un'espressione di query come illustrato in precedenza. Dopo aver impostato i metadati nel writer di query, eseguire il commit del codificatore di metadati veloce per finalizzare l'aggiornamento dei metadati. Il codice seguente illustra l'impostazione e il commit delle modifiche ai metadati


```
    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



Se **il commit** ha esito negativo per qualsiasi motivo, sarà necessario codificare nuovamente l'immagine per assicurarsi che i nuovi metadati vengono aggiunti all'immagine.

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

[Panoramica dell'estendibilità dei metadati](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Procedura: Codificare nuovamente un'immagine JPEG con metadati](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
