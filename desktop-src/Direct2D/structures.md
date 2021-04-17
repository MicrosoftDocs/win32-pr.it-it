---
title: Strutture Direct2D
description: Direct2D fornisce le seguenti strutture. Altre strutture sono definite nello spazio dei nomi D2D1.
ms.assetid: 6c34a8c8-4b0b-4a95-8f13-25ca25c370ba
keywords:
- Direct2D, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba4b668e143b3ab5b166582e504c68a05722da7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299826"
---
# <a name="direct2d-structures"></a>Strutture Direct2D

Direct2D fornisce le seguenti strutture. Altre strutture sono definite nello [spazio dei nomi D2D1](d2d1-namespace.md).

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**D2D \_ colore \_ F**](d2d-color-f.md) | Descrive i componenti rosso, verde, blu e alfa di un colore. |
| [**\_Matrice D2D \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) | Rappresenta una matrice 3 per 2. |
| [**\_Matrice D2D \_ 4x3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f) | Descrive una matrice a virgola mobile 4 per 3. |
| [**D2D \_ Matrix \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f) | Descrive una matrice a virgola mobile 4 per 4. |
| [**\_Matrice D2D \_ 5x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f) | Descrive una matrice a virgola mobile 5 per 4. |
| [**D2D \_ punto \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f) | Rappresenta una coordinata x e una coppia di coordinate y, espressa come valori a virgola mobile, nello spazio bidimensionale. |
| [**Punto di D2D \_ \_ 2L**](/previous-versions/windows/desktop/legacy/jj219217(v=vs.85)) | La \_ struttura D2D Point \_ 2L definisce le coordinate x e y di un punto. |
| [**Punto di D2D \_ \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u) | Rappresenta una coordinata x e una coppia di coordinate y, espressa come valore intero senza segno a 32 bit, nello spazio bidimensionale. |
| [**D2D \_ Rect \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) | Rappresenta un rettangolo definito dalle coordinate dell'angolo superiore sinistro (a sinistra, superiore) e le coordinate dell'angolo inferiore destro (a destra, in basso).  |
| [**D2D \_ Rect \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) | La struttura a [**\_ \_ L Rect D2D**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) definisce le coordinate degli angoli superiore sinistro e inferiore destro di un rettangolo. |
| [**\_U D2D Rect \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_u) | Rappresenta un rettangolo definito dalla coppia di coordinate dell'angolo superiore sinistro (a sinistra, superiore) e dall'angolo inferiore destro della coppia di coordinate (a destra, in basso). Queste coordinate sono espresse come valori integer a 32 bit. |
| [**\_Dimensioni D2D \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f) | Archivia una coppia ordinata di valori a virgola mobile, in genere la larghezza e l'altezza di un rettangolo.  |
| [**D2D \_ dimensioni \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u) | Memorizza una coppia ordinata di interi, generalmente la larghezza e l'altezza di un rettangolo. |
| [**D2D \_ vector \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f) | Vettore 2D costituito da due valori a virgola mobile e precisione singola (x, y).  |
| [**\_Vettore D2D \_ 3F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f) | Vettore 3D costituito da tre valori a virgola mobile e precisione singola (x, y, z). |
| [**D2D \_ vector \_ 4F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f) | Vettore 4D costituito da quattro valori a virgola mobile a precisione singola (x, y, z, w). |
| [**\_Segmento di arco d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_arc_segment) | Descrive un arco ellittico tra due punti. |
| [**\_Segmento di Bezier d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) | Rappresenta un segmento di Bezier cubico tracciato tra due punti. |
| [**\_Proprietà del \_ pennello \_ bitmap d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) | Descrive le modalità di estensione e la modalità di interpolazione di un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). |
| [**\_ \_ PROPERTIES1 pennello bitmap \_ d2d1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1) | Descrive le modalità di estensione e la modalità di interpolazione di un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). |
| [**\_Proprietà bitmap \_ d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) | Descrive il formato pixel e il valore dpi di una bitmap. |
| [**\_PROPERTIES1 bitmap \_ d2d1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) | Questa struttura consente la creazione di un [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1) con opzioni bitmap e informazioni sul contesto colori disponibili.  |
| [**Descrizione di D2D1 \_ Blend \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) | Definisce una descrizione di Blend da usare in una trasformazione Blend particolare. |
| [**\_Proprietà del pennello d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties) | Descrive l'opacità e la trasformazione di un pennello. |
| [**D2D1 \_ colore \_ F**](d2d1-color-f.md) | Descrive i componenti rosso, verde, blu e alfa di un colore. |
| [**\_Proprietà di creazione d2d1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_creation_properties) | Specifica le opzioni con cui vengono creati la periferica [Direct2D](./direct2d-portal.md) , la factory e il contesto di dispositivo.  |
| [**\_Proprietà del \_ buffer dei vertici personalizzati d2d1 \_ \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_custom_vertex_buffer_properties) | Definisce un vertex shader e la descrizione dell'elemento di input per definire il layout di input. |
| [**\_ \_ Descrizione dello stato del disegno d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description) | Descrive lo stato di disegno di una destinazione di rendering.  |
| [**\_ \_ DESCRIPTION1 stato disegno \_ d2d1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_drawing_state_description1) | Descrive lo stato di disegno di un contesto di dispositivo. |
| [**\_ \_ Descrizione input effetto \_ d2d1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_effect_input_description) | Descrive le funzionalità di un effetto. |
| [**\_Ellisse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) | Contiene il punto centrale, il raggio x e il raggio y di un'ellisse. |
| [**\_Opzioni factory \_ d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_factory_options) | Contiene il livello di debug di un oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .  |
| [**\_ \_ Duplicazione dei dati della funzionalità d2d1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_doubles) | Viene descritto il supporto per i valori Double negli shader. |
| [**\_ \_ \_ Opzioni hardware di D3D10 \_ X \_ per \_ i dati delle funzionalità d2d1**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_d3d10_x_hardware_options) | Viene descritto il supporto compute shader, che è un'opzione a livello di funzionalità D3D10. |
| [**\_Patch mesh d2d1 gradiente \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) | Rappresenta una patch di tensore con 16 punti di controllo, 4 colori d'angolo e flag di limite. Un ID2D1GradientMesh è costituito da una o più patch mesh con sfumature. Usare la [**funzione GradientMeshPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatch) o la [**funzione GradientMeshPatchFromCoonsPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatchfromcoonspatch) per crearne una.  |
| [**\_Cursore sfumatura d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) | Contiene la posizione e il colore di un cursore sfumatura.  |
| [**\_Proprietà di \_ \_ destinazione rendering HWND d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) | Contiene le opzioni HWND, pixel size e Presentation per un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget). |
| [**\_Proprietà di \_ stile input penna d2d1 \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties) | Definisce la forma generale di suggerimento penna e la trasformazione utilizzata in un oggetto [**ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle) .  |
| [**\_Proprietà del \_ pennello \_ immagine d2d1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_image_brush_properties) | Descrive le funzionalità del pennello immagine. |
| [**\_Segmento di \_ Bezier input penna d2d1 \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment) | Rappresenta un segmento di Bezier da utilizzare nella creazione di un oggetto [**ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink) . Questa struttura è diversa dal [**\_ \_ segmento di Bezier d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) in quanto è composta da [**\_ \_ punti di input penna d2d1**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point), che contengono un raggio, oltre alle coordinate x e y.  |
| [**\_Punto di input penna d2d1 \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point) | Rappresenta una coppia di punti, RADIUS che fa parte di un [**\_ segmento di \_ Bezier \_ d2d1 input penna**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment). |
| [**\_Descrizione input \_ d2d1**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_description) | Descrive le opzioni che le trasformazioni possono impostare sulle trame di input. |
| [**D2D1 \_ \_ elemento input \_ DESC**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_element_desc) | Descrizione di un singolo elemento nel layout del vertice. |
| [**\_Parametri del livello d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) | Contiene i limiti del contenuto, le informazioni sulla maschera, le impostazioni di opacità e altre opzioni per una risorsa livello.  |
| [**\_PARAMETERS1 livello \_ d2d1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) | Contiene i limiti del contenuto, le informazioni sulla maschera, le impostazioni di opacità e altre opzioni per una risorsa livello. |
| [**\_Proprietà del \_ pennello sfumato lineare \_ d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) | Contiene il punto iniziale e l'endpoint dell'asse delle sfumature per un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).  |
| [**\_Matrice d2d1 \_ 3x2 \_ F**](d2d1-matrix-3x2-f.md) | Rappresenta una matrice 3 per 2.  |
| [**\_Matrice d2d1 \_ 4x3 \_ F**](d2d1-matrix-4x3-f.md) | Rappresenta una matrice 4 per 3.  |
| [**D2D1 \_ Matrix \_ 4x4 \_ F**](d2d1-matrix-4x4-f.md) | Rappresenta una matrice 4 per 4.  |
| [**\_Matrice d2d1 \_ 5x4 \_ F**](d2d1-matrix-5x4-f.md) | Rappresenta una matrice di 5 per 4.  |
| [**\_Rect mappato d2d1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_mapped_rect) | Descrive la memoria mappata dall'API [**ID2D1Bitmap1:: Map**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map) . |
| [**\_Formato pixel \_ d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) | Contiene il formato dati e la modalità Alpha per una bitmap o una destinazione di rendering.  |
| [**D2D1 \_ punto \_ 2F**](d2d1-point-2f.md) | Rappresenta una coordinata x e una coppia di coordinate y nello spazio bidimensionale. |
| [**Punto di D2D1 \_ \_ 2L**](/previous-versions/windows/desktop/legacy/hh847948(v=vs.85)) | La struttura POINT definisce le coordinate x e y di un punto. |
| [**Punto di D2D1 \_ \_ 2U**](d2d1-point-2u.md) | Rappresenta una coordinata x e una coppia di coordinate y nello spazio bidimensionale.  |
| [**\_Descrizione del punto di d2d1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_point_description) | Descrive un punto su una geometria del percorso. |
| [**\_Proprietà del \_ controllo di stampa d2d1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_print_control_properties) | Proprietà di creazione per un oggetto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) . |
| [**\_Binding della proprietà d2d1 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) | Definisce un'associazione di proprietà a una coppia di funzioni che ottengono e impostano la proprietà corrispondente.  |
| [**\_Segmento di Bezier quadratico d2d1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_quadratic_bezier_segment) | Contiene il punto di controllo e il punto finale per un segmento di Bezier quadratico. |
| [**\_Proprietà del \_ pennello sfumatura RADIAle d2d1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) | Contiene l'offset di origine sfumatura e le dimensioni e la posizione dell'ellisse sfumatura per un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).  |
| [**D2D1 \_ Rect \_ F**](d2d1-rect-f.md) | Rappresenta un rettangolo definito dalle coordinate dell'angolo superiore sinistro (a sinistra, superiore) e le coordinate dell'angolo inferiore destro (a destra, in basso).  |
| [**D2D1 \_ Rect \_ L**](/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)) | La struttura RECT definisce le coordinate degli angoli superiore sinistro e inferiore destro di un rettangolo. |
| [**\_U d2d1 Rect \_**](d2d1-rect-u.md) | Rappresenta un rettangolo definito dalle coordinate dell'angolo superiore sinistro (a sinistra, superiore) e le coordinate dell'angolo inferiore destro (a destra, in basso).  |
| [**\_Proprietà della \_ trama della risorsa d2d1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_resource_texture_properties) | Definisce una trama di risorse quando viene creata la trama della risorsa originale. |
| [**\_Utilizzo delle risorse di d2d1 \_**](/previous-versions/windows/desktop/legacy/hh404326(v=vs.85)) | Descrive la memoria utilizzata dalle trame dell'immagine e dagli shader. |
| [**\_Proprietà di \_ destinazione di rendering d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) | Contiene le opzioni di rendering (hardware o software), il formato pixel, le informazioni DPI, le opzioni remote e i requisiti di supporto Direct3D per una destinazione di rendering.  |
| [**\_Controlli di rendering d2d1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_rendering_controls) | Descrive le limitazioni da applicare al renderer di un effetto di imaging. |
| [**\_Rect d2d1 arrotondato \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_rounded_rect) | Contiene le dimensioni e il raggio dell'angolo di un rettangolo arrotondato. |
| [**\_ \_ Profilo colore semplice \_ d2d1**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_simple_color_profile) | Descrizione semplice di uno spazio colore. |
| [**\_Dimensioni d2d1 \_ F**](d2d1-size-f.md) | Archivia una coppia ordinata di float, in genere la larghezza e l'altezza di un rettangolo. |
| [**D2D1 \_ dimensioni \_ U**](d2d1-size-u.md) | Memorizza una coppia ordinata di interi, generalmente la larghezza e l'altezza di un rettangolo. |
| [**\_ \_ Proprietà stile tratto \_ d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_stroke_style_properties) | Descrive il tratto che delinea una forma.  |
| [**\_ \_ PROPERTIES1 stile tratto \_ d2d1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_stroke_style_properties1) | Descrive il tratto che delinea una forma. |
| [**\_Lunghezza SVG \_ d2d1**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_length) | Rappresenta una lunghezza SVG. |
| [**Proporzioni D2D1 \_ SVG \_ Preserve \_ \_**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_preserve_aspect_ratio) | Rappresenta tutte le impostazioni preserveAspectRatio SVG. |
| [**D2D1 \_ SVG \_ VIEWBOX**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_viewbox) | Rappresenta un viewBox SVG. |
| [**D2D1 le \_ proprietà di \_ origine dell'immagine trasformate \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_transformed_image_source_properties) | Proprietà di un'origine immagine trasformata. |
| [**\_Triangolo d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_triangle) | Contiene i tre vertici che descrivono un triangolo. |
| [**D2D1 \_ vector \_ 2F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_2f) | Vettore di 2 valori FLOAT (x, y). |
| [**\_Vettore d2d1 \_ 3F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_3f) | Vettore di 3 valori FLOAT (x, y, z). |
| [**D2D1 \_ vector \_ 4F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_4f) | Vettore di 4 valori FLOAT (x, y, z, w). |
| [**\_Proprietà del \_ buffer \_ Vertex d2d1**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_buffer_properties) | Definisce le proprietà di un buffer di vertice che sono standard per tutte le definizioni del vertex shader. |
| [**\_Intervallo vertici d2d1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_range) | Definisce un intervallo di vertici utilizzati quando il rendering è inferiore al contenuto completo di un buffer del vertice. |
| [**D3DCOLORVALUE**](/previous-versions/windows/desktop/legacy/dd368193(v=vs.85)) | Archivia le informazioni relative al colore e al canale alfa. |
| [*\_Factory effetti \_ PD2D1*](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) | Viene descritta l'implementazione di un effetto. |