---
title: Informazioni di riferimento per HLSL
description: La documentazione di riferimento HLSL specifica le caratteristiche del linguaggio. È suddiviso in diverse sezioni.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425dc1d56801bbbd6b73429d8d17024a78dffe47a045ec6b34d5cd45b752bcca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513850"
---
# <a name="reference-for-hlsl"></a>Informazioni di riferimento per HLSL

La documentazione di riferimento HLSL specifica le caratteristiche del linguaggio. È suddiviso in diverse sezioni.

-   [Sintassi del linguaggio (DirectX HLSL):](dx-graphics-hlsl-language-syntax.md) per la programmazione di shader in HLSL è necessario comprendere la sintassi del linguaggio, ovvero la modalità di scrittura del codice HLSL. Include il codice per dichiarare e inizializzare le variabili, scrivere funzioni shader definite dall'utente e aggiungere istruzioni di controllo di flusso per rendere le funzioni più potenti.
-   [Modelli shader e profili shader:](dx-graphics-hlsl-models.md) il compilatore HLSL implementa regole e restrizioni in base ai modelli shader. Il codice in ogni vertex shader, geometry shader (se si usa Direct3D 10) e pixel shader vengono convalidati in base a un modello shader, fornito in fase di compilazione.
-   [**Funzioni intrinseche (DirectX HLSL):**](dx-graphics-hlsl-intrinsic-functions.md) HLSL ha molte funzioni intrinseche. Questi vengono implementati e testati in modo che sia possibile usarli sapendo che sono già in fase di debug e che hanno prestazioni molto performate. Se si sceglie di scrivere funzioni personalizzate, vedere la sezione relativa alla sintassi del linguaggio per la scrittura di funzioni definite dall'utente.
-   [Informazioni di riferimento su Asm Shader:](dx9-graphics-reference-asm.md) istruzioni assembly che è possibile usare per programmare ed eseguire il debug degli shader.
-   [Riferimento A D3DCompiler:](dx-graphics-d3dcompiler-reference.md) compila l'origine HLSL non elaborata.
-   Informazioni di riferimento sulla [conversione](inline-format-conversion-reference.md) del formato inline: il file DXGIFormatConvert.inl D3DX contiene funzioni di conversione del formato inline che è possibile usare nello shader di calcolo o \_ pixel shader nell'hardware Direct3D 11. È possibile usare queste funzioni nell'applicazione per leggere e scrivere contemporaneamente in una trama. In altre informazioni, è possibile eseguire la modifica sul posto delle immagini. Per usare queste funzioni di conversione del formato inline, includere il \_ file DXGIFormatConvert.inl D3DX nell'applicazione.
-   [Appendice (DirectX HLSL):](dx-graphics-hlsl-appendix.md) l'appendice è inclusa per la completezza. Include un elenco delle parole chiave e delle parole riservate. queste parole non possono essere usate come identificatori nei programmi. Include anche un elenco della grammatica del linguaggio per riferimento.
-   [**Errori e avvisi HLSL:**](hlsl-errors-and-warnings.md) fornisce codici di errore e di avviso che possono essere restituiti da uno shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hlsl](dx-graphics-hlsl.md)
</dt> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




