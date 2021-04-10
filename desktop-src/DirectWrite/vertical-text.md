---
title: Testo verticale
description: A partire da Windows 8, DirectWrite include una serie di nuove API che consentono di usare il testo verticale nelle app.
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db8788a6be97a55911694942a930e17dc69976a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963127"
---
# <a name="vertical-text"></a>Testo verticale

A partire da Windows 8, [DirectWrite](direct-write-portal.md) include una serie di nuove API che consentono di usare il testo verticale nelle app.

## <a name="drawing-vertical-text"></a>Disegno di testo verticale

È possibile creare testo verticale con Direct2D usando i metodi [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) . Per estrarre il testo verticalmente, passare [**la \_ direzione di lettura di DWrite dall' \_ \_ alto \_ verso il \_ basso**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) al metodo [**IDWriteTextFormat:: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) e la [**direzione del flusso DWrite da \_ \_ \_ destra \_ a \_ sinistra**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) al metodo [**IDWriteTextFormatSetFlowDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) . È quindi possibile creare e creare un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verticale.

## <a name="analyzing-character-orientation"></a>Analisi dell'orientamento dei caratteri

Ogni carattere ha un orientamento carattere preferito o la direzione in cui il carattere deve essere orientato in qualsiasi layout direzionale. Nel layout orizzontale tradizionale, ad esempio, il testo latino e il testo cinese sono orientati verticalmente. D'altra parte, in un layout verticale, il testo cinese rimane verticale e il testo latino viene ruotato di 90 gradi. Questa differenza di orientamento è illustrata nell'esempio riportato di seguito.

![immagine del testo in inglese e cinese nei layout orizzontale e verticale.](images/vertical-text.png)

Per determinare l'orientamento del testo di cui si dispone, è necessario implementare le interfacce [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) e [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) . L'origine e il sink vengono eseguiti nel glifo e consentono di controllare se sono orientati verticalmente o meno.

Dopo aver implementato l'origine e il sink, chiamare il metodo [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) . Nell'immagine di esempio, questa funzione restituisce 3 esecuzioni: "English", "中国" e "English".

## <a name="going-from-characters-to-glyphs"></a>Passare da caratteri a glifi

Ora che si sa che l'esecuzione contiene glifi verticali, è necessario ottenere l'accesso a tali glifi. Nell'esempio fino a questo punto, sono presenti 3 esecuzioni: una con glifi verticali e due senza. Per eseguire la transizione da caratteri a glifi, chiamare [**GetGlyphIndices**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices). Questo metodo restituisce gli indici di glifo corrispondenti per i caratteri nell'esempio. Poiché il metodo [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) restituisce un'esecuzione con glifi verticali, è necessario chiamare [**GetVerticalGlyphVariants**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants), che restituisce gli ID del glifo orientati verticalmente al posto degli ID di glifo correnti.

## <a name="drawing-text-vertically"></a>Disegno verticale del testo

Infine, è necessario disporre e creare il testo. Poiché si sta disegnando il testo verticalmente, è necessario ottenere altre informazioni in modo che il testo latino venga disegnato correttamente. Se si estrae tutto il testo lungo la linea di base centrale, il testo latino sembra fluttuare al centro della riga. Per allineare il testo correttamente, è necessario accedere sia alla baseline centrale che alla linea di base romana. Usare il metodo [**IDWriteTextAnalyzer1:: GetBaseline**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) per ottenere i valori numerici delle linee di base specificate. È possibile sottrarre la baseline romana dalla linea di base centrale per ottenere l'offset tra i due.

Con tutte queste informazioni è possibile creare il testo sullo schermo. Chiamare innanzitutto il metodo [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform) con i risultati degli oggetti [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) e [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) .

Se si usa [Direct2D](rendering-by-using-direct2d.md) è anche necessario impostare la trasformazione globale sulla destinazione di rendering Direct2D per il rendering verticale.

Infine, chiamare [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) tre volte, una volta per ogni blocco di testo. Nei due blocchi di testo in inglese, è necessario applicare l'offset calcolato tra le linee di base romane e centrali.

A questo punto, il testo nell'app verrà disegnato verticalmente, con l'orientamento corretto per il glifo.

 

 