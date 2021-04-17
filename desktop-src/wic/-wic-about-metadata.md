---
description: In questo argomento viene illustrato il supporto dei metadati di imaging fornito da Windows Imaging Component (WIC).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Cenni preliminari sui metadati WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563732"
---
# <a name="wic-metadata-overview"></a>Cenni preliminari sui metadati WIC

In questo argomento viene illustrato il supporto dei metadati di imaging fornito da Windows Imaging Component (WIC). Viene fornita un'introduzione alla lettura e alla scrittura dei metadati delle immagini, del linguaggio di query dei metadati e dell'estensibilità del gestore di metadati.

I metadati delle immagini sono dati incorporati all'interno di un file di immagine che fornisce informazioni aggiuntive sull'immagine, ad esempio il dispositivo usato per acquisire l'immagine o le dimensioni dell'immagine. Sebbene sia contenuto all'interno del file di immagine, questi metadati non fanno parte dei dati di rendering. WIC fornisce interfacce che consentono di leggere e scrivere questi metadati per diversi formati di metadati comuni, tra cui Extensible Metadata Platform (XMP), Scambioable image file (EXIF) e dati testuali png (testo).

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Introduzione](#introduction)
-   [Lettura dei metadati delle immagini](#reading-image-metadata)
-   [Scrittura dei metadati delle immagini](#writing-image-metadata)
-   [Estensibilità dei metadati](#metadata-extensibility)
-   [Formati di metadati supportati](#supported-metadata-formats)
-   [Riepilogo componenti metadati](#metadata-component-summary)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario conoscere le interfacce del codificatore e del decodificatore WIC e i relativi componenti COM (Component Object Model), come descritto in [Panoramica dei componenti di Windows Imaging](-wic-about-windows-imaging-codec.md). Consente inoltre di avere una certa familiarità con alcuni formati di metadati di imaging attualmente in uso.

## <a name="introduction"></a>Introduzione

I metadati forniscono informazioni estese su un'immagine. Queste informazioni possono essere usate in diversi modi. Un'immagine potrebbe contenere metadati, ad esempio una descrizione, una classificazione, tag di categoria e informazioni sul copyright. L'accesso ai metadati rende più semplice eseguire attività quali la gestione delle risorse, il percorso del file o la determinazione delle informazioni sul copyright. La raccolta foto di Windows in Windows Vista, ad esempio, consente di aggiungere descrizioni e tag di categoria alle immagini. Questo consente una migliore individuabilità delle immagini e un modo pratico per suddividere in categorie le immagini. Utilizzando le API WIC e i formati di metadati comuni, le applicazioni possono scrivere o leggere facilmente questo tipo di metadati in o da immagini.

Il diagramma seguente illustra il contenuto di un file JPEG che include i blocchi di metadati incorporati e gli elementi di metadati.

![immagine JPEG con metadati di classificazione](graphics/jpeg.png)

In questa immagine di esempio, i metadati sono incorporati nel file di immagine in un frame di immagine. Il formato JPEG non supporta più frame immagine, quindi i metadati vengono associati concettualmente a questo singolo frame. I formati che supportano più frame, ad esempio TIFF, possono avere metadati collegati a ogni fotogramma immagine come illustrato nel diagramma. Sebbene non sia attualmente comune e non supportato dai codec di immagini native, alcuni formati di immagine possono supportare anche i metadati all'esterno di un frame di immagine. WIC è sufficientemente flessibile per gestire metadati a livello di frame e metadati al di fuori del singolo frame di un'immagine.

## <a name="reading-image-metadata"></a>Lettura dei metadati delle immagini

Le API WIC forniscono componenti COM che semplificano la lettura e la scrittura dei metadati delle immagini da parte delle applicazioni.

Il modo principale per leggere i metadati consiste nell'usare un lettore di query di metadati ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) per accedere a elementi di metadati specifici. Il componente lettore di query dei metadati viene implementato dal codec ed è accessibile a livello di decodificatore o con singoli fotogrammi immagine, che è il metodo più comune. Il codice seguente illustra come accedere a un lettore di query per un singolo frame usando il metodo **GetMetadataQueryReader** del lettore di query.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Un lettore di query fornisce metodi per ottenere informazioni su metadati specifici e un metodo per specificare un elemento di metadati da recuperare. Nel codice seguente viene usata un'espressione di query per richiedere un elemento di metadati specifico all'interno del blocco IFD (App1 nested image file directory). Questa operazione viene eseguita usando il metodo **GetMetadataByName** del lettore di query. Nel codice seguente viene illustrato l'utilizzo di query Reader per ottenere il valore della classificazione MicrosoftPhoto.


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



La variabile pwzRatingQuery nell'esempio precedente è la stringa di query per accedere alla classificazione MicrosoftPhoto dell'elemento dei metadati. Questa stringa viene creata utilizzando il linguaggio di query dei metadati. Per creare questa stringa, è necessario conoscere il formato dei metadati e il linguaggio di query dei metadati per recuperare singoli elementi di metadati. Per ulteriori informazioni sul linguaggio di query dei metadati, vedere [Cenni preliminari sul linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md).

Dietro le quinte, un lettore di query usa un lettore di metadati ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) per accedere ai metadati descritti dall'espressione di query. Oltre a usare un lettore di query, è anche possibile accedere direttamente a un lettore di metadati per leggere i metadati. È possibile ottenere un lettore di metadati dal decodificatore o da singoli frame eseguendo una query per un'interfaccia di lettura a blocchi ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)).

## <a name="writing-image-metadata"></a>Scrittura dei metadati delle immagini

Il processo di scrittura dei metadati è simile al modo in cui viene letto, ad eccezione del fatto che viene utilizzato un writer di query di metadati ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). L'interfaccia del writer di query è implementata dal codificatore di immagini e, come nel lettore di query, si accede ai metadati sia nel codificatore che nei singoli frame, a seconda del supporto del formato di immagine.

Nel codice seguente viene illustrato come ottenere un writer di query da un frame del codificatore e rimuovere il valore della classificazione precedentemente letto.


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



Un altro modo per scrivere i metadati consiste nell'eseguire aggiornamenti rapidi dei metadati. La codifica rapida dei metadati è un modo per scrivere i metadati delle immagini senza dover codificare nuovamente un file di immagine. Questa operazione viene eseguita scrivendo nuove informazioni sui metadati in un'area imbottita del formato dei metadati. Il codificatore di metadati rapido ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) viene ottenuto dalla factory del componente, in base al decodificatore di immagini. Il codificatore di metadati veloci ottiene quindi un writer di query usato per scrivere i metadati. Infine, il codificatore Fast conferma la modifica.

Il codice seguente illustra come ottenere un codificatore di metadati rapido e usarlo per scrivere il valore MicrosoftRating.


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



Non tutti i formati di metadati supportano metadati veloci. Per vedere quali formati supportati in modo nativo supportano la codifica dei metadati veloce, vedere la tabella nella sezione [formati di metadati supportati](#supported-metadata-formats) più avanti in questo documento.

Dietro le quinte, un writer di query utilizza un writer di metadati ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) per scrivere i metadati descritti dall'espressione di query. Oltre a usare un lettore di query, è anche possibile accedere direttamente a un writer di metadati per la scrittura dei metadati. È possibile ottenere un writer di metadati dal decodificatore o da singoli frame usando l'esecuzione di query per un'interfaccia di writer di blocco ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).

## <a name="metadata-extensibility"></a>Estensibilità dei metadati

Come indicato in precedenza, WIC fornisce diversi gestori di metadati per la lettura e la scrittura dei metadati per i formati di metadati comuni. Tuttavia, esistono alcuni formati di metadati che non sono supportati in modo nativo. WIC fornisce pertanto le API per la creazione di gestori di metadati aggiuntivi che possono estendere il supporto dei metadati ad altri formati.

Per supportare completamente altri formati di metadati, è necessario sviluppare due tipi di gestori, ovvero un lettore di metadati per leggere i metadati e un writer di metadati per la scrittura dei metadati. Sebbene questi due gestori vengono in genere implementati in coppie per un formato specifico, questo non è un requisito. Potrebbero esserci alcuni casi in cui è necessaria solo la capacità di lettura o solo la funzionalità di scrittura.

Per ulteriori informazioni sull'estendibilità dei metadati mediante le API WIC, vedere [Cenni preliminari sull'estendibilità dei metadati](-wic-codec-metadatahandlers.md).

## <a name="supported-metadata-formats"></a>Formati di metadati supportati

WIC fornisce supporto per diversi formati di metadati comuni. Nella tabella seguente sono elencati i formati di metadati supportati, le relative versioni, i formati di immagine che supportano il formato dei metadati e se il formato dei metadati supporta la codifica rapida dei metadati. Per ulteriori informazioni sulla codifica rapida dei metadati, vedere la sezione [scrittura dei metadati delle immagini](#writing-image-metadata) più indietro in questo documento.



| Formati di metadati supportati | Versione della specifica dei metadati | Supporto del formato immagine | Supporta la codifica rapida dei metadati |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| App0                       | JFIF 1,02                      | JPEG                 | No                              |
| App1                       | JFIF 1,02                      | JPEG, TIFF           | No                              |
| App13                      | Sconosciuto                        | JPEG, TIFF           | No                              |
| IFD                        | TIFF 6,0                       | JPEG, TIFF           | Sì                             |
| IRB                        | Sconosciuto                        | JPEG, TIFF           | No                              |
| Exif                       | EXIF 2,2                       | JPEG, TIFF           | Sì                             |
| XMP                        | XMP 1,0 (settembre 2005)            | JPEG, TIFF           | Sì                             |
| GPS                        | EXIF 2,2                       | JPEG, TIFF           | Sì                             |
| IPTC                       | IPTC 4,0                       | JPEG, TIFF           | Sì                             |
| Testo                       | PNG 1,2                        | PNG                  | No                              |



 

> [!Note]  
> IPTC supporta solo FME se le dimensioni dei blocchi aumentano, perché IPTC non supporta la spaziatura interna.

 

## <a name="metadata-component-summary"></a>Riepilogo componenti metadati

Nella tabella seguente vengono descritte le interfacce WIC che supportano i metadati e i relativi componenti. Questi componenti forniscono l'accesso ai metadati di un'immagine. Per ulteriori informazioni su questi componenti, vedere [Cenni preliminari sul componente Windows Imaging](-wic-about-windows-imaging-codec.md). 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Decodificatore bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</td>
<td><ul>
<li>Legge un flusso di immagini e produce un'origine bitmap utilizzabile. Associato a un formato di contenitore, ad esempio Tagged Image File Format (TIFF) o Joint Photographic Experts Group (JPEG).</li>
<li>Implementa un'interfaccia <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> per enumerare tutti i blocchi di metadati nel flusso di dati del decodificatore che non si trovano all'interno di un frame.</li>
<li>Espone un lettore di query per leggere i metadati associati all'immagine che non si trova all'interno di un frame.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bitmap frame Decode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</td>
<td><ul>
<li>Accede a singoli frame dal flusso di immagini utilizzato dal decodificatore.</li>
<li>Implementa un'interfaccia <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> per enumerare tutti i blocchi di metadati nel flusso di dati del frame.</li>
<li>Espone un lettore di query per leggere i metadati associati al frame, usando espressioni di query.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Codificatore bitmap (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</td>
<td><ul>
<li>Scrive un'origine bitmap in un flusso di immagini. Associato a un formato di contenitore, ad esempio TIFF o JPEG.</li>
<li>Implementa un'interfaccia <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> per creare un elenco di blocchi di metadati da scrivere nel flusso di dati del codificatore.</li>
<li>Espone un writer di query per scrivere i metadati associati all'immagine, usando espressioni di query.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bitma frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</td>
<td><ul>
<li>Crea un frame che verrà codificato nel flusso utilizzato dal codificatore.</li>
<li>Implementa un'interfaccia <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> per creare un elenco di blocchi di metadati da scrivere nel flusso di dati del frame.</li>
<li>Espone un writer di query per scrivere i metadati associati al frame, usando espressioni di query.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Nella tabella seguente vengono descritti i componenti dei metadati WIC. Questi componenti consentono di leggere e scrivere i metadati in un'immagine esposta dai componenti elencati nella tabella precedente. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lettore di query dei metadati (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</td>
<td><ul>
<li>Accetta una stringa di query e sposta la gerarchia dei metadati sottostante per ottenere i metadati.</li>
</ul></td>
</tr>
<tr class="even">
<td>Writer di query dei metadati (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</td>
<td><ul>
<li>Accetta una stringa di query e sposta la gerarchia dei metadati sottostante per ottenere, impostare e rimuovere i metadati.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lettore di blocchi di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</td>
<td><ul>
<li>Gestisce una raccolta di sola lettura di oggetti <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> all'inizio della gerarchia dei metadati e Abilita l'enumerazione di tutti i blocchi di metadati.</li>
<li>Implementata da un decodificatore bitmap e da un frame bitmap decodificato.</li>
<li>Implementato da sviluppatori di componenti di terze parti per codec personalizzati.</li>
</ul></td>
</tr>
<tr class="even">
<td>Writer del blocco di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</td>
<td><ul>
<li>Gestisce una raccolta di lettura e scrittura di oggetti <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> all'inizio della gerarchia dei metadati.</li>
<li>Implementata da un codificatore bitmap e da una codifica di frame bitmap.</li>
<li>Implementato da sviluppatori di componenti di terze parti per codec personalizzati.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lettore di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</td>
<td><ul>
<li>Analizza un flusso di metadati e gestisce una raccolta di sola lettura degli elementi di metadati. Associato a un formato di metadati, ad esempio EXIF, IFD e XMP.</li>
<li>Funge da dizionario, restituendo un valore quando viene fornita una coppia di formato e ID.</li>
<li>Implementato da sviluppatori di componenti di terze parti per i tipi di metadati personalizzati.</li>
</ul></td>
</tr>
<tr class="even">
<td>Writer di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</td>
<td><ul>
<li>Analizza e serializza un flusso di metadati e gestisce una raccolta di lettura/scrittura di elementi di metadati.</li>
<li>Implementato da sviluppatori di componenti di terze parti per i tipi di metadati personalizzati.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Fast Metadata encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></td>
<td><ul>
<li>Espone la semantica per la scrittura in una gerarchia di metadati che aggiornerà i metadati senza ricodificare l'immagine.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Cenni preliminari sul linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Panoramica della lettura e della scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Panoramica dell'estendibilità dei metadati](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Procedura: ricodificare un'immagine JPEG con i metadati](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



