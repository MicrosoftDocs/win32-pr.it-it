---
description: In questo argomento viene fornita una panoramica di come è possibile utilizzare le API di Windows Imaging Component (WIC) per la lettura e la scrittura di metadati incorporati nei file di immagine.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Panoramica della lettura e della scrittura dei metadati delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967695"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a>Panoramica della lettura e della scrittura dei metadati delle immagini

In questo argomento viene fornita una panoramica di come è possibile utilizzare le API di Windows Imaging Component (WIC) per la lettura e la scrittura di metadati incorporati nei file di immagine.

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Introduzione](#introduction)
-   [Lettura di Metadadata tramite un lettore di query](#reading-metadadata-using-a-query-reader)
    -   [Recupero di un lettore di query](#obtaining-a-query-reader)
    -   [Lettura dei metadati](#reading-metadata)
    -   [Metodi di lettura query aggiuntivi](#additional-query-reader-methods)
-   [Scrittura di metadati tramite un writer di query](#writing-metadata-using-a-query-writer)
    -   [Recupero di un writer di query](#obtaining-a-query-writer)
    -   [Aggiunta di metadati](#adding-metadata)
    -   [Rimozione di metadati](#removing-metadata)
    -   [Copia dei metadati per la ricodifica](#copying-metadata-for-re-encoding)
-   [Codifica rapida dei metadati](#fast-metadata-encoding)
    -   [Aggiunta di spaziatura interna ai blocchi di metadati](#adding-padding-to-metadata-blocks)
    -   [Acquisizione di un codificatore di metadati rapido](#obtaining-a-fast-metadata-encoder)
    -   [Uso del codificatore di metadati veloci](#using-the-fast-metadata-encoder)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere familiarità con il sistema di metadati WIC, come descritto in [Panoramica dei metadati di WIC](-wic-about-metadata.md). È anche necessario conoscere il linguaggio di query usato per leggere e scrivere i metadati, come descritto in [Cenni preliminari sul linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md).

## <a name="introduction"></a>Introduzione

WIC fornisce agli sviluppatori di applicazioni i componenti Component Object Model (COM) per la lettura e la scrittura dei metadati incorporati nei file di immagine. Esistono due modi per leggere e scrivere i metadati:

-   Utilizzo di una query Reader/Writer e di un'espressione di query per eseguire query sui blocchi di metadati per blocchi annidati o metadati specifici all'interno di un blocco.
-   Utilizzo di un gestore di metadati (un lettore di metadati o un writer di metadati) per accedere ai blocchi di metadati annidati o a metadati specifici all'interno dei blocchi di metadati.

Il più semplice consiste nell'usare un reader/writer di query e un'espressione di query per accedere ai metadati. Un lettore di query ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) viene utilizzato per leggere i metadati mentre per la scrittura dei metadati viene utilizzato un writer di query ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). Entrambi usano un'espressione di query per leggere o scrivere i metadati desiderati. Dietro le quinte, un lettore di query (e un writer) usa un gestore di metadati per accedere ai metadati descritti dall'espressione di query.

Il metodo più avanzato consiste nell'accedere direttamente ai gestori di metadati. Un gestore di metadati viene ottenuto dai singoli frame utilizzando un reader di blocco ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) o un writer di blocco ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)). I due tipi di gestori di metadati disponibili sono il lettore di metadati ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) e il writer dei metadati ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).

Il diagramma seguente del contenuto di un file di immagine JPEG viene usato in tutti gli esempi di questo argomento. L'immagine rappresentata dal diagramma è stata creata tramite Microsoft Paint; i metadati della classificazione sono stati aggiunti utilizzando la funzionalità raccolta foto di Windows Vista.

![illustrazione dell'immagine JPEG con i metadati di classificazione](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a>Lettura di Metadadata tramite un lettore di query

Il modo più semplice per leggere i metadati consiste nell'usare l'interfaccia di lettura query, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader). Il lettore di query consente di leggere i blocchi di metadati e gli elementi all'interno di blocchi di metadati usando un'espressione di query.

È possibile ottenere un lettore di query in tre modi: tramite un decodificatore bitmap ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), tramite i singoli frame ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) o tramite un writer di query ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).

### <a name="obtaining-a-query-reader"></a>Recupero di un lettore di query

Il codice di esempio seguente illustra come ottenere un decodificatore bitmap dalla factory di imaging e come recuperare un singolo frame bitmap. Questo codice esegue anche le operazioni di installazione necessarie per ottenere un lettore di query da un frame decodificato.


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



Il decodificatore bitmap per il file di test.jpg viene ottenuto usando il metodo **CreateDecoderFromFilename** della factory di imaging. In questo metodo, il quarto parametro è impostato sul valore WICDecodeMetadataCacheOnDemand dall'enumerazione [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) . Ciò indica al decodificatore di memorizzare nella cache i metadati quando sono necessari i metadati; ottenendo un lettore di query o il lettore di metadati sottostante. L'uso di questa opzione consente di mantenere il flusso ai metadati necessari per la codifica rapida dei metadati e consente la decodifica senza perdita di codice dell'immagine JPEG. In alternativa, è possibile usare l'altro valore di **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, che memorizza nella cache i metadati dell'immagine incorporata non appena l'immagine viene caricata.

Per ottenere il lettore di query del frame, effettuare una semplice chiamata al metodo **GetMetadataQueryReader** del frame. Il codice seguente illustra questa chiamata.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Analogamente, è possibile ottenere un lettore di query anche a livello di decodificatore. Una semplice chiamata al metodo **GetMetadataQueryReader** del decodificatore ottiene il lettore di query del decodificatore. Il lettore di query di un decodificatore, a differenza del lettore di query di un frame, legge i metadati per un'immagine che si trova all'esterno dei singoli frame. Tuttavia, questo scenario non è comune e i formati di immagini native non supportano questa funzionalità. I CODEC di immagini native forniti da WIC leggono e scrivono i metadati a livello di frame anche per i formati a singolo frame, ad esempio JPEG.

### <a name="reading-metadata"></a>Lettura dei metadati

Prima di passare alla lettura effettiva dei metadati, esaminare il diagramma seguente di un file JPEG che include blocchi di metadati incorporati e dati effettivi da recuperare. Questo diagramma fornisce callout a blocchi di metadati e elementi specifici all'interno dell'immagine fornendo l'espressione di query dei metadati a ogni blocco o elemento.

![illustrazione dell'immagine JPEG con callout di metadati](graphics/jpegwithcallouts.png)

Per eseguire una query per i blocchi di metadati incorporati o per elementi specifici in base al nome, chiamare il metodo **GetMetadataByName** . Questo metodo accetta un'espressione di query e un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in cui viene restituito l'elemento dei metadati. Il codice seguente esegue una query per un blocco di metadati annidato e converte il componente [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) fornito dal valore PROPVARIANT in un lettore di query, se trovato.


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



L'espressione di query "/app1/IFD" sta eseguendo una query per il blocco IFD annidato nel blocco App1. Il file di immagine JPEG contiene il blocco di metadati annidati IFD, in modo che [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) venga restituito con un tipo di variabile (VT) `VT_UNKNOWN` e un puntatore a un'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (punkVal). Viene quindi eseguita una query sull'interfaccia IUnknown per un lettore di query.

Nel codice seguente viene illustrata una nuova query basata sul nuovo Reader di query relativo al blocco IFD annidato.


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



L'espressione di query "/{ushort = 18249}" esegue una query sul blocco IFD per la classificazione MicrosoftPhoto incorporata nel tag 18249. Il valore [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) conterrà ora un tipo di valore `VT_UI2` e un valore di dati di 50.

Tuttavia, non è necessario ottenere un blocco annidato prima di eseguire query per valori di dati specifici. Ad esempio, anziché eseguire una query per il IFD annidato e quindi per la classificazione MicrosoftPhoto, è possibile usare invece il blocco di metadati radice e la query illustrata nel codice seguente per ottenere le stesse informazioni.


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



Oltre a eseguire query per elementi di metadati specifici in un blocco di metadati, è anche possibile enumerare tutti gli elementi di metadati in un blocco di metadati (esclusi gli elementi di metadati nei blocchi di metadati annidati). Per enumerare gli elementi di metadati nel blocco corrente, viene usato il metodo **GetEnumeration** del Visualizzatore di query. Questo metodo ottiene un'interfaccia **IEnumString** popolata con gli elementi di metadati nel blocco corrente. Il codice seguente, ad esempio, enumera la classificazione XMP e la classificazione MicrosoftPhoto per il blocco IFD annidato ottenuto in precedenza.


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



Per altre informazioni sull'identificazione dei tag appropriati per diversi formati di immagine e formati di metadati, vedere [query di metadati del formato di immagine nativo](-wic-native-image-format-metadata-queries.md).

### <a name="additional-query-reader-methods"></a>Metodi di lettura query aggiuntivi

Oltre a leggere i metadati, è anche possibile ottenere informazioni aggiuntive sull'Reader di query e ottenere i metadati tramite altri metodi. In query Reader sono disponibili due metodi che forniscono informazioni su query Reader, **GetContainerFormat** e **getLocation**.

Con il lettore di query incorporato è possibile utilizzare **GetContainerFormat** per determinare il tipo di blocco di metadati ed è possibile chiamare **getLocation** per ottenere il percorso relativo al blocco di metadati radice. Nel codice seguente viene eseguita una query sul lettore di query incorporato per la relativa posizione.


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



La chiamata a **GetContainerFormat** per il lettore di query incorporato restituisce il GUID del formato dei metadati IFD. La chiamata a **getLocation** restituisce uno spazio dei nomi "/app1/IFD"; fornisce il percorso relativo da cui verranno eseguite le successive query al nuovo Reader di query. Naturalmente, il codice precedente non è molto utile, ma illustra come usare il metodo **getLocation** per trovare i blocchi di metadati annidati.

## <a name="writing-metadata-using-a-query-writer"></a>Scrittura di metadati tramite un writer di query

> [!Note]  
> Alcuni esempi di codice forniti in questa sezione non vengono visualizzati nel contesto dei passaggi effettivi necessari per la scrittura dei metadati. Per visualizzare gli esempi di codice nel contesto di un esempio funzionante, vedere l'esercitazione Procedura: ricodificare un'immagine con metadati.

 

Il componente principale per la scrittura dei metadati è il writer di query ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). Il writer di query consente di impostare e rimuovere i blocchi di metadati e gli elementi all'interno di un blocco di metadati.

Come il lettore di query, è possibile ottenere un writer di query in tre modi: tramite un codificatore di bitmap ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), tramite i singoli frame ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) o tramite un codificatore di metadati rapido ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).

### <a name="obtaining-a-query-writer"></a>Recupero di un writer di query

Il writer di query più comune è per un singolo frame di una bitmap. Questo writer di query imposta e rimuove i blocchi di metadati e gli elementi di un frame di immagini. Per ottenere un writer di query del fotogramma immagine, chiamare il metodo **GetMetadataQueryWriter** del frame. Il codice seguente illustra la chiamata al metodo semplice per ottenere il writer di query di un frame.


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



Analogamente, è possibile ottenere un writer di query anche per il livello del codificatore. Una semplice chiamata al metodo **GetMetadataQueryWriter** del codificatore ottiene il writer di query del codificatore. Un writer di query del codificatore, a differenza del writer di query di un frame, scrive i metadati per un'immagine all'esterno del singolo frame. Tuttavia, questo scenario non è comune e i formati di immagini native non supportano questa funzionalità. I codec di immagini native forniti da WIC leggono e scrivono i metadati a livello di frame anche per i formati a singolo frame, ad esempio JPEG.

È anche possibile ottenere un writer di query direttamente dalla factory di imaging ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)). Esistono due metodi di creazione di immagini che restituiscono un writer di query: **CreateQueryWriter** e **CreateQueryWriterFromReader**.

**CreateQueryWriter** crea un writer di query per il formato di metadati e il fornitore specificati. Questo writer di query consente di scrivere metadati per un formato di metadati specifico e di aggiungerli all'immagine. Il codice seguente illustra una chiamata **CreateQueryWriter** per creare un writer di query XMP.


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



In questo esempio, il nome descrittivo `GUID_MetadataFormatXMP` viene usato come parametro *guidMetadataFormat* . Rappresenta il GUID del formato dei metadati XMP e il fornitore rappresenta il gestore creato da Microsoft. In alternativa, è possibile passare **null** come parametro *pguidVendor* con gli stessi risultati se non esiste alcun altro gestore XMP. Se insieme al gestore XMP nativo viene installato un gestore XMP personalizzato, il passaggio di un **valore null** per il fornitore comporterà la restituzione del GUID più basso.

**CreateQueryWriterFromReader** è simile al metodo **CreateQueryWriter** con la differenza che il nuovo writer di query viene prepopolato con i dati forniti dal lettore di query. Questa operazione è utile per ricodificare un'immagine mantenendo i metadati esistenti o per rimuovere i metadati indesiderati. Il codice seguente illustra una chiamata **CreateQueryWriterFromReader** .


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

Dopo aver ottenuto un writer di query, è possibile usarlo per aggiungere blocchi ed elementi di metadati. Per scrivere i metadati, utilizzare il metodo **SetMetadataByName** del writer di query. **SetMetadataByName** accetta due parametri: un'espressione di query (*wzName*) e un puntatore a un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*). L'espressione di query definisce il blocco o l'elemento da impostare mentre PROPVARIANT fornisce il valore di dati effettivo da impostare.

Nell'esempio seguente viene illustrato come aggiungere un titolo utilizzando il writer di query XMP ottenuto in precedenza tramite il metodo **CreateQueryWriter** .


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



In questo esempio, il tipo del valore (VT) viene impostato su `VT_LPWSTR` , a indicare che verrà utilizzata una stringa come valore di dati. Poiché il tipo del *valore* è una stringa, *pwszVal* viene usato per impostare il titolo da usare. **SetMetadataByName** viene quindi chiamato usando l'espressione di query "/DC: title" e il nuovo set [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). L'espressione di query utilizzata indica che è necessario impostare la proprietà title nello schema della fotocamera digitale (DC). Si noti che l'espressione non è "/XMP/DC: title"; Questo perché il writer di query è già specifico di XMP e non contiene un blocco XMP incorporato, che verrà suggerito da "/XMP/DC: title".

Fino a questo punto non sono stati effettivamente aggiunti metadati a un frame di immagine. È stato semplicemente popolato un writer di query con i dati. Per aggiungere a un frame un blocco di metadati rappresentato dal writer di query, è necessario chiamare di nuovo **SetMetadataByName** usando il writer di query come valore di [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). In questo modo i metadati del writer di query vengono copiati nel frame dell'immagine. Il codice seguente illustra come aggiungere i metadati nel writer di query XMP precedentemente ottenuto al blocco di metadati radice di un frame.


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



In questo esempio viene usato un tipo di valore (VT), `VT_UNKOWN` che indica un tipo di valore dell'interfaccia com. Il writer di query XMP (piXMPWriter) viene quindi usato come valore di [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), aggiungendovi un riferimento usando il metodo AddRef. Infine, il writer di query XMP viene impostato chiamando il metodo **SetMetadataByName** del frame e passando l'espressione di query "/", indicando il blocco radice e il PROPVARIANT appena impostato.

> [!Note]  
> Se il frame contiene già il blocco di metadati che si sta tentando di aggiungere, i metadati che si aggiungono verranno aggiunti e i metadati esistenti verranno sovrascritti.

 

### <a name="removing-metadata"></a>Rimozione di metadati

Un writer di query consente inoltre di rimuovere i metadati chiamando il metodo **RemoveMetadataByName** . **RemoveMetadataByName** accetta un'espressione di query e rimuove il blocco o l'elemento di metadati, se esistente. Il codice seguente illustra come rimuovere il titolo aggiunto in precedenza.


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



### <a name="copying-metadata-for-re-encoding"></a>Copia dei metadati per la ricodifica

> [!Note]  
> Il codice contenuto in questa sezione è valido solo se i formati di immagine di origine e di destinazione sono uguali. Non è possibile copiare tutti i metadati di un'immagine in un'unica operazione quando si esegue la codifica in un formato di immagine diverso.

 

Per mantenere i metadati durante la ricodifica di un'immagine nello stesso formato di immagine, sono disponibili metodi per la copia di tutti i metadati in un'unica operazione. Ognuna di queste operazioni segue un modello simile. ogni imposta i metadati del frame decodificato direttamente nel nuovo frame da codificare.

Il metodo preferito per la copia dei metadati consiste nell'inizializzare il writer del blocco del nuovo frame con il lettore di blocco del frame decodificato. Il codice seguente illustra questo metodo.


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



In questo esempio, il Reader di blocco e il writer del blocco vengono ottenuti rispettivamente dal fotogramma di origine e dal frame di destinazione. Il writer di blocco viene quindi inizializzato dal lettore del blocco. Viene così inizializzato il reader del blocco con i metadati precompilati del lettore di blocchi.

Un altro metodo per copiare i metadati consiste nel scrivere il blocco di metadati a cui fa riferimento il lettore di query utilizzando il writer di query del codificatore. Il codice seguente illustra questo metodo.


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



In questo caso, un lettore di query viene ottenuto dal fotogramma decodificato e quindi usato come valore della proprietà di [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) con un tipo di valore impostato su VT \_ Unknown. Viene ottenuto il writer di query per il codificatore e l'espressione di query "/" viene utilizzata per impostare i metadati nel percorso di navigazione radice. È inoltre possibile utilizzare questo metodo quando si impostano blocchi di metadati annidati, modificando l'espressione di query nella posizione desiderata.

Analogamente, è possibile creare un writer di query basato sul lettore di query del frame decodificato usando il metodo **CreateQueryWriterFromReader** della factory di imaging. Il writer di query creato in questa operazione verrà prepopolato con i metadati dall'Reader di query e potrà essere impostato nel frame. Il codice seguente illustra l'operazione di copia **CreateQueryWriterFromReader** .


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



Questo metodo utilizza un writer di query separato basato sui dati del lettore di query. Questo nuovo writer di query viene quindi impostato nel frame.

Anche in questo caso, queste operazioni per la copia dei metadati funzionano solo quando le immagini di origine e di destinazione hanno lo stesso formato. Questo è dovuto al fatto che i diversi formati di immagine archiviano i blocchi di metadati in posizioni diverse. Ad esempio, JPEG e TIFF supportano i blocchi di metadati XMP. Nelle immagini JPEG il blocco XMP si trova nel blocco di metadati radice, come illustrato nella [Panoramica dei metadati di WIC](-wic-about-metadata.md). Tuttavia, in un'immagine TIFF, il blocco XMP è annidato in un blocco IFD radice. Il diagramma seguente illustra le differenze tra un'immagine JPEG e un'immagine TIFF con gli stessi metadati di valutazione.

![confronto tra JPEG e TIFF.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a>Codifica rapida dei metadati

Non è sempre necessario codificare nuovamente un'immagine per scrivervi nuovi metadati. I metadati possono anche essere scritti usando un codificatore di metadati rapido. Un codificatore di metadati veloce può scrivere una quantità limitata di metadati in un'immagine senza ricodificare l'immagine. Questa operazione viene eseguita scrivendo i nuovi metadati all'interno della spaziatura interna vuota fornita da alcuni formati di metadati. I formati di metadati nativi che supportano la spaziatura dei metadati sono EXIF, IFD, GPS e XMP.

### <a name="adding-padding-to-metadata-blocks"></a>Aggiunta di spaziatura interna ai blocchi di metadati

Prima di poter eseguire la codifica rapida dei metadati, è necessario che nel blocco di metadati sia disponibile spazio per la scrittura di più metadati. Se lo spazio disponibile nella spaziatura interna esistente non è sufficiente per la scrittura dei nuovi metadati, la codifica rapida dei metadati avrà esito negativo. Per aggiungere la spaziatura dei metadati a un'immagine, l'immagine deve essere codificata nuovamente. È possibile aggiungere spaziatura interna nello stesso modo in cui si aggiungono altri elementi di metadati, usando un'espressione di query, se il blocco di metadati che si sta riempiendo lo supporta. Nell'esempio seguente viene illustrato come aggiungere spaziatura interna a un blocco IFD incorporato in un blocco App1.


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



Per aggiungere spaziatura interna, creare un PROPVARIANT di tipo VT \_ UI4 e un valore corrispondente al numero di byte di spaziatura interna da aggiungere. Un valore tipico è 4096 byte. Le query sui metadati per JPEG, TIFF e JPEG-XR sono disponibili in questa tabella.



| Formato metadati | Query di metadati JPEG                  | Query di metadati TIFF, JPEG-XR    |
|-----------------|--------------------------------------|---------------------------------|
| IFD             | /app1/ifd/PaddingSchema: riempimento      | /ifd/PaddingSchema: riempimento      |
| EXIF            | /app1/ifd/exif/PaddingSchema: riempimento | /ifd/exif/PaddingSchema: riempimento |
| XMP             | /xmp/PaddingSchema: riempimento           | /ifd/xmp/PaddingSchema: riempimento  |
| GPS             | /app1/ifd/gps/PaddingSchema: riempimento  | /ifd/gps/PaddingSchema: riempimento  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a>Acquisizione di un codificatore di metadati rapido

Quando si dispone di un'immagine con riempimento dei metadati, è possibile ottenere un codificatore di metadati rapido usando i metodi **CreateFastMetadataEncoderFromDecoder** e **CreateFastMetadataEncoderFromFrameDecode** di imaging Factory.

Come suggerisce il nome, **CreateFastMetadataEncoderFromDecoder** crea un codificatore di metadati rapido per i metadati a livello di decodificatore. I formati di immagine nativi forniti da WIC non supportano i metadati a livello di decodificatore, ma questo metodo viene fornito nel caso in cui tale formato di immagine venga sviluppato in futuro.

Lo scenario più comune consiste nell'ottenere un codificatore di metadati veloce da un frame di immagini usando **CreateFastMetadataEncoderFromFrameDecode**. Il codice seguente ottiene un codificatore di metadati Fast del frame decodificato e modifica il valore della classificazione nel blocco App1.


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



### <a name="using-the-fast-metadata-encoder"></a>Uso del codificatore di metadati veloci

Dal codificatore di metadati rapido, è possibile ottenere un writer di query. Questo consente di scrivere i metadati usando un'espressione di query, come illustrato in precedenza. Dopo aver impostato i metadati nel writer di query, eseguire il commit del codificatore di metadati rapido per finalizzare l'aggiornamento dei metadati. Il codice seguente illustra l'impostazione e il commit delle modifiche dei metadati


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



Se il **commit** ha esito negativo per qualsiasi motivo, è necessario codificare nuovamente l'immagine per assicurarsi che i nuovi metadati vengano aggiunti all'immagine.

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

[Panoramica dell'estendibilità dei metadati](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Procedura: ricodificare un'immagine JPEG con i metadati](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
