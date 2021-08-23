---
title: Novità di Direct2D
description: Ecco alcune delle nuove aggiunte a Direct2D.
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 595a0833e88948585622d79907c81a1465e3fa7b11d1ebc8d6bbd697312509bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430471"
---
# <a name="whats-new-in-direct2d"></a>Novità di Direct2D

Ecco alcune delle nuove aggiunte a Direct2D.

## <a name="whats-new-for-windows-10-creators-update"></a>Novità di Windows 10 Creators Update

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10 Creators Update.

### <a name="support-for-svg-image-rendering"></a>Supporto per il rendering delle immagini SVG

A partire da Windows 10 Creators Update, Direct2D offre il supporto per l'analisi e il disegno di immagini SVG, consentendo agli sviluppatori di eseguire il rendering degli asset prodotti nei propri strumenti di grafica vettoriale preferiti senza convertirli prima in immagini raster. Usare questa funzionalità per migliorare il footprint del disco e il comportamento di ridimensionamento dell'iconografia in-app e usare le nuove API del modello a oggetti SVG di Direct2D per apportare modifiche a livello di codice al gruppo SVG dell'app. Si noti che Direct2D supporta solo un subset limitato di SVG adatto per le immagini e non supporta tutte le funzionalità di disegno SVG. Se è necessaria la compatibilità SVG di livello browser o le funzionalità orientate al Web di SVG, è consigliabile usare il controllo [WebView XAML.](/uwp/api/Windows.UI.Xaml.Controls.WebView) Per altre informazioni, vedere i seguenti argomenti:

-   [Esempio di rendering di immagini Direct2D SVG](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [Supporto SVG](svg-support.md)
-   [**Metodo ID2D1DeviceContext5::CreateSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument)
-   [**Metodo ID2D1DeviceContext5::D rawSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument)
-   [**Interfaccia ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)

### <a name="improved-support-for-color-management"></a>Supporto migliorato per la gestione dei colori

A partire da Windows 10 Creators Update, Direct2D offre funzionalità migliorate di gestione del colore. Gli sviluppatori non necessitano più di un profilo ICC per usare l'effetto di gestione dei colori di Direct2D. possono ora usare spazi colori DXGI o costruire la propria definizione dello spazio colori con parametri. Per altre informazioni, vedere i seguenti argomenti:

-   [Effetto di gestione del colore](color-management.md)
-   [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))

## <a name="whats-new-for-windows-10-anniversary-update"></a>Novità dell'aggiornamento Windows 10'anniversario

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per l Windows 10'aggiornamento dell'anniversario.

### <a name="improved-support-for-color-fonts"></a>Supporto migliorato per i tipi di carattere a colori

A partire da Windows 10 Anniversary Update, Direct2D supporta ora il rendering di una gamma più ampia di formati di carattere a colori, consentendo agli sviluppatori di usare più tipi di carattere nelle app basate su Direct2D che mai. È incluso il supporto di:

-   Tabella OpenType "COLR", che consente contenuto vettoriale compatto nei tipi di carattere. (Supportato dal Windows 8.1.
-   Tabella OpenType 'SVG', che abilita il contenuto SVG nei tipi di carattere.
-   Tabella OpenType "CBDT", che consente il contenuto bitmap a colori nei tipi di carattere.
-   Tabella OpenType "sbix", che consente il contenuto bitmap a colori nei tipi di carattere.

Direct2D supporta automaticamente questi formati di carattere a colori quando è abilitato il flag [**D2D1 \_ DRAW TEXT OPTIONS ENABLE COLOR \_ \_ \_ \_ \_ FONT.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) Per altre informazioni, vedere i seguenti argomenti:

-   [Caratteri a colori](/windows/desktop/DirectWrite/color-fonts)
-   [DirectWrite campione di glifi a colori](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a>Nuovi effetti immagine

A partire Windows 10'aggiornamento dell'anniversario, Direct2D include gli effetti AlphaMask, CrossFade, Opacity e Tint. Questa funzionalità era disponibile in precedenza da configurazioni specifiche degli effetti Composito, ArithmeticComposite e ColorMatrix, ma i nuovi effetti predefiniti rendono più semplice eseguire queste operazioni comuni.

## <a name="whats-new-for-windows-10"></a>Novità di Windows 10

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10.

### <a name="sprite-batches"></a>Batch di sprite

A partire da Windows 10, Direct2D fornisce il supporto per la creazione e il rendering di batch di sprite. Rispetto al metodo [**DrawImage**](id2d1devicecontext-drawimage-overload.md) per utilizzo generico, i batch sprite comportano un sovraccarico della CPU per immagine notevolmente inferiore. Questo li rende ideali per scenari che coinvolgono centinaia o migliaia di immagini simultanee, ad esempio sprite di giochi o sistemi di particelle. Per altre informazioni, vedere i seguenti argomenti:

-   [**Metodo ID2D1DeviceContext3::CreateSpriteBatch**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch)
-   [**METODI ID2D1DeviceContext3::D rawSpriteBatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options))
-   [**Interfaccia ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch)

### <a name="gradient-meshes"></a>Mesh sfumato

A partire da Windows 10, Direct2D fornisce una nuova primitiva per le mesh sfumato. Le mesh sfumato vengono spesso usate dagli illustratori professionisti nel software di progettazione grafica e consentono agli artisti di eseguire il rendering di forme multicolore complesse (anche foto realistiche) con tutti i vantaggi di memoria e scalabilità dei vettori. Per altre informazioni, vedere gli argomenti seguenti:

-   [Esempio di mesh sfumata di Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   [**D2D1 \_ Struttura \_ PATCH \_ MESH SFUMATURA**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch)
-   [**Metodo ID2D1DeviceContext2::D rawGradientMesh**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh)

### <a name="improved-image-loading-apis"></a>API di caricamento delle immagini migliorate

A partire da Windows 10, Direct2D offre una nuova API per il caricamento delle immagini, ID2D1ImageSource. L'origine dell'immagine migliora le API di caricamento delle immagini esistenti, tra cui CreateBitmapFromWicBitmap, l'effetto Origine bitmap e l'effetto YCbCr. L'origine immagine Direct2D combina le funzionalità di queste API con il supporto per immagini arbitrariamente di grandi dimensioni, una facile integrazione con la stampa e gli effetti e numerose ottimizzazioni, tra cui YCbCr JPEG e JPEG indicizzato. Per altre informazioni, vedere gli argomenti seguenti:

-   [Esempio di Direct2D Photo Adjustment SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [IWICJpegFrameDecode::SetIndexing](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a>Supporto migliorato per il rendering dell'input penna

A partire da Windows 10, Direct2D fornisce una nuova primitiva per rappresentare i tratti input penna. I tratti input penna Direct2D sono definiti dalle curve di Bézier, supportano forme e trasformazioni di nib diverse e possono avere spessore fisso o variabile. Il supporto incorporato di Direct2D per i tratti input penna consente alle app di eseguire facilmente il rendering dell'input penna più veloce e più bello rispetto agli approcci precedenti, che in genere richiedevano alle app di gestire l'input penna, come una serie di ellissi e quadrilaterali. Per altre informazioni, vedere i seguenti argomenti:

-   [**Interfaccia ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [**Metodo ID2D1DeviceContext2::D rawInk**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [**Interfaccia ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a>Collegamento degli effetti shader

Gli effetti Direct2D vengono implementati usando pixel, vertici e/o compute shader HLSL. A partire da Windows 10, Direct2D ora analizza automaticamente i grafici degli effetti per trovare opportunità di combinare ed eseguire singoli shader insieme. Ciò può offrire un aumento significativo della velocità effettiva. I consumer di effetti predefiniti non devono eseguire operazioni per trarre vantaggio dal collegamento degli shader con effetti, ma gli sviluppatori che compilano i propri effetti personalizzati devono seguire le procedure consigliate aggiornate per sfruttare il collegamento degli shader degli effetti. Per altre informazioni, vedere i seguenti argomenti:

-   [Collegamento degli shader degli effetti](effect-shader-linking.md)
-   [Helper HLSL Direct2D](hlsl-helpers.md)
-   [Esempio di SDK per effetti personalizzati Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

Il collegamento degli effetti shader è progettato per non influire sull'output visivo degli effetti. Tuttavia, ciò non è sempre possibile a causa di un comportamento specifico intorno alla precisione dell'effetto e al ritaglio numerico. Per altre informazioni su come controllare questi comportamenti, vedere:

-   [Controllo della precisione e del ritaglio numerico nei grafici degli effetti](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a>Nuovi effetti predefiniti

A partire Windows 10, Direct2D include un set completo di nuovi effetti predefiniti che consentono di risolvere le principali richieste degli sviluppatori e di abilitare nuovi tipi di scenari visivi. I nuovi effetti sono:

### <a name="color"></a>Colore:

-   [Effetto da RGB a tonalità](rgb-to-hue-effect.md)
-   [Effetto Da tonalità a RGB](hue-to-rgb-effect.md)
-   [Effetto tabella di ricerca 3D](3d-lookup-table-effect.md)

### <a name="photo"></a>Foto:

-   [Effetto di contrasto](contrast-effect.md)
-   [Effetto di esposizione](exposure-effect.md)
-   [Effetto scala di grigi](grayscale-effect.md)
-   [Effetto Evidenziazioni e ombreggiature](highlights-and-shadows-effect.md)
-   [Effetto Inverti](invert-effect.md)
-   [Effetto seppia](sepia-effect.md)
-   [Effetto di affilare](sharpen-effect.md)
-   [Effetto raddrizza](straighten-effect.md)
-   [Temperatura e effetto tinta](temperature-and-tint-effect.md)
-   [Effetto della vignetta](vignette-effect.md)

### <a name="filter"></a>Filter:

-   [Effetto di rilevamento dei bordi](edge-detection-effect.md)

### <a name="stylize"></a>Stilizza:

-   [Effetto Rilievo](emboss-effect.md)
-   [Effetto Posterize](posterize-effect.md)

### <a name="transparency"></a>Trasparenza:

-   [Effetto chroma-key](chromakey-effect.md)

Gli effetti raddrizzamento, saturazione, contrasto, evidenziazioni e ombreggiature e temperatura e tinta sono illustrati nell'esempio [direct2D Photo Adjustment SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment).

## <a name="whats-new-for-windows-81"></a>Novità di Windows 8.1

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 8.1.

A partire Windows 8.1, Direct2D è basato su Direct3D 11.2.

### <a name="geometry-realizations"></a>Realizzazioni geometry

A partire Windows 8.1, Direct2D offre realizzazioni geometriche. Le realizzazioni geometry consentono alle applicazioni di migliorare le prestazioni di rendering della geometria in determinate situazioni, senza alcuni degli svantaggi della rasterizzazione della geometria in una bitmap. Per altre informazioni, vedere i seguenti argomenti:

-   [**Interfaccia ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1)
-   [**METODO ID2D1DeviceContext1::D rawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization)

### <a name="support-for-jpeg-ycbcr-images"></a>Supporto per immagini YCbCr JPEG

A partire Windows 8.1, Direct2D fornisce il supporto per il rendering dei dati immagine nel formato JPEG Y'CbCr. Le app possono eseguire il rendering del contenuto JPEG nella relativa rappresentazione Y'CbCr nativa anziché decomprimere in BGRA. Ciò può ridurre in modo significativo il consumo di memoria grafica e il tempo di creazione delle risorse. Per altre informazioni, vedere i seguenti argomenti:

-   Effetto Direct2D [YCbCr](ycbcr-effect.md)
-   [**Interfaccia IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)

### <a name="support-for-block-compressed-formats-dds-files"></a>Supporto per formati compressi a blocchi (file DDS)

A partire da Windows 8.1, Direct2D fornisce il supporto per le bitmap che contengono dati in pixel DXGI \_ FORMAT \_ BC1 \_ UNORM, DXGI \_ FORMAT BC2 UNORM e \_ \_ DXGI \_ FORMAT \_ BC3 \_ UNORM. Le app possono sostituire gli asset immagine con immagini DDS compresse a blocchi. Ciò può ridurre in modo significativo il consumo di memoria grafica e il tempo di creazione delle risorse. Per altre informazioni, vedere i seguenti argomenti:

-   [**Metodo ID2D1DeviceContext::CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md)
-   [**Interfaccia IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="rendering-priority"></a>Priorità di rendering

A partire da Windows 8.1, Direct2D fornisce il supporto per la priorità di rendering per dispositivo. Questa nuova funzionalità consente alle app di passare da una priorità di rendering normale (predefinita) a una bassa (in cui il dispositivo non bloccherà altre attività di rendering nel sistema). È consigliabile che le app usino una priorità di rendering bassa per le attività che non sono fondamentali per la velocità di risposta dell'utente, ad esempio il pre-rendering del contenuto, il rendering ridotto a icona e altre operazioni in genere eseguite in background. Per altre informazioni, vedere i seguenti argomenti:

-   [**Metodo ID2D1Device1::SetRenderingPriority**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority)
-   [**D2D1 \_ Enumerazione \_ RENDERING PRIORITY**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority)

## <a name="whats-new-for-windows-8"></a>Novità di Windows 8

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 8.

Le nuove interfacce Direct2D sono supportate in Windows 7 con l'aggiornamento della piattaforma [per Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7) installato.

La semantica di Direct2D per i dispositivi e i contesti di dispositivo è stata aggiornata in modo da essere più simile alla semantica usata da Direct3D e per fornire un'operazione concisa sulle app di Windows Store. Per [altre informazioni, vedere](devices-and-device-contexts.md) Dispositivi e contesti di dispositivo.

API correlate selezionate:

-   [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

L'API dell'elenco di comandi consente di condividere il percorso di rendering per il rendering e la stampa su schermo. Consente anche di usare primitive per creare un pennello immagine per il riempimento delle primitive.

API correlate selezionate:

-   [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

[Gli effetti Direct2D](effects-overview.md) sono un set di API, nuove Windows 8, per l'applicazione di effetti di alta qualità alle immagini. Include anche API che consentono di creare effetti personalizzati.

API correlate selezionate:

-   [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

A partire Windows 8, Direct2D include API aggiuntive per la creazione di app multithreading. Per [altre informazioni, vedere App Direct2D multithreading.](multi-threaded-direct2d-apps.md)

API correlate selezionate:

-   [**ID2D1MultiThread**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [**TIPO FACTORY D2D1 \_ \_ \_ \_ MULTI-THREAD**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 