---
description: Windows Imaging Component (WIC) è stato aggiornato con le nuove versioni di Windows. In questo argomento viene fornita una rapida introduzione a queste nuove funzionalità.
ms.assetid: 710B71CE-6FCC-46DA-A65C-6E4FC6A04275
title: Novità in WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b8b3783ac2fd8ef6a971f785cec80f868a6b80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319100"
---
# <a name="whats-new-in-wic"></a>Novità in WIC

Windows Imaging Component (WIC) è stato aggiornato con le nuove versioni di Windows. In questo argomento viene fornita una rapida introduzione a queste nuove funzionalità.

## <a name="whats-new-for-windows-10-version-1507"></a>Novità di Windows 10 versione 1507

### <a name="access-to-low-level-jpeg-data-for-wic-decoding-and-encoding"></a>Accesso ai dati JPEG di basso livello per la decodifica e la codifica di WIC

A partire da Windows 10, versione 1507, WIC fornisce l'accesso alle strutture di dati JPEG di basso livello, incluse le tabelle Huffman e Quantity. Per altre informazioni, vedere i seguenti argomenti:

-   Interfaccia [**IWICJpegFrameDecode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframedecode)
-   Interfaccia [**IWICJpegFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframeencode)

### <a name="jpeg-indexing"></a>Indicizzazione JPEG

L'indicizzazione JPEG è una tecnica che migliora significativamente le prestazioni di accesso casuale ad aree secondarie di un'immagine JPEG di grandi dimensioni, al costo di un utilizzo di memoria aggiuntivo. L'indicizzazione JPEG può essere sfruttata da qualsiasi chiamante di WIC.

L'interfaccia [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) è progettata per sfruttare l'indicizzazione JPEG se è attivata. L'API ID2D1ImageSource, ad esempio, richiederà solo le sezioni necessarie dell'immagine in uno scenario come Pan e zoom per un'immagine di risoluzione di grandi dimensioni. Per altre informazioni, vedere i seguenti argomenti:

-   Metodo [**IWICJpegFrameDecode:: SetIndex**](/windows/win32/api/Wincodec/nf-wincodec-iwicjpegframedecode-setindexing)
-   Interfaccia [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)

## <a name="whats-new-for-windows-81"></a>Novità di Windows 8.1

### <a name="support-for-jpeg-ycbcr-images"></a>Supporto per immagini JPEG YCbCr

A partire da Windows 8.1, WIC fornisce supporto per la decodifica, la trasformazione e la codifica dei dati dell'immagine JPEG CbCr nel formato nativo. Ciò consente alle app di ridurre significativamente il tempo di elaborazione e il consumo di memoria per determinate operazioni di imaging quando si utilizzano JPEG con codifica CbCr. Per altre informazioni, vedere i seguenti argomenti:

-   [](-wic-sample-d2d-viewer.md)[Effetto YCbCr](../direct2d/ycbcr-effect.md) Direct2D
-   Interfaccia [**IWICPlanarBitmapSourceTransform**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
-   Interfaccia [**IWICPlanarBitmapFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode)

### <a name="support-for-block-compressed-formats-dds-files"></a>Supporto per formati compressi a blocchi (file DDS)

A partire da Windows 8.1, WIC aggiunge un nuovo codec che supporta le immagini DDS codificate nei formati seguenti: DXGI \_ Format \_ BC1 \_ UNORM, DXGI \_ Format \_ BC2 UNORM \_ e DXGI \_ Format BC3 \_ UNORM \_ . È possibile accedere ai dati compressi del blocco DDS in un formato decodificato utilizzando interfacce WIC standard o a cui si accede direttamente usando le nuove interfacce DDS specifiche. Per altre informazioni, vedere i seguenti argomenti:

-   Interfaccia [**IWICDdsDecoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsdecoder)
-   Interfaccia [**IWICDdsEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsencoder)

## <a name="whats-new-for-windows-8"></a>Novità di Windows 8

In Windows 8, WIC è stato aggiornato con alcune nuove funzionalità. La versione aggiornata di WIC è disponibile anche in Windows 7 e Windows Server 2008 R2 tramite l' [aggiornamento della piattaforma per Windows 7](../direct3darticles/platform-update-for-windows-7.md), disponibile tramite l' [aggiornamento della piattaforma per Windows 7](https://support.microsoft.com/kb/2670838).

### <a name="improved-direct2d-integration"></a>Integrazione Direct2D migliorata

WIC in Windows 8 fornisce queste API per migliorare l'integrazione Direct2D con WIC:

-   [**IWICImageEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicimageencoder) : nuova interfaccia che consente di codificare il contenuto [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) Direct2D in un [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md). I metodi di questa interfaccia accettano un puntatore a [**WICImageParameters**](/windows/win32/api/Wincodec/ns-wincodec-wicimageparameters), che sono parametri per controllare la codifica.
-   [**IWICImagingFactory2**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory2) : nuova Factory WIC con il metodo [**CreateImageEncoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder) . Questa interfaccia eredita dalla factory WIC originale, [**IWICImagingFactory**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory), e viene creata allo stesso modo.

### <a name="changes-to-bmp-codec-alpha-support"></a>Modifiche al supporto per il codec BMP

WIC in Windows 8 supporta il caricamento di file di immagine [**BITMAPV5HEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) come immagini in formato [WICPixelFormat32bppBGRA](-wic-codec-native-pixel-formats.md). Inoltre, il codificatore BMP supporta una nuova opzione del codificatore booleano "EnableV5Header32bppBGRA", che indica al codificatore di scrivere un **BITMAPV5HEADER** con i dati dell'immagine 32bppBGRA.

Per altre informazioni sui formati BMP, vedere [Cenni preliminari sul formato BMP](bmp-format-overview.md).

### <a name="new-pixel-formats"></a>Nuovi formati pixel

WIC in Windows 8 definisce questi nuovi formati pixel:

-   GUID \_ WICPixelFormat32bppRGB
-   GUID \_ WICPixelFormat64bppRGB
-   GUID \_ WICPixelFormat96bppRGBFloat
-   GUID \_ WICPixelFormat64bppPRGBAHalf

> [!Note]  
> Il codec predefinito TIFF restituirà i dati GUID \_ WICPixelFormat96bppRGBFloat. Gli altri tre formati non vengono usati dai codec predefiniti.

 

### <a name="restrictions-to-component-extensibility-in-appcontainer"></a>Restrizioni per l'estendibilità di componenti in AppContainer

Quando si esegue un processo AppContainer, che include tutte le app di Windows Store, in WIC verranno utilizzati solo i componenti forniti da Windows, indipendentemente dal fatto che nel sistema siano installati componenti aggiuntivi. L'app che non è in esecuzione in AppContainer non è interessata.

Per le app non è necessario apportare modifiche al codice per l'esecuzione in un AppContainger, ma i parametri del flag [**WICComponentEnumerateOptions**](/windows/win32/api/Wincodec/ne-wincodec-wiccomponentenumerateoptions) e del GUID del fornitore non avranno alcun effetto. WIC non riuscirà a caricare un'immagine se non può essere decodificata da un codec fornito da Windows e la chiamata al metodo [**CreateComponentEnumerator**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentenumerator) restituirà solo i componenti forniti da Windows.

### <a name="changes-to-clsid_wicpngdecoder-and-png-decoder-color-context-support"></a>Modifiche al \_ supporto del contesto di colore del decodificatore CLSID WICPngDecoder e png

**CLSID \_ WICPngDecoder1** è stato aggiunto con lo stesso GUID di **CLSID \_ WICPngDecoder** e è stato aggiunto **CLSID \_ WICPngDecoder2** .

Quando viene compilato con Windows 8 SDK, **CLSID \_ WICPngDecoder** viene \# definito per **CLSID \_ WICPngDecoder2** per promuovere le nuove app compilate usando il nuovo comportamento del decodificatore PNG. Le app devono continuare a specificare **CLSID \_ WICPngDecoder**.

Se si specifica **CLSID \_ WICPngDecoder2** , viene creata una versione del decodificatore PNG WIC che genererà un [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) dai blocchi chrm e Gama. Questo consente di usare questi metadati dello spazio colore con altre API Windows per la gestione dei colori dell'immagine di origine. Un **IWICColorContext** non viene generato dai blocchi Gama e chrm se è presente un blocco ICCP, se è presente un blocco sRGB o se i blocchi Gama e chrm indicano uno spazio colore sRGB.

Un'app può specificare **CLSID \_ WICPngDecoder1** per creare una versione del decodificatore PNG di WIC che non genera un [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) dai blocchi Gama e chrm. Corrisponde al comportamento del decodificatore PNG nelle versioni precedenti di Windows.

### <a name="changes-to-wincodec_sdk_version"></a>Modifiche alla versione di WINCODEC \_ SDK \_

Quando viene compilato con Windows 8 SDK, **la \_ \_ versione di WINCODEC SDK** viene \# definita in **WINCODEC \_ SDK \_ VERSION2** per promuovere le nuove app compilate usando il nuovo comportamento del decodificatore PNG. In caso contrario, viene \# definito in **WINCODEC \_ SDK \_ Version1**. Le app devono continuare a specificare la **\_ \_ versione dell'SDK di WINCODEC**.

Se si specifica la **\_ \_ versione dell'SDK di WINCODEC** quando si chiama il [**\_ proxy WICCreateImagingFactory**](-wic-codec-wiccreateimagingfactory-proxy.md) per creare la factory di imaging, viene creato il **CLSID \_ WICPngDecoder2** anziché il **CLSID \_ WICPngDecoder1** dal metodo [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) e le relative varianti. Inoltre, un enumeratore info componente decodificatore restituisce **CLSID \_ WICPngDecoder2** informazioni sul componente, ma non **CLSID \_ WICPngDecoder1** info.

Se si specifica **WINCODEC \_ SDK \_ Version1** , verrà utilizzato **CLSID \_ WICPngDecoder1** anziché **CLSID \_ WICPngDecoder2** nei casi precedenti.

### <a name="changes-to-clsid_wicimagingfactory"></a>Modifiche a CLSID \_ WICImagingFactory

**CLSID \_ WICImagingFactory1** è stato aggiunto con lo stesso GUID di **CLSID \_ WICImagingFactory** e è stato aggiunto **CLSID \_ WICImagingFactory2** .

Quando viene compilato con Windows 8 SDK, **CLSID \_ WICImagingFactory** viene \# definito per **CLSID \_ WICImagingFactory2** per promuovere le nuove app compilate usando il nuovo comportamento del decodificatore PNG. Le app devono continuare a specificare **CLSID \_ WICImagingFactory**.

Se si specifica **CLSID \_ WICImagingFactory2** quando si chiama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare la factory di imaging, viene creato **CLSID \_ WICPngDecoder2** anziché **CLSID \_ WICPngDecoder1** dal metodo [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) e dalle relative varianti. Inoltre, un enumeratore info componente decodificatore restituisce **CLSID \_ WICPngDecoder2** informazioni sul componente, ma non **CLSID \_ WICPngDecoder1** info.

Se si specifica **CLSID \_ WICImagingFactory1** , viene utilizzato **CLSID \_ WICPngDecoder1** anziché **CLSID \_ WICPngDecoder2** nei casi precedenti.

## <a name="whats-new-for-windows-7"></a>Novità di Windows 7

In Windows 7, WIC è stato aggiornato con alcune nuove funzionalità. In questo argomento viene fornita una rapida introduzione a queste nuove funzionalità.

### <a name="updates-to-the-tiff-codec"></a>Aggiornamenti per il codec TIFF

Il codec TIFF WIC è stato aggiornato per Windows 7 per supportare diverse funzionalità non supportate dalla versione precedente di WIC.

-   Supporto per file TIFF di grandi dimensioni.
-   Decodifica le immagini TIFF affiancate.
-   Decodifica immagini TIFF Flat (planari).
-   Decodifica le immagini TIFF codificate JPEG.

### <a name="progressive-decoding"></a>Decodifica progressiva

La decodifica progressiva consente di decodificare in modo incrementale ed eseguire il rendering di parti di un'immagine prima del completamento del download dell'intera immagine. Questa funzionalità migliora notevolmente l'esperienza utente durante la visualizzazione di immagini da Internet, in quanto l'utente non deve attendere il download dell'intera immagine prima che possa iniziare la decodifica. Con la decodifica progressiva, gli utenti possono visualizzare un'anteprima dell'immagine con dati disponibili molto prima che venga scaricata l'intera immagine. Questa funzionalità è essenziale per qualsiasi applicazione utilizzata per visualizzare immagini da Internet o da origini dati con larghezza di banda limitata.

Per ulteriori informazioni, vedere [Cenni preliminari sulla decodifica progressiva](-wic-progressive-decoding.md).

### <a name="extended-metadata-support-for-jpeg-png-and-gif"></a>Supporto dei metadati estesi per JPEG, PNG e GIF

In Windows 7, WIC ha esteso il supporto dei metadati per le immagini JPEG, PNG e GIF.

-   Aggiunta del supporto per le proprietà GIF e GIF animate.
-   Gestori dei metadati JPG espansi per supportare i metadati cromatura, Luminance e comment.
-   Gestori di metadati PNG espansi per supportare i metadati tIME, sRGB, iCCP, cron, cHRM, iTXt, bKGD e gAMA.
-   Aggiunta di nuovi gestori di metadati 8BIM per metadati ResolutionInfo e metadati digest IPTC.
-   Sono stati aggiunti nuovi gestori di metadati per il descrittore di schermate logiche (LSD), il descrittore di immagini (IMD), le estensioni del controllo grafico (GCE) e i metadati di Application Extensions (APE).
-   Supporto per i metadati che si estendono su blocchi APPn.

### <a name="multi-threaded-apartment-support"></a>Supporto per Apartment multithread

Gli oggetti all'interno di un Apartment a thread multipli (MTA) possono essere chiamati simultaneamente da un numero qualsiasi di thread all'interno dell'MTA, consentendo prestazioni migliori nei sistemi multicore e in alcuni scenari server. Inoltre, i codec WIC che risiedono all'interno di un MTA possono chiamare altri oggetti che risiedono all'interno dell'MTA senza il costo del marshalling associato alla chiamata tra thread che si trovano in diversi apartment STA. In Windows 7, tutti i codec WIC inclusi sono stati aggiornati per supportare MTA, tra cui JPEG, TIFF, PNG, GIF, ICO e BMP. È consigliabile scrivere codec per supportare l'MTA. I codec che non supportano MTA provocheranno un notevole peggioramento delle prestazioni nelle applicazioni multithread a causa del marshalling. Per abilitare il supporto MTA, è necessario implementare correttamente la sincronizzazione nel codec. L'implementazione esatta di queste tecniche di sincronizzazione esula dall'ambito di questo documento. Di seguito è riportato un riferimento generale per la sincronizzazione di oggetti Component Object Model (COM).

### <a name="metadata-working-group-implementations"></a>Implementazioni del gruppo di lavoro dei metadati

Attualmente è disponibile un'ampia gamma di formati di archiviazione di metadati che contengono proprietà sovrapposte, senza alcun chiaro standard di settore o linee guida sui metodi coerenti per la lettura e la scrittura di questi formati di metadati. Per semplificare questa varietà di formati e proprietà, è stato creato il gruppo di lavoro dei metadati (MWG). Lo scopo di MWG è fornire linee guida per garantire l'interoperabilità tra un'ampia gamma di piattaforme, applicazioni e dispositivi. Le linee guida stabilite da MWG si applicano ai campi di metadati XMP, EXIF e IPTC e ai formati di immagine JPEG, TIFF e PSD.

In Windows 7, il gestore dei metadati delle foto e il livello di criteri dei metadati sono stati aggiornati per leggere e scrivere i metadati delle immagini in base alle linee guida stabilite da MWG. Per ulteriori informazioni sul gruppo di lavoro dei metadati (MWG), visualizzare le [linee guida per i metadati stabilite](https://s3.amazonaws.com/software.tagthatphoto.com/docs/mwg_guidance.pdf).

### <a name="windows-7-features-supported-on-windows-vista-and-windows-server-2008"></a>Funzionalità di Windows 7 supportate in Windows Vista e Windows Server 2008

L' [aggiornamento della piattaforma per Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md) è costituito da un set di librerie di runtime che consente agli sviluppatori di utilizzare le applicazioni in Windows 7 e Windows Vista. L'aggiornamento della piattaforma per Windows Server 2008 è costituito da un set di librerie di runtime che consente agli sviluppatori di utilizzare le applicazioni in Windows Server 2008 R2 e Windows Server 2008. L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono avere Windows Update rilevare se l'aggiornamento richiesto è installato; in caso contrario, Windows Update lo scaricherà e installerà in background. Per ulteriori informazioni su entrambi gli aggiornamenti, vedere Aggiornamento della piattaforma per Windows Vista

 

 
