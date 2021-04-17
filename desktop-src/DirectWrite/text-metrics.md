---
title: Metrica testo
description: Per supportare il layout, la selezione dei tipi di carattere personalizzati e altre operazioni con utilizzo intensivo di metriche, a partire da Windows 8, DirectWrite include una serie di nuove API per esprimere tutte le informazioni sui tipi di carattere che potrebbero essere necessari per sviluppare app di testo RTF.
ms.assetid: 9df8c675-6f4d-4de7-916e-7dc51f5f04aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73647ae4521b23afb399a4c66c8b25cdc46ba1b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300371"
---
# <a name="text-metrics"></a>Metrica testo

Per supportare il layout, la selezione dei tipi di carattere personalizzati e altre operazioni con utilizzo intensivo di metriche, a partire da Windows 8, [DirectWrite](direct-write-portal.md) include una serie di nuove API per esprimere tutte le informazioni sui tipi di carattere che potrebbero essere necessari per sviluppare app di testo RTF.

## <a name="panose"></a>PANOSE

PANOse è un sistema di classificazione visiva per l'identificazione dei caratteri tipografici. La classificazione PANOa contiene informazioni sulla famiglia, lo stile Serif, il peso, la proporzione, il contrasto, il tratto, lo stile ARM, l'altezza X e così via. Queste informazioni descrivono lo stile di visualizzazione del tipo di carattere. Queste informazioni sono importanti perché i tipi di carattere con valori di PANOse simili hanno un aspetto simile. Questa operazione è molto utile in situazioni in cui un tipo di carattere non è disponibile e l'app deve eseguire il fallback a un tipo di carattere disponibile. Il confronto tra i valori di PANOse per i tipi di carattere consente di scegliere un tipo di carattere simile visivamente al tipo di carattere originale.

Per accedere alle informazioni relative a PANOl per un tipo di carattere, usare il metodo [**Getpanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) sulle interfacce [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) e [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) . Questo metodo restituisce un'enumerazione [**DWrite \_ Panose**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_panose) che contiene tutte le informazioni PANOSE per il tipo di carattere.

## <a name="additional-metrics"></a>Metriche aggiuntive

A partire da Windows 8, l'API di [DirectWrite](direct-write-portal.md) supporta anche una serie di nuove metriche per poter esprimere informazioni utili sui tipi di carattere per l'app. Queste nuove metriche includono queste informazioni.

-   Metriche del rettangolo di delimitazione dei glifi a sinistra, a destra, in alto e in basso.
-   Posizionamento X e Y per gli elementi apice e pedice.
-   Informazioni sul ridimensionamento X e Y per gli elementi apice e pedice.
-   Indica se il tipo di carattere è costituito da metriche tipografiche.

Queste informazioni sono tutte disponibili tramite il nuovo metodo [**GetMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics) sulle interfacce [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) . Questo metodo restituisce una [**struttura \_ \_ METRICS1 del tipo di carattere DWrite**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_font_metrics1) contenente tutte queste informazioni.

## <a name="caret-metrics"></a>Metriche del cursore

Per creare app di modifica del testo è necessario accedere alle informazioni su come creare il cursore che sposta il testo. A partire da Windows 8, [DirectWrite](direct-write-portal.md) fornisce il metodo [**GetCaretMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics) sulle interfacce [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) per questo scenario. **GetCaretMetrics** restituisce un' [**enumerazione \_ \_ metrica del cursore DWrite**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_caret_metrics) che contiene informazioni sulla pendenza e sull'offset per il punto di inserimento lungo la linea di base.

Queste informazioni sono particolarmente utili se si desidera essere in grado di applicare la pendenza del punto di inserimento in modo appropriato con il testo in corsivo.

## <a name="monospaced-discoverability"></a>Individuabilità a spaziatura fissa

Le app che consentono agli utenti di scrivere codice del computer spesso usano caratteri a spaziatura fissa al posto di tipi di carattere più tradizionali. Quindi, è possibile avere maggiore controllo sulla selezione dei tipi di carattere nelle app correlate allo sviluppo, [DirectWrite](direct-write-portal.md) esprime se un tipo di carattere è a spaziatura fissa tramite l'API. Il metodo [**IsMonospacedFont**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-ismonospacedfont) sull'interfaccia [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) restituisce un valore booleano che indica se il tipo di carattere è a spaziatura fissa.

## <a name="font-name-matching"></a>Corrispondenza dei nomi dei tipi di carattere

Per le app con testo RTF, ad esempio i lettori PDF, è necessario poter associare i tipi di carattere ai tipi di carattere del sistema e accedere ai nomi completi dei tipi di carattere in più formati. Per una migliore corrispondenza dei tipi di carattere, [DirectWrite](direct-write-portal.md) contiene un'enumerazione che esprime informazioni di denominazione complete su un tipo di carattere in molti formati.

usare l'enumerazione [**DWrite \_ Informational \_ String \_ ID**](/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id) per ottenere il nome completo, il nome del post-script e il nome CID del post-script di qualsiasi tipo di carattere nel sistema. Queste informazioni sono utili quando è necessario trovare la corrispondenza dei tipi di carattere nell'app con i tipi di carattere appropriati nel sistema locale.

## <a name="glyph-advances"></a>Avanzamenti glifo

Il metodo **GetGlyphAdvances** sulle interfacce [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) acquisisce il numero di glifi e gli indici necessari per anticipare le informazioni e quindi restituisce i progressi per i glifi in questione.

## <a name="unicode-ranges"></a>Intervalli Unicode

Le app che vogliono gestire la propria selezione dei tipi di carattere devono accedere agli intervalli Unicode supportati dal tipo di carattere. In questo modo, se un punto di riferimento Unicode non è supportato dal tipo di carattere, l'app può scegliere un tipo di carattere appropriato che contenga tale glifo. Senza queste informazioni, l'app può usare un tipo di carattere che non contiene tutti i glifi necessari per visualizzare le informazioni presenti.

Il metodo [**GetUnicodeRanges**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getunicoderanges) sulle interfacce [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) accetta il numero massimo di intervalli passati dal client e restituisce gli intervalli effettivi supportati dal tipo di carattere.

## <a name="eudc-font-collection"></a>Raccolta di tipi di carattere EUDC

Usare il metodo [**GetEudcFontCollection**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefactory1-geteudcfontcollection) sull'interfaccia [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) per accedere alla raccolta di tipi di carattere EUDC. Questo metodo funziona allo stesso modo di [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection), ma restituisce invece un puntatore a una raccolta di tipi di carattere EUDC.

 

 