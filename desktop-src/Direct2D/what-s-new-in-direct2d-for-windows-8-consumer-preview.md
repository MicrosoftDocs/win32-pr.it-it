---
title: Novità di Direct2D
description: Di seguito sono riportate alcune delle nuove aggiunte a Direct2D.
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9208ded926bda197baf41d9195c13cacd8f7079b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338166"
---
# <a name="whats-new-in-direct2d"></a>Novità di Direct2D

Di seguito sono riportate alcune delle nuove aggiunte a Direct2D.

## <a name="whats-new-for-windows-10-creators-update"></a>Novità di Windows 10 Creators Update

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10 Creators Update.

### <a name="support-for-svg-image-rendering"></a>Supporto per il rendering di immagini SVG

A partire da Windows 10 Creators Update, Direct2D fornisce il supporto per l'analisi e il disegno di immagini SVG, consentendo agli sviluppatori di eseguire il rendering di asset prodotti nei propri strumenti di grafica vettoriale preferiti senza convertirli prima in immagini raster. Usare questa funzionalità per migliorare il footprint del disco e il comportamento di ridimensionamento dell'iconografia in-app e usare le convenzioni nuove API del modello a oggetti SVG per apportare modifiche a livello di codice all'SVG dell'app. Si noti che Direct2D supporta solo un subset limitato di SVG adatto per le immagini e non supporta tutte le funzionalità di disegno SVG. Se è necessaria la compatibilità SVG di livello browser o le funzionalità orientate al Web di SVG, provare a usare invece il [controllo WebView XAML](/uwp/api/Windows.UI.Xaml.Controls.WebView) . Per altre informazioni, vedere i seguenti argomenti:

-   [Esempio di rendering dell'immagine di Direct2D SVG](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [Supporto per SVG](svg-support.md)
-   Metodo [**ID2D1DeviceContext5:: CreateSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument)
-   [**ID2D1DeviceContext5::D Metodo rawsvgdocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument)
-   Interfaccia [**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)

### <a name="improved-support-for-color-management"></a>Supporto migliorato per la gestione dei colori

A partire da Windows 10 Creators Update, Direct2D offre funzionalità migliorate per la gestione dei colori. Gli sviluppatori non hanno più bisogno di un profilo ICC per usare l'effetto di gestione colori le convenzioni; ora possono usare spazi dei colori DXGI o creare una definizione dello spazio dei colori con parametri. Per altre informazioni, vedere i seguenti argomenti:

-   [Effetto di gestione colori](color-management.md)
-   [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))

## <a name="whats-new-for-windows-10-anniversary-update"></a>Novità dell'aggiornamento dell'anniversario di Windows 10

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per l'aggiornamento dell'anniversario di Windows 10.

### <a name="improved-support-for-color-fonts"></a>Supporto migliorato per i tipi di carattere a colori

A partire dall'aggiornamento dell'anniversario di Windows 10, Direct2D supporta ora il rendering di una varietà più ampia di formati di caratteri colore, consentendo agli sviluppatori di usare più tipi di caratteri nelle app basate su Direct2D che mai. È incluso il supporto di:

-   Tabella OpenType ' COLR ', che consente il contenuto di un vettore compatto nei tipi di carattere. (Supportato da Windows 8.1.)
-   Tabella OpenType ' SVG ', che consente il contenuto SVG nei tipi di carattere.
-   Tabella OpenType ' CBDT ', che consente il contenuto della bitmap di colore nei tipi di carattere.
-   Tabella OpenType ' sbix ', che consente il contenuto della bitmap di colore nei tipi di carattere.

Direct2D supporta automaticamente questi formati dei tipi di carattere colore quando l' [**opzione d2d1 di testo di traccia Abilita il flag del \_ \_ tipo di \_ \_ \_ \_ carattere colore**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) è abilitata. Per altre informazioni, vedere i seguenti argomenti:

-   [Caratteri a colori](/windows/desktop/DirectWrite/color-fonts)
-   [Esempio di glifo colori DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a>Nuovi effetti immagine

A partire dall'aggiornamento dell'anniversario di Windows 10, Direct2D include gli effetti AlphaMask, crossfader, Opacity e color. Questa funzionalità era in precedenza disponibile in configurazioni specifiche di effetti compositi, ArithmeticComposite e ColorMatrix, ma i nuovi effetti predefiniti rendono più semplice eseguire queste operazioni comuni.

## <a name="whats-new-for-windows-10"></a>Novità di Windows 10

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10.

### <a name="sprite-batches"></a>Batch sprite

A partire da Windows 10, Direct2D fornisce supporto per la creazione e il rendering di batch sprite. Rispetto al metodo [**DrawImage**](id2d1devicecontext-drawimage-overload.md) per utilizzo generico, i batch sprite comportano un sovraccarico della CPU per ogni immagine notevolmente inferiore. Questo li rende ideali per gli scenari che coinvolgono centinaia o migliaia di immagini simultanee, ad esempio sprite del gioco o sistemi particellari. Per altre informazioni, vedere i seguenti argomenti:

-   Metodo [**ID2D1DeviceContext3:: CreateSpriteBatch**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch)
-   [**ID2D1DeviceContext3::D Metodi rawspritebatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options))
-   Interfaccia [**ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch)

### <a name="gradient-meshes"></a>Mesh con gradienti

A partire da Windows 10, Direct2D fornisce un nuovo primitivo per le mesh con gradienti. Le mesh con gradienti vengono spesso usate da autori professionisti del software di progettazione grafica e consentono agli artisti di eseguire il rendering di forme complesse (anche foto-realistiche) a colori multicolore con tutti i vantaggi in merito a memoria e scalabilità dei vettori. Per ulteriori informazioni, vedere gli argomenti seguenti:

-   [Esempio di mesh sfumata di Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   [**D2d1 \_ Struttura \_ \_ patch mesh con gradienti**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch)
-   [**ID2D1DeviceContext2::D Metodo rawgradientmesh**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh)

### <a name="improved-image-loading-apis"></a>API di caricamento delle immagini migliorate

A partire da Windows 10, Direct2D offre una nuova API per il caricamento di immagini, ID2D1ImageSource. L'origine dell'immagine migliora le API di caricamento delle immagini esistenti, tra cui CreateBitmapFromWicBitmap, l'effetto di origine della bitmap e l'effetto YCbCr. L'origine dell'immagine Direct2D combina le funzionalità di queste API con il supporto per immagini arbitrariamente grandi, facile integrazione con stampa ed effetti e numerose ottimizzazioni, tra cui YCbCr JPEG e indexed JPEG. Per altre informazioni, vedere gli argomenti seguenti:

-   [Esempio dell'SDK per la regolazione della foto Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [IWICJpegFrameDecode:: sedicizzazione](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a>Supporto migliorato per il rendering dell'input penna

A partire da Windows 10, Direct2D fornisce un nuovo primitivo per rappresentare i tratti di input penna. I tratti di input penna Direct2D sono definiti dalle curve di Bezier, supportano diverse forme e trasformazioni del pennino e possono avere uno spessore fisso o variabile. Il supporto incorporato di le convenzioni per i tratti di input penna consente alle app di eseguire facilmente il rendering di input penna più veloce e accattivante rispetto agli approcci precedenti, che in genere richiedono le app per gestire l'input penna, come una serie di ellissi e quadrilateri. Per altre informazioni, vedere i seguenti argomenti:

-   [**Interfaccia ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [**ID2D1DeviceContext2::D Metodo rawInk**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [**Interfaccia ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a>Collegamento Effect shader

Gli effetti Direct2D vengono implementati usando HLSL pixel, vertex e/o compute shader. A partire da Windows 10, Direct2D ora analizza automaticamente i grafici degli effetti per le opportunità di combinare ed eseguire insieme singoli shader. Questo può offrire un aumento significativo della velocità effettiva. I consumer di effetti predefiniti non devono eseguire alcuna operazione per trarre vantaggio dal collegamento Effect shader, ma gli sviluppatori che creano effetti personalizzati devono seguire le procedure consigliate aggiornate per sfruttare il collegamento Effect shader. Per altre informazioni, vedere i seguenti argomenti:

-   [Collegamento Effect shader](effect-shader-linking.md)
-   [Helper HLSL Direct2D](hlsl-helpers.md)
-   [Esempio di SDK per effetti personalizzati Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

Il collegamento Effect shader è progettato in modo da non influire sull'output visivo degli effetti. Tuttavia, ciò non è sempre possibile a causa di un comportamento specifico sulla precisione degli effetti e sul ritaglio numerico. Per ulteriori informazioni su come controllare questi comportamenti, vedere:

-   [Controllo della precisione e ritaglio numerico nei grafici effettivi](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a>Nuovi effetti predefiniti

A partire da Windows 10, Direct2D include un set completo di nuovi effetti predefiniti che risolvono le richieste principali per gli sviluppatori e consentono nuovi tipi di scenari visivi. I nuovi effetti sono:

### <a name="color"></a>Colore:

-   [Effetto RGB a Hue](rgb-to-hue-effect.md)
-   [Effetto tonalità su RGB](hue-to-rgb-effect.md)
-   [effetto tabella di ricerca 3D](3d-lookup-table-effect.md)

### <a name="photo"></a>Foto

-   [Effetto contrasto](contrast-effect.md)
-   [Effetto esposizione](exposure-effect.md)
-   [Effetto scala di grigi](grayscale-effect.md)
-   [Effetti evidenziazione e ombreggiatura](highlights-and-shadows-effect.md)
-   [Inverti effetto](invert-effect.md)
-   [Effetto seppia](sepia-effect.md)
-   [Effetto Nitidezza](sharpen-effect.md)
-   [Effetto di raddrizzamento](straighten-effect.md)
-   [Effetto temperatura e tinta](temperature-and-tint-effect.md)
-   [Effetto vignette](vignette-effect.md)

### <a name="filter"></a>Filter:

-   [Effetto rilevamento bordi](edge-detection-effect.md)

### <a name="stylize"></a>Applica stili a

-   [Effetto rilievo](emboss-effect.md)
-   [Effetto Posterizzazione](posterize-effect.md)

### <a name="transparency"></a>Trasparenza:

-   [Effetto chiave Chroma](chromakey-effect.md)

Gli effetti di raddrizzamento, saturazione, contrasto, evidenziazione e ombreggiatura e temperatura e tonalità sono illustrati nell'esempio di SDK per la [regolazione della foto Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment).

## <a name="whats-new-for-windows-81"></a>Novità di Windows 8.1

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 8.1.

A partire da Windows 8.1, Direct2D si basa su Direct3D 11,2.

### <a name="geometry-realizations"></a>Realizzazioni di geometria

A partire da Windows 8.1, Direct2D offre le realizzazioni di geometria. Le realizzazioni di geometria consentono alle applicazioni di migliorare le prestazioni di rendering della geometria in determinate situazioni, senza alcuni svantaggi della rasterizzazione della geometria in una bitmap. Per altre informazioni, vedere i seguenti argomenti:

-   Interfaccia [**ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1)
-   [**ID2D1DeviceContext1::D Metodo rawgeometryrealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization)

### <a name="support-for-jpeg-ycbcr-images"></a>Supporto per immagini JPEG YCbCr

A partire da Windows 8.1, Direct2D fornisce il supporto per il rendering dei dati immagine nel formato JPEG CbCr. Le app possono eseguire il rendering del contenuto JPEG nella relativa rappresentazione CbCr nativa anziché decomprimerlo in BGRA. Questo può ridurre significativamente il consumo di memoria grafica e il tempo di creazione delle risorse. Per altre informazioni, vedere i seguenti argomenti:

-   [Effetto YCbCr](ycbcr-effect.md) Direct2D
-   Interfaccia [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)

### <a name="support-for-block-compressed-formats-dds-files"></a>Supporto per formati compressi a blocchi (file DDS)

A partire da Windows 8.1, Direct2D fornisce il supporto per le bitmap che contengono DXGI \_ Format \_ BC1 \_ UNORM, DXGI \_ Format \_ BC2 UNORM \_ e DXGI Format BC3 UNORM \_ \_ \_ pixel data. Le app possono sostituire le proprie risorse immagini con le immagini DDS compresse in blocchi. Questo può ridurre significativamente il consumo di memoria grafica e il tempo di creazione delle risorse. Per altre informazioni, vedere i seguenti argomenti:

-   Metodo [**ID2D1DeviceContext:: CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md)
-   Interfaccia [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="rendering-priority"></a>Priorità di rendering

A partire da Windows 8.1, Direct2D fornisce il supporto per la priorità di rendering per ogni dispositivo. Questa nuova funzionalità consente alle app di passare un dispositivo tra la priorità di rendering normale (impostazione predefinita) e la priorità di rendering bassa (in cui il dispositivo non bloccherà altre attività di rendering nel sistema). È consigliabile che le app usino una priorità di rendering bassa per le attività che non sono cruciali per la velocità di risposta dell'utente, ad esempio il contenuto di pre-rendering, il rendering ridotto al minimo e altre operazioni che vengono in genere eseguite in background. Per altre informazioni, vedere i seguenti argomenti:

-   Metodo [**ID2D1Device1:: SetRenderingPriority**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority)
-   [**D2d1 \_ Enumerazione \_ priorità di rendering**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority)

## <a name="whats-new-for-windows-8"></a>Novità di Windows 8

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 8.

Le nuove interfacce Direct2D sono supportate in Windows 7 con l' [aggiornamento della piattaforma per Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7) installato.

La semantica di le convenzioni per i dispositivi e i contesti di dispositivo è stata aggiornata in modo da essere più simile alla semantica usata da Direct3D e per fornire un'operazione concisa sulle app di Windows Store. Per altre informazioni, vedere [dispositivi e contesti di dispositivo](devices-and-device-contexts.md) .

API correlate selezionate:

-   [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

L'API elenco dei comandi consente di condividere il percorso di rendering per il rendering e la stampa dello schermo. Consente inoltre di usare le primitive per creare un pennello immagine per riempire le primitive.

API correlate selezionate:

-   [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

[Gli effetti Direct2D](effects-overview.md) sono un set di API, una novità di Windows 8, per l'applicazione di effetti di alta qualità alle immagini. Include anche API che consentono di creare effetti personalizzati.

API correlate selezionate:

-   [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

A partire da Windows 8, Direct2D include API aggiuntive per la compilazione di app multithread. Per altre informazioni, vedere [app Direct2D multithread](multi-threaded-direct2d-apps.md) .

API correlate selezionate:

-   [**ID2D1MultiThread**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [**\_Tipo di \_ Factory \_ d2d1 \_ multithread**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 