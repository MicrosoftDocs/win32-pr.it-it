---
title: Miglioramento delle prestazioni delle app Direct2D
description: Vengono descritte le tecniche per migliorare le prestazioni di Direct2D.
ms.assetid: e6b02925-4e75-42b0-b0c4-00f1ddb85e46
keywords:
- Direct2D, prestazioni
- Direct2D, bitmap
- Direct2D, utilizzo risorse
- Direct2D, metodo Flush
- Direct2D, contenuto statico
- prestazioni per Direct2D
- bitmap per Direct2D
- Direct2D, interoperatività GDI
- Direct2D, interoperabilità
- interoperabilità, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilità, Graphics Device Interface (GDI)
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5a413b96e00514b64b3cf1b1ee451a84a9e9ff09
ms.sourcegitcommit: 6eb53540b8d882fd035d428567d7d1c5ec17042c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2020
ms.locfileid: "104474588"
---
# <a name="improving-the-performance-of-direct2d-apps"></a>Miglioramento delle prestazioni delle app Direct2D

Sebbene l'hardware [Direct2D](./direct2d-portal.md) sia accelerato ed è destinato a prestazioni elevate, è necessario utilizzare correttamente le funzionalità per ottimizzare la velocità effettiva. Le tecniche illustrate di seguito derivano dallo studio di scenari comuni e potrebbero non essere applicabili a tutti gli scenari di app. Pertanto, una conoscenza attenta del comportamento delle app e degli obiettivi di prestazioni può aiutare a ottenere i risultati desiderati.

-   [Utilizzo delle risorse](#resource-usage)
    -   [Riutilizza risorse](#reuse-resources)
-   [Limita l'uso dello scaricamento](#restrict-the-use-of-flush)
-   [Bitmap](#create-large-bitmaps)
    -   [Crea bitmap di grandi dimensioni](#create-large-bitmaps)
    -   [Creare un Atlante di bitmap](#create-an-atlas-of-bitmaps)
    -   [Crea bitmap condivise](#create-shared-bitmaps)
    -   [Copia di bitmap](#copying-bitmaps)
-   [Usa la bitmap affiancata su trattino](#use-tiled-bitmap-over-dashing)
-   [Linee guida generali per il rendering di contenuto statico complesso](#general-guidelines-for-rendering-complex-static-content)
    -   [Memorizzazione nella cache completa della scena utilizzando una bitmap a colori](#full-scene-caching-using-a-color-bitmap)
    -   [Per la memorizzazione nella cache primitiva con una bitmap a8 e il metodo FillOpacityMask](#per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method)
-   [Caching per primitive con le realizzazioni di geometria](#per-primitive-caching-using-geometry-realizations)
-   [Rendering Geometry](#geometry-rendering)
    -   [Usa una primitiva di estrazione specifica sulla geometria di tipo](#use-specific-draw-primitive-over-draw-geometry)
    -   [Rendering della geometria statica](#rendering-static-geometry)
    -   [Usare un contesto di dispositivo multithread](#use-a-multithreaded-device-context)
-   [Disegno di testo con Direct2D](#use-a-multithreaded-device-context)
    -   [Confronto tra DrawTextLayout e DrawText](#drawtextlayout-vs-drawtext)
    -   [Scelta della modalità di rendering del testo corretta](#choosing-the-right-text-rendering-mode)
    -   [Memorizzazione nella cache](#full-scene-caching-using-a-color-bitmap)
-   [Ritaglio di una forma arbitraria](#clipping-an-arbitrary-shape)
    -   [PushLayer in Windows 8](#pushlayer-in-windows-8)
    -   [Clip allineate asse](#axis-aligned-clips)
-   [Interoperabilità DXGI: evitare cambi frequenti](#dxgi-interoperability-avoid-frequent-switches)
-   [Conosce il formato pixel](#know-your-pixel-format)
-   [Complessità della scena](#scene-complexity)
    -   [Comprendere la complessità della scena](#understand-scene-complexity)
-   [Miglioramento delle prestazioni per le app di stampa Direct2D](#improving-performance-for-direct2d-printing-apps)
    -   [Impostare i valori di proprietà corretti quando si crea il controllo di stampa D2D](#set-the-right-property-values-when-you-create-the-d2d-print-control)
    -   [Evitare di usare determinati modelli di disegno Direct2D](#avoid-using-certain-direct2d-drawing-patterns)
    -   [Creare testo in modo diretto e normale](#draw-text-in-a-direct-and-plain-way)
    -   [Estrai le bitmap originali quando possibile](#draw-the-original-bitmaps-when-possible)
-   [Conclusione](#conclusion)

## <a name="resource-usage"></a>Utilizzo delle risorse

Una risorsa è un'allocazione di un certo tipo, sia nella memoria video che nel sistema. Bitmap e pennelli sono esempi di risorse.

In Direct2D è possibile creare risorse in software e hardware. La creazione e l'eliminazione di risorse nell'hardware sono operazioni costose perché richiedono un sovraccarico per la comunicazione con la scheda video. Vediamo come Direct2D esegue il rendering del contenuto in una destinazione.

In Direct2D tutti i comandi di rendering sono racchiusi tra una chiamata a [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e una chiamata a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw). Queste chiamate vengono effettuate a una destinazione di rendering. Prima di chiamare le operazioni di rendering, è necessario chiamare il metodo **BeginDraw** . Dopo aver chiamato **BeginDraw** , un contesto crea in genere un batch di comandi di rendering, ma ritarda l'elaborazione di questi comandi fino a quando non viene soddisfatta una di queste istruzioni:

-   [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) si è verificato. Quando viene chiamato **EndDraw** , il completamento di tutte le operazioni di disegno in batch e restituisce lo stato dell'operazione.
-   Viene eseguita una chiamata esplicita a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush): il metodo **Flush** causa l'elaborazione del batch e l'esecuzione di tutti i comandi in sospeso.
-   Il buffer che contiene i comandi di rendering è pieno. Se il buffer si riempie prima dell'evasione delle due condizioni precedenti, i comandi di rendering vengono scaricati.

Fino a quando le primitive non vengono scaricate, Direct2D mantiene i riferimenti interni a risorse corrispondenti, come bitmap e pennelli.

### <a name="reuse-resources"></a>Riutilizza risorse

Come già indicato, la creazione e l'eliminazione di risorse sono costose sull'hardware. Quindi, riutilizzare le risorse quando possibile. Eseguire l'esempio di creazione di bitmap nello sviluppo di giochi. In genere, le bitmap che compongono una scena in un gioco vengono create contemporaneamente con tutte le diverse varianti necessarie per il rendering frame-frame successivo. Al momento del rendering e del nuovo rendering della scena effettiva, le bitmap vengono riutilizzate anziché ricreate.

> [!Note]  
> Non è possibile riutilizzare le risorse per l'operazione di ridimensionamento della finestra. Quando una finestra viene ridimensionata, è necessario ricreare alcune risorse dipendenti dalla scala, ad esempio destinazioni di rendering compatibili ed eventualmente alcune risorse di livello, perché il contenuto della finestra deve essere ridisegnato. Questo può essere importante per mantenere la qualità complessiva della scena di cui è stato eseguito il rendering.

 

## <a name="restrict-the-use-of-flush"></a>Limita l'uso dello scaricamento

Poiché il metodo [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) causa l'elaborazione dei comandi per il rendering in batch, è consigliabile non usarlo. Per gli scenari più comuni, lasciare la gestione delle risorse a Direct2D.

## <a name="bitmaps"></a>Bitmap

Come indicato in precedenza, la creazione e l'eliminazione di risorse sono operazioni molto costose nell'hardware. Una bitmap è un tipo di risorsa usata spesso. La creazione di bitmap nella scheda video è dispendiosa. Il riutilizzo consente di velocizzare l'applicazione.

### <a name="create-large-bitmaps"></a>Crea bitmap di grandi dimensioni

Le schede video in genere hanno una dimensione minima di allocazione della memoria. Se viene richiesta un'allocazione di dimensioni minori, viene allocata una risorsa di questa dimensione minima e la memoria in eccedenza viene sprecata e non è disponibile per altri elementi. Se sono necessarie molte piccole bitmap, una tecnica migliore consiste nell'allocazione di una bitmap di grandi dimensioni e nell'archiviazione di tutti i contenuti bitmap di dimensioni ridotte in questa bitmap di grandi dimensioni. Quindi, le sottoaree della bitmap più grande possono essere lette laddove sono necessarie le bitmap più piccole. Spesso è necessario includere spaziatura interna (pixel neri trasparenti) tra le piccole bitmap per evitare qualsiasi interazione tra le immagini più piccole durante le operazioni. Si tratta anche di un *Atlante*, che offre il vantaggio di ridurre il sovraccarico della creazione di bitmap e lo spreco di memoria di piccole allocazioni bitmap. Si consiglia di ridurre la maggior parte delle bitmap ad almeno 64 KB e di limitare il numero di bitmap inferiori a 4 KB.

### <a name="create-an-atlas-of-bitmaps"></a>Creare un Atlante di bitmap

Esistono alcuni scenari comuni per i quali un Atlante bitmap può essere utilizzato molto bene. Le bitmap piccole possono essere archiviate all'interno di una bitmap di grandi dimensioni. Queste piccole bitmap possono essere estratte dalla bitmap più grande quando sono necessarie specificando il rettangolo di destinazione. Ad esempio, un'applicazione deve creare più icone. Tutte le bitmap associate alle icone possono essere caricate in una bitmap di grandi dimensioni. E in fase di rendering, possono essere recuperati dalla bitmap di grandi dimensioni.

> [!Note]  
> Una bitmap Direct2D creata nella memoria video è limitata alla dimensione massima della bitmap supportata dall'adapter in cui è archiviata. La creazione di una bitmap di dimensioni superiori potrebbe causare un errore.

 

> [!Note]  
> A partire da Windows 8, Direct2D include un [effetto Atlas](atlas.md) che rende più semplice questo processo.

 

### <a name="create-shared-bitmaps"></a>Crea bitmap condivise

La creazione di bitmap condivise consente ai chiamanti avanzati di creare oggetti bitmap Direct2D supportati direttamente da un oggetto esistente, già compatibili con la destinazione di rendering. In questo modo si evita la creazione di più superfici e contribuisce a ridurre il sovraccarico delle prestazioni.

> [!Note]  
> Le bitmap condivise sono in genere limitate a destinazioni software o a destinazioni interoperabili con DXGI. Usare i metodi [**CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)), [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))e [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) per creare bitmap condivise.

 

### <a name="copying-bitmaps"></a>Copia di bitmap

La creazione di una superficie DXGI è un'operazione costosa, quindi riutilizzare le superfici esistenti quando possibile. Anche nel software, se una bitmap è prevalentemente nel formato desiderato, ad eccezione di una piccola parte, è preferibile aggiornare tale porzione anziché generare l'intera bitmap e ricreare tutti gli elementi. Sebbene sia possibile usare [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) per ottenere gli stessi risultati, il rendering è in genere un'operazione molto più costosa rispetto alla copia. Questo perché, per migliorare la località della cache, l'hardware non archivia effettivamente una bitmap nello stesso ordine di memoria in cui viene indirizzata la bitmap. Al contrario, la bitmap potrebbe essere swizzled. Il swizzling è nascosto dalla CPU dal driver (lento e usato solo sulle parti di fascia inferiore) o dal gestore della memoria sulla GPU. A causa dei vincoli sul modo in cui i dati vengono scritti in una destinazione di rendering durante il rendering, le destinazioni di rendering non sono in genere swizzled o swizzled in modo che sia meno ottimale di quanto possa essere raggiunto se si è certi che non è mai necessario eseguire il rendering sulla superficie. Pertanto, [](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap) \* vengono forniti i metodi CopyFrom per la copia di rettangoli da un'origine alla bitmap Direct2D.

CopyFrom può essere utilizzato in uno dei tre formati seguenti:

-   [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)
-   [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)

## <a name="use-tiled-bitmap-over-dashing"></a>Usa la bitmap affiancata su trattino

Il rendering di una linea tratteggiata è un'operazione molto costosa a causa dell'elevata qualità e accuratezza dell'algoritmo sottostante. Per la maggior parte dei casi che non coinvolgono geometrie rettilinee, lo stesso effetto può essere generato più velocemente usando bitmap affiancate.

## <a name="general-guidelines-for-rendering-complex-static-content"></a>Linee guida generali per il rendering di contenuto statico complesso

Memorizza nella cache il contenuto se si esegue il rendering dello stesso frame di contenuto sul frame, soprattutto quando la scena è complessa.

Sono disponibili tre tecniche di Caching che è possibile usare:

-   Memorizzazione nella cache completa della scena utilizzando una bitmap a colori.
-   Per la memorizzazione nella cache primitiva con una bitmap a8 e il metodo [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) .
-   Caching per primitive con le realizzazioni di geometria.

Esaminiamo ognuna di queste informazioni in modo più dettagliato.

### <a name="full-scene-caching-using-a-color-bitmap"></a>Memorizzazione nella cache completa della scena utilizzando una bitmap a colori

Quando si esegue il rendering di contenuto statico, in scenari come l'animazione, creare un'altra bitmap a colori completi anziché scrivere direttamente nella bitmap dello schermo. Salvare la destinazione corrente, impostare la destinazione sulla bitmap intermedia ed eseguire il rendering del contenuto statico. Tornare quindi alla bitmap della schermata originale e creare la bitmap intermedia.

Ecco un esempio:


```C++
// Create a bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_B8G8R8A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &sceneBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render static content to the sceneBitmap.
m_d2dContext->SetTarget(sceneBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Render sceneBitmap to oldTarget.
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->DrawBitmap(sceneBitmap.Get());
```



Questo esempio USA bitmap intermedie per la memorizzazione nella cache e passa la bitmap a cui punta il contesto di dispositivo durante il rendering. In questo modo si evita la necessità di creare una destinazione di rendering compatibile per lo stesso scopo.

### <a name="per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method"></a>Per la memorizzazione nella cache primitiva con una bitmap a8 e il metodo FillOpacityMask

Quando la scena completa non è statica, ma è costituita da elementi come la geometria o il testo statici, è possibile usare una tecnica per la memorizzazione nella cache primitiva. Questa tecnica conserva le caratteristiche di anti-aliasing della primitiva che viene memorizzata nella cache e funziona con la modifica dei tipi di pennello. Usa una bitmap a8 dove a8 è un tipo di formato pixel che rappresenta un canale alfa con 8 bit. Le bitmap a8 sono utili per disegnare geometria/testo come maschera. Quando è necessario modificare l'opacità del contenuto statico, anziché modificare il contenuto stesso, è possibile tradurre, ruotare, inclinare o ridimensionare l'opacità della maschera.

Ecco un esempio:


```C++
// Create an opacity bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render to the opacityBitmap.
m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Call the FillOpacityMask method
// Note: for this call to work correctly the anti alias mode must be D2D1_ANTIALIAS_MODE_ALIASED. 
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->FillOpacityMask(
    opacityBitmap.Get(),
    m_contentBrush().Get(),
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS);
```



## <a name="per-primitive-caching-using-geometry-realizations"></a>Caching per primitive con le realizzazioni di geometria

Un'altra tecnica di memorizzazione nella cache per primitiva, denominata realizzazioni di geometria, offre una maggiore flessibilità nella gestione della geometria. Quando si desidera creare ripetutamente le geometrie con alias o con alias, è più veloce convertirle in realizzazioni di geometria e creare ripetutamente le realizzazioni rispetto a quelle per creare ripetutamente le geometrie. Anche le realizzazioni di geometria utilizzano in genere meno memoria rispetto alle maschere di opacità (soprattutto per geometrie di grandi dimensioni) e sono meno sensibili alle modifiche della scala. Per altre informazioni, vedere [Cenni preliminari sulle realizzazioni di geometria](geometry-realizations-overview.md).

Ecco un esempio:


```C++
    // Compute a flattening tolerance based on the scales at which the realization will be used.
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(...);

    ComPtr<ID2D1GeometryRealization> geometryRealization;

    // Create realization of the filled interior of the geometry.
    m_d2dDeviceContext1->CreateFilledGeometryRealization(
        geometry.Get(),
        flatteningTolerance,
        &geometryRealization
        );

    // In your app's rendering code, draw the geometry realization with a brush.
    m_d2dDeviceContext1->BeginDraw();
    m_d2dDeviceContext1->DrawGeometryRealization(
        geometryRealization.Get(),
        m_brush.Get()
        );
    m_d2dDeviceContext1->EndDraw();
```



## <a name="geometry-rendering"></a>Rendering Geometry

### <a name="use-specific-draw-primitive-over-draw-geometry"></a>Usa una primitiva di estrazione specifica sulla geometria di tipo

Usare chiamate *primitive* di estrazione più specifiche come [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) su chiamate [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) generiche. Questo è dovuto al fatto che, con **DrawRectangle**, la geometria è già nota, quindi il rendering è più veloce.

### <a name="rendering-static-geometry"></a>Rendering della geometria statica

Negli scenari in cui la geometria è statica, usare le tecniche di memorizzazione nella cache per primitive descritte in precedenza. Le maschere di opacità e le realizzazioni di geometria possono migliorare significativamente la velocità di rendering delle scene che contengono la geometria statica.

### <a name="use-a-multithreaded-device-context"></a>Usare un contesto di dispositivo multithread

Le applicazioni che prevedono di eseguire il rendering di quantità significative di contenuto geometrico complesso devono considerare la possibilità di specificare le [**Opzioni del contesto di dispositivo d2d1 Abilita il flag di \_ \_ \_ \_ \_ \_ \_ ottimizzazione**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options) multithread quando si crea un contesto di dispositivo [Direct2D](./direct2d-portal.md) . Quando si specifica questo flag, Direct2D distribuisce il rendering in tutti i core logici presenti nel sistema, che possono ridurre significativamente il tempo di rendering complessivo.

Note:

-   A partire da Windows 8.1, questo flag influiscono solo sul rendering della geometria del percorso. Non ha alcun effetto sulle scene contenenti solo altri tipi primitivi, ad esempio testo, bitmap o realizzazioni di geometria.
-   Questo flag non ha alcun effetto anche quando viene eseguito il rendering nel software, ad esempio quando viene eseguito il rendering con un dispositivo Direct3D WARP. Per controllare il multithreading del software, i chiamanti devono usare D3D11 \_ Create \_ Device per impedire l' \_ \_ \_ ottimizzazione del threading interno \_ quando si crea il dispositivo Direct3D Warp.
-   La specifica di questo flag può aumentare la working set di picco durante il rendering e può anche aumentare la contesa di thread nelle applicazioni che già sfruttano l'elaborazione multithreading.

## <a name="drawing-text-with-direct2d"></a>Disegno di testo con Direct2D

La funzionalità di rendering del testo Direct2D è disponibile in due parti. La prima parte, esposta come metodo [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , consente a un chiamante di passare una stringa e i parametri di formattazione oppure un oggetto di layout di testo DWrite per più formati. Questo deve essere adatto per la maggior parte dei chiamanti. Il secondo modo per eseguire il rendering del testo, esposto come metodo [**ID2D1RenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) , fornisce la rasterizzazione per i clienti che conoscono già la posizione dei glifi di cui si vuole eseguire il rendering. Le due regole generali seguenti consentono di migliorare le prestazioni del testo durante il disegno in Direct2D.

### <a name="drawtextlayout-vs-drawtext"></a>Confronto tra DrawTextLayout e DrawText

Sia [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) che [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) consentono a un'applicazione di eseguire facilmente il rendering del testo formattato dall'API [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) . **DrawTextLayout** disegna un oggetto [**DWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) esistente in [**renderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)e **DrawText** costruisce un layout DirectWrite per il chiamante, in base ai parametri passati. Se è necessario eseguire il rendering dello stesso testo più volte, utilizzare **DrawTextLayout** invece di **DrawText**, perché **DrawText** crea un layout ogni volta che viene chiamato.

### <a name="choosing-the-right-text-rendering-mode"></a>Scelta della modalità di rendering del testo corretta

Impostare la modalità antialias del testo su [**d2d1 \_ Text \_ antialias \_ mode \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) in modo esplicito. La qualità del rendering del testo in scala di grigi è paragonabile a ClearType ma è molto più veloce.

### <a name="caching"></a>Memorizzazione nella cache

Usare la scena completa o la memorizzazione nella cache di bitmap primitive, come per il disegno di altre primitive.

## <a name="clipping-an-arbitrary-shape"></a>Ritaglio di una forma arbitraria

La figura seguente mostra il risultato dell'applicazione di una clip a un'immagine.

![immagine che mostra un esempio di immagine prima e dopo un clip.](images/clip.png)

È possibile ottenere questo risultato usando i livelli con una maschera di geometria o il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello di opacità.

Di seguito è riportato un esempio che usa un livello:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Di seguito è riportato un esempio che usa il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



In questo esempio di codice, quando si chiama il metodo PushLayer, non si passa un livello creato dall'app. Direct2D crea automaticamente un livello. Direct2D è in grado di gestire l'allocazione e l'eliminazione di questa risorsa senza alcun intervento da parte dell'app. Questo consente a Direct2D di riutilizzare i livelli internamente e di applicare le ottimizzazioni di gestione delle risorse.

In Windows 8 sono state apportate numerose ottimizzazioni all'utilizzo dei livelli ed è consigliabile provare a usare le API di livello anziché [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) quando possibile.

### <a name="pushlayer-in-windows-8"></a>PushLayer in Windows 8

L'interfaccia [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) è derivata dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) ed è fondamentale per visualizzare il contenuto Direct2D in Windows 8. per ulteriori informazioni su questa interfaccia, vedere [dispositivi e contesti di dispositivo](devices-and-device-contexts.md). Con l'interfaccia del contesto di dispositivo, è possibile ignorare la chiamata al metodo [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e quindi passare null al metodo [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) . Direct2D gestisce automaticamente la risorsa livello e può condividere le risorse tra i livelli e i grafici degli effetti.

### <a name="axis-aligned-clips"></a>Clip allineate asse

Se l'area da ritagliare è allineata all'asse della superficie di disegno, anziché arbitraria. Questo caso è adatto per l'utilizzo di un rettangolo di ritaglio anziché di un livello. Il miglioramento delle prestazioni è maggiore per la geometria con alias rispetto alla geometria con alias. Per altre informazioni sulle clip allineate asse, vedere l'argomento [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .

## <a name="dxgi-interoperability-avoid-frequent-switches"></a>Interoperabilità DXGI: evitare cambi frequenti

Direct2D può interagire senza interruzioni con le superfici Direct3D. Questa operazione è molto utile per la creazione di applicazioni che eseguono il rendering di una combinazione di contenuto 2D e 3D. Tuttavia, ogni passaggio tra il disegno del contenuto Direct2D e Direct3D influiscono sulle prestazioni.

Quando si esegue il rendering in una superficie DXGI, Direct2D Salva lo stato dei dispositivi Direct3D durante il rendering e il ripristino quando il rendering viene completato. Ogni volta che viene completato un batch di rendering Direct2D, il costo di questo salvataggio e ripristino e il costo di scaricamento di tutte le operazioni 2D vengono pagati, ma il dispositivo Direct3D non viene scaricato. Pertanto, per aumentare le prestazioni, limitare il numero di commutazioni di rendering tra Direct2D e Direct3D.

## <a name="know-your-pixel-format"></a>Conosce il formato pixel

Quando si crea una destinazione di rendering, è possibile usare la struttura del [**\_ \_ formato pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) per specificare il formato pixel e la modalità Alpha usati dalla destinazione di rendering. Un canale alfa fa parte del formato pixel che specifica il valore di code coverage o le informazioni sull'opacità. Se una destinazione di rendering non usa il canale alfa, è necessario crearla usando la [**modalità d2d1 \_ Alpha \_ \_ Ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) la modalità Alpha. In questo modo viene risparmiato il tempo impiegato per il rendering di un canale alfa non necessario.

Per ulteriori informazioni sui formati pixel e sulle modalità Alpha, vedere [formati pixel supportati e modalità Alpha](supported-pixel-formats-and-alpha-modes.md).

## <a name="scene-complexity"></a>Complessità della scena

Quando si analizzano le aree sensibili delle prestazioni in una scena che verrà sottoposta a rendering, sapere se la scena è associata a una velocità di riempimento o un limite di vertici può fornire informazioni utili.

-   Velocità di riempimento: la velocità di riempimento si riferisce al numero di pixel per cui una scheda grafica può eseguire il rendering e scrivere nella memoria video al secondo.
-   Limite di vertici: una scena è associata ai vertici quando contiene molti Geometry complessi.

### <a name="understand-scene-complexity"></a>Comprendere la complessità della scena

È possibile analizzare la complessità della scena modificando la dimensione della destinazione di rendering. Se il miglioramento delle prestazioni è visibile per una riduzione proporzionale della destinazione di rendering, l'applicazione è associata a una velocità di riempimento. In caso contrario, la complessità della scena rappresenta il collo di bottiglia delle prestazioni.

Quando una scena è associata a una velocità di riempimento, la riduzione delle dimensioni della destinazione di rendering può migliorare le prestazioni. Questo perché il numero di pixel di cui eseguire il rendering viene ridotto proporzionalmente alle dimensioni della destinazione di rendering.

Quando una scena è associata al vertice, ridurre la complessità della geometria. Tuttavia, tenere presente che questa operazione viene eseguita a scapito della qualità dell'immagine. Pertanto, è necessario prendere una decisione di compromesso attenta tra la qualità desiderata e le prestazioni necessarie.

## <a name="improving-performance-for-direct2d-printing-apps"></a>Miglioramento delle prestazioni per le app di stampa Direct2D

[Direct2D](./direct2d-portal.md) offre compatibilità con la stampa. È possibile inviare gli stessi comandi di disegno Direct2D (sotto forma di elenchi di comandi Direct2D) al controllo di stampa Direct2D per la stampa, se non si conoscono i dispositivi da disegnare o il modo in cui il disegno viene convertito in stampa.

È possibile ottimizzare ulteriormente l'utilizzo del controllo di stampa [Direct2D](./direct2d-portal.md) e dei comandi di disegno Direct2D per fornire risultati di stampa con prestazioni migliori.

Il controllo di stampa [Direct2D](./direct2d-portal.md) genera messaggi di debug quando rileva un modello di codice Direct2D che comporta una riduzione della qualità di stampa o delle prestazioni (ad esempio, i modelli di codice elencati più avanti in questo argomento) per ricordare dove è possibile evitare problemi di prestazioni. Per visualizzare i messaggi di debug, è necessario abilitare il [livello di debug Direct2D](direct2ddebuglayer-portal.md) nel codice. Per istruzioni su come abilitare l'output del messaggio di debug, vedere [messaggi di debug](direct2ddebuglayer-debugmessages.md) .

### <a name="set-the-right-property-values-when-you-create-the-d2d-print-control"></a>Impostare i valori di proprietà corretti quando si crea il controllo di stampa D2D

Sono disponibili tre proprietà che è possibile impostare quando si crea il controllo di stampa [Direct2D](./direct2d-portal.md) . Due di queste proprietà influiscano sul modo in cui il controllo di stampa Direct2D gestisce determinati comandi Direct2D e a loro volta influisca sulle prestazioni complessive.

-   Modalità subset del tipo di carattere: il controllo di stampa [Direct2D](./direct2d-portal.md) imposta le risorse dei tipi di carattere utilizzate in ogni pagina prima di inviare la pagina da stampare. Questa modalità riduce le dimensioni delle risorse della pagina necessarie per la stampa. A seconda dell'utilizzo dei tipi di carattere nella pagina, è possibile scegliere diverse modalità di subset dei tipi di carattere per ottenere prestazioni ottimali.
    -   [**D2d1 \_ La \_ \_ \_ modalità \_ predefinita del subset di caratteri di stampa**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) fornisce le migliori prestazioni di stampa nella maggior parte dei casi. Se impostata su questa modalità, il controllo di stampa [Direct2D](./direct2d-portal.md) utilizza una strategia euristica per decidere quando sottoporre a subset i tipi di carattere.
    -   Per i processi di stampa brevi con 1 o 2 pagine, è consigliabile [**d2d1 \_ Print \_ Font \_ \_ mode subset Mode \_ EACHPAGE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) , dove il controllo di stampa [Direct2D](./direct2d-portal.md) subset e incorpora le risorse dei tipi di carattere in ogni pagina, quindi Elimina il subset del tipo di carattere dopo la stampa della pagina. Questa opzione assicura che ogni pagina possa essere stampata immediatamente dopo la generazione, ma aumenta leggermente le dimensioni delle risorse della pagina necessarie per la stampa (con subset di caratteri di grandi dimensioni).
    -   Per i processi di stampa con molte pagine di testi e piccole dimensioni dei tipi di carattere, ad esempio 100 pagine di testo che usano un solo tipo di carattere, è consigliabile usare la [](./direct2d-portal.md) modalità di subset dei [**tipi di carattere di stampa d2d1, in cui il controllo di stampa Direct2D non esegue il subset delle risorse del \_ \_ \_ \_ \_**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode)tipo di carattere, bensì Invia le risorse del tipo di carattere originali insieme alla pagina che usa per prima cosa il tipo di carattere e riutilizza le risorse del tipo di carattere per le pagine successive senza inviarle nuovamente.
-   DPI di rasterizzazione: quando il controllo di stampa [Direct2D](./direct2d-portal.md) deve rasterizzare i comandi Direct2D durante la conversione DIRECT2D-XPS, usa questo valore dpi per la rasterizzazione. In altre parole, se la pagina non contiene contenuto rasterizzato, l'impostazione di qualsiasi valore DPI non modificherà le prestazioni e la qualità. A seconda dell'utilizzo della rasterizzazione nella pagina, è possibile scegliere diversi dpi di rasterizzazione per il migliore equilibrio tra fedeltà e prestazioni.
    -   150 è il valore predefinito se non si specifica un valore quando si crea il controllo di stampa [Direct2D](./direct2d-portal.md) , che rappresenta il migliore equilibrio tra la qualità della stampa e le prestazioni di stampa nella maggior parte dei casi.
    -   I valori DPI più elevati in genere comportano una migliore qualità di stampa, come in altri dettagli conservati, ma con prestazioni ridotte a causa delle bitmap più grandi generate. Non è consigliabile alcun valore DPI maggiore di 300 poiché questo non introdurrà informazioni aggiuntive visivamente percepibili dagli occhi umani.
    -   I valori DPI inferiori possono comportare prestazioni migliori ma possono produrre anche una qualità inferiore.

### <a name="avoid-using-certain-direct2d-drawing-patterns"></a>Evitare di usare determinati modelli di disegno Direct2D

Esistono differenze tra gli elementi che [Direct2D](./direct2d-portal.md) possono rappresentare visivamente e ciò che il sottosistema di stampa può gestire e trasportare lungo l'intera pipeline di stampa. Il controllo di stampa Direct2D colma tali gap approssimando o rasterizzando le primitive Direct2D che il sottosistema di stampa non supporta in modo nativo. Questa approssimazione in genere comporta una riduzione della fedeltà di stampa, una riduzione delle prestazioni di stampa o entrambi. Pertanto, anche se un cliente può usare gli stessi schemi di disegno per il rendering dello schermo e di stampa, non è ideale in tutti i casi. È preferibile non usare tali primitive e modelli Direct2D il più possibile per il percorso di stampa oppure per eseguire la rasterizzazione in cui si ha il controllo completo della qualità e delle dimensioni delle immagini rasterizzate.

Di seguito è riportato un elenco di casi in cui le prestazioni e la qualità di stampa non saranno ideali e potrebbe essere necessario valutare la possibilità di variare il percorso del codice per ottenere prestazioni di stampa ottimali.

-   Evitare di usare la modalità di Blend primitiva diversa da [**d2d1 \_ primitive \_ Blend \_ SOURCEOVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend).
-   Evitare di usare le modalità di composizione durante il disegno di un'immagine diversa dall' [**\_ \_ \_ origine \_ in modalità composita d2d1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) e dalla **\_ \_ destinazione della modalità \_ \_ composita d2d1**.
-   Evitare di disegnare un file di metadati GDI.
-   Evitare di eseguire il push di una risorsa di livello che copia lo sfondo dell'origine (chiamando [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) con il passaggio di [**d2d1 \_ Layer \_ OPTIONS1 \_ Inizializza \_ dallo \_ sfondo**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) allo struct **\_ \_ PARAMETERS1 layer** ).
-   Evitare di creare un pennello bitmap o un pennello immagine con il \_ morsetto della modalità di estensione d2d1 \_ \_ . Si consiglia di usare il \_ mirror della modalità di estensione d2d1 \_ \_ se non si è interessati ai pixel al di fuori dell'immagine associata (ad esempio, l'immagine collegata al pennello è nota come più grande dell'area di destinazione riempita).
-   Evitare di disegnare bitmap con [trasformazioni prospettiche](3d-perspective-transform.md).

### <a name="draw-text-in-a-direct-and-plain-way"></a>Creare testo in modo diretto e normale

Direct2D presenta diverse ottimizzazioni quando si esegue il rendering dei testi da visualizzare per ottenere prestazioni migliori e/o qualità visiva migliore. Tuttavia, non tutte le ottimizzazioni migliorano le prestazioni e la qualità della stampa, perché la stampa su carta è in genere in un valore DPI molto più elevato e la stampa non deve contenere scenari come l'animazione. È quindi consigliabile creare direttamente il testo o i glifi originali ed evitare le ottimizzazioni seguenti quando si crea l'elenco dei comandi per la stampa.

-   Evitare di disegnare testo con il metodo [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask) .
-   Evitare di disegnare testo in modalità alias.

### <a name="draw-the-original-bitmaps-when-possible"></a>Estrai le bitmap originali quando possibile

Se la bitmap di destinazione è JPEG, PNG, TIFF e JPEG-XR, è possibile creare una bitmap WIC da un file su disco o da un flusso in memoria, quindi creare una bitmap [Direct2D](./direct2d-portal.md) dalla bitmap WIC usando [**ID2D1DeviceContext:: CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))e infine passare direttamente tale bitmap Direct2D al controllo di stampa Direct2D senza ulteriori modifiche. In questo modo, il controllo di stampa Direct2D è in grado di riutilizzare il flusso bitmap, che in genere consente di migliorare le prestazioni di stampa (ignorando la codifica e la decodifica di bitmap ridondanti) e una migliore qualità di stampa (quando i metadati, ad esempio i profili dei colori, nella bitmap verranno conservati).

Il disegno della bitmap originale offre i vantaggi seguenti per le applicazioni.

-   In generale, la stampa [Direct2D](./direct2d-portal.md) conserva le informazioni originali, senza perdita o rumore, fino alla fine della pipeline, soprattutto quando le app non conoscono o non vogliono conoscere i dettagli della pipeline di stampa, ad esempio la stampante in cui viene eseguita la stampa, il valore dpi è la stampante di destinazione e così via.
-   In molti casi, ritardare la rasterizzazione delle bitmap significa migliorare le prestazioni (ad esempio quando si stampa una foto 96dpi in una stampante 600dpi).
-   In alcuni casi, il passaggio delle immagini originali è l'unico modo per rispettare la fedeltà elevata, ad esempio i profili colori incorporati.

Tuttavia, non è possibile optare per questa ottimizzazione perché:

-   Eseguendo una query sulle informazioni sulla stampante e la rasterizzazione preliminare, è possibile rasterizzare il contenuto con il controllo completo sull'aspetto finale del documento.
-   In alcuni casi, la rasterizzazione anticipata potrebbe effettivamente migliorare le prestazioni end-to-end di un'app, ad esempio la stampa di portafogli, le foto delle dimensioni.
-   In alcuni casi, per passare le bitmap originali è necessario modificare in modo significativo l'architettura del codice esistente, ad esempio il caricamento ritardato delle immagini e i percorsi di aggiornamento delle risorse presenti in alcune applicazioni.

## <a name="conclusion"></a>Conclusione

Sebbene l'hardware Direct2D sia accelerato ed è destinato a prestazioni elevate, è necessario utilizzare correttamente le funzionalità per ottimizzare la velocità effettiva. Le tecniche esaminate di seguito derivano dallo studio di scenari comuni e potrebbero non essere applicabili a tutti gli scenari di applicazione.

 

 
