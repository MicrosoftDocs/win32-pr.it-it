---
title: Strutture Direct2D
description: Direct2D fornisce le strutture seguenti. Altre strutture sono definite nello spazio dei nomi D2D1.
ms.assetid: 6c34a8c8-4b0b-4a95-8f13-25ca25c370ba
keywords:
- Direct2D, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6be3735335abc5b9242ec150ac583f837ae5c15936aaca677b322526b1c19f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537701"
---
# <a name="direct2d-structures"></a>Strutture Direct2D

Direct2D fornisce le strutture seguenti. Altre strutture sono definite nello spazio dei [nomi D2D1](d2d1-namespace.md).

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**COLORE D2D \_ \_ F**](d2d-color-f.md) | Descrive i componenti rosso, verde, blu e alfa di un colore. |
| [**MATRICE D2D \_ \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) | Rappresenta una matrice 3 per 2. |
| [**MATRICE D2D \_ \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f) | Descrive una matrice a virgola mobile 4 per 3. |
| [**MATRICE D2D \_ \_ 4X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f) | Descrive una matrice a virgola mobile 4 per 4. |
| [**MATRICE D2D \_ \_ 5X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f) | Descrive una matrice a virgola mobile 5 per 4. |
| [**PUNTO D2D \_ \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f) | Rappresenta una coppia di coordinate x e y, espresse come valori a virgola mobile, nello spazio bidimensionale. |
| [**PUNTO D2D \_ \_ 2L**](/previous-versions/windows/desktop/legacy/jj219217(v=vs.85)) | La struttura D2D \_ POINT \_ 2L definisce le coordinate x e y di un punto. |
| [**PUNTO D2D \_ \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u) | Rappresenta una coppia di coordinate x e y, espressa come valore intero senza segno a 32 bit, nello spazio bidimensionale. |
| [**D2D \_ RECT \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) | Rappresenta un rettangolo definito dalle coordinate dell'angolo superiore sinistro (sinistra, superiore) e dalle coordinate dell'angolo inferiore destro (destra, inferiore).  |
| [**D2D \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) | La [**struttura D2D \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) definisce le coordinate degli angoli superiore sinistro e inferiore destro di un rettangolo. |
| [**D2D \_ RECT \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_u) | Rappresenta un rettangolo definito dalla coppia di coordinate dell'angolo superiore sinistro (sinistra, superiore) e dall'angolo inferiore destro delle coordinate (destra, inferiore). Queste coordinate sono espresse come valori interi a 32 bit. |
| [**DIMENSIONI D2D \_ \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f) | Archivia una coppia ordinata di valori a virgola mobile, in genere la larghezza e l'altezza di un rettangolo.  |
| [**DIMENSIONI D2D \_ \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u) | Memorizza una coppia ordinata di interi, generalmente la larghezza e l'altezza di un rettangolo. |
| [**VETTORE D2D \_ \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f) | Vettore 2D costituito da due valori a virgola mobile a precisione singola (x, y).  |
| [**VETTORE D2D \_ \_ 3F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f) | Vettore 3D costituito da tre valori a virgola mobile a precisione singola (x, y, z). |
| [**VETTORE D2D \_ \_ 4F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f) | Vettore 4D costituito da quattro valori a virgola mobile a precisione singola (x, y, z, w). |
| [**SEGMENTO ARC \_ D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_arc_segment) | Descrive un arco ellittico tra due punti. |
| [**SEGMENTO DI BÉZIER D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) | Rappresenta un segmento di Bézier cubico disegnato tra due punti. |
| [**PROPRIETÀ DEL PENNELLO BITMAP D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) | Descrive le modalità di estensione e la modalità di interpolazione di [**un oggetto ID2D1BitmapBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) |
| [**PROPRIETÀ PENNELLO \_ BITMAP D2D111 \_ \_**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1) | Descrive le modalità di estensione e la modalità di interpolazione di [**un oggetto ID2D1BitmapBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) |
| [**PROPRIETÀ BITMAP \_ D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) | Descrive il formato pixel e il dpi di una bitmap. |
| [**PROPRIETÀ BITMAP \_ D2D111 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) | Questa struttura consente di creare [**un oggetto ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1) con le opzioni bitmap e le informazioni sul contesto dei colori disponibili.  |
| [**DESCRIZIONE DI D2D1 \_ \_ BLEND**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) | Definisce una descrizione di blend da usare in una particolare trasformazione di blend. |
| [**PROPRIETÀ DEL PENNELLO D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties) | Descrive l'opacità e la trasformazione di un pennello. |
| [**COLORE D2D1 \_ \_ F**](d2d1-color-f.md) | Descrive i componenti rosso, verde, blu e alfa di un colore. |
| [**PROPRIETÀ DI CREAZIONE D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_creation_properties) | Specifica le opzioni con cui vengono creati [il dispositivo Direct2D,](./direct2d-portal.md) la factory e il contesto di dispositivo.  |
| [**PROPRIETÀ PERSONALIZZATE DEL \_ \_ \_ VERTEX BUFFER \_ D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_custom_vertex_buffer_properties) | Definisce un vertex shader e la descrizione dell'elemento di input per definire il layout di input. |
| [**DESCRIZIONE DELLO STATO DEL DISEGNO D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description) | Descrive lo stato di disegno di una destinazione di rendering.  |
| [**D2D1 \_ DRAWING \_ STATE \_ DESCRIPTION1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_drawing_state_description1) | Descrive lo stato di disegno di un contesto di dispositivo. |
| [**DESCRIZIONE \_ DELL'INPUT DELL'EFFETTO D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_effect_input_description) | Descrive le funzionalità di un effetto. |
| [**ELLISSE \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) | Contiene il punto centrale, il raggio x e il raggio y di un'ellisse. |
| [**OPZIONI FACTORY \_ D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_factory_options) | Contiene il livello di debug di un [**oggetto ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)  |
| [**D2D1 \_ FEATURE \_ DATA \_ DOUBLES**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_doubles) | Descrive il supporto per i valori double negli shader. |
| [**D2D1 \_ FEATURE \_ DATA \_ D3D10 X HARDWARE OPTIONS (OPZIONI HARDWARE D2D1 FEATURE DATA D3D10 \_ \_ \_ X)**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_d3d10_x_hardware_options) | Descrive il supporto dello shader di calcolo, che è un'opzione a livello di funzionalità D3D10. |
| [**PATCH DI MESH \_ SFUMATO D2D1 \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) | Rappresenta una patch tensore con 16 punti di controllo, 4 colori d'angolo e flag limite. Id2D1GradientMesh è costituito da 1 o più patch di mesh sfumato. Usare la [**funzione GradientMeshPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatch) o [**GradientMeshPatchFromCoonsPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatchfromcoonspatch) per crearne una.  |
| [**CURSORE SFUMATURA D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) | Contiene la posizione e il colore di un cursore sfumatura.  |
| [**PROPRIETÀ DELLA DESTINAZIONE \_ DI RENDERING HWND D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) | Contiene le opzioni HWND, dimensioni in pixel e presentazione per [**id2D1HwndRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) |
| [**PROPRIETÀ DELLO STILE INPUT PENNA D2D1 \_ \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties) | Definisce la forma generale della punta della penna e la trasformazione usata in un [**oggetto ID2D1InkStyle.**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)  |
| [**PROPRIETÀ DEL \_ PENNELLO IMMAGINE D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_image_brush_properties) | Descrive le funzionalità del pennello immagine. |
| [**SEGMENTO DI \_ BÉZIER INPUT PENNA D2D1 \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment) | Rappresenta un segmento di Bézier da utilizzare nella creazione di un [**oggetto ID2D1Ink.**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink) Questa struttura è diversa da [**D2D1 \_ BEZIER \_ SEGMENT**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) in quanto è composta da [**D2D1 \_ INK \_ POINT**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point)s, che contengono un raggio oltre alle coordinate x e y.  |
| [**PUNTO INPUT PENNA D2D1 \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point) | Rappresenta una coppia di punti e raggio che costituisce parte di un SEGMENTO [**\_ DI \_ BÉZIER \_ INK D2D1**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment). |
| [**DESCRIZIONE INPUT D2D1 \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_description) | Descrive le opzioni che le trasformazioni possono impostare nelle trame di input. |
| [**ELEMENTO DI \_ INPUT D2D1 \_ \_ DESC**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_element_desc) | Descrizione di un singolo elemento nel layout dei vertici. |
| [**PARAMETRI DEL LIVELLO D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) | Contiene i limiti di contenuto, le informazioni sulla maschera, le impostazioni di opacità e altre opzioni per una risorsa livello.  |
| [**PARAMETRI LIVELLO \_ D2D111 \_**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) | Contiene i limiti di contenuto, le informazioni sulla maschera, le impostazioni di opacità e altre opzioni per una risorsa livello. |
| [**PROPRIETÀ DEL PENNELLO A \_ \_ SFUMATURA \_ \_ LINEARE D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) | Contiene il punto iniziale e l'endpoint dell'asse sfumatura per [**un oggetto ID2D1LinearGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)  |
| [**D2D1 \_ MATRIX \_ 3X2 \_ F**](d2d1-matrix-3x2-f.md) | Rappresenta una matrice 3 per 2.  |
| [**D2D1 \_ MATRIX \_ 4X3 \_ F**](d2d1-matrix-4x3-f.md) | Rappresenta una matrice 4 per 3.  |
| [**D2D1 \_ MATRIX \_ 4X4 \_ F**](d2d1-matrix-4x4-f.md) | Rappresenta una matrice 4 per 4.  |
| [**D2D1 \_ MATRIX \_ 5X4 \_ F**](d2d1-matrix-5x4-f.md) | Rappresenta una matrice 5 per 4.  |
| [**RECT MAPPATO D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_mapped_rect) | Descrive la memoria mappata dall'API [**ID2D1Bitmap1::Map.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map) |
| [**FORMATO PIXEL D2D1 \_ \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) | Contiene il formato dati e la modalità alfa per una bitmap o una destinazione di rendering.  |
| [**D2D1 \_ POINT \_ 2F**](d2d1-point-2f.md) | Rappresenta una coppia di coordinate x e y nello spazio bidimensionale. |
| [**D2D1 \_ POINT \_ 2L**](/previous-versions/windows/desktop/legacy/hh847948(v=vs.85)) | La struttura POINT definisce le coordinate x e y di un punto. |
| [**D2D1 \_ POINT \_ 2U**](d2d1-point-2u.md) | Rappresenta una coppia di coordinate x e y nello spazio bidimensionale.  |
| [**DESCRIZIONE DEL PUNTO D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_point_description) | Descrive un punto su una geometria di percorso. |
| [**PROPRIETÀ DEL CONTROLLO DI STAMPA D2D1 \_ \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_print_control_properties) | Proprietà di creazione per un [**oggetto ID2D1PrintControl.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) |
| [**ASSOCIAZIONE DI PROPRIETÀ D2D1 \_ \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) | Definisce un'associazione di proprietà a una coppia di funzioni che ottengono e impostano la proprietà corrispondente.  |
| [**SEGMENTO DI \_ \_ BÉZIER \_ QUADRATICO D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_quadratic_bezier_segment) | Contiene il punto di controllo e il punto finale per un segmento di Bézier quadratico. |
| [**PROPRIETÀ DEL PENNELLO \_ SFUMATURA RADIALE D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) | Contiene l'offset dell'origine della sfumatura e le dimensioni e la posizione dell'ellisse sfumatura per [**un oggetto ID2D1RadialGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)  |
| [**D2D1 \_ RECT \_ F**](d2d1-rect-f.md) | Rappresenta un rettangolo definito dalle coordinate dell'angolo superiore sinistro (sinistra, superiore) e dalle coordinate dell'angolo inferiore destro (destra, inferiore).  |
| [**D2D1 \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)) | La struttura RECT definisce le coordinate degli angoli superiore sinistro e inferiore destro di un rettangolo. |
| [**D2D1 \_ RECT \_ U**](d2d1-rect-u.md) | Rappresenta un rettangolo definito dalle coordinate dell'angolo superiore sinistro (sinistra, superiore) e dalle coordinate dell'angolo inferiore destro (destra, inferiore).  |
| [**PROPRIETÀ TRAMA RISORSA D2D1 \_ \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_resource_texture_properties) | Definisce una trama di risorse quando viene creata la trama della risorsa originale. |
| [**UTILIZZO DELLE RISORSE D2D1 \_ \_**](/previous-versions/windows/desktop/legacy/hh404326(v=vs.85)) | Descrive la memoria usata dalle trame delle immagini e dagli shader. |
| [**PROPRIETÀ DELLA DESTINAZIONE DI RENDERING D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) | Contiene le opzioni di rendering (hardware o software), il formato pixel, le informazioni DPI, le opzioni di comunicazione remota e i requisiti di supporto Direct3D per una destinazione di rendering.  |
| [**CONTROLLI DI RENDERING D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_rendering_controls) | Descrive le limitazioni da applicare a un renderer dell'effetto di creazione dell'immagine. |
| [**RETTANGOLO ARROTONDATO D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_rounded_rect) | Contiene le dimensioni e i raggi d'angolo di un rettangolo arrotondato. |
| [**PROFILO COLORI SEMPLICE D2D1 \_ \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_simple_color_profile) | Descrizione semplice di uno spazio colore. |
| [**D2D1 \_ SIZE \_ F**](d2d1-size-f.md) | Archivia una coppia ordinata di valori float, in genere la larghezza e l'altezza di un rettangolo. |
| [**D2D1 \_ SIZE \_ U**](d2d1-size-u.md) | Memorizza una coppia ordinata di interi, generalmente la larghezza e l'altezza di un rettangolo. |
| [**PROPRIETÀ DELLO STILE DEL TRATTO D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_stroke_style_properties) | Descrive il tratto che delinea una forma.  |
| [**PROPRIETÀ STILE \_ TRATTO D2D111 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_stroke_style_properties1) | Descrive il tratto che delinea una forma. |
| [**LUNGHEZZA D2D1 \_ \_ SVG**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_length) | Rappresenta una lunghezza SVG. |
| [**D2D1 \_ SVG \_ PRESERVE \_ ASPECT \_ RATIO**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_preserve_aspect_ratio) | Rappresenta tutte le impostazioni SVG preserveAspectRatio. |
| [**D2D1 \_ SVG \_ VIEWBOX**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_viewbox) | Rappresenta un oggetto viewBox SVG. |
| [**PROPRIETÀ ORIGINE IMMAGINE \_ TRASFORMATA D2D1 \_ \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_transformed_image_source_properties) | Proprietà di un'origine immagine trasformata. |
| [**TRIANGOLO D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_triangle) | Contiene i tre vertici che descrivono un triangolo. |
| [**VETTORE D2D1 \_ \_ 2F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_2f) | Vettore di 2 valori FLOAT (x, y). |
| [**D2D1 \_ VECTOR \_ 3F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_3f) | Vettore di 3 valori FLOAT (x, y, z). |
| [**D2D1 \_ VECTOR \_ 4F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_4f) | Vettore di 4 valori FLOAT (x, y, z, w). |
| [**PROPRIETÀ DEL \_ \_ VERTEX BUFFER D2D1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_buffer_properties) | Definisce le proprietà di un vertex buffer standard per tutte le definizioni di vertex shader. |
| [**INTERVALLO DI VERTICI D2D1 \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_range) | Definisce un intervallo di vertici usati per il rendering inferiore al contenuto completo di un vertex buffer. |
| [**D3DCOLORVALUE**](/previous-versions/windows/desktop/legacy/dd368193(v=vs.85)) | Archivia le informazioni sui colori e sui canali alfa. |
| [*FACTORY DEGLI EFFETTI PD2D1 \_ \_*](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) | Descrive l'implementazione di un effetto. |