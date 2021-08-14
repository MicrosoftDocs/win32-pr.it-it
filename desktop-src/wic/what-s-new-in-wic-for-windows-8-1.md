---
description: Windows Il componente di creazione dell'immagine (WIC) è stato aggiornato con le nuove versioni di Windows. Questo argomento offre una rapida introduzione a queste nuove funzionalità.
ms.assetid: 710B71CE-6FCC-46DA-A65C-6E4FC6A04275
title: Novità in WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420d501dd495081764a7fba89f73d21077c04b05d92e7c2b47c3c2c2d51d7d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204016"
---
# <a name="whats-new-in-wic"></a>Novità in WIC

Windows Il componente di creazione dell'immagine (WIC) è stato aggiornato con le nuove versioni di Windows. Questo argomento offre una rapida introduzione a queste nuove funzionalità.

## <a name="whats-new-for-windows-10-version-1507"></a>Novità di Windows 10 versione 1507

### <a name="access-to-low-level-jpeg-data-for-wic-decoding-and-encoding"></a>Accesso ai dati JPEG di basso livello per la decodifica e la codifica WIC

A partire Windows 10 versione 1507, WIC fornisce l'accesso a strutture di dati JPEG di basso livello, tra cui le tabelle di quantizzazione e Huffman. Per altre informazioni, vedere i seguenti argomenti:

-   [**Interfaccia IWICJpegFrameDecode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframedecode)
-   [**Interfaccia IWICJpegFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframeencode)

### <a name="jpeg-indexing"></a>Indicizzazione JPEG

L'indicizzazione JPEG è una tecnica che migliora significativamente le prestazioni dell'accesso casuale a piccole sottoaree di un'immagine JPEG di grandi dimensioni, a costo di un utilizzo aggiuntivo della memoria. L'indicizzazione JPEG può essere sfruttata da qualsiasi chiamante di WIC.

[**L'interfaccia ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) è progettata per sfruttare l'indicizzazione JPEG se è attivata. Ad esempio, l'API ID2D1ImageSource richiederà solo le sezioni necessarie dell'immagine in uno scenario come panoramica e zoom per un'immagine con risoluzione di grandi dimensioni. Per altre informazioni, vedere i seguenti argomenti:

-   [**Metodo IWICJpegFrameDecode::SetIndexing**](/windows/win32/api/Wincodec/nf-wincodec-iwicjpegframedecode-setindexing)
-   [**Interfaccia ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)

## <a name="whats-new-for-windows-81"></a>Novità di Windows 8.1

### <a name="support-for-jpeg-ycbcr-images"></a>Supporto per immagini YCbCr JPEG

A partire Windows 8.1, WIC fornisce il supporto per la decodifica, la trasformazione e la codifica dei dati di immagine JPEG Y'CbCr nel formato nativo. Ciò consente alle app di ridurre significativamente il tempo di elaborazione e l'utilizzo della memoria per determinate operazioni di creazione di immagini quando si lavora con JPEG con codifica Y'CbCr. Per altre informazioni, vedere i seguenti argomenti:

-   [Effetto Direct2D](-wic-sample-d2d-viewer.md)[YCbCr](../direct2d/ycbcr-effect.md)
-   [**Interfaccia IWICPlanarBitmapSourceTransform**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
-   [**Interfaccia IWICPlanarBitmapFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode)

### <a name="support-for-block-compressed-formats-dds-files"></a>Supporto per formati compressi a blocchi (file DDS)

A partire da Windows 8.1, WIC aggiunge un nuovo codec che supporta immagini DDS codificate nei formati seguenti: \_ \_ DXGI FORMAT BC1 \_ UNORM, DXGI \_ FORMAT BC2 UNORM e \_ \_ DXGI \_ FORMAT \_ BC3 \_ UNORM. È possibile accedere ai dati compressi in blocchi DDS in forma decodificata usando interfacce WIC standard o direttamente usando nuove interfacce specifiche di DDS. Per altre informazioni, vedere i seguenti argomenti:

-   [**Interfaccia IWICDdsDecoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsdecoder)
-   [**Interfaccia IWICDdsEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsencoder)

## <a name="whats-new-for-windows-8"></a>Novità di Windows 8

In Windows 8, WIC è stato aggiornato con diverse nuove funzionalità. La versione aggiornata di WIC è disponibile anche in Windows 7 e Windows Server 2008 R2 tramite l'aggiornamento della piattaforma [per Windows 7,](../direct3darticles/platform-update-for-windows-7.md)disponibile tramite l'aggiornamento della piattaforma per [Windows 7](https://support.microsoft.com/kb/2670838).

### <a name="improved-direct2d-integration"></a>Integrazione di Direct2D migliorata

WIC in Windows 8 queste API per migliorare l'integrazione direct2D con WIC:

-   [**IWICImageEncoder:**](/windows/win32/api/Wincodec/nn-wincodec-iwicimageencoder) nuova interfaccia in grado di codificare il contenuto [**DIRECT2D ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in [un oggetto IWICBitmapFrameEncode.](-wic-imp-iwicbitmapframeencode.md) I metodi di questa interfaccia accettano un puntatore a [**WICImageParameters,**](/windows/win32/api/Wincodec/ns-wincodec-wicimageparameters)che sono parametri per controllare la codifica.
-   [**IWICImagingFactory2:**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory2) nuova factory WIC con il [**metodo CreateImageEncoder.**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder) Questa interfaccia eredita dalla factory WIC originale, [**IWICImagingFactory,**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory)e viene creata allo stesso modo.

### <a name="changes-to-bmp-codec-alpha-support"></a>Modifiche al supporto alfa del codec BMP

WIC in Windows 8 supporta il caricamento [**di file di immagine BITMAPV5HEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) come immagini in formato [WICPixelFormat32bppBGRA.](-wic-codec-native-pixel-formats.md) Inoltre, il codificatore BMP supporta una nuova opzione booleana del codificatore "EnableV5Header32bppBGRA", che indica al codificatore di scrivere un **OGGETTO BITMAPV5HEADER** con i dati immagine di 32bppBGRA.

Per altre informazioni sui formati BMP, vedere [Panoramica del formato BMP.](bmp-format-overview.md)

### <a name="new-pixel-formats"></a>Nuovi formati di pixel

WIC in Windows 8 definisce questi nuovi formati di pixel:

-   GUID \_ WICPixelFormat32bppRGB
-   GUID \_ WICPixelFormat64bppRGB
-   GUID \_ WICPixelFormat96bppRGBFloat
-   GUID \_ WICPixelFormat64bppPRGBAHalf

> [!Note]  
> Il codec predefinito TIFF restituirà i dati \_ GUID WICPixelFormat96bppRGBFloat. Gli altri tre formati non vengono usati dai codec predefiniti.

 

### <a name="restrictions-to-component-extensibility-in-appcontainer"></a>Restrizioni all'estendibilità dei componenti in AppContainer

Quando viene eseguito in un processo AppContainer, che include tutte le app di Windows Store, WIC userà solo componenti forniti da Windows, indipendentemente dal fatto che nel sistema siano installati componenti aggiuntivi. L'app che non è in esecuzione in AppContainer non è interessata.

Le app non devono apportare modifiche al codice per l'esecuzione in un AppContainger, ma il flag [**WICComponentEnumerateOptions**](/windows/win32/api/Wincodec/ne-wincodec-wiccomponentenumerateoptions) e i parametri GUID del fornitore non avranno alcun effetto. WiC non riuscirà a caricare un'immagine se non può essere decodificata da un codec fornito da Windows e la chiamata al metodo [**CreateComponentEnumerator**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentenumerator) restituirà solo Windows componenti forniti.

### <a name="changes-to-clsid_wicpngdecoder-and-png-decoder-color-context-support"></a>Modifiche al supporto del contesto colori del decodificatore PNG e \_ WICPngDecoder CLSID

**CLSID \_ WICPngDecoder1** è stato aggiunto con lo stesso GUID del **CLSID \_ WICPngDecoder** e **il CLSID \_ WICPngDecoder2** è stato aggiunto.

Quando viene compilato in Windows 8 SDK, **CLSID \_ WICPngDecoder** viene definito in \# **CLSID \_ WICPngDecoder2** per promuovere le app appena compilate usando il nuovo comportamento del decodificatore PNG. Le app devono continuare a specificare **CLSID \_ WICPngDecoder**.

Se si specifica **CLSID \_ WICPngDecoder2,** verrà creata una versione del decodificatore PNG WIC che genererà un [**oggetto IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) dai blocchi cHRM e gAMA. In questo modo è possibile usare questi metadati dello spazio colore con altre API Windows per la gestione del colore dell'immagine di origine. Un **oggetto IWICColorContext** non viene generato dai blocchi gAMA e cHRM se è presente un blocco iCCP, se è presente un blocco sRGB o se i blocchi gAMA e cHRM indicano uno spazio colore sRGB.

Un'app può specificare **\_ CLSID WICPngDecoder1** per creare una versione del decodificatore PNG WIC che non genera [**un oggetto IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) dai blocchi gAMA e cHRM. Corrisponde al comportamento del decodificatore PNG nelle versioni precedenti di Windows.

### <a name="changes-to-wincodec_sdk_version"></a>Modifiche a WINCODEC \_ SDK \_ VERSION

Quando viene compilato in Windows 8 SDK, **WINCODEC \_ SDK \_ VERSION** viene definito in \# **WINCODEC \_ SDK \_ VERSION2** per promuovere le app appena compilate usando il nuovo comportamento del decodificatore PNG. In caso contrario, \# viene definito in **WINCODEC \_ SDK \_ VERSION1.** Le app devono continuare a specificare **WINCODEC \_ SDK \_ VERSION**.

Se si specifica **WINCODEC \_ SDK \_ VERSION** quando si chiama [**il \_ proxy WICCreateImagingFactory**](-wic-codec-wiccreateimagingfactory-proxy.md) per creare la factory di creazione dell'immagine, viene creato **CLSID \_ WICPngDecoder2** anziché **CLSID \_ WICPngDecoder1** dal [**metodo CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) e dalle relative varianti. Inoltre, un enumeratore di informazioni sul componente del decodificatore restituirà informazioni sul componente **\_ CLSID WICPngDecoder2,** ma non informazioni **su \_ CLSID WICPngDecoder1.**

Se si **specifica WINCODEC \_ SDK \_ VERSION1,** verrà usato **\_ CLSID WICPngDecoder1** anziché **\_ CLSID WICPngDecoder2** nei casi precedenti.

### <a name="changes-to-clsid_wicimagingfactory"></a>Modifiche a CLSID \_ WICImagingFactory

**CLSID \_ WICImagingFactory1** è stato aggiunto con lo stesso GUID del **CLSID \_ WICImagingFactory** e **il CLSID \_ WICImagingFactory2** è stato aggiunto.

Quando viene compilato in Windows 8 SDK, **CLSID \_ WICImagingFactory** viene definito in \# **CLSID \_ WICImagingFactory2** per promuovere le app appena compilate usando il nuovo comportamento del decodificatore PNG. Le app devono continuare a specificare **CLSID \_ WICImagingFactory.**

Se si specifica **CLSID \_ WICImagingFactory2** quando si chiama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare la factory di creazione dell'immagine, viene creato **CLSID \_ WICPngDecoder2** anziché **CLSID \_ WICPngDecoder1** dal [**metodo CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) e dalle relative varianti. Inoltre, un enumeratore di informazioni sul componente del decodificatore restituirà informazioni sul componente **\_ CLSID WICPngDecoder2,** ma non informazioni **su \_ CLSID WICPngDecoder1.**

Se si specifica **\_ CLSID WICImagingFactory1,** verrà usato **\_ CLSID WICPngDecoder1** anziché **\_ CLSID WICPngDecoder2** nei casi precedenti.

## <a name="whats-new-for-windows-7"></a>Novità di Windows 7

In Windows 7, WIC è stato aggiornato con diverse nuove funzionalità. Questo argomento offre una rapida introduzione a queste nuove funzionalità.

### <a name="updates-to-the-tiff-codec"></a>Aggiornamenti al codec TIFF

Il codec WIC TIFF è stato aggiornato per Windows 7 per supportare diverse funzionalità non supportate dalla versione precedente di WIC.

-   Supporto per file TIFF di grandi dimensioni.
-   Decodificare immagini TIFF affiancate.
-   Decodificare immagini TIFF flat (planari).
-   Decodificare immagini TIFF con codifica JPEG.

### <a name="progressive-decoding"></a>Decodifica progressiva

La decodifica progressiva consente di decodificare ed eseguire il rendering incrementale di parti di un'immagine prima del termine del download dell'intera immagine. Questa funzionalità migliora notevolmente l'esperienza utente durante la visualizzazione di immagini da Internet, perché l'utente non deve attendere il download dell'intera immagine prima che possa iniziare la decodifica. Con la decodifica progressiva, gli utenti possono visualizzare un'anteprima dell'immagine con i dati disponibili molto prima che venga scaricata l'intera immagine. Questa funzionalità è essenziale per qualsiasi applicazione usata per visualizzare immagini da Internet o da origini dati con larghezza di banda limitata.

Per altre informazioni, vedere Cenni [preliminari sulla decodifica progressiva.](-wic-progressive-decoding.md)

### <a name="extended-metadata-support-for-jpeg-png-and-gif"></a>Supporto dei metadati estesi per JPEG, PNG e GIF

In Windows 7, WIC ha esteso il supporto dei metadati per le immagini JPEG, PNG e GIF.

-   Aggiunta del supporto per le proprietà GIF e GIF animate.
-   Gestori di metadati JPG espansi per supportare i metadati di chrominance, luminance e comment.
-   Gestori di metadati PNG espansi per supportare i metadati tIME, sRGB, iCCP, hIST, cHRM, iTXt, bKGD e gAMA.
-   Sono stati aggiunti nuovi gestori di metadati 8BIM per i metadati ResolutionInfo e i metadati digest IPTC.
-   Sono stati aggiunti nuovi gestori di metadati per i metadati LSD (Logical Screen Descriptor), Image Descriptor (IMD), Graphic Control Extensions (GCE) e Application Extensions (APE).
-   Supporto per i metadati che si estendono sui blocchi APPn.

### <a name="multi-threaded-apartment-support"></a>Supporto di apartment multi-thread

Gli oggetti all'interno di un apartment multithreading (MTA) possono essere chiamati contemporaneamente da qualsiasi numero di thread all'interno dell'MTA, consentendo prestazioni migliori nei sistemi multicore e in determinati scenari server. Inoltre, i codec WIC che si trovano all'interno di un MTA possono chiamare altri oggetti che si trovano all'interno dell'MTA senza il costo di marshalling associato alla chiamata tra thread che si trova in apartment STA diversi. Nella Windows 7, tutti i codec WIC predefiniti sono stati aggiornati per supportare MTA, tra cui JPEG, TIFF, PNG, GIF, ICO e BMP. È consigliabile scrivere codec per supportare L'agente di trasferimento messaggi. I codec che non supportano L'agente di trasferimento messaggi causeranno una riduzione significativa delle prestazioni nelle applicazioni multithreading a causa del marshalling. L'abilitazione del supporto MTA richiede l'implementazione della sincronizzazione appropriata nel codec. L'implementazione esatta di queste tecniche di sincronizzazione non è nell'ambito di questo documento. Di seguito viene fornito un riferimento generale per Component Object Model oggetti com(COM).

### <a name="metadata-working-group-implementations"></a>Implementazioni di gruppi di lavoro dei metadati

Esistono attualmente diversi formati di archiviazione dei metadati che contengono proprietà sovrapposte, senza standard di settore chiari o indicazioni su metodi coerenti per la lettura e la scrittura di questi formati di metadati. Per facilitare questa varietà di formati e proprietà, è stato formato il gruppo di lavoro metadati (MWG). L'obiettivo del gruppo MWG è fornire linee guida che garantiscono l'interoperabilità tra un'ampia gamma di piattaforme, applicazioni e dispositivi. Le linee guida stabilite dal MWG si applicano ai campi di metadati XMP, Exif e IPTC e ai formati di immagine JPEG, TIFF e PSD.

Nella Windows 7, il gestore dei metadati delle foto e il livello dei criteri dei metadati sono stati aggiornati per leggere e scrivere i metadati dell'immagine in base alle linee guida stabilite dal MWG. Per altre informazioni sul gruppo di lavoro dei metadati (MWG), vedere le linee guida [sui metadati stabilite.](https://s3.amazonaws.com/software.tagthatphoto.com/docs/mwg_guidance.pdf)

### <a name="windows-7-features-supported-on-windows-vista-and-windows-server-2008"></a>Windows 7 funzionalità supportate in Windows Vista e Windows Server 2008

[L'aggiornamento della piattaforma Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md) è un set di librerie di runtime che consente agli sviluppatori di scegliere come destinazione le applicazioni Windows 7 e Windows Vista. L'aggiornamento della piattaforma per Windows Server 2008 è un set di librerie di runtime che consente agli sviluppatori di scegliere come destinazione le applicazioni Windows Server 2008 R2 e Windows Server 2008. L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono fare in modo che Windows Update rilevi se l'aggiornamento richiesto è installato; In caso contrario, Windows update lo scariderà e lo installerà in background. Per altre informazioni su entrambi gli aggiornamenti, vedere Aggiornamento della piattaforma per Windows Vista

 

 
