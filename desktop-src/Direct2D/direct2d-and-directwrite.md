---
title: Rendering del testo con Direct2D e DirectWrite
description: A differenza di altre API, ad esempio GDI, GDI+ o WPF, Direct2D interagisce con un'altra API, DirectWrite, per modificare ed eseguire il rendering del testo. In questo argomento vengono descritti i vantaggi e l'interoperabilità di questi componenti separati.
ms.assetid: 1d5b8deb-34e2-433c-8de3-4ef66fb4e49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd95e7644b5f429d4dd91d2276213d5b7ffb92b058d8e530bfcf47fee77fea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698245"
---
# <a name="text-rendering-with-direct2d-and-directwrite"></a>Rendering del testo con Direct2D e DirectWrite

A differenza di altre API, ad esempio [GDI](/windows/desktop/gdi/windows-gdi), GDI+ o WPF, [Direct2D](./direct2d-portal.md) interagisce con un'altra API, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), per modificare ed eseguire il rendering del testo. In questo argomento vengono descritti i vantaggi e l'interoperabilità di questi componenti separati.

In questo argomento sono contenute le sezioni seguenti.

-   [Direct2D consente l'adozione incrementale](#direct2d-enables-incremental-adoption)
-   [Servizi di testo e rendering del testo](#text-services-versus-text-rendering)
-   [Confronto tra glifi e testo](#glyphs-versus-text)
-   [DirectWrite e Direct2D](#directwrite-and-direct2d)
    -   [Drawtext](#drawtextlayout)
    -   [DrawTextLayout](#drawtextlayout)
    -   [DrawGlyphRun](#drawglyphrun)
-   [Rendering del glifo](#glyph-rendering)
-   [Conclusione](#conclusion)

## <a name="direct2d-enables-incremental-adoption"></a>Direct2D consente l'adozione incrementale

Lo spostamento di un'applicazione da un'API grafica a un'altra può essere difficile o meno per vari motivi. Ciò potrebbe essere dovuto al fatto che è necessario supportare plug-in che accettano ancora le interfacce meno recenti, perché l'applicazione stessa è troppo grande per il port over a una nuova API in una versione o perché una parte dell'API più recente è auspicabile, ma l'API precedente funziona abbastanza bene per altre parti dell'applicazione.

Poiché [Direct2D](./direct2d-portal.md) [e DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) sono implementati come componenti separati, è possibile aggiornare l'intero sistema di grafica 2D o solo la parte di testo. Ad esempio, è possibile aggiornare un'applicazione in modo da usare DirectWrite per il testo, ma usare [comunque GDI](/windows/desktop/gdi/windows-gdi) o GDI+ per il rendering.

## <a name="text-services-versus-text-rendering"></a>Servizi di testo e rendering del testo

Con l'evoluzione delle applicazioni, i requisiti di elaborazione del testo sono diventati sempre più complessi. All'inizio, il testo era in genere limitato all'interfaccia utente strutturata in modo statico ed è stato eseguito il rendering del testo in una casella ben definita, ad esempio un pulsante. Poiché le applicazioni iniziavano a essere disponibili in un numero crescente di lingue, questo approccio è diventato più difficile da sostenere perché sia la larghezza che l'altezza del testo tradotto possono variare in modo significativo tra le lingue. Per adattarsi, le applicazioni hanno iniziato a creare dinamicamente il ridimensionare l'interfaccia utente in modo che dipendesse dalle dimensioni effettive di rendering del testo, invece che dall'altra parte.

Per consentire alle applicazioni di completare questa [attività, DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) l'interfaccia [**IDWriteTextLayout.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) Questa API consente a un'applicazione di specificare una parte di testo con caratteristiche complesse, ad esempio tipi di carattere e dimensioni dei caratteri diversi, sottolineature, barrato, testo bidirezionale, effetti, puntini di sospensione e anche caratteri non glifi incorporati (ad esempio un'emoticon bitmap o un'icona). L'applicazione può quindi modificare diverse caratteristiche del testo in quanto ne determina in modo iterativo il layout dell'interfaccia utente. [L DirectWrite Hello World di](/samples/browse/?redirectedfrom=MSDN-samples)esempio , illustrato nella figura seguente e nell'argomento Esercitazione: Attività iniziali [con DirectWrite,](/windows/desktop/DirectWrite/getting-started-with-directwrite) illustra molti di questi effetti.

![screenshot dell'esempio "hello world".](images/dwrite-hello-world.png)

Il layout può posizionare i glifi idealmente in base alla relativa larghezza (come wpf) oppure può allineare i glifi alle posizioni in pixel più vicine (come [GDI).](/windows/desktop/gdi/windows-gdi)

Oltre a ottenere misurazioni del testo, l'applicazione può eseguire l'hit test di varie parti del testo. Ad esempio, potrebbe essere necessario sapere che è stato fatto clic su un collegamento ipertestuale nel testo. Per altre informazioni sull'hit testing, vedere [l'argomento How to Perform Hit Testing on a Text Layout](/windows/desktop/DirectWrite/how-to-perform-hit-testing-on-a-text-layout) .)

L'interfaccia del layout di testo è disaccoccodata dall'API di rendering utilizzata dall'applicazione, come illustrato nel diagramma seguente:

![diagramma dell'API di layout di testo e grafica.](images/direct2d-directwrite1.png)

Questa separazione è possibile perché DirectWrite un'interfaccia di rendering ([**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)) che le applicazioni possono implementare per eseguire il rendering del testo usando qualsiasi API grafica desiderata. L'applicazione ha implementato il metodo di callback [**IDWriteTextRenderer::D rawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) viene chiamato da DirectWrite durante il rendering di un layout di testo. È responsabilità di questo metodo eseguire le operazioni di disegno o passarle.

Per il disegno di glifi, [Direct2D](./direct2d-portal.md) fornisce [**ID2D1RenderTarget::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) per disegnare su una superficie Direct2D e DirectWrite fornisce [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) per il disegno su una superficie GDI che può quindi essere trasferita [a](/windows/desktop/DirectWrite/direct-write-portal) una finestra tramite GDI. **DrawGlyphRun** in Direct2D e DirectWrite ha parametri esattamente compatibili con il metodo [**DrawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) implementato dall'applicazione in [**IDWriteTextRenderer.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)

Dopo una separazione simile, le funzionalità specifiche del testo (ad esempio l'enumerazione e la gestione dei tipi di carattere, l'analisi dei glifi e così via) vengono gestite da [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) invece di [Direct2D.](./direct2d-portal.md) Gli DirectWrite vengono accettati direttamente da Direct2D. Per consentire alle applicazioni GDI esistenti di sfruttare DirectWrite, fornisce l'interfaccia del metodo [**IDWriteGdiInterop**](/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop) con i metodi per eseguire le operazioni seguenti:

-   Creare un [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) carattere da un tipo di [carattere logico GDI](/windows/desktop/gdi/windows-gdi) ([**CreateFontFromLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)).
-   Eseguire la conversione [da DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) tipo di carattere a un tipo di carattere [logico GDI](/windows/desktop/gdi/windows-gdi) ([**ConvertFontFaceToLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)).
-   Recuperare il [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) tipo di carattere da quello selezionato in un HDC. ([**CreateFontFaceFromHdc**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc))
-   Creare una [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) [**di rendering bitmap**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) nella memoria di sistema ([**CreateBitmapRenderTarget**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)).

## <a name="glyphs-versus-text"></a>Confronto tra glifi e testo

Il testo è un set di punti di codice Unicode (caratteri), con vari modificatori stilistici (tipi di carattere, pesi, sottolineature, barrati e così via) disposti in un rettangolo. Un glifo, al contrario, è un indice specifico in un particolare file del tipo di carattere. Un glifo definisce un set di curve di cui è possibile eseguire il rendering, ma che non ha alcun significato testuale. Esiste potenzialmente un mapping molti-a-molti tra glifi e caratteri. Una sequenza di glifi provenienti dalla stessa faccia del carattere e disposti in sequenza su una linea di base è denominata [GlyphRun.](/windows/desktop/DirectWrite/glyphs-and-glyph-runs) Sia [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) che [Direct2D](./direct2d-portal.md) chiamano l'API [**drawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) per il rendering del glifo più precisa e hanno firme molto simili. Di seguito è riportato [**id2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) in Direct2D:


```
STDMETHOD_(void, DrawGlyphRun)(
        D2D1_POINT_2F baselineOrigin,
        __in CONST DWRITE_GLYPH_RUN *glyphRun,
        __in ID2D1Brush *foregroundBrush,
        DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL 
        ) PURE;
```



Questo metodo deriva da [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) in [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal):


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



La [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) precedente mantiene l'origine della baseline, la modalità di misurazione e i parametri di esecuzione del glifo e include parametri aggiuntivi.

[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) consente anche di usare un renderer personalizzato per i glifi implementando [**l'interfaccia IDWriteTextRenderer.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) Questa interfaccia ha anche un **metodo DrawGlyphRun,** come illustrato nell'esempio di codice seguente.


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



Questa versione include più parametri utili quando si implementa un [renderer di testo personalizzato.](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) Il parametro finale viene usato per gli effetti di disegno personalizzati implementati dall'applicazione. Per altre informazioni sugli effetti di disegno client, vedere [How to Add Client Drawing Effects to a Text Layout](/windows/desktop/DirectWrite/how-to-add-custom-drawing-efffects-to-a-text-layout).

Ogni esecuzione del glifo inizia in corrispondenza di un'origine e viene inserita in una riga che inizia da questa origine. I glifi vengono modificati dalla trasformazione del mondo corrente e dalle impostazioni di rendering del testo selezionate nella destinazione di rendering associata. Questa API viene in genere chiamata direttamente solo dalle applicazioni che escrivono il proprio layout (ad esempio, un elaboratore di testo) o da un'applicazione che ha implementato [**l'interfaccia IDWriteTextRenderer.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)

## <a name="directwrite-and-direct2d"></a>DirectWrite e Direct2D

[Direct2D fornisce](./direct2d-portal.md) servizi di rendering a livello di glifo [**tramite DrawGlyphRun.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) Tuttavia, ciò richiede che l'applicazione implementi i dettagli del rendering, che fondamentalmente riproduce la funzionalità dell'API [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) da GDI in modo proprio.

[Direct2D](./direct2d-portal.md) fornisce pertanto API che accettano testo anziché glifi: [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) e [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)). Entrambi i metodi eseguono il rendering su una superficie Direct2D. Per eseguire il rendering in una superficie GDI, viene fornito [**IDWriteBitmapRenderTarget::D rawGlyphRun.**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) Questo metodo richiede tuttavia l'implementazione di un renderer di testo personalizzato da parte dell'applicazione. Per altre informazioni, vedere l'argomento [Eseguire il rendering in una superficie GDI.](/windows/desktop/DirectWrite/render-to-a-gdi-surface)

L'uso del testo da parte di un'applicazione inizia in genere in modo semplice: ad esempio, inserire **OK** o **Annulla** in un pulsante con layout fisso. Tuttavia, nel corso del tempo, diventa più complesso con l'internazionalizzazione e l'aggiunta di altre funzionalità. Alla fine molte applicazioni doranno usare gli [DirectWrite layout](/windows/desktop/DirectWrite/direct-write-portal) di testo e implementare il renderer di testo.

[Direct2D offre quindi](./direct2d-portal.md) API a più livelli che consentono a un'applicazione di iniziare semplicemente e diventare più sofisticata senza dover eseguire il back-track o abbandonare il codice funzionante. Una visualizzazione semplificata è illustrata nel diagramma seguente:

![Diagramma applicazioni directwrite e direct2d.](images/direct2d-directwrite2.png)

### <a name="drawtext"></a>Drawtext

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) è la più semplice delle API da usare. Accetta una stringa Unicode, un pennello in primo piano, un singolo oggetto di formato e un rettangolo di destinazione. Verrà eseguito il layout e il rendering dell'intera stringa all'interno del rettangolo di layout e, facoltativamente, verrà ritagliata. Ciò è utile quando si inserisci una semplice parte di testo in una parte dell'interfaccia utente a layout fisso.

### <a name="drawtextlayout"></a>DrawTextLayout

Creando un oggetto [**IDWriteTextLayout,**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) un'applicazione può iniziare a misurare e disporre il testo e altri elementi dell'interfaccia utente e supportare più tipi di carattere, stili, sottolineature e barrature. [Direct2D fornisce](./direct2d-portal.md) l'API [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) che accetta direttamente questo oggetto ed esegue il rendering del testo in un determinato punto. La larghezza e l'altezza vengono fornite dall'oggetto layout. Oltre a implementare tutte le funzionalità di layout di testo previste, Direct2D interpreterà qualsiasi oggetto effetto come pennello e lo applierà all'intervallo di glifi selezionato. Chiamerà anche tutti gli oggetti inline. Un'applicazione può quindi inserire caratteri non glifi (icone) nel testo, se lo si desidera. Un altro vantaggio dell'uso di un oggetto layout di testo è che le posizioni del glifo vengono memorizzate nella cache. Di conseguenza, è possibile ottenere prestazioni elevate riutilizzando lo stesso oggetto layout per più chiamate di disegno ed evitando di ricalcolare le posizioni dei glifi per ogni chiamata. Questa funzionalità non è presente per [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))di GDI.

### <a name="drawglyphrun"></a>DrawGlyphRun

Infine, l'applicazione può implementare l'interfaccia [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) stessa e chiamare [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) [**e FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)) stesso o qualsiasi altra API di rendering. Tutte le interazioni esistenti con l'oggetto Layout di testo rimarranno invariate.

Per un esempio di come implementare un renderer di testo personalizzato, vedere l'argomento [Rendering con un renderer di testo](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) personalizzato.

## <a name="glyph-rendering"></a>Rendering degli glifi

[L DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) a un'applicazione GDI esistente consente all'applicazione di usare l'API [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) per il rendering dei glifi. Il metodo [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) fornito da DirectWrite eseguirà il rendering a tinta unita in un controller di dominio di memoria senza richiedere API aggiuntive, ad esempio [Direct2D.](./direct2d-portal.md)

In questo modo l'applicazione può ottenere funzionalità avanzate di rendering del testo, come le seguenti:

-   ClearType sub-pixel consente a un'applicazione di inserire glifi nelle posizioni dei sotto-pixel per consentire sia il rendering degli glifi acuti che il layout dei glifi.
-   L'antialiasing della direzione Y consente un rendering più uniforme delle curve su glifi più grandi.

Un'applicazione che [si sposta in Direct2D](./direct2d-portal.md) o ottiene anche le funzionalità seguenti:

-   Accelerazione hardware.
-   Possibilità di riempire il testo con un pennello [Direct2D](./direct2d-portal.md) arbitrario, ad esempio sfumature radiali, sfumature lineari e bitmap.
-   Maggiore supporto per la creazione di livelli e il ritaglio tramite le API [**PushAxisAlignedClip,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**CreateCompatibleRenderTarget.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))
-   Possibilità di supportare il rendering del testo in scala di grigi. In questo modo il canale alfa di destinazione viene popolato correttamente in base all'opacità del pennello del testo e all'antialiasing del testo.

Per supportare in modo efficiente l'accelerazione hardware, [Direct2D](./direct2d-portal.md) usa un'approssimazione leggermente diversa rispetto alla correzione gamma denominata *correzione alfa.* Questo non richiede Direct2D per controllare il pixel del colore di destinazione del rendering durante il rendering del testo.

## <a name="conclusion"></a>Conclusione

Questo argomento illustra le differenze e le analogie tra [Direct2D](./direct2d-portal.md) [e DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) e le motivazioni dell'architettura per fornirle come API separate e cooperativi.

 

 