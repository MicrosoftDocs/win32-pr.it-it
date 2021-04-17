---
title: Panoramica dell'API Direct2D
description: Viene fornita una panoramica del modello a oggetti Direct2D.
ms.assetid: b1362ef6-40fc-4fa5-ba5b-22c622c39f04
keywords:
- Direct2D, informazioni
- Direct2D, file di intestazione
- Direct2D, modello a oggetti
- Direct2D, interfacce
- Interfaccia ID2D1Factory
- Direct2D, destinazioni di rendering
- destinazioni di rendering, informazioni
- Direct2D, comandi di disegno
- destinazioni di rendering, comandi di disegno
- Direct2D, gestione degli errori
- destinazioni di rendering, gestione degli errori
- gestione degli errori
- pennelli
- destinazioni di rendering, pennelli
- geometries
- Direct2D, geometrie
- bitmap per Direct2D
- Direct2D, bitmap
- Primitives
- Direct2D, primitive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858d03f626fe337b174f074d7725dcb1a636b463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300028"
---
# <a name="direct2d-api-overview"></a>Panoramica dell'API Direct2D

Direct2D fornisce un'API, simile a Direct3D, per l'uso con C o C++. L'API espone un'ampia gamma di funzionalità correlate al disegno:

-   Destinazioni di rendering per la visualizzazione e il rendering fuori schermo tramite Direct2D, Direct3D o GDI.
-   Oggetti per la gestione dello stato di disegno, ad esempio le trasformazioni dello spazio delle coordinate e le modalità anti-aliasing.
-   Rappresentazioni per i dati geometrici e funzioni per l'elaborazione geometrica.
-   Funzionalità di rendering per bitmap, geometrie e testo.
-   Provisioning per l'utilizzo di contenuto grafico creato con GDI o Direct3D.

Questo argomento fornisce una panoramica degli oggetti che compongono l'API Direct2D. Contiene le sezioni seguenti:

-   [File di intestazione Direct2D](#direct2d-header-files)
-   [Interfacce Direct2D](#direct2d-interfaces)
-   [Interfaccia ID2D1Factory](#the-id2d1factory-interface)
-   [Destinazioni di rendering](#render-targets)
    -   [Funzionalità di destinazione di rendering](#render-target-features)
    -   [Risorse di destinazione di rendering](#render-target-resources)
    -   [Disegno di comandi](#drawing-commands)
    -   [Gestione degli errori](#error-handling)
-   [Creazione di risorse](#drawing-resources)
    -   [Pennelli](#brushes)
    -   [Geometrie](#geometries)
    -   [Bitmap](#bitmaps)
-   [Disegno di testo](#drawing-text)
-   [Primitive Direct2D](#direct2d-primitives)
-   [Argomenti correlati](#related-topics)

## <a name="direct2d-header-files"></a>File di intestazione Direct2D

L'API Direct2D è definita dai file di intestazione seguenti.

| File di intestazione         | Descrizione                                                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------|
| d2d1. h              | Definisce le versioni C e C++ dell'API Direct2D primario.                                                                      |
| d2d1helper. h        | Definisce le funzioni, le classi e le strutture di Helper C++.                                                                       |
| d2dbasetypes. h      | Definisce primitive di disegno per Direct2D, ad esempio punti e rettangoli. Questa intestazione è inclusa in d2d1. h.                 |
| d2derr. h            | Definisce i codici di errore per Direct2D. Questa intestazione è inclusa in d2d1. h.                                                   |
| d2d1 \_ 1. h           | Definisce le versioni C e C++ dell'API Direct2D primario per Windows 8 e versioni successive.                                              |
| d2d1 \_ 1helper. h     | Definisce funzioni, classi e strutture Helper C++ per Windows 8 e versioni successive.                                               |
| d2d1effects. h       | Definisce le versioni C e C++ della parte relativa agli effetti immagine dell'API Direct2D per Windows 8 e versioni successive.                            |
| d2d1effecthelpers. h | Definisce le funzioni, le classi e le strutture di Helper C++ della parte dell'API Direct2D per Windows 8 e versioni successive. |



 

Per usare Direct2D, l'applicazione deve includere il file di intestazione d2d1. h.

Per compilare un'applicazione Direct2D, aggiungere d2d1. lib all'elenco di librerie. È possibile trovare d2d1. h e d2d1. lib in [Windows Software Development Kit (SDK) per Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

Le sezioni seguenti descrivono alcune delle interfacce comuni fornite dall'API Direct2D.

## <a name="direct2d-interfaces"></a>Interfacce Direct2D

Alla radice dell'API Direct2D si trovano le interfacce [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) e [**ID2D1Resource**](/windows/win32/api/d2d1/nn-d2d1-id2d1resource) . Un oggetto **ID2D1Factory** crea oggetti **ID2D1Resource** e funge da punto di partenza per l'utilizzo di Direct2D. Tutti gli altri oggetti Direct2D ereditano dall'interfaccia **ID2D1Resource** . Esistono due tipi di risorse Direct2D: risorse indipendenti dal dispositivo e risorse dipendenti dal dispositivo.

-   Le risorse indipendenti dal dispositivo non sono associate a un particolare dispositivo di rendering e possono essere mantenute per il ciclo di vita di un'applicazione.
-   Le risorse dipendenti dal dispositivo sono associate a un particolare dispositivo di rendering e smettono di funzionare se il dispositivo è stato rimosso.

Per ulteriori informazioni sulle risorse e sulla condivisione delle risorse, vedere [Panoramica delle risorse](resources-and-resource-domains.md).

## <a name="the-id2d1factory-interface"></a>Interfaccia ID2D1Factory

L'interfaccia [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) è il punto di partenza per l'utilizzo di Direct2D. Usare un **ID2D1Factory** per creare un'istanza delle risorse Direct2D. Per creare un ID2D1Factory, usare uno dei metodi [**CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) .

Una factory definisce un set di metodi Create *Resource* che possono produrre le seguenti risorse di disegno:

-   Le destinazioni di rendering sono oggetti che eseguono il rendering di comandi di disegno.
-   I blocchi di stato di disegno sono oggetti che archiviano le informazioni sullo stato di disegno, ad esempio la trasformazione corrente e la modalità di anti-aliasing.
-   Le geometrie sono oggetti che rappresentano forme semplici e potenzialmente complesse.

Uno degli oggetti più utili che una factory può creare è [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), descritto nella sezione seguente.

## <a name="render-targets"></a>Destinazioni di rendering

Una destinazione di rendering è una risorsa che eredita dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Una destinazione di rendering crea risorse per il disegno e l'esecuzione di operazioni di disegno. Esistono diversi tipi di destinazioni di rendering che è possibile utilizzare per eseguire il rendering della grafica nei modi seguenti:

-   Gli oggetti [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) eseguono il rendering del contenuto in una finestra.
-   Gli oggetti [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) eseguono il rendering in un contesto di dispositivo GDI.
-   Gli oggetti di destinazione di rendering bitmap eseguono il rendering del contenuto in una bitmap fuori schermo.
-   DXGI rendering degli oggetti di destinazione rendering in una superficie DXGI per l'uso con Direct3D.

Poiché una destinazione di rendering è associata a un particolare dispositivo di rendering, si tratta di una risorsa dipendente dal dispositivo e smette di funzionare se il dispositivo viene rimosso.

### <a name="render-target-features"></a>Funzionalità di destinazione di rendering

È possibile specificare se una destinazione di rendering deve utilizzare l'accelerazione hardware e se deve essere eseguito il rendering della visualizzazione remota dal computer locale o remoto. Le destinazioni di rendering possono essere impostate per il rendering con alias o con alias. Per il rendering di scene con un numero elevato di primitive, uno sviluppatore può anche eseguire il rendering di grafica 2D in modalità con alias e utilizzare l'anti-aliasing di D3D multisample per ottenere una maggiore scalabilità.

Le destinazioni di rendering possono inoltre raggruppare le operazioni di disegno in livelli rappresentati dall'interfaccia [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) . I livelli sono utili per raccogliere le operazioni di disegno da comporre insieme durante il rendering di un frame. Per alcuni scenari, può trattarsi di un'alternativa utile per eseguire il rendering in una destinazione di rendering bitmap e quindi riutilizzare il contenuto della bitmap, perché i costi di allocazione per i livelli sono inferiori rispetto a quelli di un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Le destinazioni di rendering possono creare nuove destinazioni di rendering compatibili con se stesse, che risulta utile per il rendering intermedio all'esterno dello schermo, mantenendo al tempo stesso le varie proprietà di destinazione di rendering impostate nell'oggetto originale.

È anche possibile eseguire il rendering usando GDI in una destinazione di rendering Direct2D chiamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) in una destinazione di rendering per [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), che contiene metodi [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) e [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) che possono essere usati per recuperare un contesto di dispositivo GDI. Il rendering tramite GDI è possibile solo se la destinazione di rendering è stata creata con il flag di [**utilizzo della destinazione di rendering d2d1 impostato su \_ \_ \_ \_ GDI \_**](/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage) . Questa operazione è utile per le applicazioni che eseguono principalmente il rendering con Direct2D ma hanno un modello di estendibilità o altri contenuti legacy che richiedono la possibilità di eseguire il rendering con GDI. Per ulteriori informazioni, vedere [Cenni preliminari sull'interoperabilità Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Risorse di destinazione di rendering

Analogamente a una factory, una destinazione di rendering può creare risorse di disegno. Tutte le risorse create da una destinazione di rendering sono risorse dipendenti dal dispositivo, proprio come la destinazione di rendering. Una destinazione di rendering può creare i tipi di risorse seguenti:

-   Bitmap
-   Pennelli
-   Livelli
-   Mesh

### <a name="drawing-commands"></a>Disegno di comandi

Per eseguire il rendering del contenuto, usare i metodi di disegno della destinazione di rendering. Prima di iniziare a disegnare, chiamare il metodo [**ID2D1RenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Al termine del disegno, chiamare il metodo [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Tra queste chiamate, si usano i metodi Draw e Fill per eseguire il rendering delle risorse di disegno. La maggior parte dei metodi di disegno e riempimento accetta una forma, ovvero una primitiva o una geometria, e un pennello per riempire o delineare la forma.

Le destinazioni di rendering forniscono anche metodi per il ritaglio, l'applicazione di maschere di opacità e la trasformazione dello spazio delle coordinate.

Direct2D usa un sistema di coordinate a sinistra: i valori positivi dell'asse x procedono verso destra e i valori positivi dell'asse y procedono verso il basso.

### <a name="error-handling"></a>Gestione degli errori

I comandi di disegno della destinazione di rendering non indicano se l'operazione richiesta è stata eseguita correttamente. Per determinare se sono stati creati errori di disegno, chiamare il metodo [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) della destinazione di rendering o il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) per ottenere un valore **HRESULT**.

## <a name="drawing-resources"></a>Creazione di risorse

Le sezioni seguenti descrivono alcune risorse che possono essere create dalla destinazione di rendering e dalle interfacce Factory.

### <a name="brushes"></a>Pennelli

Un pennello, rappresentato dall'interfaccia [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) , è una risorsa dipendente dal dispositivo, creata da una destinazione di rendering, che disegna un'area con l'output. Pennelli diversi hanno diversi tipi di output. Alcuni pennelli disegnano un'area con un colore a tinta unita, altri con una sfumatura o un'immagine. Direct2D fornisce quattro tipi di pennelli:

-   [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) disegna un'area con un colore a tinta unita.
-   [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) disegna un'area con una sfumatura lineare che combina due o più colori su una riga, l'asse delle sfumature.
-   [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) disegna un'area con una sfumatura radiale che combina due o più colori intorno a un'ellisse.
-   [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) disegna un'area con una bitmap.

Per creare un pennello, usare uno dei metodi pennello [**ID2D1RenderTarget::**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)create *<Type>* , ad esempio [**CreateRadialGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)). I pennelli possono essere utilizzati con i metodi di disegno e riempimento della destinazione di rendering, per disegnare un tratto o un contorno di forme oppure come maschera di opacità.

Per ulteriori informazioni sui pennelli, vedere [Cenni preliminari sui pennelli](direct2d-brushes-overview.md).

### <a name="geometries"></a>Geometrie

Oltre alle primitive di disegno di base, ad esempio punti, rettangoli ed ellissi, Direct2D fornisce l'interfaccia [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) per la descrizione di forme semplici e complesse. Le interfacce che ereditano da **ID2D1Geometry** definiscono tipi diversi di forme, ad esempio [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) per la rappresentazione di rettangoli, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) per la rappresentazione di rettangoli arrotondati e [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) per la rappresentazione di ellissi.

È possibile creare forme più complesse usando l'interfaccia [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) per specificare una serie di figure composte da linee, curve e archi. **ID2D1GeometrySink** viene passato al metodo Open di un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) per generare una geometria complessa. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) può essere usato anche con l'API DirectWrite per estrarre le strutture del percorso del testo formattato per il rendering artistico.

Le interfacce di geometria forniscono metodi per modificare le forme ampliando o semplificando le geometrie esistenti oppure generando l'intersezione o l'Unione di più geometrie. Forniscono anche metodi per determinare se le geometrie sono intersecate o sovrapposte, il recupero di informazioni sui limiti, il calcolo dell'area o della lunghezza di una geometria e l'interpolazione di posizioni lungo una geometria. Direct2D offre inoltre la possibilità di creare una mesh di triangoli tassellati da una geometria.

Per creare una geometria, usare uno dei metodi geometry [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory):: Create *<Type>* , ad esempio [**CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry). Una geometria è una risorsa indipendente dal dispositivo.

Per eseguire il rendering di una geometria, usare i metodi [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) di una destinazione di rendering.

Per altre informazioni sulle geometrie, vedere [Cenni preliminari sulle geometrie](direct2d-geometries-overview.md).

### <a name="bitmaps"></a>Bitmap

Direct2D non fornisce metodi per il caricamento o l'archiviazione di bitmap; consente invece di creare bitmap utilizzando [Windows Imaging Component (WIC)](../wic/-wic-about-windows-imaging-codec.md). Le risorse bitmap possono essere caricate tramite WIC e quindi usate per creare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) tramite il metodo [**ID2D1RenderTarget:: CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) .

È anche possibile creare bitmap da dati in memoria impostati con altri mezzi. Dopo la creazione di una bitmap, è possibile disegnarla tramite il metodo [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) della destinazione di rendering o con un pennello bitmap.

Poiché la creazione di risorse bitmap su destinazioni di rendering hardware è spesso un'operazione costosa, Direct2D può aggiornare il contenuto di una bitmap (o parte della bitmap) utilizzando i metodi [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap), [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)e [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory) . L'uso di questi metodi può potenzialmente salvare i costi associati ad altre allocazioni di trame della GPU.

## <a name="drawing-text"></a>Disegno di testo

Direct2D è stato progettato per funzionare con le operazioni di testo della nuova API di testo, DirectWrite. Per rendere più semplice l'utilizzo dell'API DirectWrite, le destinazioni di rendering forniscono tre metodi per il rendering di risorse di testo DirectWrite: [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)e [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Poiché Direct2D utilizza la GPU per il processo di rendering del testo ClearType, Direct2D fornisce un utilizzo della CPU inferiore rispetto a GDI per le operazioni di testo e una migliore scalabilità, perché è disponibile una maggiore potenza di elaborazione della GPU.

[**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) è progettato per gli scenari più semplici che coinvolgono il rendering di una stringa di testo Unicode con formattazione minima. Il layout più complesso e la flessibilità tipografica vengono forniti tramite il metodo [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , che usa un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) per specificare il contenuto e la formattazione di cui eseguire il rendering. **IDWriteTextLayout** consente di specificare la formattazione singola per sottostringhe di testo e altre opzioni tipografiche avanzate.

Per gli scenari in cui è necessario un controllo preciso del layout a livello di glifo, è possibile usare il metodo [**ID2D1RenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) insieme alle funzionalità di misurazione fornite da [DirectWrite](../directwrite/direct-write-portal.md).

Per usare l'API DirectWrite, includere l'intestazione DWrite. h. Come Direct2D, DirectWrite usa una factory [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) per creare oggetti di testo. Usare la funzione [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) per creare una factory e quindi usare i metodi create per creare risorse DirectWrite, ad esempio [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)).

Per ulteriori informazioni su DirectWrite, vedere l'argomento [Introducing DirectWrite](../directwrite/introducing-directwrite.md) .

## <a name="direct2d-primitives"></a>Primitive Direct2D

Direct2D definisce un set di primitive simili a quelle fornite da altre API di disegno. Fornisce una struttura dei colori, una struttura della matrice per l'esecuzione di trasformazioni e versioni a virgola mobile e Integer di punti, rettangoli, ellissi e strutture di dimensioni. In genere, si usano le versioni a virgola mobile di queste strutture.

Non si usa una factory o una destinazione di rendering per creare un'istanza di primitive Direct2D. È possibile crearli direttamente o usare i metodi helper definiti in d2d1helper. h per crearli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Direct2D](reference.md)
</dt> <dt>

[Esempio di Hello World DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples)
</dt> <dt>

[Introduzione a DirectWrite](../directwrite/introducing-directwrite.md)
</dt> <dt>

[Panoramica delle risorse](resources-and-resource-domains.md)
</dt> <dt>

[Windows Imaging Component (WIC)](../wic/-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 