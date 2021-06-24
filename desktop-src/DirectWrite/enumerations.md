---
title: Enumerazioni DirectWrite
description: DirectWrite definisce le enumerazioni seguenti.
ms.assetid: 809ccacd-ff23-4d7b-a177-e7a9937c0c5a
keywords:
- DirectWrite, enumerazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf26901583a84e34d64a2a1c72fdfa17bbc903b
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587932"
---
# <a name="directwrite-enumerations"></a>Enumerazioni DirectWrite

DirectWrite definisce le enumerazioni seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes"><strong>DWRITE_AUTOMATIC_FONT_AXES</strong></a></td>
<td>Definisce costanti che specificano determinati assi che possono essere applicati automaticamente nel layout durante la selezione del tipo di carattere.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE</strong></a></td>
<td>L DWRITE_BASELINE enumere contiene valori che specificano la linea di base per l'allineamento del testo. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition"><strong>DWRITE_BREAK_CONDITION</strong></a></td>
<td>Indica la condizione ai bordi dell'oggetto inline o del testo utilizzato per determinare il comportamento di interruzione di riga.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_container_type"><strong>DWRITE_CONTAINER_TYPE</strong></a></td>
<td>Specifica il formato del contenitore di una risorsa tipo di carattere. Un formato contenitore è diverso da un formato di file di tipo di carattere (DWRITE_FONT_FILE_TYPE) perché il contenitore descrive il contenitore in cui è in pacchetto il file del tipo di carattere sottostante. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE</strong></a></td>
<td>Specifica il tipo di oggetto factory DirectWrite.</td>
</tr>
<tr>
<td><a href="/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE (DWriteCore)</strong></a></td>
<td>Specifica il tipo di oggetto factory DirectWrite.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction"><strong>DWRITE_FLOW_DIRECTION</strong></a></td>
<td>Indica la direzione di posizione delle righe di testo l'una rispetto all'altra. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes"><strong>DWRITE_FONT_AXIS_ATTRIBUTES</strong></a></td>
<td>Definisce costanti che specificano gli attributi per un asse del tipo di carattere.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag"><strong>DWRITE_FONT_AXIS_TAG</strong></a></td>
<td>Definisce costanti che specificano un identificatore di quattro caratteri per un asse del tipo di carattere.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_face_type"><strong>DWRITE_FONT_FACE_TYPE</strong></a></td>
<td>Indica il formato di file di un carattere completo.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model"><strong>DWRITE_FONT_FAMILY_MODEL</strong></a></td>
<td>Definisce costanti che specificano la modalità di raggruppamento delle famiglie di caratteri.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag"><strong>DWRITE_FONT_FEATURE_TAG</strong></a></td>
<td>Valore che indica la funzionalità tipografica del testo fornito dal tipo di carattere.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_file_type"><strong>DWRITE_FONT_FILE_TYPE</strong></a></td>
<td>Tipo di carattere rappresentato da un singolo file del tipo di carattere. Formati di carattere costituiti da più file, ad esempio Tipo 1. PFM e . PFB, hanno valori di enumerazione separati per ogni tipo di file.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage"><strong>DWRITE_FONT_LINE_GAP_USAGE</strong></a></td>
<td>Specificare se <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics"><strong>DWRITE_FONT_METRICS</strong></a>valore ::lineGap deve far parte delle metriche di riga</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id"><strong>DWRITE_FONT_PROPERTY_ID</strong></a></td>
<td>Identifica una stringa in un tipo di carattere.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations"><strong>DWRITE_FONT_SIMULATIONS</strong></a></td>
<td>Specifica simulazioni di stile algoritmico da applicare al viso del tipo di carattere. Le simulazioni in grassetto e obliqua possono essere combinate tramite l'operazione OR bit per bit.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type"><strong>DWRITE_FONT_SOURCE_TYPE</strong></a></td>
<td>Definisce costanti che specificano il meccanismo in base al quale un tipo di carattere deve essere incluso in un set di caratteri.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch"><strong>DWRITE_FONT_STRETCH</strong></a></td>
<td>Rappresenta il grado di estensione di un tipo di carattere rispetto alle normali proporzioni di un tipo di carattere.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style"><strong>DWRITE_FONT_STYLE</strong></a></td>
<td>Rappresenta lo stile di un tipo di carattere come normale, corsivo o obliqua.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight"><strong>DWRITE_FONT_WEIGHT</strong></a></td>
<td>Rappresenta la densità di un carattere tipografico, in termini di leggerezza o pesantezza dei tratti.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats"><strong>DWRITE_GLYPH_IMAGE_FORMATS</strong></a></td>
<td>Specifica i formati supportati nel tipo di carattere, a livello di carattere o per glifo.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE</strong></a></td>
<td>L DWRITE_GLYPH_ORIENTATION_ANGLE enumere contiene valori che specificano come il glifo è orientato all'asse x. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode"><strong>DWRITE_GRID_FIT_MODE</strong></a></td>
<td>Specifica se abilitare l'adattamento a griglia dei contorni dei glifi (noti anche come hint).</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id"><strong>DWRITE_INFORMATIONAL_STRING_ID</strong></a></td>
<td>Enumerazione di stringhe in formato informativo che identifica una stringa incorporata in un file del tipo di carattere.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method"><strong>DWRITE_LINE_SPACING_METHOD</strong></a></td>
<td>Metodo utilizzato per l'interlinea in un layout di testo.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality"><strong>DWRITE_LOCALITY</strong></a></td>
<td>Specifica il percorso di una risorsa.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode"><strong>DWRITE_MEASURING_MODE</strong></a></td>
<td>Indica il metodo di misurazione usato per il layout del testo.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_number_substitution_method"><strong>DWRITE_NUMBER_SUBSTITUTION_METHOD</strong></a></td>
<td>Specifica come applicare la sostituzione dei numeri alle cifre e alla punteggiatura correlata.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_optical_alignment"><strong>DWRITE_OPTICAL_ALIGNMENT</strong></a></td>
<td>Modalità di allineamento del margine ottico.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD</strong></a></td>
<td>L DWRITE_OUTLINE_THRESHOLD enumere contiene valori che specificano i criteri usati dal metodo <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getrecommendedrenderingmode"><strong>IDWriteFontFace1::GetRecommendedRenderingMode</strong></a> per determinare se eseguire il rendering dei glifi in modalità struttura. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE</strong></a></td>
<td>L DWRITE_PANOSE_ARM_STYLE enumere contiene valori che specificano lo stile di terminazione dei gambi e delle forme lettera arrotondate per il testo. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT</strong></a></td>
<td>L DWRITE_PANOSE_ASPECT enumerico contiene valori che specificano il rapporto tra la larghezza e l'altezza del viso del carattere. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO</strong></a></td>
<td>L DWRITE_PANOSE_ASPECT_RATIO enumerico contiene valori che specificano informazioni sul rapporto tra larghezza e altezza del viso del carattere. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES</strong></a></td>
<td>L DWRITE_PANOSE_CHARACTER_RANGES enumere contiene valori che specificano il tipo di caratteri disponibili nel tipo di carattere. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST</strong></a></td>
<td>L DWRITE_PANOSE_CONTRAST enumere contiene valori che specificano il rapporto tra il punto più spesso e il punto più sottile del tratto per una lettera, ad esempio "O" maiuscola. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS</strong></a></td>
<td>L DWRITE_PANOSE_DECORATIVE_CLASS enumere contiene valori che specificano l'aspetto generale del viso del carattere. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY</strong></a></td>
<td>L DWRITE_PANOSE_DECORATIVE_TOPOLOGY enumere contiene valori che specificano le caratteristiche di forma complessive del tipo di carattere. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY</strong></a></td>
<td>L DWRITE_PANOSE_FAMILY enumere contiene valori che specificano il tipo di classificazione dei caratteri tipografici. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL</strong></a></td>
<td>L DWRITE_PANOSE_FILL enumere contiene valori che specificano il tipo di trattamento di riempimento e linea. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS</strong></a></td>
<td>L DWRITE_PANOSE_FINIALS enumere contiene valori che specificano il modo in cui vengono trattati i caratteri terminati e gli ascendenti minuscoli. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM</strong></a></td>
<td>L DWRITE_PANOSE_LETTERFORM enumere contiene valori che specificano l'arrotondamento di letterform per il testo. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING</strong></a></td>
<td>L DWRITE_PANOSE_LINING enumere contiene valori che specificano la gestione del contorno per il carattere tipografico decorativo. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE</strong></a></td>
<td>L DWRITE_PANOSE_MIDLINE enumere contiene valori che specificano informazioni sulla posizione della linea mediana tra caratteri maiuscoli e sul trattamento dei apice di gambo diagonale. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION</strong></a></td>
<td>L DWRITE_PANOSE_PROPORTION enumere contiene valori che specificano la proporzione della forma del glifo considerando dettagli aggiuntivi rispetto ai caratteri standard. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM</strong></a></td>
<td>L DWRITE_PANOSE_SCRIPT_FORM enumere contiene valori che specificano l'aspetto generale del viso del carattere, con considerazione della pendenza e delle code. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY</strong></a></td>
<td>L DWRITE_PANOSE_SCRIPT_TOPOLOGY enumere contiene valori che specificano la topologia dei letterform. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE</strong></a></td>
<td>L DWRITE_PANOSE_SERIF_STYLE enumero contiene valori che specificano l'aspetto del testo serif. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING</strong></a></td>
<td>L DWRITE_PANOSE_SPACING enumere contiene valori che specificano la spaziatura tra caratteri (monospazio e proporzionale). <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION</strong></a></td>
<td>L DWRITE_PANOSE_STROKE_VARIATION enumere contiene valori che specificano la relazione tra i gambi thin e thick dei caratteri di testo. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</strong></a></td>
<td>L DWRITE_PANOSE_SYMBOL_ASPECT_RATIO enumere contiene valori che specificano le proporzioni dei caratteri simbolici. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND</strong></a></td>
<td>L DWRITE_PANOSE_SYMBOL_KIND enumere contiene valori che specificano il tipo di set di simboli. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND</strong></a></td>
<td>L DWRITE_PANOSE_TOOL_KIND enumere contiene valori che specificano il tipo di strumento usato per creare forme carattere. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT</strong></a></td>
<td>L DWRITE_PANOSE_WEIGHT enumere contiene valori che specificano il peso dei caratteri. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT</strong></a></td>
<td>L DWRITE_PANOSE_XASCENT enumere contiene valori che specificano le dimensioni relative delle lettere minuscole. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT</strong></a></td>
<td>L DWRITE_PANOSE_XHEIGHT enumere contiene valori che specificano informazioni sulla dimensione relativa delle lettere minuscole e sul trattamento dei segni diacritici (xheight). <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_paragraph_alignment"><strong>DWRITE_PARAGRAPH_ALIGNMENT</strong></a></td>
<td>Specifica l'allineamento del testo del paragrafo lungo l'asse di direzione del flusso, rispetto alla parte superiore e inferiore della casella di layout del flusso. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry"><strong>DWRITE_PIXEL_GEOMETRY</strong></a></td>
<td>Rappresenta la struttura interna di un pixel del dispositivo, ovvero la disposizione fisica dei componenti di colore rosso, verde e blu, che si presuppone ai fini del rendering del testo. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction"><strong>DWRITE_READING_DIRECTION</strong></a></td>
<td>Specifica la direzione di avanzamento della lettura. 
<blockquote>
[!Note]<br />
<strong>DWRITE_READING_DIRECTION_TOP_TO_BOTTOM</strong> e <strong>DWRITE_READING_DIRECTION_BOTTOM_TO_TOP</strong> sono disponibili solo in Windows 8.1 e versioni successive.
</blockquote>
</td>
</tr>
<tr>
<td><a href="/windows/win32/directwrite/dwrite-rendering-mode-enumerations">DWRITE_RENDERING_MODE enumerazioni</a></td>
<td>A partire da Windows 8, <strong>l'DWRITE_RENDERING_MODE</strong> ha aggiunto nuovi valori di enumerazione e ne ha deprecati altri.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_rendering_mode1"><strong>DWRITE_RENDERING_MODE1</strong></a></td>
<td>Specifica la modalità di rendering dei glifi.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_script_shapes"><strong>DWRITE_SCRIPT_SHAPES</strong></a></td>
<td>Indica requisiti di data shaping aggiuntivi per il testo.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment"><strong>DWRITE_TEXT_ALIGNMENT</strong></a></td>
<td>Specifica l'allineamento del testo del paragrafo lungo l'asse di direzione di lettura, rispetto al bordo iniziale e finale della casella di layout.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE</strong></a></td>
<td>L DWRITE_TEXT_ANTIALIAS_MODE enumere contiene valori che specificano il tipo di antialiasing da usare per il testo quando la modalità di rendering chiama l'antialiasing. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_texture_type"><strong>DWRITE_TEXTURE_TYPE</strong></a></td>
<td>Identifica un tipo di trama alfa.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_trimming_granularity"><strong>DWRITE_TRIMMING_GRANULARITY</strong></a></td>
<td>Specifica la granularità del testo utilizzata per tagliare il testo che trabocca la casella di layout.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION</strong></a></td>
<td>L DWRITE_VERTICAL_GLYPH_ORIENTATION enumere contiene valori che specificano il tipo desiderato di orientamento del glifo per il testo. <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong></strong></a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_word_wrapping"><strong>DWRITE_WORD_WRAPPING</strong></a></td>
<td>Specifica il ritorno a capo automatico da utilizzare in un particolare paragrafo su più righe. 
<blockquote>
[!Note]<br />
<strong>DWRITE_WORD_WRAPPING_EMERGENCY_BREAK,</strong> <strong>DWRITE_WORD_WRAPPING_WHOLE _WORD</strong>e <strong>DWRITE_WORD_WRAPPING_CHARACTER</strong> sono disponibili solo in Windows 8.1 e versioni successive.
</blockquote>
</td>
</tr>
</tbody>
</table>



 

 

 





