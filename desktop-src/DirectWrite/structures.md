---
title: DirectWrite strutture
description: DirectWrite definisce le strutture seguenti.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite,strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa3d4d98588e3585022bb0887c6224e29d67e0c0d011437526b33ff0bcf1334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815954"
---
# <a name="directwrite-structures"></a>DirectWrite strutture

DirectWrite definisce le strutture seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32) | Rappresenta i dati bitmap in formato BGRA32. |
| [**METRICHE DEL \_ CARET \_ DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | La [**struttura DWRITE \_ CARET \_ METRICS**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) specifica le metriche per il posizionamento del punto di inserimento in un tipo di carattere. |
| [**METRICHE DEL \_ CLUSTER \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Contiene informazioni su un cluster di glifi. |
| [**COLORE DWRITE \_ \_ F**](dwrite-color-f.md) | Descrive i componenti rosso, verde, blu e alfa di un colore. |
| [**ESECUZIONE DEL \_ \_ GLIFO A COLORI \_ DWRITE**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Contiene le informazioni necessarie ai renderer per disegnare esecuzioni di glifi con informazioni sul colore dei glifi. |
| [**DWRITE \_ COLOR \_ GLYPH \_ RUN1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Rappresenta una combinazione di glifi a colori. Il metodo IDWriteFactory4::TranslateColorGlyphRun restituisce una raccolta ordinata di esecuzioni di glifi a colori di tipi diversi a seconda del tipo di carattere che supporta. |
| [**FRAMMENTO \_ DI FILE \_ DWRITE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Rappresenta un intervallo di byte in un file del tipo di carattere. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Rappresenta l'intervallo minimo e massimo dei valori possibili per un asse del tipo di carattere. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Rappresenta un valore per un asse del tipo di carattere. Usato durante l'esecuzione di query e la creazione di istanze del tipo di carattere. |
| [**FUNZIONALITÀ DEL TIPO \_ DI CARATTERE \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Specifica le proprietà utilizzate per identificare ed eseguire caratteristiche tipografiche nel tipo di carattere corrente. |
| [**METRICHE DEI \_ TIPI DI CARATTERE \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | La [**struttura DWRITE \_ FONT \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) specifica le metriche applicabili a tutti i glifi all'interno del tipo di carattere. |
| [**METRICHE DEI \_ TIPI DI CARATTERE \_ DWRITE1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | La [**struttura DWRITE \_ FONT \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) specifica le metriche applicabili a tutti i glifi all'interno del tipo di carattere. |
| [**PROPRIETÀ FONT DI \_ \_ DWRITE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Proprietà Font usata per filtrare i set di caratteri e compilare un set di caratteri con proprietà esplicite. |
| [**DWRITE GLYPH IMAGE DATA (DWRITE \_ GLYPH \_ IMAGE \_ DATA)**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Dati per un singolo glifo da GetGlyphImageData. |
| [**METRICHE DEL \_ GLIFO \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Specifica le metriche di un singolo glifo. |
| [**OFFSET \_ DEL GLIFO DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | Regolazione facoltativa della posizione di un glifo. |
| [**ESECUZIONE \_ DEL GLIFO \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Contiene le informazioni necessarie ai renderer per disegnare le esecuzioni di glifi. |
| [**DESCRIZIONE \_ DELL'ESECUZIONE DEL \_ GLIFO DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Contiene proprietà aggiuntive correlate a quelle in [**DWRITE \_ GLYPH \_ RUN.**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) |
| [**METRICHE DI \_ HIT \_ TEST DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Descrive l'area ottenuta da un hit test. |
| [**DWRITE INLINE OBJECT METRICS (METRICHE DEGLI OGGETTI INLINE DI \_ \_ \_ SCRITTURA)**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Contiene proprietà che descrivono la misura geometrica di un oggetto inline definito dall'applicazione. |
| [**OPPORTUNITÀ DI \_ GIUSTIFICAZIONE DELLA SCRITTURA \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | La [**struttura DWRITE \_ JUSTIFICATION \_ OPPORTUNITY**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) specifica le informazioni di giustificazione per ogni glifo. |
| [**PUNTO DI \_ INTERRUZIONE RIGA DI \_ SCRITTURA**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Caratteristiche del punto di interruzione riga di un carattere. |
| [**METRICHE DI DWRITE \_ \_ LINE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Contiene informazioni su una riga di testo formattata. |
| [**DWRITE \_ LINE \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Contiene informazioni su una riga di testo formattata. |
| [**DWRITE \_ LINE \_ SPACING**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**MATRICE DI SCRITTURA \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | La [**struttura DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) specifica la trasformazione grafica da applicare ai glifi sottoposti a rendering. |
| [**DWRITE \_ OVERHANG \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Indica il livello di overhoot di tutti i DIP visibili (DIP indipendenti dal dispositivo) su ogni lato del layout o degli oggetti inline. |
| [**DWRITE \_ PANOSE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | [**L'unione DWRITE \_ PANOSE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) descrive i valori di classificazione dei caratteri tipografici utilizzati con [**IDWriteFont1::GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) per selezionare e associare il tipo di carattere. |
| [**ANALISI DEGLI SCRIPT DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Archivia l'associazione del testo e il relativo script di sistema di scrittura, nonché alcuni attributi di visualizzazione. |
| [**PROPRIETÀ DELLO \_ SCRIPT \_ DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | La [**struttura DWRITE \_ SCRIPT \_ PROPERTIES**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) specifica le proprietà dello script per la navigazione e la giustificazione del caret. |
| [**PROPRIETÀ DEL \_ \_ GLIFO DWRITE SHAPING \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Contiene le proprietà di output di shaping per un glifo di output. |
| [**PROPRIETÀ DI DATA \_ SHAPING \_ DEL \_ TESTO**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Proprietà di output di data shaping per un glifo di output. |
| [**DWRITE \_ STRIKETHROUGH**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Contiene informazioni relative alle dimensioni e alla posizione dei barrati. |
| [**METRICHE DI \_ SCRITTURA \_ DEL TESTO**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Contiene le metriche associate al testo dopo il layout. |
| [**DWRITE \_ TEXT \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Contiene le metriche associate al testo dopo il layout. |
| [**DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Specifica un intervallo di posizioni di testo in cui il formato viene applicato nel testo rappresentato da un [**oggetto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) |
| [**RIMOZIONE \_ DI DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Specifica l'opzione di taglio per il testo che causa l'overflow della casella di layout.  |
| [**CARATTERISTICHE \_ TIPOGRAFICHE DI \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Contiene un set di caratteristiche tipografiche da applicare durante la modellazione del testo. |
| [**SOTTOLINEATURA \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Contiene informazioni su larghezza, spessore, offset, altezza di esecuzione, direzione di lettura e direzione di flusso di una sottolineatura.  |
| [**DWRITE \_ UNICODE \_ RANGE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | La [**struttura DWRITE \_ UNICODE \_ RANGE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) specifica l'intervallo di punti di codice Unicode. |



 

