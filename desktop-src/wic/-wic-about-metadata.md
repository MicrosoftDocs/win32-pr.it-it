---
description: Questo argomento presenta il supporto dei metadati di creazione dell'immagine fornito da Windows Imaging Component (WIC).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Panoramica dei metadati WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f5031759dd73861a97aace623b35f229b75952
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472027"
---
# <a name="wic-metadata-overview"></a>Panoramica dei metadati WIC

Questo argomento presenta il supporto dei metadati di creazione dell'immagine fornito da Windows Imaging Component (WIC). Fornisce un'introduzione alla lettura e alla scrittura dei metadati dell'immagine, al linguaggio di query dei metadati e all'estendibilità del gestore di metadati.

I metadati dell'immagine sono dati incorporati all'interno di un file di immagine che forniscono informazioni aggiuntive sull'immagine, ad esempio il dispositivo usato per acquisire l'immagine o le dimensioni dell'immagine. Sebbene sia contenuto all'interno del file di immagine stesso, questi metadati non fanno parte dei dati di rendering. WIC offre interfacce che consentono di leggere e scrivere questi metadati per diversi formati di metadati comuni, tra cui Extensible Metadata Platform (XMP), EXIF (Exchangeable Image File) e Png Textual Data (tEXt).

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Introduzione](#introduction)
-   [Lettura dei metadati delle immagini](#reading-image-metadata)
-   [Scrittura di metadati dell'immagine](#writing-image-metadata)
-   [Estensibilità dei metadati](#metadata-extensibility)
-   [Formati di metadati supportati](#supported-metadata-formats)
-   [Riepilogo dei componenti dei metadati](#metadata-component-summary)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere familiarità con le interfacce del codificatore e del decodificatore WIC e con i componenti com (Component Object Model) correlati, come descritto in Panoramica del componente [di creazione](-wic-about-windows-imaging-codec.md)dell'immagine Windows . Consente inoltre di avere una conoscenza generale di alcuni dei formati di metadati di creazione dell'immagine attualmente in uso.

## <a name="introduction"></a>Introduzione

I metadati forniscono informazioni estese su un'immagine. Queste informazioni possono essere usate in diversi modi. Un'immagine può contenere metadati come una descrizione, una classificazione, tag di categoria e informazioni sul copyright. L'accesso ai metadati semplifica l'esecuzione di attività quali la gestione degli asset, la posizione dei file o la determinazione delle informazioni sul copyright. Ad esempio, il Windows Raccolta foto in Windows Vista consente di aggiungere descrizioni e tag di categoria alle immagini. Ciò consente una migliore individuabilità delle immagini e un modo pratico per classificare le immagini. Usando le API WIC e i formati di metadati comuni, le applicazioni possono scrivere o leggere facilmente questo tipo di metadati in o da immagini.

Il diagramma seguente illustra il contenuto di un file JPEG che include blocchi di metadati incorporati ed elementi di metadati.

![Immagine jpeg con metadati di classificazione](graphics/jpeg.png)

In questa immagine di esempio i metadati sono incorporati nel file di immagine all'interno di un frame di immagine. Il formato JPEG non supporta più fotogrammi immagine, quindi i metadati sono concettualmente collegati a questo singolo frame. I formati che supportano più fotogrammi, ad esempio TIFF, possono avere metadati collegati a ogni frame di immagine, come illustrato nel diagramma. Anche se attualmente non è comune e non è supportata dai codec di immagini native, alcuni formati di immagine possono supportare anche i metadati all'esterno di un frame di immagine. WIC è sufficientemente flessibile da gestire sia i metadati a livello di frame che i metadati all'esterno del singolo frame di un'immagine.

## <a name="reading-image-metadata"></a>Lettura dei metadati delle immagini

Le API WIC forniscono componenti COM che semplificano la lettura e la scrittura dei metadati delle immagini da parte delle applicazioni.

Il modo principale per leggere i metadati è usare un lettore di query dei metadati ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) per accedere a elementi di metadati specifici. Il componente lettore di query dei metadati viene implementato dal codec ed è accessibile a livello di decodificatore o tramite singoli fotogrammi immagine, che è il metodo più comune. Il codice seguente illustra come accedere a un lettore di query per un singolo frame usando il metodo **GetMetadataQueryReader** del lettore di query.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Un lettore di query fornisce metodi per ottenere informazioni su metadati specifici e un mezzo per specificare un elemento di metadati da recuperare. Il codice seguente usa un'espressione di query per richiedere un elemento di metadati specifico all'interno del blocco IFD (Nested Image File Directory) app1. Questa operazione viene eseguita usando il metodo **GetMetadataByName** del lettore di query. Il codice seguente illustra l'uso del lettore di query per ottenere il valore di classificazione MicrosoftPhoto.


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



La variabile pwzRatingQuery nell'esempio precedente è la stringa di query per accedere alla classificazione MicrosoftPhoto dell'elemento di metadati. Questa stringa viene creata usando il linguaggio di query dei metadati. Per creare questa stringa, è necessario conoscere il formato dei metadati e il linguaggio di query dei metadati per recuperare i singoli elementi di metadati. Per altre informazioni sul linguaggio di query dei metadati, vedere Panoramica [del linguaggio di query sui metadati.](-wic-codec-metadataquerylanguage.md)

In background, un lettore di query usa un lettore di metadati ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) per accedere ai metadati descritti dall'espressione di query. Oltre a usare un lettore di query, è anche possibile accedere direttamente a un lettore di metadati per leggere i metadati. È possibile ottenere un lettore di metadati dal decodificatore o dai singoli frame cercando un'interfaccia del lettore di blocchi [**(IWICMetadataBlockReader).**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)

## <a name="writing-image-metadata"></a>Scrittura di metadati dell'immagine

Il processo di scrittura dei metadati è simile al modo in cui vengono letti, ad eccezione del fatto che viene usato un writer di query di metadati ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). L'interfaccia del writer di query viene implementata dal codificatore di immagini e, come nel lettore di query, l'accesso ai metadati viene eseguito sia nel codificatore che nei singoli fotogrammi (a seconda del supporto del formato di immagine).

Il codice seguente illustra come ottenere un writer di query da un frame del codificatore e rimuovere il valore di classificazione letto in precedenza.


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



Un altro modo per scrivere metadati è tramite aggiornamenti rapidi dei metadati. La codifica rapida dei metadati è un modo per scrivere i metadati delle immagini senza dover codificare nuovamente un file di immagine. Questa operazione viene eseguita scrivendo nuove informazioni sui metadati in un'area riempita del formato dei metadati. Il codificatore di metadati veloce ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) viene ottenuto dalla factory dei componenti, in base al decodificatore di immagine. Il codificatore di metadati rapido ottiene quindi un writer di query usato per scrivere i metadati. Infine, il codificatore rapido esegue il commit della modifica.

Il codice seguente illustra come ottenere un codificatore di metadati veloce e usarlo per scrivere il valore MicrosoftRating.


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

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



Non tutti i formati di metadati supportano i metadati veloci. Per vedere quali formati supportati in modo nativo supportano la codifica rapida dei metadati, vedere la tabella nella [sezione Formati](#supported-metadata-formats) di metadati supportati più avanti in questo documento.

Dietro le quinte, un writer di query usa un writer di metadati ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) per scrivere i metadati descritti dall'espressione di query. Oltre a usare un lettore di query, è anche possibile accedere direttamente a un writer di metadati per scrivere metadati. È possibile ottenere un writer di metadati dal decodificatore o dai singoli frame usando l'esecuzione di query per un'interfaccia del writer di blocchi [**(IWICMetadataBlockWriter).**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)

## <a name="metadata-extensibility"></a>Estensibilità dei metadati

Come accennato in precedenza, WIC fornisce diversi gestori di metadati per leggere e scrivere metadati per formati di metadati comuni. Tuttavia, alcuni formati di metadati non sono supportati in modo nativo. WiC fornisce quindi API per la creazione di gestori di metadati aggiuntivi che possono estendere il supporto dei metadati ad altri formati.

Per supportare completamente altri formati di metadati, è necessario sviluppare due tipi di gestori: un lettore di metadati per leggere i metadati e un writer di metadati per scrivere i metadati. Anche se questi due gestori vengono in genere implementati a coppie per un formato specifico, questo non è un requisito. In alcuni casi potrebbe essere necessaria solo la capacità di lettura o solo la capacità di scrittura.

Per altre informazioni sull'estendibilità dei metadati tramite le API WIC, vedere Cenni [preliminari sull'estendibilità dei metadati.](-wic-codec-metadatahandlers.md)

## <a name="supported-metadata-formats"></a>Formati di metadati supportati

WIC offre il supporto per diversi formati di metadati comuni. Nella tabella seguente sono elencati i formati di metadati supportati, le relative versioni, i formati di immagine che supportano il formato dei metadati e se il formato dei metadati supporta la codifica rapida dei metadati. Per altre informazioni sulla codifica rapida dei metadati, vedere la [sezione Scrittura di](#writing-image-metadata) metadati delle immagini più indietro in questo documento.



| Formati di metadati supportati | Versione della specifica dei metadati | Supporto del formato immagine | Supporta la codifica rapida dei metadati |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| App0                       | JFIF 1.02                      | JPEG                 | No                              |
| App1                       | JFIF 1.02                      | JPEG, TIFF           | No                              |
| App13                      | Sconosciuto                        | JPEG, TIFF           | No                              |
| IFD                        | TIFF 6.0                       | JPEG, TIFF           | Sì                             |
| IRB                        | Sconosciuto                        | JPEG, TIFF           | No                              |
| Exif                       | Exif 2.2                       | JPEG, TIFF           | Sì                             |
| XMP                        | XMP 1.0 (settembre 2005)            | JPEG, TIFF           | Sì                             |
| GPS                        | Exif 2.2                       | JPEG, TIFF           | Sì                             |
| IPTC                       | IPTC 4.0                       | JPEG, TIFF           | Sì                             |
| Testo                       | PNG 1.2                        | PNG                  | No                              |



 

> [!Note]  
> IPTC supporta FME solo se le dimensioni dei blocchi aumentano, perché IPTC non supporta la spaziatura interna.

 

## <a name="metadata-component-summary"></a>Riepilogo dei componenti dei metadati

Nella tabella seguente vengono descritte le interfacce WIC che supportano i metadati e i componenti corrispondenti. Questi componenti forniscono l'accesso ai metadati di un'immagine. Per altre informazioni su questi componenti, vedere cenni preliminari sul [Windows imaging.](-wic-about-windows-imaging-codec.md) 


| Componente | Descrizione | 
|-----------|-------------|
| Decodificatore bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>) | <ul><li>Legge un flusso di immagini e produce un'origine bitmap utilizzabile. Associato a un formato di contenitore, ad esempio Tagged Image File Format (TIFF) o Joint Photographic Experts Group (JPEG).</li><li>Implementa <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>un'interfaccia IWICMetadataBlockReader</strong></a> per enumerare tutti i blocchi di metadati nel flusso di dati del decodificatore che non si trova all'interno di un frame.</li><li>Espone un lettore di query per leggere i metadati associati all'immagine che non si trova all'interno di un frame.</li></ul> | 
| Decodifica di fotogrammi bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>) | <ul><li>Accede ai singoli fotogrammi dal flusso dell'immagine mantenuto dal decodificatore.</li><li>Implementa <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>un'interfaccia IWICMetadataBlockReader</strong></a> per enumerare tutti i blocchi di metadati nel flusso di dati del frame.</li><li>Espone un lettore di query per leggere i metadati associati al frame, utilizzando espressioni di query.</li></ul> | 
| Codificatore bitmap (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>) | <ul><li>Scrive un'origine bitmap in un flusso di immagine. Associato a un formato di contenitore, ad esempio TIFF o JPEG.</li><li>Implementa <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>un'interfaccia IWICMetadataBlockWriter</strong></a> per creare un elenco di blocchi di metadati da scrivere nel flusso di dati del codificatore.</li><li>Espone un writer di query per scrivere i metadati associati all'immagine, usando espressioni di query.</li></ul> | 
| Codifica di frame di bitma (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>) | <ul><li>Crea un frame che verrà codificato nel flusso mantenuto dal codificatore.</li><li>Implementa <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>un'interfaccia IWICMetadataBlockWriter</strong></a> per creare un elenco di blocchi di metadati da scrivere nel flusso di dati del frame.</li><li>Espone un writer di query per scrivere i metadati associati al frame, utilizzando espressioni di query.</li></ul> | 




 

Nella tabella seguente vengono descritti i componenti dei metadati WIC. Questi componenti consentono di leggere e scrivere i metadati in un'immagine esposta dai componenti elencati nella tabella precedente. 


| Componente | Descrizione | 
|-----------|-------------|
| Lettore di query dei metadati (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>) | <ul><li>Accetta una stringa di query ed esplora la gerarchia dei metadati sottostante per ottenere i metadati.</li></ul> | 
| Metadata Query Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>) | <ul><li>Accetta una stringa di query e esplora la gerarchia dei metadati sottostante per ottenere, impostare e rimuovere metadati.</li></ul> | 
| Lettore di blocchi di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>) | <ul><li>Gestisce una raccolta di sola lettura di oggetti <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> all'inizio della gerarchia dei metadati e abilita l'enumerazione di tutti i blocchi di metadati.</li><li>Implementato da un decodificatore bitmap e da un frame bitmap decodificato.</li><li>Implementato dagli sviluppatori di componenti di terze parti per codec personalizzati.</li></ul> | 
| Writer di blocchi di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>) | <ul><li>Gestisce una raccolta di lettura e scrittura di <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>oggetti IWICMetadataWriter</strong></a> all'inizio della gerarchia dei metadati.</li><li>Implementato da un codificatore bitmap e da una codifica di frame bitmap.</li><li>Implementato dagli sviluppatori di componenti di terze parti per codec personalizzati.</li></ul> | 
| Lettore di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>) | <ul><li>Analizza un flusso di metadati e gestisce una raccolta di sola lettura degli elementi di metadati. Associato a un formato di metadati, ad esempio EXIF, IFD e XMP.</li><li>Funge da dizionario e restituisce un valore quando viene specificato un formato e una coppia ID.</li><li>Implementato dagli sviluppatori di componenti di terze parti per i tipi di metadati personalizzati.</li></ul> | 
| Writer di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>) | <ul><li>Analizza e serializza un flusso di metadati e gestisce una raccolta di lettura/scrittura di elementi di metadati.</li><li>Implementato dagli sviluppatori di componenti di terze parti per i tipi di metadati personalizzati.</li></ul> | 
| Fast Metadata Encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a> | <ul><li>Espone la semantica per la scrittura in una gerarchia di metadati che aggiornerà i metadati sul posto senza ri-codificare l'immagine.</li></ul> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Panoramica del linguaggio di query sui metadati](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Panoramica della lettura e della scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Panoramica dell'estendibilità dei metadati](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Procedura: Codificare nuovamente un'immagine JPEG con metadati](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



