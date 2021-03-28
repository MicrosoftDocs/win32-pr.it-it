---
title: Riferimento per HLSL
description: La documentazione di riferimento di HLSL specifica le caratteristiche del linguaggio. È suddiviso in diverse sezioni.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045101"
---
# <a name="reference-for-hlsl"></a>Riferimento per HLSL

La documentazione di riferimento di HLSL specifica le caratteristiche del linguaggio. È suddiviso in diverse sezioni.

-   [Sintassi del linguaggio (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) : per la programmazione di shader in HLSL è necessario comprendere la sintassi del linguaggio, ovvero la modalità di scrittura del codice HLSL. Questo include il codice per dichiarare e inizializzare variabili, scrivere funzioni shader definite dall'utente e aggiungere istruzioni di controllo di flusso per rendere le funzioni più potenti.
-   [Modelli shader rispetto ai profili shader](dx-graphics-hlsl-models.md) : il compilatore HLSL implementa regole e restrizioni in base ai modelli shader. Il codice in ogni vertex shader, geometry shader (se si utilizza Direct3D 10) e pixel shader vengono convalidati in base a un modello di shader, fornito in fase di compilazione.
-   [**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) -HLSL ha molte funzioni intrinseche. Vengono implementati e testati in modo che sia possibile utilizzarli sapendo che sono già sottoposti a debug e che offrono prestazioni ottimali. Se si sceglie di scrivere funzioni personalizzate, vedere la sezione relativa alla sintassi del linguaggio per la scrittura di funzioni definite dall'utente.
-   Informazioni di [riferimento su ASM shader](dx9-graphics-reference-asm.md) : istruzioni per gli assembly che è possibile usare per programmare ed eseguire il debug degli shader.
-   [Riferimento a D3DCompiler](dx-graphics-d3dcompiler-reference.md) : compila l'origine HLSL non elaborata.
-   [Riferimenti per la conversione di formato inline](inline-format-conversion-reference.md) : il \_ file D3DX DXGIFormatConvert. inl contiene funzioni di conversione di formato inline che è possibile usare in compute shader o pixel shader su hardware Direct3D 11. È possibile usare queste funzioni nell'applicazione per eseguire contemporaneamente la lettura e la scrittura in una trama. Ovvero, è possibile eseguire la modifica dell'immagine sul posto. Per usare queste funzioni di conversione del formato inline, includere il \_ file D3DX DXGIFormatConvert. inl nell'applicazione.
-   [Appendice (DirectX HLSL)](dx-graphics-hlsl-appendix.md) : l'appendice è inclusa per completezza. Include un elenco delle parole chiave e delle parole riservate. queste parole non possono essere usate come identificatori nei programmi. Include inoltre un elenco della grammatica del linguaggio per riferimento.
-   [**Errori e avvisi di HLSL**](hlsl-errors-and-warnings.md) : fornisce codici di errore e di avviso che possono essere restituiti da uno shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[HLSL](dx-graphics-hlsl.md)
</dt> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




