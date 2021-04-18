---
description: Questo argomento fornisce una panoramica delle query sul linguaggio di query dei metadati per la lettura e la scrittura di metadati supportati da immagini GIF, PNG, TIFF e JPEG.
ms.assetid: a6ab1708-dd82-4960-b908-f1daef7374ef
title: Query di metadati per formati di immagine nativi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be5e9c0f853e4c5e48fb5eb41f2d2ab27b4f4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315974"
---
# <a name="native-image-format-metadata-queries"></a>Query di metadati per formati di immagine nativi

Questo argomento fornisce una panoramica delle query sul [linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md) per la lettura e la scrittura di metadati supportati da immagini gif, PNG, TIFF e JPEG. Include metadati specifici per ogni formato di immagine, oltre ai metadati supportati da più formati.

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Espressione criterio metadati foto](#photo-metadata-policy-expression)
-   [Metadati specifici del formato di file](#file-format-specific-metadata)
    -   [Metadati GIF](#gif-metadata)
    -   [Metadati PNG](#png-metadata)
    -   [Metadati TIFF](#tiff-metadata)
    -   [Metadati JPEG](#jpeg-metadata)
-   [Metadati indipendenti dal formato di file](#file-format-independent-metadata)
    -   [Metadati IFD](#ifd-metadata)
    -   [Metadati EXIF](#exif-metadata)
    -   [Metadati GPS](#gps-metadata)
    -   [Metadati XMP](#xmp-metadata)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere familiarità con il sistema di metadati di Windows Imaging Component (WIC), come descritto in [Panoramica dei metadati di WIC](-wic-about-metadata.md). È anche necessario conoscere il linguaggio di query usato per leggere e scrivere i metadati, come descritto in [Cenni preliminari sul linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md).

## <a name="photo-metadata-policy-expression"></a>Espressione criterio metadati foto

Oltre a supportare il linguaggio di query dei metadati, [WIC](-wic-api.md) accetta anche nomi di proprietà canoniche dal [sistema di proprietà di Windows](../properties/windows-properties-system.md). WIC supporta un subset dello spazio dei nomi delle proprietà di Windows pertinente per i formati di immagine, come descritto in criteri per i [metadati delle foto](photo-metadata-policies.md). Una proprietà di Windows utilizzata come query di metadati WIC viene definita espressione di criteri per i metadati di foto.

Ad esempio, l'espressione di criteri per i metadati foto per il flag di orientamento EXIF è:

-   [System. Photo. Orientation](-wic-photoprop-system-photo-orientation.md)

In generale, le espressioni di criteri sono consigliate per le query di metadati native per gli elementi di metadati di immagine comuni coperti dallo spazio dei nomi delle proprietà di Windows. Il linguaggio di query dei metadati è particolarmente adatto per i casi in cui è necessario l'accesso di basso livello a elementi specifici di metadati dell'immagine o per elementi di metadati personalizzati o avanzati che non sono supportati dal sistema di proprietà di Windows. Per altre informazioni, vedere [espressioni di criteri dei metadati foto](-wic-codec-metadataquerylanguage.md).

## <a name="file-format-specific-metadata"></a>Metadati specifici del formato di file

Le sezioni seguenti contengono tabelle che elencano le query di metadati disponibili per ogni tipo di file di immagine. Ogni tabella contiene le colonne seguenti:

-   **Path** : percorso della query usato per recuperare l'elemento dei metadati.
-   **Nome** : il nome dell'elemento di metadati.
-   **Type** : tipo di elemento di metadati recuperato dal percorso della query. I metadati recuperati da [WIC](-wic-api.md) vengono restituiti nel formato PROPVARIANT, che segnala il tipo di dati utilizzando l'enumerazione VARTYPE. on.

I percorsi della query vengono utilizzati dall'API dei metadati WIC per accedere ai metadati incorporati di un'immagine. Il codice di esempio seguente illustra l'uso di un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) per eseguire una query per il blocco di metadati IFD di JPEG.


```
// Not shown: image decoding 
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pIFDReader = NULL;

// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

if (SUCCEEDED(hr))
{
    // Get the nested IFD reader.
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pIFDReader);
    }
    PropVariantClear(&value); // Clear value for new query.
}
```



### <a name="gif-metadata"></a>Metadati GIF

Il formato di immagine Graphics Interchange Format (GIF) supporta sia i metadati globali che quelli a livello di frame. Nelle due sezioni seguenti vengono forniti i percorsi di query dei metadati disponibili per i metadati globali e a livello di frame di GIF.

> [!Note]  
> Per un elenco completo dei metadati GIF insieme a informazioni più dettagliate, vedere lo [standard gif](https://www.w3.org/Graphics/GIF/spec-gif89a.txt) nel sito Web W3C.

 

### <a name="global-metadata"></a>Metadati globali

La tabella seguente fornisce i percorsi di query dei metadati disponibili che possono essere usati per accedere ai metadati GIF globali.



| Percorso                                               | Nome                       | Tipo                                |
|----------------------------------------------------|----------------------------|-------------------------------------|
| /commentext o/ \[ \* \] commentext dove \* = 0 a N | Estensione per i commenti          | VT \_ sconosciuto-lettura/scrittura query |
| /commentext/TextEntry                              |                            | \_LPSTR VT                           |
| /logscrdesc                                        | Descrizione della schermata logica | VT \_ sconosciuto-lettura/scrittura query |
| /logscrdesc/Signature                              |                            | \_Vettore VT Ui1 VT \| \_               |
| /logscrdesc/Width                                  |                            | \_UI2 VT                             |
| /logscrdesc/Height                                 |                            | \_UI2 VT                             |
| /logscrdesc/GlobalColorTableFlag                   |                            | \_bool VT                            |
| /logscrdesc/ColorResolution                        |                            | \_Ui1 VT                             |
| /logscrdesc/SortFlag                               |                            | \_bool VT                            |
| /logscrdesc/GlobalColorTableSize                   |                            | \_Ui1 VT                             |
| /logscrdesc/BackgroundColorIndex                   |                            | \_Ui1 VT                             |
| /logscrdesc/PixelAspectRatio                       |                            | \_Ui1 VT                             |
| /appext o/ \[ \* \] appext dove \* = 0 a N         | Estensione dell'applicazione      | VT \_ sconosciuto-lettura/scrittura query |
| /appext/Application                                |                            | \_Vettore VT Ui1 VT \| \_               |
| /appext/Data                                       |                            | \_Vettore VT Ui1 VT \| \_               |



 

### <a name="frame-metadata"></a>Metadati del frame

La tabella seguente fornisce i percorsi di query dei metadati disponibili che possono essere usati per accedere ai metadati GIF a livello di frame.



| Percorso                            | Nome                      | Tipo                              |
|---------------------------------|---------------------------|-----------------------------------|
| /grctlext                       | Estensione del controllo grafico | VT \_ sconosciuto-lettura/scrittura query |
| /grctlext/Disposal              |                           | \_Ui1 VT                           |
| /grctlext/UserInputFlag         |                           | \_bool VT                          |
| /grctlext/TransparencyFlag      |                           | \_bool VT                          |
| /grctlext/Delay                 |                           | \_UI2 VT                           |
| /grctlext/TransparentColorIndex |                           | \_Ui1 VT                           |
| /imgdesc                        | Descrittore di immagini          | VT \_ sconosciuto-lettura/scrittura query |
| /imgdesc/Left                   |                           | \_UI2 VT                           |
| /imgdesc/Top                    |                           | \_UI2 VT                           |
| /imgdesc/Width                  |                           | \_UI2 VT                           |
| /imgdesc/Height                 |                           | \_UI2 VT                           |
| /imgdesc/LocalColorTableFlag    |                           | \_bool VT                          |
| /imgdesc/InterlaceFlag          |                           | \_bool VT                          |
| /imgdesc/SortFlag               |                           | \_bool VT                          |
| /imgdesc/LocalColorTableSize    |                           | \_Ui1 VT                           |



 

### <a name="png-metadata"></a>Metadati PNG

Il formato di immagine Portable Network Graphics (PNG) supporta i metadati a livello di frame.

> [!Note]  
> Per un elenco completo dei metadati PNG con informazioni più dettagliate, vedere lo [standard png](https://www.w3.org/TR/PNG/) nel sito Web W3C.

 

### <a name="frame-metadata"></a>Metadati del frame

La tabella seguente fornisce i percorsi di query dei metadati disponibili che possono essere usati per accedere ai metadati PNG a livello di frame.



| Percorso                                                   | Nome             | Tipo                                      |
|--------------------------------------------------------|------------------|-------------------------------------------|
| /tEXt o/ \[ \* \] testo \* da cui = 0 a N                 | Blocco di testo       | \_Reader/Writer di query con testo sconosciuto VT    |
| /tEXt/{str = \* } Where \* = parola chiave di identificazione per il testo |                  | \_LPSTR VT                                 |
| /gAMA                                                  | Blocco Gama       | VT \_ sconosciuto-lettura/scrittura query Gama    |
| /gAMA/ImageGamma                                       |                  | \_UI4 VT                                   |
| /iTXt o/ \[ \* \] iTXt dove \* = 0 a N                 | Blocco IText      | VT \_ sconosciuto-iTXt query Reader/Writer    |
| /iTXt/Keyword                                          |                  | \_LPSTR VT                                 |
| /iTXt/CompressionFlag                                  |                  | \_Ui1 VT                                   |
| /iTXt/LanguageTag                                      |                  | LPSTR                                     |
| /iTXt/TranslatedKeyword                                |                  | LPWSTR                                    |
| /iTXt/TextEntry                                        |                  | LPWSTR                                    |
| /cHRM                                                  | Blocco HRM        | VT \_ sconosciuto-chrm query Reader/Writer    |
| /cHRM/WhitePointX                                      |                  | \_UI4 VT                                   |
| /cHRM/WhitePointY                                      |                  | \_UI4 VT                                   |
| /cHRM/RedX                                             |                  | \_UI4 VT                                   |
| /cHRM/RedY                                             |                  | \_UI4 VT                                   |
| /cHRM/GreenX                                           |                  | \_UI4 VT                                   |
| /cHRM/GreenY                                           |                  | \_UI4 VT                                   |
| /cHRM/BlueX                                            |                  | \_UI4 VT                                   |
| /cHRM/BlueY                                            |                  | \_UI4 VT                                   |
| /sRGB                                                  | Mandrino sRGB       | VT \_ sconosciuto-lettura/scrittura query sRGB    |
| /sRGB/RenderingIntent                                  |                  | \_Ui1 VT                                   |
| /Ora                                                  | Blocco di tempo       | \_Reader/Writer query a tempo sconosciuto VT    |
| /tIME/Year                                             |                  | \_UI2 VT                                   |
| /tIME/Month                                            |                  | \_Ui1 VT                                   |
| /tIME/Day                                              |                  | \_Ui1 VT                                   |
| /tIME/Hour                                             |                  | \_Ui1 VT                                   |
| /tIME/Minute                                           |                  | \_Ui1 VT                                   |
| /tIME/Second                                           |                  | \_Ui1 VT                                   |
| /bKGD                                                  | Blocco in background | VT \_ sconosciuto-bKGB query Reader/Writer    |
| /bKGD/BackgroundColor                                  |                  | VT \_ Ui1, VT \_ UI2 o VT \_ UI2 \| VT \_ vector |
| /hIST                                                  | Blocco di cron       | VT \_ sconosciuto-lettura/scrittura query cron    |
| /hIST/Frequencies                                      |                  | VT \_ vettore \| VT \_ UI2                     |
| /iCCP                                                  | Blocco iCCP       | VT \_ sconosciuto-ICCP query Reader/Writer    |
| /iCCP/ProfileName                                      |                  | \_LPSTR VT                                 |
| /iCCP/ProfileData                                      |                  | VT \_ vettore \| VT \_ UI1                     |



 

### <a name="tiff-metadata"></a>Metadati TIFF

Il formato di immagine Tagged Image File Format (TIFF) supporta i metadati a livello di frame.

> [!Note]  
> Per un elenco completo dei metadati TIFF insieme a informazioni più dettagliate, vedere [lo standard TIFF](https://www.adobe.io/content/dam/udp/en/open/standards/tiff/TIFF6.pdf).

 

### <a name="frame-metadata"></a>Metadati del frame

La tabella seguente fornisce i percorsi di query dei metadati disponibili che possono essere usati per accedere ai metadati TIFF a livello di frame.



| Percorso                                          | Nome            | Tipo                                |
|-----------------------------------------------|-----------------|-------------------------------------|
| /ifd                                          | 0 IFD           | VT \_ sconosciuto-lettura/scrittura query |
| /IFD/{ushort = \* } dove \* = 0 a 65535        | IFD voce in base all'ID | Variabile                            |
| /IFD/Thumb o/IFD/{ushort = 330}               | Anteprima IFD   | VT \_ sconosciuto-lettura/scrittura query |
| /IFD/XMP o/IFD/{ushort = 700}                 | XMP             | VT \_ sconosciuto-lettura/scrittura query |
| /IFD/EXIF o/IFD/{ushort = 34665}              | EXIF            | VT \_ sconosciuto-lettura/scrittura query |
| /IFD/GPS o/IFD/{ushort = 34853}               | GPS             | VT \_ sconosciuto-lettura/scrittura query |
| /IFD/EXIF/Interop o/IFD/EXIF/{ushort = 40965} | Interoperabilità         | VT \_ sconosciuto-lettura/scrittura query |
| /IFD/IPTC o/IFD/{ushort = 33723}              | IPTC            | VT \_ sconosciuto-lettura/scrittura query |
| /IFD/IPTC/{Str = \* } Where \* = parola chiave IPTC    | Voce IPTC      | Variabile                            |
| /ifd/irb/8bimiptc/iptc                        | IPTC            | VT \_ sconosciuto-lettura/scrittura query |
| /IFD/IRB/8bimiptc/IPTC/{Str = \* }               | Voce IPTC      | Variabile                            |



 

### <a name="jpeg-metadata"></a>Metadati JPEG

Il formato di immagine JPEG supporta i metadati a livello di frame.

> [!Note]  
> Per un elenco completo dei metadati JPEG insieme a informazioni più dettagliate, vedere lo [standard EXIF JPEG](http://www.cipa.jp/std/documents/e/DC-008-2010_E.pdf).

 

### <a name="frame-metadata"></a>Metadati del frame

La tabella seguente fornisce i percorsi di query dei metadati disponibili che possono essere usati per accedere ai metadati JPEG a livello di frame.



| Percorso                                                               | Nome                 | Tipo                                          |
|--------------------------------------------------------------------|----------------------|-----------------------------------------------|
| /app0                                                              | App0                 | VT \_ sconosciuto-APP0 query Reader/Writer        |
| /APP0/{ushort = 0}                                                   | Versione              | \_UI2 VT                                       |
| /APP0/{ushort = 1}                                                   | Unità                | \_Ui1 VT                                       |
| /APP0/{ushort = 2}                                                   | DpiX                 | \_UI2 VT                                       |
| /APP0/{ushort = 3}                                                   | DpiY                 | \_UI2 VT                                       |
| /APP0/{ushort = 4}                                                   | Xthumbnail           | \_Ui1 VT                                       |
| /APP0/{ushort = 5}                                                   | Ythumbnail           | \_Ui1 VT                                       |
| /APP0/{ushort = 6}                                                   | ThumbnailData        | \_BLOB VT                                      |
| /App1                                                              | App1                 | VT \_ sconosciuto-App1 query Reader/Writer        |
| /App1/IFD o/App1/{ushort = 0}                                     | 0 IFD                | VT \_ sconosciuto-IFD query Reader/Writer         |
| /App1/IFD/EXIF o/App1/IFD/{ushort = 34665}                         | IFD EXIF             | VT \_ sconosciuto – visualizzatore query EXIF/writer        |
| /App1/Thumb o/App1/{ushort = 1}                                   | Anteprima IFD        | VT \_ sconosciuto-SubIFD query Reader/Writer      |
| /app13                                                             | App13                | VT \_ sconosciuto-App13 query Reader/Writer       |
| /App13/IRB o/App13/{ushort = 0}                                    | IRB                  | VT \_ sconosciuto-lettore query IRB/writer         |
| /App13/IRB/{ULONGLONG = \* } Where \* = ID IRB (vedere la specifica IRB) | Voce IRB            | VT \_ sconosciuto-lettura/scrittura query sconosciuta     |
| /App13/IRB/{ULONGLONG = \* }/{}                                       | Contenuto voce IRB   | \_BLOB VT                                      |
| /App13/IRB/8bimiptc o/App13/IRB/{ULONGLONG = 61857348781060}       | 8BIMIPTC             | VT \_ sconosciuto-8BIMIPTC query Reader/Writer    |
| /app13/irb/8bimiptc/iptc                                           | IPTC                 | VT \_ sconosciuto-lettura/scrittura query IPTC        |
| /App13/IRB/8bimiptc/IPTC/{Str = \* }                                  | Voce IPTC           | Variabile                                      |
| /app13/irb/8bimResInfo o/App13/IRB/{ULONGLONG = 61857348781037}    | Informazioni sulla risoluzione 8BIM | VT \_ sconosciuto-lettura/scrittura query             |
| /app13/irb/8bimResInfo/PString                                     |                      | \_LPSTR VT                                     |
| /app13/irb/8bimResInfo/HResolution                                 |                      | \_UI4 VT                                       |
| /app13/irb/8bimResInfo/VResolution                                 |                      | \_UI4 VT                                       |
| /app13/irb/8bimResInfo/WidthUnit                                   |                      | \_UI2 VT                                       |
| /app13/irb/8bimResInfo/HeightUnit                                  |                      | \_UI2 VT                                       |
| /app13/irb/8bimResInfo/HResolutionUnit                             |                      | \_UI2 VT                                       |
| /app13/irb/8bimResInfo/VResolutionUnit                             |                      | \_UI2 VT                                       |
| /com                                                               | Commento JPEG         | VT \_ sconosciuto-lettura/scrittura query di commento     |
| /com/TextEntry                                                     |                      | LPSTR                                         |
| /luminance                                                         | Luminance            | \_Lettura/scrittura di query con luminosità sconosciuta del VT   |
| /luminance/TableEntry                                              |                      | \_Vettore VT Ui1 VT \| \_                         |
| /chrominance                                                       | Chrominance          | VT \_ sconosciuto-cromatura query Reader/Writer |
| /chrominance/TableEntry                                            |                      | \_Vettore VT Ui1 VT \| \_                         |
| /xmp                                                               | XMP                  | VT \_ sconosciuto-lettura/scrittura query XMP         |



 

## <a name="file-format-independent-metadata"></a>Metadati indipendenti dal formato di file

Le sezioni seguenti contengono informazioni sui formati di metadati supportati da più formati di immagine. Ogni tabella contiene le colonne seguenti:

-   **Percorso relativo** : percorso della query usato per recuperare l'elemento dei metadati, relativo al blocco di metadati.
-   **Nome** : il nome dell'elemento di metadati.
-   **Type** : tipo di elemento di metadati recuperato dal percorso della query. I metadati recuperati da [WIC](-wic-api.md) vengono restituiti nel formato PROPVARIANT, che segnala il tipo di dati utilizzando l'enumerazione VARTYPE.

> [!Note]  
> Le tabelle in questa sezione forniscono solo il percorso relativo per accedere a un elemento di metadati all'interno di un particolare formato di metadati. Per ottenere la query di metadati completo, aggiungere questo percorso relativo alla query del blocco di metadati per il formato di metadati specifico.

 

Ad esempio, per accedere al flag di [orientamento](-wic-photoprop-system-photo-orientation.md) in un file JPEG, usare l'espressione seguente:

-   /App1/IFD/{ushort = 274}

In un file TIFF usare l'espressione seguente:

-   /IFD/{ushort = 274}

In questo esempio, si noti che diversi formati di immagine possono archiviare un blocco di metadati specifico in modo diverso, quindi la query di metadati completa per accedere a un elemento di metadati specifico può essere specifica del formato di immagine. Vedere la tabella di ogni formato per trovare la query di metadati appropriata per accedere a un blocco di metadati specifico.

### <a name="ifd-metadata"></a>Metadati IFD

Una directory di file IFD o image è una struttura di dati definita nello standard TIFF che può contenere metadati di immagine. Identifica ogni elemento di metadati usando un tag di tipo UShort. JPEG, TIFF e JPEG-XR supportano i metadati IFD. I formati di terze parti, ad esempio i formati RAW della fotocamera, possono supportare anche i metadati IFD.

La tabella seguente fornisce i percorsi di query dei metadati relativi per accedere ad alcuni elementi di metadati IFD usati comunemente. La struttura dei dati IFD consente l'estendibilità di terze parti e questa tabella non è un elenco esaustivo. Per ulteriori informazioni, vedere lo standard TIFF.

> [!Note]  
> Anche se JPEG e altri formati supportano la struttura dei dati IFD, non possono usare tutti gli elementi di metadati definiti. Per ulteriori informazioni, fare riferimento allo standard di ogni formato.

 

> [!Note]  
> Per determinati elementi di metadati della tabella è necessario disporre di un'interpretazione o di informazioni aggiuntive da usare in modo corretto, fare riferimento allo standard TIFF. Ad esempio, l'elemento dei metadati [PhotometricInterpretation](-wic-photoprop-system-photo-photometricinterpretation.md) restituisce un PROPVARIANT di tipo VT \_ UI2. Tuttavia, in base allo standard TIFF, viene interpretato come un'enumerazione. Per ulteriori informazioni, vedere lo standard TIFF.

 



| Percorso relativo   | Nome                      | Tipo                                           |
|-----------------|---------------------------|------------------------------------------------|
| /{ushort = 256}   | ImageWidth                | VT \_ UI2 o VT \_ UI4                             |
| /{ushort = 257}   | ImageLength               | VT \_ UI2 o VT \_ UI4                             |
| /{ushort = 258}   | BitsPerSample             | \_UI2 VT                                        |
| /{ushort = 259}   | Compressione               | \_UI2 VT                                        |
| /{ushort = 262}   | PhotometricInterpretation | \_UI2 VT                                        |
| /{ushort = 274}   | Orientamento               | \_UI2 VT                                        |
| /{ushort = 277}   | SamplesPerPixel           | \_UI2 VT                                        |
| /{ushort = 284}   | PlanarConfiguration       | \_UI2 VT                                        |
| /{ushort = 530}   | YCbCrSubSampling          | VT \_ vettore \| VT \_ UI2                          |
| /{ushort = 531}   | YCbCrPositioning          | \_UI2 VT                                        |
| /{ushort = 282}   | XResolution               | \_UI8 VT                                        |
| /{ushort = 283}   | YResolution               | \_UI8 VT                                        |
| /{ushort = 296}   | ResolutionUnit            | \_UI2 VT                                        |
| /{ushort = 306}   | Datetime                  | \_LPSTR VT                                      |
| /{ushort = 270}   | ImageDescription          | \_LPSTR VT                                      |
| /{ushort = 271}   | Casa automobilistica                      | \_LPSTR VT                                      |
| /{ushort = 272}   | Modello                     | \_LPSTR VT                                      |
| /{ushort = 305}   | Software                  | \_LPSTR VT                                      |
| /{ushort = 315}   | Artista                    | \_LPSTR VT                                      |
| /{ushort = 33432} | Copyright                 | \_LPSTR VT                                      |
| /{ushort = 338}   | Esempi di campionamento              | \_UI2 VT                                        |
| /{ushort = 254}   | NewSubfileType            | \_UI4 VT                                        |
| /{ushort = 278}   | RowsPerStrip              | VT \_ UI2 o VT \_ UI4                             |
| /{ushort = 279}   | StripByteCounts           | VT \_ vector \| VT \_ UI2 o VT \_ vector \| VT \_ UI4 |
| /{ushort = 273}   | StripOffsets              | VT \_ vector \| VT \_ UI2 o VT \_ vector \| VT \_ UI4 |



 

### <a name="exif-metadata"></a>Metadati EXIF

I metadati EXIF sono definiti come parte della specifica EXIF JPEG. I metadati EXIF sono basati sulla struttura dei dati IFD, come definito nello standard TIFF, e forniscono attributi aggiuntivi, ad esempio informazioni sui dispositivi e sugli attributi fotografici usati per creare l'immagine. Identifica ogni elemento di metadati usando un tag di tipo UShort. JPEG, TIFF e JPEG-XR supportano i metadati EXIF. I formati di terze parti, ad esempio formati RAW della fotocamera, possono anche supportare i metadati EXIF.

La tabella seguente fornisce i percorsi di query dei metadati relativi per accedere ad alcuni elementi di metadati EXIF usati comunemente. La struttura dei dati EXIF consente l'estendibilità di terze parti e questa tabella non è un elenco esaustivo. Per ulteriori informazioni, fare riferimento allo standard EXIF.

> [!Note]  
> Molti elementi di metadati EXIF sono definiti nello standard EXIF come tipo "RATIONAL" o "SRATIONAL". Un "RAZIONALe" è costituito da un numeratore e da un denominatore, entrambi a 32 bit unsigned integer. Il numeratore è contenuto nei bit 32 alti e il denominatore nei 32 bit inferiori. In [WIC](-wic-api.md)vengono restituiti come PROPVARIANT rispettivamente con un tipo di VT \_ UI8 o VT \_ i8. il valore effettivo viene archiviato rispettivamente come ULARGE \_ Integer o \_ Integer grande. Per accedere al numeratore e al denominatore, leggere i membri HighPart e LowPart dell' \_ intero ULARGE o del \_ valore Integer grande.

 

> [!Note]  
> Alcuni elementi di metadati nella tabella seguente richiedono un'interpretazione o informazioni aggiuntive da usare correttamente. Ad esempio, l'elemento dei metadati dello [spazio dei colore](-wic-photoprop-system-image-colorspace.md) restituisce un PROPVARIANT di tipo VT \_ UI2. Tuttavia, in base allo standard EXIF, viene interpretato come un'enumerazione. Per ulteriori informazioni, vedere lo standard EXIF.

 



| Percorso relativo   | Nome                      | Tipo                  |
|-----------------|---------------------------|-----------------------|
| /{ushort = 36864} | ExifVersion               | \_BLOB VT              |
| /{ushort = 40960} | FlashpixVersion           | \_BLOB VT              |
| /{ushort = 40961} | ColorSpace                | \_UI2 VT               |
| /{ushort = 40962} | PixelXDimension           | VT \_ UI2 o VT \_ UI4    |
| /{ushort = 40963} | PixelYDimension           | VT \_ UI2 o VT \_ UI4    |
| /{ushort = 37500} | MakerNote                 | \_BLOB VT              |
| /{ushort = 37510} | UserComment               | \_LPWSTR VT            |
| /{ushort = 36867} | DateTimeOriginal          | \_LPSTR VT             |
| /{ushort = 36868} | DateTimeDigitized         | \_LPSTR VT             |
| /{ushort = 42016} | ImageUniqueID             | \_LPSTR VT             |
| /{ushort = 42032} | CameraOwnerName           | \_LPSTR VT             |
| /{ushort = 42033} | BodySerialNumber          | \_LPSTR VT             |
| /{ushort = 42034} | LensSpecification         | VT \_ vettore \| VT \_ UI8 |
| /{ushort = 42035} | LensMake                  | \_LPSTR VT             |
| /{ushort = 42036} | LensModel                 | \_LPSTR VT             |
| /{ushort = 42037} | LensSerialNumber          | \_LPSTR VT             |
| /{ushort = 33434} | ExposureTime              | \_UI8 VT               |
| /{ushort = 33437} | FNumber                   | \_UI8 VT               |
| /{ushort = 34850} | ExposureProgram           | \_UI2 VT               |
| /{ushort = 34852} | SpectralSensitivity       | \_LPSTR VT             |
| /{ushort = 34855} | PhotographicSensitivity   | VT \_ vettore \| VT \_ UI2 |
| /{ushort = 34856} | OECF                      | \_BLOB VT              |
| /{ushort = 34864} | SensitivityType           | \_UI2 VT               |
| /{ushort = 34865} | StandardOutputSensitivity | \_UI4 VT               |
| /{ushort = 34866} | RecommendedExposureIndex  | \_UI4 VT               |
| /{ushort = 34867} | ISOSpeed                  | \_UI4 VT               |
| /{ushort = 34868} | ISOSpeedLatitudeyyy       | \_UI4 VT               |
| /{ushort = 34869} | ISOSpeedLatitudezzz       | \_UI4 VT               |
| /{ushort = 37377} | ShutterSpeedValue         | \_I8 VT                |
| /{ushort = 37378} | ApertureValue             | \_UI8 VT               |
| /{ushort = 37379} | BrightnessValue           | \_I8 VT                |
| /{ushort = 37380} | ExposureBiasValue         | \_I8 VT                |
| /{ushort = 37381} | MaxApertureValue          | \_UI8 VT               |
| /{ushort = 37382} | SubjectDistance           | \_UI8 VT               |
| /{ushort = 37383} | MeteringMode              | \_UI2 VT               |
| /{ushort = 37384} | LightSource               | \_UI2 VT               |
| /{ushort = 37385} | Flash                     | \_UI2 VT               |
| /{ushort = 37386} | FocalLength               | \_UI8 VT               |
| /{ushort = 37396} | SubjectArea               | VT \_ vettore \| VT \_ UI2 |
| /{ushort = 41483} | FlashEnergy               | \_UI8 VT               |
| /{ushort = 41484} | SpatialFrequencyResponse  | \_BLOB VT              |
| /{ushort = 41486} | FocalPlaneXResolution     | \_UI8 VT               |
| /{ushort = 41487} | FocalPlaneYResolution     | \_UI8 VT               |
| /{ushort = 41488} | FocalPlaneResolutionUnit  | \_UI2 VT               |
| /{ushort = 41492} | SubjectLocation           | VT \_ vettore \| VT \_ UI2 |
| /{ushort = 41493} | ExposureIndex             | \_UI8 VT               |
| /{ushort = 41495} | SensingMethod             | \_UI2 VT               |
| /{ushort = 41728} | FileSource                | \_BLOB VT              |
| /{ushort = 41729} | SceneType                 | \_BLOB VT              |
| /{ushort = 41730} | CFAPattern                | \_BLOB VT              |
| /{ushort = 41985} | Personalizzato            | \_UI2 VT               |
| /{ushort = 41986} | ExposureMode              | \_UI2 VT               |
| /{ushort = 41987} | WhiteBalance              | \_UI2 VT               |
| /{ushort = 41988} | DigitalZoomRatio          | \_UI8 VT               |
| /{ushort = 41989} | FocalLengthIn35mmFilm     | \_UI2 VT               |
| /{ushort = 41990} | SceneCaptureType          | \_UI2 VT               |
| /{ushort = 41991} | GainControl               | \_UI8 VT               |
| /{ushort = 41992} | Si confronti                  | \_UI2 VT               |
| /{ushort = 41993} | Saturazione                | \_UI2 VT               |
| /{ushort = 41994} | Nitidezza                 | \_UI2 VT               |
| /{ushort = 41995} | DeviceSettingDescription  | \_BLOB VT              |
| /{ushort = 41996} | SubjectDistanceRange      | \_UI2 VT               |



 

### <a name="gps-metadata"></a>Metadati GPS

I metadati GPS contengono informazioni sulla georilevazione e sono definiti come parte della specifica EXIF JPEG. Identifica ogni elemento di metadati usando un tag di tipo UShort. JPEG, TIFF e JPEG-XR supportano i metadati GPS; i formati di terze parti, ad esempio formati RAW della fotocamera, possono supportare anche i metadati GPS.

La tabella seguente fornisce i percorsi di query dei metadati relativi per accedere ad alcuni elementi di metadati GPS usati comunemente. Questa tabella non è un elenco esaustivo. Per ulteriori informazioni, fare riferimento allo standard EXIF.

> [!Note]  
> Molti elementi di metadati GPS sono definiti nello standard EXIF come tipo "RATIONAL". Un "RAZIONALe" è costituito da un numeratore e da un denominatore, entrambi a 32 bit unsigned integer. Il numeratore è contenuto nei bit 32 alti e il denominatore nei 32 bit inferiori. In [WIC](-wic-api.md)questi vengono restituiti come PROPVARIANT con un tipo di UI8 VT \_ . Il valore effettivo viene archiviato come ULARGE \_ Integer. Per accedere al numeratore e al denominatore, leggere i membri HighPart e LowPart del \_ valore integer ULARGE.

 

> [!Note]  
> Per determinati elementi di metadati della tabella è necessario disporre di un'interpretazione o informazioni aggiuntive da utilizzare correttamente. Ad esempio, l'elemento dei metadati GPSLatitudeRef restituisce un PROPVARIANT di tipo VT \_ LPSTR. Secondo lo standard EXIF, questa stringa è "N" o "S", che rappresenta la latitudine nord o sud. Per ulteriori informazioni, vedere lo standard EXIF.

 



| Percorso relativo | Nome            | Tipo                                          |
|---------------|-----------------|-----------------------------------------------|
| {ushort = 0}    | GPSVersionID    | VT \_ vettore \| VT \_ UI1                         |
| {ushort = 1}    | GPSLatitudeRef  | \_LPSTR VT                                     |
| {ushort = 2}    | GPSLatitude     | VT \_ vettore \| VT \_ UI8                         |
| {ushort = 3}    | GPSLongitudeRef | \_LPSTR VT                                     |
| {ushort = 4}    | GPSLongitude    | {ushort = 4} \_ \| UI8 VT vettore GPSLongitude \_ VT |
| {ushort = 5}    | GPSAltitudeRef  | \_Ui1 VT                                       |
| {ushort = 6}    | GPSAltitude     | \_UI8 VT                                       |
| {ushort = 7}    | GPSTimeStamp    | VT \_ vettore \| VT \_ UI8                         |
| {ushort = 8}    | GPSSatellites   | \_LPSTR VT                                     |
| {ushort = 9}    | GPSStatus       | \_LPSTR VT                                     |
| {ushort = 10}   | GPSMeasureMode  | \_LPSTR VT                                     |
| {ushort = 11}   | GPSDOP          | \_UI8 VT                                       |
| {ushort = 12}   | GPSSpeedRef     | \_LPSTR VT                                     |
| {ushort = 13}   | GPSSpeed        | \_UI8 VT                                       |
| {ushort = 14}   | GPSTrackRef     | \_LPSTR VT                                     |
| {ushort = 15}   | GPSTrack        | \_UI8 VT                                       |



 

### <a name="xmp-metadata"></a>Metadati XMP

XMP è uno standard di metadati estendibile basato su XML. Gli elementi di metadati possono essere gerarchici e contenere strutture di dati complesse. JPEG, TIFF e JPEG-XR supportano i metadati XMP. I formati di terze parti, come alcuni formati RAW della fotocamera, possono anche supportare i metadati XMP.

Lo standard XMP può essere ottenuto da: <https://www.adobe.com/devnet/xmp.html> .

XMP e consente alle entità di terze parti di pubblicare i propri schemi, o spazi dei nomi, che consentono di definire nuovi elementi di metadati senza dover modificare lo standard XMP. Uno schema XMP viene identificato in modo univoco da un URL, ma [WIC](-wic-api.md) fornisce un set di identificatori descrittivi per gli schemi noti.

Gli elementi dei metadati XMP sono identificati da un nome di stringa e un identificatore dello schema. Come procedura consigliata, ogni query di metadati XMP deve specificare lo schema e il nome. Se manca l'identificatore dello schema, il formato JPEG tenterà di trovare una corrispondenza tra il nome dei metadati in tutti gli spazi dei nomi presenti nel pacchetto di metadati XMP.

Per ottenere, ad esempio, la proprietà rating definita dallo schema XMP in un'immagine JPEG, utilizzare la query seguente:

-   /XMP/{WSTR =https://ns.adobe.com/xap/1.0/}:Rating

La prima parte, "/XMP", recupera il reader/writer dei metadati XMP per l'immagine. " https://ns.adobe.com/xap/1.0/ " è l'URL dello schema XMP, come definito nello standard XMP. L'URL è racchiuso in un'espressione di dati per consentire l'utilizzo di caratteri quali una barra (/). Infine, "rating" è il nome dell'elemento di metadati effettivo definito dallo schema XMP ed è separato dall'identificatore dello schema da un segno di due punti (:).

In questo esempio, WIC fornisce un identificatore descrittivo per lo schema XMP che può essere utilizzato al posto dell'URL completo. Quindi, la query precedente può essere riscritta come segue:

-   /XMP/XMP: valutazione

[WIC](-wic-api.md) fornisce prefissi di schema intuitivi per i seguenti schemi di uso comune:



| Prefisso dello schema  | URL dello schema                                        | Collegamento a standard                                         |
|----------------|---------------------------------------------------|----------------------------------------------------------|
| RDF            | https://www.w3.org/1999/02/22-rdf-syntax-ns\#      | <https://www.w3.org/TR/REC-rdf-syntax/>                   |
| dc             | https://purl.org/dc/elements/1.1/                  | <https://www.adobe.com/devnet/xmp.html>                   |
| XMP            | https://ns.adobe.com/xap/1.0/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpidq         | https://ns.adobe.com/xmp/Identifier/qual/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpRights      | https://ns.adobe.com/xap/1.0/rights/               | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpMM          | https://ns.adobe.com/xap/1.0/mm/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpBJ          | https://ns.adobe.com/xap/1.0/bj/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpTPg         | https://ns.adobe.com/xap/1.0/t/pg/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| pdf            | https://ns.adobe.com/pdf/1.3/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| Photoshop      | https://ns.adobe.com/photoshop/1.0/                | <https://www.adobe.com/devnet/xmp.html>                   |
| tiff           | https://ns.adobe.com/tiff/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| EXIF           | https://ns.adobe.com/exif/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| stDim          | https://ns.adobe.com/xap/1.0/sType/Dimensions\#    | <https://www.adobe.com/devnet/xmp.html>                   |
| xapGImg        | https://ns.adobe.com/xap/1.0/g/img/                | <https://www.adobe.com/devnet/xmp.html>                   |
| stEvt          | https://ns.adobe.com/xap/1.0/sType/ResourceEvent\# | <https://www.adobe.com/devnet/xmp.html>                   |
| stRef          | https://ns.adobe.com/xap/1.0/sType/ResourceRef\#   | <https://www.adobe.com/devnet/xmp.html>                   |
| stVer          | https://ns.adobe.com/xap/1.0/sType/Version\#       | <https://www.adobe.com/devnet/xmp.html>                   |
| stJob          | https://ns.adobe.com/xap/1.0/sType/Job\#           | <https://www.adobe.com/devnet/xmp.html>                   |
| aux            | https://ns.adobe.com/exif/1.0/aux/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| CRS            | https://ns.adobe.com/camera-raw-settings/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpDM          | https://ns.adobe.com/xmp/1.0/DynamicMedia/         | <https://www.adobe.com/devnet/xmp.html>                   |
| Iptc4xmpCore   | https://iptc.org/std/Iptc4xmpCore/1.0/xmlns/       | <https://www.iptc.org/cms/site/index.html?channel=CH0099> |
| MicrosoftPhoto | https://ns.microsoft.com/photo/1.0/                | [Cenni preliminari sull'assegnazione di tag agli utenti](-wic-people-tagging.md)       |
| MP             | https://ns.microsoft.com/photo/1.2/                | [Cenni preliminari sull'assegnazione di tag agli utenti](-wic-people-tagging.md)       |
| MPRI           | https://ns.microsoft.com/photo/1.2/t/RegionInfo\#  | [Cenni preliminari sull'assegnazione di tag agli utenti](-wic-people-tagging.md)       |
| MPReg          | https://ns.microsoft.com/photo/1.2/t/Region\#      | [Cenni preliminari sull'assegnazione di tag agli utenti](-wic-people-tagging.md)       |



 

Se non esiste un prefisso di schema descrittivo per uno schema particolare, ad esempio se un'immagine contiene metadati XMP utilizzando uno schema di terze parti personalizzato, la query dei metadati utilizzerà l'URL completo dello schema.

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

 

 
