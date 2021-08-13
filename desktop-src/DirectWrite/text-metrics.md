---
title: Metriche di testo
description: Per facilitare il layout, la selezione personalizzata dei tipi di carattere e altre operazioni a elevato utilizzo di metriche, a partire da Windows 8, DirectWrite include una serie di nuove API per esprimere tutte le informazioni sui tipi di carattere che potrebbero essere necessarie per sviluppare app di testo RTF.
ms.assetid: 9df8c675-6f4d-4de7-916e-7dc51f5f04aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e5c5eecce93eac3726195410cf5b215bd65de3d7e48248a68d6d96858f8fed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329241"
---
# <a name="text-metrics"></a>Metriche di testo

Per facilitare il layout, la selezione personalizzata dei tipi di carattere e altre operazioni a elevato utilizzo di metriche, a partire da [Windows 8, DirectWrite](direct-write-portal.md) include una serie di nuove API per esprimere tutte le informazioni sui tipi di carattere che potrebbero essere necessarie per sviluppare app di testo RTF.

## <a name="panose"></a>PANOSE

PANOSE è un sistema di classificazione visiva per l'identificazione dei caratteri tipografici. La classificazione PANOSE contiene informazioni sulla famiglia, lo stile serif, il peso, la proporzione, il contrasto, il tratto, lo stile del arm, l'altezza X e così via. Queste informazioni descrivono lo stile di visualizzazione del tipo di carattere. Queste informazioni sono importanti perché i tipi di carattere con valori PANOSE simili sono simili. Ciò è molto utile nelle situazioni in cui un tipo di carattere non è disponibile e l'app deve eseguire il fall back a un tipo di carattere disponibile. Il confronto dei valori PANOSE per i tipi di carattere consente di scegliere un tipo di carattere simile visivamente al tipo di carattere originale.

Per accedere alle informazioni PANOSE per un tipo di carattere, usare il metodo [**GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) sulle [**interfacce IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) e [**IDWriteFontFace1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) Questo metodo restituisce [**un'enumerazione DWRITE \_ PANOSE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_panose) che contiene tutte le informazioni PANOSE per quel tipo di carattere.

## <a name="additional-metrics"></a>Metriche aggiuntive

A partire Windows 8, [l'API DirectWrite](direct-write-portal.md) supporta anche una serie di nuove metriche per esprimere informazioni utili sui tipi di carattere per l'app. Queste nuove metriche includono queste informazioni.

-   Metriche del rettangolo di selezione del glifo a sinistra, a destra, in alto e in basso.
-   Posizionamento X e Y per gli elementi apice e pedice.
-   Informazioni sul ridimensionamento X e Y per gli elementi apice e pedice.
-   Indica se il tipo di carattere ha metriche tipografiche.

Queste informazioni sono tutte disponibili tramite il nuovo [**metodo GetMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics) nelle [**interfacce IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) Questo metodo restituisce una [**struttura DWRITE \_ FONT \_ METRICS1**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_font_metrics1) che contiene tutte queste informazioni.

## <a name="caret-metrics"></a>Metriche del caret

Per creare app di modifica del testo, è necessario accedere alle informazioni su come disegnare il punto di controllo che consente di spostarsi all'interno del testo. A partire Windows 8, [DirectWrite](direct-write-portal.md) metodo [**GetCaretMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics) sulle interfacce [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) per questo scenario. **GetCaretMetrics restituisce un'enumerazione** [**DWRITE \_ CARET \_ METRICS**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_caret_metrics) che contiene informazioni sul inclinazione e sull'offset per il punto di riferimento lungo la linea di base.

Queste informazioni sono particolarmente utili se si vuole essere in grado di ottenere il relativo inclinazione del caret in modo appropriato con testo in corsivo.

## <a name="monospaced-discoverability"></a>Individuabilità monospaziata

Le app che consentono agli utenti di scrivere codice computer usano spesso tipi di carattere a spaziatura monospazia al posto di tipi di carattere più tradizionali. È quindi possibile avere un maggiore controllo sulla selezione dei tipi di [carattere](direct-write-portal.md) nelle app correlate allo sviluppo, DirectWrite indica se un tipo di carattere è o meno monospazio tramite l'API. Il [**metodo IsMonospacedFont**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-ismonospacedfont) sull'interfaccia [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) restituisce un valore booleano che indica se il tipo di carattere è monospazio.

## <a name="font-name-matching"></a>Corrispondenza dei nomi dei tipi di carattere

Le app di testo RTF, ad esempio i lettori PDF, devono essere in grado di associare i tipi di carattere del contenuto ai tipi di carattere nel sistema, devono poter accedere ai nomi completi dei tipi di carattere in più formati. È quindi possibile trovare una corrispondenza migliore con [i DirectWrite](direct-write-portal.md) contiene un'enumerazione che esprime informazioni di denominazione complete su un tipo di carattere in molti formati.

L'enumerazione [**DWRITE \_ INFORMATIONAL \_ STRING ID \_ viene**](/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id) utilizzata per ottenere il nome completo, il nome PostScript e il nome CID PostScript di qualsiasi tipo di carattere nel sistema. Queste informazioni sono utili quando è necessario associare i tipi di carattere dell'app ai tipi di carattere appropriati nel sistema locale.

## <a name="glyph-advances"></a>Avanzamenti del glifo

Il **metodo GetGlyphAdvances** sulle interfacce [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) accetta il numero di glifi e gli indici su cui sono necessarie informazioni sugli avanzamenti e quindi restituisce gli avanzamenti per i glifi in questione.

## <a name="unicode-ranges"></a>Intervalli Unicode

Le app che vogliono gestire la propria selezione del tipo di carattere devono accedere agli intervalli Unicode supportati dal tipo di carattere. In questo modo, se un punto di codice Unicode non è supportato dal tipo di carattere, l'app può scegliere un tipo di carattere appropriato che contiene tale glifo. Senza queste informazioni, l'app può usare un tipo di carattere che non contiene tutti i glifi necessari per visualizzare le informazioni presenti.

Il [**metodo GetUnicodeRanges**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getunicoderanges) sulle interfacce [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) accetta il numero massimo di intervalli passati dal client e restituisce gli intervalli effettivi supportati dal tipo di carattere.

## <a name="eudc-font-collection"></a>Raccolta di tipi di carattere EUDC

Usare il [**metodo GetEudcFontCollection nell'interfaccia**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefactory1-geteudcfontcollection) [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) per accedere alla raccolta di tipi di carattere EUDC. Questo metodo funziona allo stesso modo di [**GetSystemFontCollection,**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection)ma restituisce invece un puntatore a una raccolta di tipi di carattere EUDC.

 

 