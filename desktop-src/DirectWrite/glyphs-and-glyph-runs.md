---
title: Glifi e esecuzioni di glifi
description: I glifi e le esecuzioni di glifi sono disponibili al livello più basso di funzionalità dell'API DirectWrite, il livello di rendering dei glifi.
ms.assetid: e670cb65-1fcb-46fd-ac0b-02eaaaa51996
keywords:
- DirectWrite,glifi
- DirectWrite,esecuzioni di glifi
- esecuzioni di glifi
- icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39d1ca47249adf11f4e1e2072620f24553f7e299e0690c1cc147c4f74a4939f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902926"
---
# <a name="glyphs-and-glyph-runs"></a>Glifi e esecuzioni di glifi

I glifi e le esecuzioni di glifi sono disponibili al livello più basso di funzionalità dell'API [DirectWrite,](direct-write-portal.md) il livello di rendering dei glifi.

## <a name="glyphs"></a>Glifi

Un glifo è una rappresentazione fisica di un carattere in un determinato tipo di carattere. I caratteri possono avere molti glifi, con ogni tipo di carattere in un sistema che potenzialmente definisce un glifo diverso per tale carattere.

È anche possibile combinare due o più glifi in un singolo glifo. Questo processo è detto composizione di glifi. Questa operazione può essere eseguita anche nella direzione opposta, un singolo glifo suddiviso in più glifi, noto come scomposizione dei glifi.

### <a name="alternate-glyphs"></a>Glifi alternativi

I tipi di carattere possono fornire glifi alternativi per i caratteri, ad esempio i glifi alternativi stilistici per il tipo di carattere Pericles OpenType, come illustrato nello screenshot seguente. Il rendering dei caratteri 'A', 'E' e 'O' viene eseguito con glifi alternativi stilistici.

![Screenshot della "vecchia mitologia verde", con "a", "e" e "o" usando glifi alternativi](images/opentypealternateglyphs.png)

Un altro esempio di glifi alternativi sono glifi laviati. Lo screenshot seguente mostra glifi standard e dilavatura per il tipo di carattere Pescadero.

![Screenshot delle lettere da "a" a "n" nei glifi standard e lavati](images/opentypeswashstandard.png)

Le lavastoviglie e altre funzionalità tipografiche, inclusi glifi alternativi più elaborati, sono disponibili tramite [OpenType.](../intl/opentype-font-format.md) Le funzionalità tipografiche OpenType possono essere applicate a un intervallo di testo usando [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) e passando la costante di enumerazione [**DWRITE \_ FONT FEATURE \_ \_ TAG**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) associata alla funzionalità desiderata.

## <a name="glyph-runs"></a>Esecuzioni di glifi

Un'esecuzione di glifi rappresenta un set contiguo di glifi che hanno tutti la stessa faccia e dimensione del carattere, nonché lo stesso effetto di disegno client, se presente. La sottolineatura e il barrato non fanno parte dell'esecuzione del glifo per l'intervallo di testo a cui vengono applicati e vengono disegnati in un secondo momento. Anche gli oggetti inline, ad esempio le immagini, vengono disegnati separatamente, in quanto non fanno parte di un tipo di carattere.

### <a name="the-idwritefontface-interface"></a>Interfaccia IDWriteFontFace

[DirectWrite](direct-write-portal.md) lo stesso sistema per la classificazione dei caratteri di Windows Pesentation Foundation (WPF), quindi possono essere presenti più tipi di carattere fisici per ogni famiglia di caratteri. Un tipo di carattere, ad esempio l'interfaccia [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) in DirectWrite, rappresenta un tipo di carattere fisico, con uno spessore, un'inclinazione e un tratto specifici. Contiene il tipo di carattere viso, i riferimenti ai file appropriati, i dati di identificazione del viso e vari dati del tipo di carattere, ad esempio metriche, nomi e profili di glifi.

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) può essere creato direttamente da un nome di carattere o ottenuto da una raccolta di tipi di carattere.

### <a name="glyph-metrics"></a>Metrica del glifo

Ai singoli glifi sono associate metriche. È possibile ottenere le metriche per tutti i glifi in un glifo eseguito usando il metodo [**IDWriteFontFace::GetDesignGlyphMetrics.**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) Viene restituita una struttura [**DWRITE \_ GLYPH \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) con larghezza di avanzamento, orientamento laterale sinistro e destro, orientamento lato superiore e inferiore, altezza e origine della linea di base verticale.

Il diagramma seguente illustra varie metriche di due diversi caratteri glifi.

![diagramma delle metriche di due glifi diversi](images/twoglyphs.png)

## <a name="drawing-a-glyph-run"></a>Disegno di un'esecuzione di glifi

Quando si implementa un renderer di testo personalizzato, il rendering dei glifi viene gestito da [**IDWriteTextRenderer::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), un metodo di callback implementato come parte di una classe derivata da [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer). La struttura [**DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) passata a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) contiene un oggetto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) denominato *fontFace* che rappresenta il tipo di carattere per l'intera esecuzione del glifo.

L'oggetto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) fornisce anche il [**metodo GetGlyphRunOutline,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) che calcola i contorni del glifo usando un callback del sink geometry specificato, ad esempio [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) durante il rendering [con Direct2D.](../direct2d/direct2d-portal.md)

Per altre informazioni, vedere [l'argomento Come implementare un renderer di testo](how-to-implement-a-custom-text-renderer.md) personalizzato.

 

 