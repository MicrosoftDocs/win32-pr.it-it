---
title: Rendering del testo con Direct2D e DirectWrite
description: A differenza di altre API, ad esempio GDI, GDI+ o WPF, Direct2D interagisce con un'altra API, DirectWrite, per modificare ed eseguire il rendering del testo. In questo argomento vengono descritti i vantaggi e l'interoperabilità di questi componenti separati.
ms.assetid: 1d5b8deb-34e2-433c-8de3-4ef66fb4e49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c49a8f341377bcf78a9a99699a3bd4852411dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104560308"
---
# <a name="text-rendering-with-direct2d-and-directwrite"></a>Rendering del testo con Direct2D e DirectWrite

A differenza di altre API, ad esempio [GDI](/windows/desktop/gdi/windows-gdi), GDI+ o WPF, [Direct2D](./direct2d-portal.md) interagisce con un'altra API, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), per modificare ed eseguire il rendering del testo. In questo argomento vengono descritti i vantaggi e l'interoperabilità di questi componenti separati.

In questo argomento sono contenute le sezioni seguenti.

-   [Direct2D consente l'adozione incrementale](#direct2d-enables-incremental-adoption)
-   [Servizi di testo rispetto al rendering del testo](#text-services-versus-text-rendering)
-   [Glifi e testo](#glyphs-versus-text)
-   [DirectWrite e Direct2D](#directwrite-and-direct2d)
    -   [DrawText](#drawtextlayout)
    -   [DrawTextLayout](#drawtextlayout)
    -   [DrawGlyphRun](#drawglyphrun)
-   [Rendering del glifo](#glyph-rendering)
-   [Conclusione](#conclusion)

## <a name="direct2d-enables-incremental-adoption"></a>Direct2D consente l'adozione incrementale

Lo stato di un'applicazione da un'API grafica a un'altra può essere difficile o non quello che si desidera per diversi motivi. Questo potrebbe essere dovuto al fatto che è necessario supportare i plug-in che accettano ancora le interfacce precedenti, perché l'applicazione stessa è troppo grande per il trasferimento a una nuova API in un'unica versione o perché è auspicabile una parte dell'API più recente, ma l'API precedente funziona correttamente per altre parti dell'applicazione.

Poiché [Direct2D](./direct2d-portal.md) e [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) vengono implementati come componenti distinti, è possibile aggiornare l'intero sistema grafico 2D o solo la parte di testo. Ad esempio, è possibile aggiornare un'applicazione per usare DirectWrite per il testo, ma usare comunque [GDI](/windows/desktop/gdi/windows-gdi) o GDI+ per il rendering.

## <a name="text-services-versus-text-rendering"></a>Servizi di testo rispetto al rendering del testo

Man mano che le applicazioni si sono evolute, i requisiti di elaborazione del testo sono diventati sempre più complessi. Inizialmente, il testo era generalmente limitato all'interfaccia utente con layout statico ed era stato eseguito il rendering del testo in una casella ben definita, ad esempio un pulsante. Poiché le applicazioni iniziavano a essere disponibili in un numero crescente di lingue, questo approccio diventava più difficile da sostenere poiché la larghezza e l'altezza del testo tradotto possono variare significativamente tra le lingue. Per adattarsi, le applicazioni avviate per la disposizione dinamica dell'interfaccia utente in base alle dimensioni effettive di cui è stato eseguito il rendering del testo, anziché viceversa.

Per consentire alle applicazioni di completare questa attività, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) fornisce l'interfaccia [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) . Questa API consente a un'applicazione di specificare una porzione di testo con caratteristiche complesse, ad esempio tipi di carattere e dimensioni dei caratteri diversi, sottolineature, strikethroughs, testo bidirezionale, effetti, puntini di sospensione e caratteri non glifi incorporati (ad esempio un'emoticon bitmap o un'icona). L'applicazione può quindi modificare varie caratteristiche del testo in modo iterativo per determinare il layout dell'interfaccia utente. L' [esempio DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples), illustrato nella figura seguente e nell'argomento [esercitazione: introduzione con DirectWrite](/windows/desktop/DirectWrite/getting-started-with-directwrite) , Mostra molti di questi effetti.

![screenshot dell'esempio "Hello World".](images/dwrite-hello-world.png)

Il layout può posizionare i glifi idealmente in base alla larghezza (come avviene in WPF) oppure può bloccare i glifi nelle posizioni dei pixel più vicine (come avviene con [GDI](/windows/desktop/gdi/windows-gdi) ).

Oltre a ottenere le misurazioni del testo, l'applicazione può eseguire il test di varie parti del testo. È ad esempio possibile fare clic su un collegamento ipertestuale nel testo. Per ulteriori informazioni sugli hit testing, vedere l'argomento [How to perform hit testing on a text layout](/windows/desktop/DirectWrite/how-to-perform-hit-testing-on-a-text-layout) .

L'interfaccia di layout del testo è disaccoppiata dall'API di rendering utilizzata dall'applicazione, come illustrato nel diagramma seguente:

![diagramma del layout del testo e dell'API grafica.](images/direct2d-directwrite1.png)

Questa separazione è possibile perché DirectWrite offre un'interfaccia di rendering ([**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)) che le applicazioni possono implementare per eseguire il rendering del testo usando qualsiasi API grafica desiderata. L'applicazione ha implementato [**IDWriteTextRenderer::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) metodo di callback viene chiamato da DirectWrite durante il rendering di un layout di testo. È responsabilità di questo metodo eseguire le operazioni di disegno o passarle insieme.

Per il disegno di glifi, [Direct2D](./direct2d-portal.md) fornisce [**ID2D1RenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) per il disegno a una superficie Direct2D e [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) fornisce [**IDWriteBitmapRenderTarget::D RAWGLYPHRUN**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) per il disegno su una superficie GDI che può quindi essere trasferita a una finestra utilizzando GDI. In modo appropriato, **DrawGlyphRun** in Direct2D e DirectWrite hanno parametri esattamente compatibili con il metodo [**DrawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) implementato dall'applicazione in [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer).

Dopo una separazione simile, le funzionalità specifiche del testo, ad esempio l'enumerazione e la gestione dei tipi di carattere, l'analisi dei glifi e così via, vengono gestite da [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) anziché [Direct2D](./direct2d-portal.md). Gli oggetti DirectWrite sono accettati direttamente da Direct2D. Per consentire alle applicazioni GDI esistenti di sfruttare i vantaggi di DirectWrite, fornisce l'interfaccia del metodo [**IDWriteGdiInterop**](/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop) con i metodi per eseguire le operazioni seguenti:

-   Creare un tipo di carattere [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) da un tipo di carattere logico [GDI](/windows/desktop/gdi/windows-gdi) ([**CreateFontFromLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)).
-   Eseguire la conversione da un tipo di carattere [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) a un tipo di carattere logico [GDI](/windows/desktop/gdi/windows-gdi) ([**ConvertFontFaceToLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)).
-   Recuperare il tipo di carattere [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) da quello selezionato in un HDC. ([**CreateFontFaceFromHdc**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc))
-   Creare una [](/windows/desktop/DirectWrite/direct-write-portal) [**destinazione di rendering bitmap**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) DirectWrite in memoria di sistema ([**CreateBitmapRenderTarget**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)).

## <a name="glyphs-versus-text"></a>Glifi e testo

Il testo è un set di punti di codice Unicode (caratteri), con vari modificatori stilistici (tipi di carattere, pesi, sottolineature, strikethroughs e così via) disposti in un rettangolo. Un glifo, al contrario, è un indice specifico in un file del tipo di carattere specifico. Un glifo definisce un set di curve di cui è possibile eseguire il rendering, ma non ha alcun significato testuale. Esiste potenzialmente un mapping molti-a-molti tra glifi e caratteri. Una sequenza di glifi che provengono dallo stesso tipo di carattere e che sono disposti in sequenza su una linea di base è denominata [GlyphRun](/windows/desktop/DirectWrite/glyphs-and-glyph-runs). Sia [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) che [DIRECT2D](./direct2d-portal.md) chiamano l'API per il rendering del glifo più precisa [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) e hanno firme molto simili. Di seguito viene riportato da [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) in Direct2D:


```
STDMETHOD_(void, DrawGlyphRun)(
        D2D1_POINT_2F baselineOrigin,
        __in CONST DWRITE_GLYPH_RUN *glyphRun,
        __in ID2D1Brush *foregroundBrush,
        DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL 
        ) PURE;
```



Questo metodo viene da [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) in [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal):


```
STDMETHOD(DrawGlyphRun)(
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        IDWriteRenderingParams* renderingParams,
        COLORREF textColor,
        __out_opt RECT* blackBoxRect = NULL
        ) PURE;
```



La versione [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) mantiene l'origine di base, la modalità di misurazione e i parametri di esecuzione del glifo e includono parametri aggiuntivi.

[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) consente inoltre di utilizzare un renderer personalizzato per i glifi implementando l'interfaccia [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) . Questa interfaccia dispone anche di un metodo **DrawGlyphRun** , come illustrato nell'esempio di codice seguente.


```
STDMETHOD(DrawGlyphRun)(
        __maybenull void* clientDrawingContext,
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
        __maybenull IUnknown* clientDrawingEffect
        ) PURE;
```



Questa versione include più parametri che risultano utili quando si implementa un [renderer di testo personalizzato](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer). Il parametro finale viene usato per gli effetti di disegno personalizzati implementati dall'applicazione. Per ulteriori informazioni sugli effetti di disegno dei client [, vedere How to Add client Drawing Effects to a text layout](/windows/desktop/DirectWrite/how-to-add-custom-drawing-efffects-to-a-text-layout).

Ogni operazione di glifo inizia da un'origine e viene posizionata su una riga che inizia da questa origine. I glifi vengono modificati dalla trasformazione globale corrente e dalle impostazioni di rendering del testo selezionate nella destinazione di rendering associata. Questa API viene chiamata in genere direttamente solo da applicazioni che eseguono un layout personalizzato, ad esempio un elaboratore di testo, o da un'applicazione che ha implementato l'interfaccia [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) .

## <a name="directwrite-and-direct2d"></a>DirectWrite e Direct2D

[Direct2D](./direct2d-portal.md) fornisce servizi di rendering a livello di glifo tramite [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Tuttavia, ciò richiede che l'applicazione implementi i dettagli del rendering, che in sostanza riproduce la funzionalità dell'API [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) da GDI.

Pertanto, [Direct2D](./direct2d-portal.md) fornisce API che accettano testo anziché glifi: [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) e [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)). Entrambi i metodi eseguono il rendering in una superficie Direct2D. Per eseguire il rendering in una superficie GDI, viene specificato [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) . Questo metodo richiede tuttavia che l'applicazione implementi un renderer di testo personalizzato. Per ulteriori informazioni, vedere l'argomento [rendering in una superficie GDI](/windows/desktop/DirectWrite/render-to-a-gdi-surface) .

L'utilizzo del testo di un'applicazione viene in genere avviato in modo semplice: inserire **OK** o **Annulla** in un pulsante di layout fisso, ad esempio. Tuttavia, nel tempo, diventa più complesso come internazionalizzazione e vengono aggiunte altre funzionalità. Alla fine, molte applicazioni dovranno usare gli oggetti layout del testo [di DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) e implementare il renderer di testo.

Per questo motivo, [Direct2D](./direct2d-portal.md) fornisce API a più livelli che consentono di avviare un'applicazione in modo semplice e più sofisticato, senza dover eseguire il back-track o abbandonare il codice funzionante. Il diagramma seguente illustra una visualizzazione semplificata:

![diagramma dell'applicazione DirectWrite e Direct2D.](images/direct2d-directwrite2.png)

### <a name="drawtext"></a>DrawText

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) è la più semplice delle API da usare. Accetta una stringa Unicode, un pennello in primo piano, un singolo oggetto Format e un rettangolo di destinazione. Verrà eseguito il layout e il rendering dell'intera stringa all'interno del rettangolo di layout e, facoltativamente, la ritaglio. Questa operazione è utile quando si inserisce una semplice porzione di testo in una parte dell'interfaccia utente con layout fisso.

### <a name="drawtextlayout"></a>DrawTextLayout

Creando un oggetto [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) , un'applicazione può iniziare a misurare e organizzare il testo e altri elementi dell'interfaccia utente e supportare più tipi di carattere, stili, sottolineature e strikethroughs. [Direct2D](./direct2d-portal.md) fornisce l'API [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) che accetta direttamente questo oggetto ed esegue il rendering del testo in un determinato punto. (La larghezza e l'altezza vengono fornite dall'oggetto layout). Oltre a implementare tutte le funzionalità di layout di testo previste, Direct2D interpreta qualsiasi oggetto effetto come pennello e applica tale pennello all'intervallo di glifi selezionato. Chiamerà anche qualsiasi oggetto inline. Un'applicazione può quindi inserire caratteri non di glifo (icone) nel testo se desidera. Un altro vantaggio dell'uso di un oggetto di layout di testo è che le posizioni del glifo vengono memorizzate nella cache. Pertanto, è possibile un notevole miglioramento delle prestazioni riutilizzando lo stesso oggetto layout per più chiamate di disegno e evitando il ricalcolo delle posizioni del glifo per ogni chiamata. Questa funzionalità non è presente per [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))di GDI.

### <a name="drawglyphrun"></a>DrawGlyphRun

Infine, l'applicazione può implementare l'interfaccia [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) e chiamare [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) e [**FILLRECTANGLE**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)) stesso o qualsiasi altra API per il rendering. Tutte le interazioni esistenti con l'oggetto layout di testo rimarranno invariate.

Per un esempio di come implementare un renderer di testo personalizzato, vedere l'argomento [rendering usando un renderer di testo personalizzato](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) .

## <a name="glyph-rendering"></a>Rendering del glifo

L'aggiunta di [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) a un'applicazione GDI esistente consente all'applicazione di usare l'API [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) per eseguire il rendering dei glifi. Il metodo [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) fornito da DirectWrite eseguirà il rendering a tinta unita in un controller di dominio di memoria senza richiedere altre API, ad esempio [Direct2D](./direct2d-portal.md).

Ciò consente all'applicazione di ottenere funzionalità avanzate per il rendering del testo, come le seguenti:

-   Il valore ClearType del sottopixel consente a un'applicazione di inserire glifi sulle posizioni dei subpixel per consentire il rendering del glifo acuto e il layout del glifo.
-   L'anti-aliasing della direzione Y consente un rendering più uniforme delle curve su glifi più grandi.

Un'applicazione che passa a [Direct2D](./direct2d-portal.md) otterrà anche le funzionalità seguenti:

-   Accelerazione hardware.
-   Possibilità di riempire il testo con un pennello [Direct2D](./direct2d-portal.md) arbitrario, ad esempio sfumature radiali, sfumature lineari e bitmap.
-   Maggiore supporto per la suddivisione in livelli e il ritaglio tramite le API [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)), [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) .
-   Possibilità di supportare il rendering del testo in scala di grigi. Questa operazione consente di popolare correttamente il canale alfa di destinazione in base all'opacità del pennello del testo e all'anti-aliasing del testo.

Per supportare in modo efficiente l'accelerazione hardware, [Direct2D](./direct2d-portal.md) usa un'approssimazione leggermente diversa alla correzione gamma denominata *correzione alfa*. Non è necessario che Direct2D controlli il pixel di colore della destinazione di rendering durante il rendering del testo.

## <a name="conclusion"></a>Conclusione

In questo argomento vengono illustrate le differenze e le analogie tra [Direct2D](./direct2d-portal.md) e [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) e le motivazioni dell'architettura per fornirle come API cooperative separate.

 

 