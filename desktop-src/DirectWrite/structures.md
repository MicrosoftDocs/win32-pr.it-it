---
title: Strutture DirectWrite
description: DirectWrite definisce le strutture seguenti.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea132cde1ea6b740cc02b938767f941e9c999e5a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320344"
---
# <a name="directwrite-structures"></a>Strutture DirectWrite

DirectWrite definisce le strutture seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md) | Rappresenta i dati bitmap nel formato BGRA32. |
| [**\_metriche del cursore \_ DWrite**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | La [**struttura \_ \_ metrica del cursore DWrite**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) specifica le metriche per la posizione del punto di inserimento in un tipo di carattere. |
| [**\_metriche del cluster DWrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Contiene informazioni su un cluster di glifi. |
| [**DWRITE \_ colore \_ F**](dwrite-color-f.md) | Descrive i componenti rosso, verde, blu e alfa di un colore. |
| [**\_esecuzione del \_ glifo \_ colore DWrite**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Contiene le informazioni necessarie per i renderer per disegnare le esecuzioni di glifi con informazioni sul colore del glifo. |
| [**\_Glifo colori \_ DWrite \_ run1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Rappresenta un glifo di colore eseguito. Il metodo IDWriteFactory4:: TranslateColorGlyphRun restituisce una raccolta ordinata di esecuzioni del glifo dei colori di tipi diversi a seconda del tipo di carattere supportato da. |
| [**\_frammento di file DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Rappresenta un intervallo di byte in un file del tipo di carattere. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Rappresenta l'intervallo minimo e massimo dei valori possibili per un asse del tipo di carattere. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Rappresenta un valore per un asse dei tipi di carattere. Utilizzato durante l'esecuzione di query e la creazione di istanze del tipo di carattere. |
| [**\_funzionalità del tipo di carattere DWrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Specifica le proprietà utilizzate per identificare ed eseguire le funzionalità tipografiche nel tipo di carattere corrente. |
| [**\_metriche dei tipi di carattere DWrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | La struttura della [**\_ \_ metrica del tipo di carattere DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) specifica le metriche applicabili a tutti i glifi all'interno del tipo di carattere. |
| [**\_METRICS1 del tipo di carattere DWrite \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | La [**struttura \_ \_ METRICS1 del tipo di carattere DWrite**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) specifica le metriche applicabili a tutti i glifi all'interno del tipo di carattere. |
| [**\_proprietà del tipo di carattere DWrite \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Proprietà Font utilizzata per filtrare i set di caratteri e compilare un set di caratteri con proprietà esplicite. |
| [**\_ \_ dati immagine glifo \_ DWrite**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Dati per un singolo glifo da GetGlyphImageData. |
| [**\_metriche del glifo DWrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Specifica le metriche di un singolo glifo. |
| [**\_offset glifo \_ DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | Regolazione facoltativa della posizione di un glifo. |
| [**\_esecuzione del glifo DWrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Contiene le informazioni necessarie per i renderer per disegnare le esecuzioni di glifi. |
| [**\_Descrizione dell' \_ esecuzione del glifo DWrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Contiene proprietà aggiuntive correlate a quelle nell' [**\_ \_ esecuzione del glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run). |
| [**\_metriche di hit \_ test \_ DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Descrive l'area ottenuta da un hit test. |
| [**\_metriche oggetto inline DWrite \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Contiene proprietà che descrivono la misurazione geometrica di un oggetto inline definito dall'applicazione. |
| [**\_opportunità di giustificazione DWrite \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | La struttura di [**\_ \_ opportunità di giustificazione DWrite**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) specifica le informazioni di giustificazione per glifo. |
| [**punto \_ di \_ interruzione riga DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Caratteristiche dei punti di interruzione di riga di un carattere. |
| [**\_metriche linea \_ DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Contiene informazioni su una riga di testo formattata. |
| [**\_METRICS1 riga \_ DWrite**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Contiene informazioni su una riga di testo formattata. |
| [**interlinea DWRITE \_ \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**\_matrice DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | La struttura della [**\_ matrice DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) specifica la trasformazione grafica da applicare alle icone sottoposte a rendering. |
| [**\_metriche di sporgenza DWrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Indica il modo in cui qualsiasi DIP visibile (device independent pixel) supera ogni lato del layout o degli oggetti inline. |
| [**DWRITE \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | L'Unione [**DWrite \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) descrive i valori di classificazione dei caratteri tipografici usati con [**IDWriteFont1:: getpanoe**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) per selezionare e trovare la corrispondenza con il tipo di carattere. |
| [**\_analisi degli script DWrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Archivia l'associazione di testo e il relativo script del sistema di scrittura, oltre ad alcuni attributi di visualizzazione. |
| [**\_proprietà script \_ DWrite**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | La struttura delle [**\_ \_ proprietà dello script DWrite**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) specifica le proprietà dello script per la navigazione e la giustificazione del cursore. |
| [**DWRITE \_ shaping \_ ( \_ Proprietà glifo)**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Contiene la definizione delle proprietà di output per un glifo di output. |
| [**DWRITE \_ shaping \_ delle \_ proprietà di testo**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Shaping delle proprietà di output per un glifo di output. |
| [**\_barrato DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Contiene informazioni relative alle dimensioni e al posizionamento dei strikethroughs. |
| [**\_metrica testo \_ DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Contiene le metriche associate al testo dopo il layout. |
| [**\_METRICS1 testo \_ DWrite**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Contiene le metriche associate al testo dopo il layout. |
| [**\_intervallo di testo DWrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Specifica un intervallo di posizioni del testo in cui il formato viene applicato nel testo rappresentato da un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . |
| [**\_taglio DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Specifica l'opzione di trimming per il testo che fuoriesce dalla casella di layout.  |
| [**\_funzionalità tipografiche DWrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Contiene un set di funzionalità tipografiche da applicare durante il shaping del testo. |
| [**\_sottolineatura DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Contiene informazioni sulla larghezza, lo spessore, l'offset, l'altezza di esecuzione, la direzione di lettura e la direzione di flusso di una sottolineatura.  |
| [**DWRITE \_ \_ intervallo Unicode**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | La struttura dell' [**\_ \_ intervallo Unicode DWrite**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) specifica l'intervallo di punti di codice Unicode. |



 

