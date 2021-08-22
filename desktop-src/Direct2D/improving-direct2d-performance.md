---
title: Miglioramento delle prestazioni delle app Direct2D
description: Vengono descritte le tecniche per migliorare le prestazioni direct2D.
ms.assetid: e6b02925-4e75-42b0-b0c4-00f1ddb85e46
keywords:
- Direct2D, prestazioni
- Direct2D, bitmap
- Direct2D, utilizzo delle risorse
- Metodo Direct2D,Flush
- Direct2D, contenuto statico
- prestazioni per Direct2D
- bitmap per Direct2D
- Interoperabilità Direct2D,GDI
- Direct2D, interoperabilità
- interoperabilità, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilità, Graphics Device Interface (GDI)
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 34adfd708ef3c1b8d7a6af145d9d1c9505b01beb1ba9b31834e267123ad05b69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641501"
---
# <a name="improving-the-performance-of-direct2d-apps"></a>Miglioramento delle prestazioni delle app Direct2D

Anche [se Direct2D](./direct2d-portal.md) è accelerato dall'hardware ed è destinato a prestazioni elevate, è necessario usare correttamente le funzionalità per ottimizzare la velocità effettiva. Le tecniche illustrate di seguito derivano dallo studio di scenari comuni e potrebbero non essere applicabili a tutti gli scenari di app. Pertanto, un'attenta comprensione del comportamento dell'app e degli obiettivi di prestazioni può contribuire a ottenere i risultati desiderati.

-   [Utilizzo delle risorse](#resource-usage)
    -   [Riutilizzare le risorse](#reuse-resources)
-   [Limitare l'uso dello scaricamento](#restrict-the-use-of-flush)
-   [Bitmap](#create-large-bitmaps)
    -   [Creare bitmap di grandi dimensioni](#create-large-bitmaps)
    -   [Creare un at atlas di bitmap](#create-an-atlas-of-bitmaps)
    -   [Creare bitmap condivise](#create-shared-bitmaps)
    -   [Copia di bitmap](#copying-bitmaps)
-   [Usare una bitmap affiancata al tratteggio](#use-tiled-bitmap-over-dashing)
-   [Linee guida generali per il rendering di contenuto statico complesso](#general-guidelines-for-rendering-complex-static-content)
    -   [Memorizzazione nella cache della scena completa con una bitmap a colori](#full-scene-caching-using-a-color-bitmap)
    -   [Memorizzazione nella cache per primitiva usando una bitmap A8 e il metodo FillOpacityMask](#per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method)
-   [Memorizzazione nella cache per primitiva con realizzazioni geometry](#per-primitive-caching-using-geometry-realizations)
-   [Rendering delle geometrie](#geometry-rendering)
    -   [Usare una primitiva di disegno specifica sulla geometria di disegno](#use-specific-draw-primitive-over-draw-geometry)
    -   [Rendering della geometria statica](#rendering-static-geometry)
    -   [Usare un contesto di dispositivo multithreading](#use-a-multithreaded-device-context)
-   [Disegno di testo con Direct2D](#use-a-multithreaded-device-context)
    -   [Confronto tra DrawTextLayout e DrawText](#drawtextlayout-vs-drawtext)
    -   [Scelta della modalità di rendering del testo giusta](#choosing-the-right-text-rendering-mode)
    -   [Memorizzazione nella cache](#full-scene-caching-using-a-color-bitmap)
-   [Ritaglio di una forma arbitraria](#clipping-an-arbitrary-shape)
    -   [PushLayer in Windows 8](#pushlayer-in-windows-8)
    -   [Clip allineate all'asse](#axis-aligned-clips)
-   [Interoperabilità DXGI: evitare commutatori frequenti](#dxgi-interoperability-avoid-frequent-switches)
-   [Conoscere il formato pixel](#know-your-pixel-format)
-   [Complessità della scena](#scene-complexity)
    -   [Informazioni sulla complessità della scena](#understand-scene-complexity)
-   [Miglioramento delle prestazioni per le app di stampa Direct2D](#improving-performance-for-direct2d-printing-apps)
    -   [Impostare i valori delle proprietà appropriati quando si crea il controllo di stampa D2D](#set-the-right-property-values-when-you-create-the-d2d-print-control)
    -   [Evitare di usare determinati modelli di disegno Direct2D](#avoid-using-certain-direct2d-drawing-patterns)
    -   [Disegnare testo in modo diretto e semplice](#draw-text-in-a-direct-and-plain-way)
    -   [Disegnare le bitmap originali quando possibile](#draw-the-original-bitmaps-when-possible)
-   [Conclusione](#conclusion)

## <a name="resource-usage"></a>Utilizzo delle risorse

Una risorsa è un'allocazione di qualche tipo, nella memoria video o di sistema. Bitmap e pennelli sono esempi di risorse.

In Direct2D le risorse possono essere create sia nel software che nell'hardware. La creazione e l'eliminazione di risorse nell'hardware sono operazioni costose perché richiedono un sovraccarico elevato per la comunicazione con la scheda video. Di seguito viene illustrato come Direct2D esegue il rendering del contenuto in una destinazione.

In Direct2D tutti i comandi di rendering sono racchiusi tra una chiamata a [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e una chiamata a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw). Queste chiamate vengono effettuate a una destinazione di rendering. È necessario chiamare il **metodo BeginDraw** prima di chiamare le operazioni di rendering. Dopo aver chiamato **BeginDraw,** un contesto in genere crea un batch di comandi di rendering, ma ritarda l'elaborazione di questi comandi fino a quando una di queste istruzioni non è vera:

-   [**Si è verificato EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Quando **viene chiamato EndDraw,** tutte le operazioni di disegno in batch vengono completate e restituisce lo stato dell'operazione.
-   Si effettua una chiamata esplicita a [**Flush:**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)il **metodo Flush** determina l'elaborazione del batch e l'esecuzione di tutti i comandi in sospeso.
-   Il buffer contenente i comandi di rendering è pieno. Se questo buffer diventa pieno prima che le due condizioni precedenti siano soddisfatte, i comandi di rendering vengono scaricati.

Finché le primitive non vengono scaricate, Direct2D mantiene i riferimenti interni alle risorse corrispondenti, ad esempio bitmap e pennelli.

### <a name="reuse-resources"></a>Riutilizzare le risorse

Come già accennato, la creazione e l'eliminazione delle risorse sono costose per l'hardware. Riutilizzare quindi le risorse quando possibile. Si consideri l'esempio della creazione di bitmap nello sviluppo di giochi. In genere, le bitmap che costituiscono una scena in un gioco vengono tutte create contemporaneamente con tutte le diverse varianti necessarie per il successivo rendering frame-frame. Al momento del rendering effettivo della scena e del nuovo rendering, queste bitmap vengono riutilizzate anziché ri-create.

> [!Note]  
> Non è possibile riutilizzare le risorse per l'operazione di ridimensionamento della finestra. Quando una finestra viene ridimensionata, alcune risorse dipendenti dalla scala, ad esempio destinazioni di rendering compatibili ed eventualmente alcune risorse di livello, devono essere ri-create perché il contenuto della finestra deve essere ridisegnato. Questo può essere importante per mantenere la qualità complessiva della scena sottoposta a rendering.

 

## <a name="restrict-the-use-of-flush"></a>Limitare l'uso dello scaricamento

Poiché il [**metodo Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) determina l'elaborazione dei comandi di rendering in batch, è consigliabile non usarli. Per gli scenari più comuni, lasciare la gestione delle risorse su Direct2D.

## <a name="bitmaps"></a>Bitmap

Come accennato in precedenza, la creazione e l'eliminazione delle risorse sono operazioni molto costose nell'hardware. Una bitmap è un tipo di risorsa usata spesso. La creazione di bitmap nella scheda video è costosa. Il riutilizzo può contribuire a rendere l'applicazione più veloce.

### <a name="create-large-bitmaps"></a>Creare bitmap di grandi dimensioni

Le schede video hanno in genere una dimensione minima di allocazione di memoria. Se viene richiesta un'allocazione inferiore a questa, viene allocata una risorsa di queste dimensioni minime e la memoria in eccesso viene sprecata e non disponibile per altri elementi. Se sono necessarie molte bitmap di piccole dimensioni, una tecnica migliore consiste nell'allocare una bitmap di grandi dimensioni e archiviare tutto il contenuto della bitmap di piccole dimensioni in questa bitmap di grandi dimensioni. È quindi possibile leggere le sottoaree della bitmap più grande in cui sono necessarie le bitmap più piccole. Spesso, è necessario includere la spaziatura interna (pixel neri trasparenti) tra le bitmap di piccole dimensioni per evitare qualsiasi interazione tra le immagini più piccole durante le operazioni. Questa operazione è nota anche come *atlas* e offre il vantaggio di ridurre il sovraccarico della creazione di bitmap e lo spreco di memoria di piccole allocazioni di bitmap. È consigliabile mantenere la maggior parte delle bitmap ad almeno 64 KB e limitare il numero di bitmap inferiori a 4 KB.

### <a name="create-an-atlas-of-bitmaps"></a>Creare un at atlas di bitmap

Esistono alcuni scenari comuni per i quali un at atlas bitmap può essere molto utile. Le bitmap di piccole dimensioni possono essere archiviate all'interno di una bitmap di grandi dimensioni. Queste bitmap di piccole dimensioni possono essere estrarte dalla bitmap più grande quando sono necessarie specificando il rettangolo di destinazione. Ad esempio, un'applicazione deve disegnare più icone. Tutte le bitmap associate alle icone possono essere caricate in anticipo in una bitmap di grandi dimensioni. E in fase di rendering, possono essere recuperati dalla bitmap di grandi dimensioni.

> [!Note]  
> Una bitmap Direct2D creata nella memoria video è limitata alle dimensioni massime della bitmap supportate dalla scheda in cui è archiviata. La creazione di una bitmap di dimensioni maggiori di potrebbe causare un errore.

 

> [!Note]  
> A partire Windows 8, Direct2D include un [effetto Atlas](atlas.md) che può semplificare questo processo.

 

### <a name="create-shared-bitmaps"></a>Creare bitmap condivise

La creazione di bitmap condivise consente ai chiamanti avanzati di creare oggetti bitmap Direct2D supportati direttamente da un oggetto esistente, già compatibile con la destinazione di rendering. In questo modo si evita la creazione di più superfici e si riduce il sovraccarico delle prestazioni.

> [!Note]  
> Le bitmap condivise sono in genere limitate alle destinazioni software o alle destinazioni interoperabili con DXGI. Usare i [**metodi CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)), [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))e [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) per creare bitmap condivise.

 

### <a name="copying-bitmaps"></a>Copia di bitmap

La creazione di una superficie DXGI è un'operazione costosa, quindi riutilizzare le superfici esistenti quando possibile. Anche nel software, se una bitmap è principalmente nel formato desiderato, ad eccezione di una piccola parte, è meglio aggiornare tale parte anziché eliminare l'intera bitmap e creare nuovamente tutto. Sebbene sia possibile usare [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) per ottenere gli stessi risultati, il rendering è in genere un'operazione molto più costosa rispetto alla copia. Questo perché, per migliorare la posizione della cache, l'hardware non archivia effettivamente una bitmap nello stesso ordine di memoria a cui è indirizzata la bitmap. Al contrario, la bitmap potrebbe essere swizzle. Lo swizzling è nascosto dalla CPU dal driver (che è lento e usato solo nelle parti di fascia inferiore) o dal gestore di memoria nella GPU. A causa dei vincoli sul modo in cui i dati vengono scritti in una destinazione di rendering durante il rendering, le destinazioni di rendering non vengono in genere swizzle o swizzle in modo che sia meno ottimale di quanto sia possibile ottenere se si sa che non è mai necessario eseguire il rendering sulla superficie. Di conseguenza, i [metodi CopyFrom](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap) \* vengono forniti per copiare rettangoli da un'origine alla bitmap Direct2D.

CopyFrom può essere usato in uno dei tre formati seguenti:

-   [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)
-   [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)

## <a name="use-tiled-bitmap-over-dashing"></a>Usare una bitmap affiancata al trattino

Il rendering di una linea tratteggiata è un'operazione molto costosa a causa della qualità e dell'accuratezza elevate dell'algoritmo sottostante. Per la maggior parte dei casi in cui non sono coinvolte geometrie rectilineari, lo stesso effetto può essere generato più velocemente usando bitmap affiancate.

## <a name="general-guidelines-for-rendering-complex-static-content"></a>Linee guida generali per il rendering di contenuto statico complesso

Memorizzare nella cache il contenuto se si esegue il rendering dello stesso frame di contenuto sul fotogramma, soprattutto quando la scena è complessa.

È possibile usare tre tecniche di memorizzazione nella cache:

-   Memorizzazione nella cache della scena completa con una bitmap a colori.
-   Memorizzazione nella cache per primitiva usando una bitmap A8 e [**il metodo FillOpacityMask.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f))
-   Memorizzazione nella cache per primitiva tramite realizzazioni geometriche.

Diamo un'occhiata a ognuno di questi elementi in modo più dettagliato.

### <a name="full-scene-caching-using-a-color-bitmap"></a>Memorizzazione nella cache della scena completa con una bitmap a colori

Quando si esegue il rendering di contenuto statico, in scenari come l'animazione creare un'altra bitmap a colori invece di scrivere direttamente nella bitmap dello schermo. Salvare la destinazione corrente, impostare la destinazione sulla bitmap intermedia ed eseguire il rendering del contenuto statico. Tornare quindi alla bitmap dello schermo originale e disegnare la bitmap intermedia su di essa.

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



Questo esempio usa bitmap intermedie per la memorizzazione nella cache e cambia la bitmap a cui punta il contesto di dispositivo durante il rendering. In questo modo si evita la necessità di creare una destinazione di rendering compatibile per lo stesso scopo.

### <a name="per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method"></a>Memorizzazione nella cache per primitiva con una bitmap A8 e il metodo FillOpacityMask

Quando la scena completa non è statica, ma è costituita da elementi come geometry o text statici, è possibile usare una tecnica di memorizzazione nella cache per primitiva. Questa tecnica mantiene le caratteristiche di anti-aliasing della primitiva memorizzata nella cache e funziona con la modifica dei tipi di pennello. Usa una bitmap A8 dove A8 è un tipo di formato pixel che rappresenta un canale alfa con 8 bit. Le bitmap A8 sono utili per disegnare geometria/testo come maschera. Quando è necessario modificare l'opacità del contenuto statico, anziché modificare il contenuto stesso, è possibile traslare, ruotare, inclinare o ridimensionare l'opacità della maschera.

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



## <a name="per-primitive-caching-using-geometry-realizations"></a>Memorizzazione nella cache per primitiva con realizzazioni geometriche

Un'altra tecnica di memorizzazione nella cache per primitiva, denominata realizzazioni geometriche, offre maggiore flessibilità quando si lavora con la geometria. Quando si desidera disegnare ripetutamente geometrie con alias o con anti-aliasing, è più veloce convertirle in realizzazioni geometriche e disegnare ripetutamente le realizzazioni rispetto al disegno ripetuto delle geometrie stesse. Le realizzazioni di geometria in genere utilizzano anche meno memoria rispetto alle maschere di opacità (soprattutto per geometrie di grandi dimensioni) e sono meno sensibili ai cambiamenti di scala. Per altre informazioni, vedere [Cenni preliminari sulle realizzazioni di geometria.](geometry-realizations-overview.md)

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



## <a name="geometry-rendering"></a>Rendering delle geometrie

### <a name="use-specific-draw-primitive-over-draw-geometry"></a>Usare una primitiva di disegno specifica sulla geometria di disegno

Usare chiamate *primitive di disegno* più specifiche, [**ad esempio DrawRectangle,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) [**su chiamate DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) generiche. Ciò è dovuto al fatto **che con DrawRectangle** la geometria è già nota, quindi il rendering è più veloce.

### <a name="rendering-static-geometry"></a>Rendering della geometria statica

Negli scenari in cui la geometria è statica, usare le tecniche di memorizzazione nella cache per primitiva illustrate in precedenza. Le maschere di opacità e le realizzazioni geometriche possono migliorare notevolmente la velocità di rendering delle scene che contengono geometria statica.

### <a name="use-a-multithreaded-device-context"></a>Usare un contesto di dispositivo multithreading

Le applicazioni che prevedono di eseguire il rendering di quantità significative di contenuto geometrico complesso devono considerare la possibilità di specificare il flag [**D2D1 \_ DEVICE CONTEXT OPTIONS ENABLE MULTI \_ \_ \_ \_ \_ THREADED \_ OPTIMIZATIONS**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options) durante la creazione di un contesto di dispositivo [Direct2D.](./direct2d-portal.md) Quando questo flag viene specificato, Direct2D distribuirà il rendering tra tutti i core logici presenti nel sistema, con una riduzione significativa del tempo di rendering complessivo.

Note:

-   Al Windows 8.1, questo flag influisce solo sul rendering della geometria del tracciato. Non ha alcun impatto sulle scene contenenti solo altri tipi primitivi(ad esempio testo, bitmap o realizzazioni di geometria).
-   Questo flag non ha alcun impatto anche durante il rendering nel software, ad esempio quando si esegue il rendering con un dispositivo Direct3D WARP. Per controllare il multithreading software, i chiamanti devono usare il flag D3D11 CREATE DEVICE PREVENT INTERNAL THREADING OPTIMIZATIONS durante la creazione del \_ \_ dispositivo \_ \_ \_ \_ Direct3D WARP.
-   La specifica di questo flag può aumentare i picchi working set durante il rendering e può anche aumentare la contentione dei thread nelle applicazioni che sfruttano già l'elaborazione multithreading.

## <a name="drawing-text-with-direct2d"></a>Disegno di testo con Direct2D

La funzionalità di rendering del testo Direct2D è disponibile in due parti. La prima parte, esposta come [**metodo ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e [**ID2D1RenderTarget::D rawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) consente a un chiamante di passare una stringa e i parametri di formattazione o un oggetto layout di testo DWrite per più formati. Deve essere adatto per la maggior parte dei chiamanti. Il secondo modo per eseguire il rendering del testo, esposto come metodo [**ID2D1RenderTarget::D rawGlyphRun,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) fornisce la rasterizzazione per i clienti che conoscono già la posizione dei glifi di cui eseguire il rendering. Le due regole generali seguenti consentono di migliorare le prestazioni del testo durante il disegno in Direct2D.

### <a name="drawtextlayout-vs-drawtext"></a>Confronto tra DrawTextLayout e DrawText

Sia [**DrawText che**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [**DrawTextLayout consentono**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) a un'applicazione di eseguire facilmente il rendering del testo formattato dall'API [DirectWrite.](/windows/desktop/DirectWrite/direct-write-portal) **DrawTextLayout** disegna un oggetto [**DWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) esistente in [**RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)e **DrawText** costruisce un layout DirectWrite per il chiamante, in base ai parametri passati. Se è necessario eseguire più volte il rendering dello stesso testo, usare **DrawTextLayout** anziché **DrawText**, perché **DrawText** crea un layout ogni volta che viene chiamato.

### <a name="choosing-the-right-text-rendering-mode"></a>Scelta della modalità di rendering del testo più a destra

Impostare la modalità antialias di testo su [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE \_ GRAYSCALE in modo**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) esplicito. La qualità del rendering del testo in scala di grigi è paragonabile a ClearType, ma è molto più veloce.

### <a name="caching"></a>Memorizzazione nella cache

Usa la memorizzazione nella cache della scena completa o per ogni bitmap primitiva, ad esempio con il disegno di altre primitive.

## <a name="clipping-an-arbitrary-shape"></a>Ritaglio di una forma arbitraria

La figura seguente mostra il risultato dell'applicazione di un clip a un'immagine.

![immagine che mostra un esempio di immagine prima e dopo un clip.](images/clip.png)

È possibile ottenere questo risultato usando i livelli con una maschera geometrica o il [**metodo FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello di opacità.

Ecco un esempio che usa un livello:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Ecco un esempio che usa il [**metodo FillGeometry:**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)


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



In questo esempio di codice, quando si chiama il metodo PushLayer, non si passa un livello creato dall'app. Direct2D crea automaticamente un livello. Direct2D è in grado di gestire l'allocazione e la distruzione di questa risorsa senza alcun intervento da parte dell'app. In questo modo Direct2D può riutilizzare i livelli internamente e applicare le ottimizzazioni di gestione delle risorse.

In Windows 8 sono state apportate molte ottimizzazioni all'utilizzo dei livelli ed è consigliabile provare a usare le API del livello anziché [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) quando possibile.

### <a name="pushlayer-in-windows-8"></a>PushLayer in Windows 8

[**L'interfaccia ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) deriva dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) ed è fondamentale per visualizzare il contenuto Direct2D in Windows 8. Per altre informazioni su questa interfaccia, vedere [Dispositivi](devices-and-device-contexts.md)e contesti di dispositivo. Con l'interfaccia del contesto di dispositivo, è possibile ignorare la chiamata al metodo [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e quindi passare NULL al metodo [**ID2D1DeviceContext::P ushLayer.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) Direct2D gestisce automaticamente la risorsa livello e può condividere le risorse tra i livelli e i grafici degli effetti.

### <a name="axis-aligned-clips"></a>Clip allineate all'asse

Se l'area da ritagliare è allineata all'asse della superficie di disegno, anziché arbitraria. Questo caso è adatto per l'uso di un rettangolo di ritaglio anziché di un livello. Il miglioramento delle prestazioni è maggiore per la geometria con alias rispetto alla geometria con antialias. Per altre informazioni sulle clip allineate all'asse, vedi [**l'argomento PushAxisAlignedClip.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))

## <a name="dxgi-interoperability-avoid-frequent-switches"></a>Interoperabilità DXGI: evitare commutatori frequenti

Direct2D può interagire senza problemi con le superfici Direct3D. Ciò è molto utile per la creazione di applicazioni che eseguono il rendering di una combinazione di contenuto 2D e 3D. Tuttavia, ogni passaggio tra il disegno di contenuto Direct2D e Direct3D influisce sulle prestazioni.

Quando si esegue il rendering su una superficie DXGI, Direct2D salva lo stato dei dispositivi Direct3D durante il rendering e lo ripristina al termine del rendering. Ogni volta che viene completato un batch di rendering Direct2D, vengono pagato il costo di questo salvataggio e ripristino e il costo dello scaricamento di tutte le operazioni 2D, ma il dispositivo Direct3D non viene scaricato. Pertanto, per migliorare le prestazioni, limitare il numero di commutatori di rendering tra Direct2D e Direct3D.

## <a name="know-your-pixel-format"></a>Conoscere il formato pixel

Quando si crea una destinazione di rendering, è possibile usare la struttura [**D2D1 \_ PIXEL \_ FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) per specificare il formato pixel e la modalità alfa usati dalla destinazione di rendering. Un canale alfa fa parte del formato pixel che specifica il valore di copertura o le informazioni sull'opacità. Se una destinazione di rendering non usa il canale alfa, deve essere creata usando la modalità [**alfa D2D1 \_ ALPHA MODE \_ \_ IGNORE.**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Ciò consente di risparmiare il tempo impiegato per il rendering di un canale alfa che non è necessario.

Per altre informazioni sui formati pixel e sulle modalità alfa, vedere [Formati di pixel e modalità alfa supportati.](supported-pixel-formats-and-alpha-modes.md)

## <a name="scene-complexity"></a>Complessità della scena

Quando si analizzano le aree sensibili delle prestazioni in una scena di cui verrà eseguito il rendering, sapere se la scena è associata alla velocità di riempimento o al vertice può fornire informazioni utili.

-   Frequenza di riempimento: la velocità di riempimento si riferisce al numero di pixel di cui una scheda grafica può eseguire il rendering e la scrittura nella memoria video al secondo.
-   Vertex Bound (Limite vertice): una scena è associata a vertici quando contiene molte geometrie complesse.

### <a name="understand-scene-complexity"></a>Informazioni sulla complessità della scena

È possibile analizzare la complessità della scena modificando le dimensioni della destinazione di rendering. Se i miglioramenti delle prestazioni sono visibili per una riduzione proporzionale delle dimensioni della destinazione di rendering, l'applicazione è associata alla velocità di riempimento. In caso contrario, la complessità della scena è il collo di bottiglia delle prestazioni.

Quando una scena è associata alla velocità di riempimento, la riduzione delle dimensioni della destinazione di rendering può migliorare le prestazioni. Questo perché il numero di pixel di cui eseguire il rendering verrà ridotto proporzionalmente con le dimensioni della destinazione di rendering.

Quando una scena è associata a vertici, ridurre la complessità della geometria. Tenere tuttavia presente che questa operazione viene eseguita a scapito della qualità dell'immagine. Pertanto, è necessario prendere un attento compromesso tra la qualità desiderata e le prestazioni necessarie.

## <a name="improving-performance-for-direct2d-printing-apps"></a>Miglioramento delle prestazioni per le app di stampa Direct2D

[Direct2D offre](./direct2d-portal.md) compatibilità con la stampa. È possibile inviare gli stessi comandi di disegno Direct2D (sotto forma di elenchi di comandi Direct2D) al controllo di stampa Direct2D per la stampa, se non si conoscono i dispositivi in cui si sta disegnando o come il disegno viene convertito in stampa.

È possibile ottimizzare ulteriormente l'utilizzo del controllo di stampa [Direct2D](./direct2d-portal.md) e dei comandi di disegno Direct2D per ottenere risultati di stampa con prestazioni migliori.

Il controllo di stampa [Direct2D](./direct2d-portal.md) restituisce messaggi di debug quando viene visualizzato un modello di codice Direct2D che comporta una qualità di stampa o prestazioni inferiori (ad esempio, i modelli di codice elencati più avanti in questo argomento) per ricordare dove è possibile evitare problemi di prestazioni. Per visualizzare questi messaggi di debug, è necessario abilitare [il livello di debug Direct2D](direct2ddebuglayer-portal.md) nel codice. Per [istruzioni su come abilitare l'output](direct2ddebuglayer-debugmessages.md) dei messaggi di debug, vedere Messaggi di debug.

### <a name="set-the-right-property-values-when-you-create-the-d2d-print-control"></a>Impostare i valori delle proprietà appropriati quando si crea il controllo di stampa D2D

Quando si crea il controllo di stampa [Direct2D,](./direct2d-portal.md) è possibile impostare tre proprietà. Due di queste proprietà influiscono sul modo in cui il controllo di stampa Direct2D gestisce determinati comandi Direct2D e, a sua volta, influiscono sulle prestazioni complessive.

-   Modalità subset di tipi di carattere: il controllo di stampa [Direct2D](./direct2d-portal.md) consente di creare subset di risorse dei tipi di carattere usate in ogni pagina prima di inviare la pagina da stampare. Questa modalità riduce le dimensioni delle risorse di pagina necessarie per la stampa. A seconda dell'utilizzo del tipo di carattere nella pagina, è possibile scegliere diverse modalità di subset dei tipi di carattere per ottenere prestazioni ottimali.
    -   [**D2D1 \_ PRINT \_ FONT SUBSET MODE DEFAULT \_ \_ \_ offre**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) le migliori prestazioni di stampa nella maggior parte dei casi. Se impostato su questa modalità, il controllo di stampa [Direct2D](./direct2d-portal.md) usa una strategia euristica per decidere quando creare un subset dei tipi di carattere.
    -   Per i processi di stampa brevi con 1 o 2 pagine, è consigliabile usare [**D2D1 \_ PRINT FONT SUBSET MODE \_ \_ \_ \_ EACHPAGE,**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) in cui il controllo di stampa [Direct2D](./direct2d-portal.md) consente di creare subset e incorporare le risorse dei tipi di carattere in ogni pagina, quindi rimuove tale subset di caratteri dopo la stampa della pagina. Questa opzione garantisce che ogni pagina possa essere stampata immediatamente dopo la generazione, ma aumenta leggermente le dimensioni delle risorse di pagina necessarie per la stampa (con in genere subset di caratteri di grandi dimensioni).
    -   Per i processi di stampa con molte pagine di testo e caratteri di piccole dimensioni (ad esempio 100 pagine di testo che usa un singolo tipo di carattere), è consigliabile usare [**D2D1 \_ PRINT FONT SUBSET MODE \_ \_ \_ \_ NONE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode), in cui il controllo di stampa [Direct2D](./direct2d-portal.md) non crea alcun subset delle risorse del tipo di carattere, ma invia le risorse del tipo di carattere originali insieme alla pagina che usa prima il tipo di carattere e usa nuovamente le risorse del tipo di carattere per le pagine successive senza inviarle nuovamente.
-   DPI di rasterizzazione: quando il controllo di stampa [Direct2D](./direct2d-portal.md) deve rasterizzare i comandi Direct2D durante la conversione Direct2D-XPS, usa questo valore DPI per la rasterizzazione. In altre parole, se la pagina non ha contenuto rasterizzato, l'impostazione di un valore DPI non modificherà le prestazioni e la qualità. A seconda dell'utilizzo della rasterizzazione nella pagina, è possibile scegliere DPI di rasterizzazione diversi per ottenere il miglior equilibrio tra fedeltà e prestazioni.
    -   150 è il valore predefinito se non si specifica un valore quando si crea il controllo di stampa [Direct2D,](./direct2d-portal.md) che rappresenta il miglior equilibrio tra qualità di stampa e prestazioni di stampa nella maggior parte dei casi.
    -   Valori DPI più elevati comportano in genere una migliore qualità di stampa (come in altri dettagli conservati), ma prestazioni inferiori a causa delle bitmap più grandi generate. Non è consigliabile usare valori DPI maggiori di 300 perché non introducono informazioni aggiuntive visivamente percepibili dagli occhi umani.
    -   Un valore DPI inferiore può significare prestazioni migliori, ma può anche produrre una qualità inferiore.

### <a name="avoid-using-certain-direct2d-drawing-patterns"></a>Evitare di usare determinati modelli di disegno Direct2D

Esistono differenze tra ciò che [Direct2D](./direct2d-portal.md) può rappresentare visivamente e ciò che il sottosistema di stampa può gestire e trasportare lungo l'intera pipeline di stampa. Il controllo di stampa Direct2D colma tali lacune approssimando o rasterizzando primitive Direct2D non supportate dal sottosistema di stampa in modo nativo. Tale approssimazione comporta in genere una fedeltà di stampa inferiore, prestazioni di stampa inferiori o entrambe. Pertanto, anche se un cliente può usare gli stessi modelli di disegno per il rendering dello schermo e di stampa, non è ideale in tutti i casi. È meglio non usare le primitive e i modelli Direct2D il più possibile per il percorso di stampa o la rasterizzazione in cui si ha il controllo completo della qualità e delle dimensioni delle immagini rasterizzate.

Di seguito è riportato un elenco di casi in cui le prestazioni e la qualità di stampa non saranno ideali e potrebbe essere necessario prendere in considerazione la possibilità di variare il percorso del codice per ottenere prestazioni di stampa ottimali.

-   Evitare di usare la modalità blend primitiva diversa da [**D2D1 \_ PRIMITIVE \_ BLEND \_ SOURCEOVER.**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)
-   Evitare di usare le modalità di composizione quando si disegna un'immagine diversa da [**D2D1 \_ COMPOSITE MODE SOURCE \_ \_ \_ OVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) e **D2D1 \_ COMPOSITE MODE DESTINATION \_ \_ \_ OVER**.
-   Evitare di disegnare un metafile GDI.
-   Evitare di eseguire il push di una risorsa di livello che copia lo sfondo di origine (chiamando [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) passando [**D2D1 \_ LAYER \_ OPTIONS1 \_ INITIALIZE FROM \_ \_ BACKGROUND**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) allo struct **D2D1 \_ LAYER \_ PARAMETERS1).**
-   Evitare di creare un pennello bitmap o un pennello immagine con \_ CLAMP D2D1 EXTEND \_ \_ MODE. È consigliabile usare D2D1 EXTEND MODE MIRROR se non si è interessati ai pixel \_ \_ \_ all'esterno dell'immagine associata (ad esempio, l'immagine collegata al pennello è nota come più grande dell'area di destinazione riempita).
-   Evitare di disegnare bitmap con [trasformazioni prospettica.](3d-perspective-transform.md)

### <a name="draw-text-in-a-direct-and-plain-way"></a>Disegnare testo in modo diretto e semplice

Direct2D include diverse ottimizzazioni per il rendering dei testi da visualizzare per ottenere prestazioni migliori e/o una migliore qualità visiva. Tuttavia, non tutte le ottimizzazioni migliorano le prestazioni e la qualità della stampa poiché la stampa su carta è in genere in un valore DPI molto più elevato e non è necessario che la stampa supporti scenari come l'animazione. È quindi consigliabile disegnare direttamente il testo o i glifi originali ed evitare le ottimizzazioni seguenti durante la creazione dell'elenco di comandi per la stampa.

-   Evitare di disegnare testo con [**il metodo FillOpacityMask.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask)
-   Evitare di disegnare testo in modalità con alias.

### <a name="draw-the-original-bitmaps-when-possible"></a>Disegnare le bitmap originali quando possibile

Se la bitmap di destinazione è jpeg, PNG, TIFF o JPEG-XR, è possibile creare una bitmap WIC da un file su disco o da un flusso in memoria, quindi creare una bitmap [Direct2D](./direct2d-portal.md) da tale bitmap WIC usando [**ID2D1DeviceContext::CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))e infine passare direttamente tale bitmap Direct2D al controllo di stampa Direct2D senza ulteriori modifiche. In questo modo, il controllo di stampa Direct2D è in grado di riutilizzare il flusso bitmap, che in genere comporta prestazioni di stampa migliori (ignorando la codifica e la decodifica ridondante delle bitmap) e una migliore qualità di stampa (quando i metadati, ad esempio i profili colori, nella bitmap vengono mantenuti).

Il disegno della bitmap originale offre i vantaggi seguenti per le applicazioni.

-   In generale, la stampa [Direct2D](./direct2d-portal.md) mantiene le informazioni originali (senza perdita o rumore) fino alla fine della pipeline, soprattutto quando le app non conoscono (o non vogliono conoscere) i dettagli della pipeline di stampa (ad esempio la stampante in cui viene stampata, il valore DPI della stampante di destinazione e così via).
-   In molti casi, il ritardo della rasterizzazione delle bitmap comporta prestazioni migliori, ad esempio quando si stampa una foto a 96dpi su una stampante a 600dpi.
-   In alcuni casi, il passaggio delle immagini originali è l'unico modo per rispettare l'alta fedeltà ,ad esempio i profili colori incorporati.

Tuttavia, non è possibile acconsentire esplicitamente a tale ottimizzazione perché:

-   Tramite l'esecuzione di query sulle informazioni della stampante e la rasterizzazione anticipata, è possibile rasterizzare il contenuto con il controllo completo dell'aspetto finale sulla carta.
-   In alcuni casi, la rasterizzazione anticipata potrebbe effettivamente migliorare le prestazioni end-to-end di un'app, ad esempio la stampa di foto di portafoglio di dimensioni elevate.
-   In alcuni casi, il passaggio delle bitmap originali richiede una modifica significativa dell'architettura del codice esistente, ad esempio il caricamento ritardato delle immagini e i percorsi di aggiornamento delle risorse trovati in determinate applicazioni.

## <a name="conclusion"></a>Conclusione

Anche se Direct2D è accelerato dall'hardware e ha lo scopo di ottenere prestazioni elevate, è necessario usare correttamente le funzionalità per ottimizzare la velocità effettiva. Le tecniche qui illustrate derivano dallo studio di scenari comuni e potrebbero non essere applicabili a tutti gli scenari applicativi.

 

 
