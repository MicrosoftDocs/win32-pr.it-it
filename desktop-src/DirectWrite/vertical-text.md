---
title: Testo verticale
description: A partire dal Windows 8, DirectWrite nuove API che consentono di usare il testo verticale nelle app.
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa5e6626ae77e610c38bfb90def7cfe068db80f7f300f58a734969fb107a46a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632547"
---
# <a name="vertical-text"></a>Testo verticale

A partire dal Windows 8, [DirectWrite](direct-write-portal.md) una serie di nuove API che consentono di usare il testo verticale nelle app.

## <a name="drawing-vertical-text"></a>Disegno di testo verticale

È possibile disegnare testo verticale con Direct2D usando i [**metodi DrawTextLayout.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) Per disegnare il testo verticalmente, passare [**DWRITE \_ READING DIRECTION TOP TO \_ \_ \_ \_ BOTTOM**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) al metodo [**IDWriteTextFormat::SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) e [**DWRITE FLOW DIRECTION RIGHT \_ \_ TO \_ \_ \_ LEFT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) al metodo [**IDWriteTextFormatSetFlowDirection.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) È quindi possibile creare e disegnare un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verticale.

## <a name="analyzing-character-orientation"></a>Analisi dell'orientamento dei caratteri

Ogni carattere ha un orientamento di carattere preferito o la direzione in cui il carattere deve essere orientato in qualsiasi layout direzionale. Nel layout orizzontale tradizionale, ad esempio, sia il testo latino che il testo cinese sono orientati verticalmente. D'altra parte, in un layout verticale il testo cinese rimane in posizione verticale e il testo latino viene ruotato di 90 gradi. Questa differenza di orientamento è illustrata nell'esempio seguente.

![immagine del testo inglese e cinese nei layout orizzontale e verticale.](images/vertical-text.png)

Per determinare l'orientamento del testo, è necessario implementare le [**interfacce IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) e [**IDWriteTextAnalysisSource1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) L'origine e il sink accettano le esecuzioni del glifo e consentono di controllare se sono orientati verticalmente o meno.

Dopo aver implementato l'origine e il sink, chiamare il [**metodo AnalyzeVerticalGlyphOrientation.**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) Nell'immagine di esempio questa funzione restituisce 3 esecuzioni: "English", "中国" e "English".

## <a name="going-from-characters-to-glyphs"></a>Andare da caratteri a glifi

Ora che l'esecuzione contiene glifi verticali, è necessario ottenere l'accesso a tali glifi. Nell'esempio finora sono presenti 3 esecuzioni: una con glifi verticali e due senza. Per passare da caratteri a glifi, chiamare [**GetGlyphIndices**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices). Questo metodo restituisce gli indici dei glifi corrispondenti per i caratteri nell'esempio. Poiché il [**metodo AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) restituisce un'esecuzione con glifi verticali, è necessario chiamare [**GetVerticalGlyphVariants**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants), che restituisce gli ID dei glifi orientati verticalmente al posto degli ID glifi correnti.

## <a name="drawing-text-vertically"></a>Disegno verticale del testo

Infine, è necessario disporre e disegnare il testo. Poiché si disegna il testo verticalmente, è necessario ottenere altre informazioni in modo che il testo latino venga disegnato correttamente. Se si disegna tutto il testo lungo la linea di base centrale, il testo latino appare mobile al centro della linea. Per allineare correttamente il testo, è necessario accedere sia alla linea di base centrale che a una linea di base romana. Usare il [**metodo IDWriteTextAnalyzer1::GetBaseline**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) per ottenere i valori numerici delle linee di base specificate. È possibile sottrarre la linea di base romana dalla linea di base centrale per ottenere l'offset tra i due.

Con tutte queste informazioni, è possibile disegnare il testo sullo schermo. Chiamare prima il [**metodo GetGlyphOrientationTransform**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform) con i risultati degli oggetti [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) e [**IDWriteTextAnalysisSource1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1)

Se si usa [Direct2D,](rendering-by-using-direct2d.md) è anche necessario impostare la trasformazione world nella destinazione di rendering Direct2D per il rendering verticale.

Chiamare infine [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) tre volte, una volta su ogni blocco di testo. Nei due blocchi di testo in inglese è necessario applicare l'offset calcolato tra le linee di base romane e centrali.

A questo punto, il testo nell'app verrà disegnato verticalmente, con l'orientamento corretto del glifo.

 

 