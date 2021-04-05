---
title: Glifi ed esecuzioni di glifi
description: Glifi ed esecuzioni di glifi sono disponibili nel livello più basso di funzionalità dell'API DirectWrite, il livello di rendering del glifo.
ms.assetid: e670cb65-1fcb-46fd-ac0b-02eaaaa51996
keywords:
- DirectWrite, glifi
- DirectWrite, esecuzioni glifo
- esecuzioni glifo
- icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c5c6b30c9a44cde4704e6afd231cebbc91d2be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117967"
---
# <a name="glyphs-and-glyph-runs"></a>Glifi ed esecuzioni di glifi

Glifi ed esecuzioni di glifi sono disponibili nel livello più basso di funzionalità dell'API [DirectWrite](direct-write-portal.md) , il livello di rendering del glifo.

## <a name="glyphs"></a>Glifi

Un glifo è una rappresentazione fisica di un carattere in un tipo di carattere specificato. I caratteri possono avere molti glifi, ognuno dei quali è potenzialmente in grado di definire un glifo diverso per tale carattere.

Due o più glifi possono anche essere combinati in un unico glifo, questo processo è denominato composizione glifo. Questa operazione può essere eseguita anche nella direzione opposta, mentre un singolo glifo viene suddiviso in più glifi, noto come decomposizione del glifo.

### <a name="alternate-glyphs"></a>Glifi alternativi

I tipi di carattere possono fornire glifi alternativi per i caratteri, ad esempio i glifi alternativi stilistici per il tipo di carattere OpenType di Pericle, come illustrato nella schermata seguente. Il rendering dei caratteri ' A ',' È è O ' viene eseguito con glifi alternativi stilistici.

![screenshot della "mitologia verde antica", con "a", "e" e "o" usando glifi alternativi](images/opentypealternateglyphs.png)

Un altro esempio di glifi alternativi è costituito da glifi ornati. Lo screenshot seguente Mostra glifi standard e ornati per il tipo di carattere Pescadero.

![screenshot delle lettere da "a" a "n" nei glifi standard e ornati](images/opentypeswashstandard.png)

Ornati e altre funzionalità tipografiche, tra cui glifi alternativi più elaborati, sono disponibili tramite [OpenType](../intl/opentype-font-format.md). Le funzionalità tipografiche OpenType possono essere applicate a un intervallo di testo usando [**IDWriteTextLayout:: setypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) e passando la costante di enumerazione dei tag della funzionalità del [**tipo di \_ carattere \_ \_ DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) associata alla funzionalità desiderata.

## <a name="glyph-runs"></a>Esecuzioni glifo

Un'esecuzione di glifo rappresenta un set di glifi contigui che hanno tutti lo stesso tipo di carattere e le stesse dimensioni, nonché lo stesso effetto di disegno del client, se disponibile. La sottolineatura e la barratura non fanno parte dell'esecuzione del glifo per l'intervallo di testo a cui vengono applicati e vengono disegnate in un secondo momento. Gli oggetti inline, ad esempio le immagini, vengono anche disegnati separatamente, in quanto non fanno parte di un tipo di carattere.

### <a name="the-idwritefontface-interface"></a>Interfaccia IDWriteFontFace

[DirectWrite](direct-write-portal.md) usa lo stesso sistema per la classificazione dei tipi di carattere di Windows pesentation Foundation (WPF), quindi possono essere presenti più tipi di carattere fisici per ogni famiglia di caratteri. Un tipo di carattere, ad esempio l'interfaccia [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) in DirectWrite, rappresenta un tipo di carattere fisico con un peso, un inclinazione e un'estensione specifici. Contiene il tipo di carattere, i riferimenti ai file appropriati, i dati di identificazione della faccia e i vari dati di tipo carattere, ad esempio le metriche, i nomi e le strutture di glifi.

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) può essere creato direttamente da un nome di tipo di carattere o ottenuto da una raccolta di tipi di carattere.

### <a name="glyph-metrics"></a>Metrica del glifo

Ai singoli glifi sono associate metriche. È possibile ottenere le metriche per tutti i glifi in un'icona eseguita usando il metodo [**IDWriteFontFace:: GetDesignGlyphMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) . Viene restituita una struttura di [**\_ \_ metrica del glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) con la larghezza di avanzamento, il cuscinetto sinistro e destro, il cuscinetto di parte superiore e inferiore, l'altezza e l'origine della linea di base verticale.

Il diagramma seguente mostra diverse metriche di due caratteri di glifo diversi.

![diagramma delle metriche di due glifi diversi](images/twoglyphs.png)

## <a name="drawing-a-glyph-run"></a>Disegno di un'esecuzione di glifo

Quando si implementa un renderer di testo personalizzato, il rendering dei glifi viene gestito da [**IDWriteTextRenderer::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), un metodo di callback implementato come parte di una classe derivata da [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer). La struttura di [**\_ \_ esecuzione del glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) passata a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) contiene un oggetto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , denominato *fontFace*, che rappresenta il tipo di carattere per l'intera esecuzione del glifo.

L'oggetto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) fornisce anche il metodo [**GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , che calcola il glifo in linea usando un callback di sink di geometria specificato, ad esempio [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) durante il rendering con [Direct2D](../direct2d/direct2d-portal.md).

Per ulteriori informazioni, vedere l'argomento [How to implement a Custom Text renderer](how-to-implement-a-custom-text-renderer.md) .

 

 