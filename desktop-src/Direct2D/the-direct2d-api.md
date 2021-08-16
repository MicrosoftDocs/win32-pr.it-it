---
title: Panoramica dell'API Direct2D
description: Fornisce una panoramica del modello a oggetti Direct2D.
ms.assetid: b1362ef6-40fc-4fa5-ba5b-22c622c39f04
keywords:
- Direct2D, informazioni su
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
- Primitive
- Direct2D, primitive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f318e3542d54ee92817193ef6b749a3ba1cf4678407ca7a12f28c6c187ae86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074995"
---
# <a name="direct2d-api-overview"></a>Panoramica dell'API Direct2D

Direct2D fornisce un'API, simile a Direct3D, per l'uso con C o C++. L'API espone un'ampia gamma di funzionalità correlate al disegno:

-   Destinazioni di rendering per la visualizzazione e il rendering fuori schermo usando Direct2D, Direct3D o GDI.
-   Oggetti per la gestione dello stato del disegno, ad esempio trasformazioni dello spazio delle coordinate e modalità di antialiasing.
-   Rappresentazioni per i dati geometrici e funzioni per l'elaborazione geometrica.
-   Funzionalità di rendering per bitmap, geometrie e testo.
-   Esegue il provisioning per l'uso di contenuto grafico creato con GDI o Direct3D.

Questo argomento offre una panoramica degli oggetti che costituiscono l'API Direct2D. Contiene le sezioni seguenti:

-   [File di intestazione Direct2D](#direct2d-header-files)
-   [Interfacce Direct2D](#direct2d-interfaces)
-   [Interfaccia ID2D1Factory](#the-id2d1factory-interface)
-   [Destinazioni di rendering](#render-targets)
    -   [Funzionalità di destinazione di rendering](#render-target-features)
    -   [Eseguire il rendering delle risorse di destinazione](#render-target-resources)
    -   [Comandi di disegno](#drawing-commands)
    -   [Gestione degli errori](#error-handling)
-   [Disegno di risorse](#drawing-resources)
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
| d2d1.h              | Definisce le versioni C e C++ dell'API Direct2D primaria.                                                                      |
| d2d1helper.h        | Definisce funzioni, classi e strutture helper C++.                                                                       |
| d2dbasetypes.h      | Definisce le primitive di disegno per Direct2D, ad esempio punti e rettangoli. Questa intestazione è inclusa in d2d1.h.                 |
| d2derr.h            | Definisce i codici di errore per Direct2D. Questa intestazione è inclusa in d2d1.h.                                                   |
| d2d1 \_ 1.h           | Definisce le versioni C e C++ dell'API Direct2D primaria per Windows 8 e versioni successive.                                              |
| d2d1 \_ 1helper.h     | Definisce funzioni, classi e strutture helper C++ per Windows 8 e versioni successive.                                               |
| d2d1effects.h       | Definisce le versioni C e C++ degli effetti immagine parte dell'API Direct2D per Windows 8 e versioni successive.                            |
| d2d1effecthelpers.h | Definisce funzioni, classi e strutture helper C++ della parte degli effetti immagine dell'API Direct2D per Windows 8 e versioni successive. |



 

Per usare Direct2D, l'applicazione deve includere il file di intestazione d2d1.h.

Per compilare un'applicazione Direct2D, aggiungere d2d1.lib all'elenco di librerie. È possibile trovare d2d1.h e d2d1.lib in [Windows Software Development Kit (SDK) per](https://msdn.microsoft.com/windows/bb980924.aspx)Windows 7 .

Le sezioni seguenti descrivono alcune delle interfacce comuni fornite dall'API Direct2D.

## <a name="direct2d-interfaces"></a>Interfacce Direct2D

Alla radice dell'API Direct2D sono presenti le [**interfacce ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) e [**ID2D1Resource.**](/windows/win32/api/d2d1/nn-d2d1-id2d1resource) Un **oggetto ID2D1Factory** crea **oggetti ID2D1Resource** e funge da punto di partenza per l'uso di Direct2D. Tutti gli altri oggetti Direct2D ereditano **dall'interfaccia ID2D1Resource.** Esistono due tipi di risorse Direct2D: risorse indipendenti dal dispositivo e risorse dipendenti dal dispositivo.

-   Le risorse indipendenti dal dispositivo non sono associate a un particolare dispositivo di rendering e possono essere mantenute per la durata di un'applicazione.
-   Le risorse dipendenti dal dispositivo sono associate a un particolare dispositivo di rendering e cessano di funzionare se tale dispositivo viene rimosso.

Per altre informazioni sulle risorse e sulla condivisione delle risorse, vedere Panoramica [delle risorse.](resources-and-resource-domains.md)

## <a name="the-id2d1factory-interface"></a>Interfaccia ID2D1Factory

[**L'interfaccia ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) è il punto di partenza per l'uso di Direct2D. Usare **id2D1Factory per creare un'istanza** delle risorse Direct2D. Per creare un id2D1Factory, usare uno dei [**metodi CreateFactory.**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory)

Una factory definisce un set di metodi Create *Resource* che possono produrre le risorse di disegno seguenti:

-   Le destinazioni di rendering sono oggetti che eseguono il rendering dei comandi di disegno.
-   I blocchi di stato di disegno sono oggetti che archiviano informazioni sullo stato del disegno, ad esempio la trasformazione corrente e la modalità di antialiasing.
-   Le geometrie sono oggetti che rappresentano forme semplici e potenzialmente complesse.

Uno degli oggetti più utili che una factory può creare è [**ID2D1RenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)descritto nella sezione seguente.

## <a name="render-targets"></a>Destinazioni di rendering

Una destinazione di rendering è una risorsa che eredita [**dall'interfaccia ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Una destinazione di rendering crea risorse per il disegno ed esegue operazioni di disegno. Esistono diversi tipi di destinazioni di rendering che è possibile usare per eseguire il rendering della grafica nei modi seguenti:

-   [**Gli oggetti ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) eseguono il rendering del contenuto in una finestra.
-   [**Il rendering degli oggetti ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) viene eseguito in un contesto di dispositivo GDI.
-   Gli oggetti destinazione di rendering bitmap eseguono il rendering del contenuto in una bitmap fuori schermo.
-   Gli oggetti destinazione di rendering DXGI eseguono il rendering su una superficie DXGI per l'uso con Direct3D.

Poiché una destinazione di rendering è associata a un particolare dispositivo di rendering, è una risorsa dipendente dal dispositivo e smette di funzionare se il dispositivo viene rimosso.

### <a name="render-target-features"></a>Funzionalità di destinazione di rendering

È possibile specificare se una destinazione di rendering deve usare l'accelerazione hardware e se il rendering dello schermo remoto deve essere eseguito dal computer locale o remoto. Le destinazioni di rendering possono essere impostate per il rendering con alias o con antialias. Per il rendering di scene con un numero elevato di primitive, uno sviluppatore può anche eseguire il rendering di grafica 2D in modalità con alias e usare l'anti-aliasing multicampionamento D3D per ottenere una maggiore scalabilità.

Le destinazioni di rendering possono anche raggruppare le operazioni di disegno in livelli rappresentati [**dall'interfaccia ID2D1Layer.**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) I livelli sono utili per raccogliere le operazioni di disegno da comporre insieme durante il rendering di un frame. Per alcuni scenari, questa può essere un'alternativa utile al rendering in una destinazione di rendering bitmap e quindi al riutilizzo del contenuto della bitmap, in quanto i costi di allocazione per la visualizzazione su più livelli sono inferiori a quelli per [**id2D1BitmapRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)

Le destinazioni di rendering possono creare nuove destinazioni di rendering compatibili con se stesse, il che è utile per il rendering intermedio fuori schermo mantenendo le varie proprietà della destinazione di rendering impostate nell'originale.

È anche possibile eseguire il rendering usando GDI in una destinazione di rendering Direct2D chiamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su una destinazione di rendering per [**ID2D1GdiInteropRenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)che dispone di metodi [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) e [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) che possono essere usati per recuperare un contesto di dispositivo GDI. Il rendering tramite GDI è possibile solo se la destinazione di rendering è stata creata con il flag [**D2D1 \_ RENDER TARGET USAGE \_ \_ \_ GDI \_ COMPATIBLE**](/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage) impostato. Ciò è utile per le applicazioni che eseguono principalmente il rendering con Direct2D, ma hanno un modello di estendibilità o altro contenuto legacy che richiede la possibilità di eseguire il rendering con GDI. Per altre informazioni, vedere [Cenni preliminari sull'interoperabilità direct2D e GDI.](direct2d-and-gdi-interoperation-overview.md)

### <a name="render-target-resources"></a>Eseguire il rendering delle risorse di destinazione

Analogamente a una factory, una destinazione di rendering può creare risorse di disegno. Tutte le risorse create da una destinazione di rendering sono risorse dipendenti dal dispositivo (proprio come la destinazione di rendering). Una destinazione di rendering può creare i tipi di risorse seguenti:

-   Bitmap
-   Pennelli
-   Livelli
-   Mesh

### <a name="drawing-commands"></a>Comandi di disegno

Per eseguire il rendering del contenuto, usare i metodi di disegno della destinazione di rendering. Prima di iniziare a disegnare, chiamare il [**metodo ID2D1RenderTarget::BeginDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) Al termine del disegno, chiamare il [**metodo ID2D1RenderTarget::EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Tra queste chiamate si usano i metodi Draw e Fill per eseguire il rendering delle risorse di disegno. La maggior parte dei metodi Draw e Fill accetta una forma (primitiva o geometria) e un pennello per il riempimento o la struttura della forma.

Le destinazioni di rendering forniscono anche metodi per il ritaglio, l'applicazione di maschere di opacità e la trasformazione dello spazio delle coordinate.

Direct2D usa un sistema di coordinate a sinistra: i valori positivi dell'asse x procedono verso destra e i valori positivi dell'asse y procedono verso il basso.

### <a name="error-handling"></a>Gestione degli errori

I comandi di disegno della destinazione di rendering non indicano se l'operazione richiesta è riuscita. Per verificare se si sono verificati errori di disegno, chiamare il metodo Flush della destinazione [**di**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) rendering o [**il metodo EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) per ottenere un **HRESULT.**

## <a name="drawing-resources"></a>Risorse di disegno

Le sezioni seguenti descrivono alcune delle risorse che possono essere create dalle interfacce di destinazione di rendering e factory.

### <a name="brushes"></a>Pennelli

Un pennello, rappresentato [**dall'interfaccia ID2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) è una risorsa dipendente dal dispositivo, creata da una destinazione di rendering, che disegna un'area con il relativo output. Pennelli diversi hanno diversi tipi di output. Alcuni pennelli disegnano un'area con un colore a tinta unita, altri con una sfumatura o un'immagine. Direct2D offre quattro tipi di pennelli:

-   [**ID2D1SolidColorBrush disegna**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) un'area con un colore a tinta unita.
-   [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) disegna un'area con una sfumatura lineare che unisce due o più colori su una linea, l'asse delle sfumature.
-   [**ID2D1RadialGradientBrush disegna**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) un'area con una sfumatura radiale che unisce due o più colori intorno a un'ellisse.
-   [**ID2D1BitmapBrush disegna**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) un'area con una bitmap.

Per creare un pennello, usa uno dei metodi [**ID2D1RenderTarget::**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Create Brush, ad esempio *<Type>* [**CreateRadialGradientBrush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) I pennelli possono essere usati con i metodi Draw e Fill di una destinazione di rendering, per disegnare un tratto o un contorno di forma o come maschera di opacità.

Per altre informazioni sui pennelli, vedere [Cenni preliminari sui pennelli.](direct2d-brushes-overview.md)

### <a name="geometries"></a>Geometrie

Oltre alle primitive di disegno di base, ad esempio punti, rettangoli ed ellissi, Direct2D fornisce [**l'interfaccia ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) per descrivere forme semplici e complesse. Le interfacce che ereditano da **ID2D1Geometry** definiscono tipi diversi di forme, ad esempio [**ID2D1RectangleGeometry per**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) la rappresentazione di rettangoli, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) per la rappresentazione di rettangoli arrotondati e [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) per rappresentare ellissi.

È possibile creare forme più complesse usando l'interfaccia [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) per specificare una serie di figure costituite da linee, curve e archi. **ID2D1GeometrySink** viene passato al metodo Open di [**id2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) per generare una geometria complessa. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) può essere usato anche con l'API DirectWrite per estrarre i contorni del percorso del testo formattato per il rendering del colore.

Le interfacce geometry forniscono metodi per modificare le forme ampliando o semplificando le geometrie esistenti o generando l'intersezione o l'unione di più geometrie. Forniscono anche metodi per determinare se le geometrie si intersecano o si sovrappongono, recuperano informazioni sui limiti, calcolano l'area o la lunghezza di una geometria e interpolano le posizioni lungo una geometria. Direct2D offre anche la possibilità di creare una mesh di triangoli a scorrimento da una geometria.

Per creare una geometria, usare uno dei metodi [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)::Create Geometry, ad esempio *<Type>* [**CreatePathGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) Una geometria è una risorsa indipendente dal dispositivo.

Per eseguire il rendering di una geometria, si usano i [**metodi DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) di una destinazione di rendering.

Per altre informazioni sulle geometrie, vedere [Cenni preliminari sulle geometrie.](direct2d-geometries-overview.md)

### <a name="bitmaps"></a>Bitmap

Direct2D non fornisce metodi per il caricamento o l'archiviazione di bitmap. consente invece di creare bitmap usando il componente [Windows Imaging Component (WIC).](../wic/-wic-about-windows-imaging-codec.md) Le risorse bitmap possono essere caricate tramite WIC e quindi usate per creare un [**oggetto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) tramite il [**metodo ID2D1RenderTarget::CreateBitmapFromWicBitmap.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap))

È anche possibile creare bitmap da dati in memoria che sono stati impostati in altri mezzi. Dopo la creazione, una bitmap può essere disegnata dal metodo [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) di destinazione di rendering o con un pennello bitmap.

Poiché la creazione di risorse bitmap nelle destinazioni di rendering hardware è spesso un'operazione costosa, Direct2D può aggiornare il contenuto di una bitmap (o di una parte della bitmap) usando i metodi [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap), [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)e [**CopyFromMemory.**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory) L'uso di questi metodi può potenzialmente ridurre i costi associati ad allocazioni di trame GPU aggiuntive.

## <a name="drawing-text"></a>Disegno di testo

Direct2D è stato progettato per funzionare con le operazioni di testo della nuova API di testo, DirectWrite. Per semplificare l'uso dell'API DirectWrite, le destinazioni di rendering forniscono tre metodi per il rendering DirectWrite risorse di testo: [**DrawText,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)e [**DrawGlyphRun.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) Poiché Direct2D usa la GPU per il processo di rendering del testo ClearType, Direct2D offre un utilizzo della CPU inferiore rispetto a GDI per le operazioni di testo e una migliore scalabilità con maggiore potenza di elaborazione della GPU disponibile.

[**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) è progettato per gli scenari più semplici che prevedono il rendering di una stringa di testo Unicode con formattazione minima. Il layout più complesso e la flessibilità tipografica vengono forniti tramite il metodo [**ID2D1RenderTarget::D rawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) che usa un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) per specificare il contenuto e la formattazione di cui eseguire il rendering. **IDWriteTextLayout consente** di specificare la formattazione singola per le sottostringhe di testo e altre opzioni tipografiche avanzate.

Per gli scenari in cui è necessario un controllo preciso del layout a livello di glifo, è possibile usare il metodo [**ID2D1RenderTarget::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) insieme alle funzionalità di misurazione fornite da [DirectWrite](../directwrite/direct-write-portal.md).

Per usare l'API DirectWrite, includere l'intestazione dwrite.h. Come Direct2D, DirectWrite usa una factory, [**IDWriteFactory,**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) per creare oggetti di testo. Usare la [**funzione DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) per creare una factory e quindi usare i relativi metodi Create per creare DirectWrite risorse, ad esempio [**IDWriteTextFormat.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))

Per altre informazioni sui DirectWrite, vedere l'argomento [Introduzione DirectWrite.](../directwrite/introducing-directwrite.md)

## <a name="direct2d-primitives"></a>Primitive Direct2D

Direct2D definisce un set di primitive simili a quelle fornite da altre API di disegno. Fornisce una struttura dei colori, una struttura matrice per l'esecuzione di trasformazioni e versioni a virgola mobile e integer di punti, rettangoli, ellissi e strutture di dimensioni. In genere, si usano le versioni a virgola mobile di queste strutture.

Non si usa una factory o una destinazione di rendering per creare istanze di primitive Direct2D. È possibile crearli direttamente o usare i metodi helper definiti in d2d1helper.h per crearli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> <dt>

[DirectWrite Hello World esempio](/samples/browse/?redirectedfrom=MSDN-samples)
</dt> <dt>

[Introduzione a DirectWrite](../directwrite/introducing-directwrite.md)
</dt> <dt>

[Panoramica delle risorse](resources-and-resource-domains.md)
</dt> <dt>

[Windows Imaging Component (WIC)](../wic/-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 