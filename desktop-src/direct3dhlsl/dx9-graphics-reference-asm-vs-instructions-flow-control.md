---
title: Limiti di nidificazione del controllo di flusso
description: Le istruzioni per il controllo di flusso vertex shader presentano due restrizioni speciali.
ms.assetid: c9f80a97-8245-4974-a284-7974e2d2e504
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ebb5b491e074c2275081aa3fe629a2486a24c6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714491"
---
# <a name="flow-control-nesting-limits"></a>Limiti di nidificazione del controllo di flusso

Le istruzioni per il controllo di flusso vertex shader presentano due restrizioni speciali. Le profondità di annidamento limitano il numero di istruzioni che possono essere chiamate tra loro. Ogni istruzione dispone inoltre di un numero di slot di istruzioni che si applica al numero massimo di istruzioni che uno shader può supportare.

> [!Note]  
> Quando si usano i \* \_ \_ profili dello \_ shader HLSL a 4 0 di livello \_ 9 \_ , si usano in modo implicito i profili [Shader Model 2. x](dx-graphics-hlsl-sm2.md) per supportare l'hardware compatibile con Direct3D 9. I profili Shader Model 2. x supportano un comportamento di controllo di flusso più limitato rispetto ai profili [4. x](dx-graphics-hlsl-sm4.md) e successivi del modello shader.

 

## <a name="depth-count-per-instruction-for-vs_2_0"></a>Conteggio profondità per istruzione per vs \_ 2 \_ 0

Ogni istruzione viene conteggiata in base a uno o più limiti di profondità di nidificazione. Questa tabella mostra il numero di profondità che ogni istruzione aggiunge o sottrae dalla profondità esistente:



| Istruzione                              | Annidamento statico | Annidamento dinamico | annidamento ciclo/Rep | annidamento delle chiamate | Numero di flussi statici                        |
|------------------------------------------|----------------|-----------------|------------------|--------------|------------------------------------------|
| [Se bool-vs](if-bool---vs.md)         | 0              | 0               | 0                | 0            | 1                                        |
| [Se \_ comp-vs](if-comp---vs.md)        | n/d            | n/d             | n/d              | n/d          | n/d                                      |
| [Se prede-vs](if-pred---vs.md)         | n/d            | n/d             | n/d              | n/d          | n/d                                      |
| [else-vs](else---vs.md)               | 0              | 0               | 0                | 0            | 1 (solo[se bool-vs](if-bool---vs.md) ) |
| [endif-vs](endif---vs.md)             | -1             | 0               | 0                | 0            | 0                                        |
| [Rep-vs](rep---vs.md)                 | 0              | 0               | 1                | 0            | 1                                        |
| [endrep-vs](endrep---vs.md)           | 0              | 0               | -1               | 0            | 0                                        |
| [ciclo-vs](loop---vs.md)               | 0              | 0               | 1                | 0            | 1                                        |
| [endloop-vs](endloop---vs.md)         | 0              | 0               | -1               | 0            | 0                                        |
| [Break-vs](break---vs.md)             | n/d            | n/d             | n/d              | n/d          | n/d                                      |
| [Interrompi \_ comp-vs](break-comp---vs.md)  | n/d            | n/d             | n/d              | n/d          | n/d                                      |
| [Breakp-vs](breakp---vs.md)           | n/d            | n/d             | n/d              | n/d          | n/d                                      |
| [Call-vs](call---vs.md)               | 0              | 0               | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0              | 0               | 0                | 1            | 1                                        |
| [callnz Predator-vs](callnz-pred---vs.md) | n/d            | n/d             | n/d              | n/d          | n/d                                      |
| [RET-vs](ret---vs.md)                 | 0              | 0               | 0                | -1           | 0                                        |
| [setp \_ comp-vs](setp-comp---vs.md)    | n/d            | n/d             | n/d              | n/d          | n/d                                      |



 

### <a name="nesting-depth"></a>Profondità di annidamento

Profondità di annidamento consente di definire il numero di istruzioni che possono essere chiamate tra loro. Ogni tipo di istruzione ha uno o più limiti di annidamento:



| Tipo di istruzione  | Massimo                               |
|-------------------|---------------------------------------|
| Annidamento statico    | Limitato solo dal numero di flussi statici |
| Annidamento dinamico   | n/d                                   |
| annidamento ciclo/Rep  | 1                                     |
| annidamento delle chiamate      | 1                                     |
| Numero di flussi statici | 16                                    |



 

## <a name="depth-count-per-instruction-for-vs_2_x"></a>Conteggio profondità per istruzione per vs \_ 2 \_ x

Ogni istruzione viene conteggiata in base a uno o più limiti di profondità di nidificazione. Questa tabella mostra il numero di profondità che ogni istruzione aggiunge o sottrae dalla profondità esistente:



| Istruzione                              | Annidamento statico                       | Annidamento dinamico                                                           | annidamento ciclo/Rep | annidamento delle chiamate | Numero di flussi statici                        |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|------------------------------------------|
| [Se bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | 1                                        |
| [Se \_ comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [Se prede-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | 1 (solo[se bool-vs](if-bool---vs.md) ) |
| [endif-vs](endif---vs.md)             | -1 ([se bool-vs](if-bool---vs.md)) | -1 ([se prede-vs](if-pred---vs.md) o [if \_ comp-vs](if-comp---vs.md)) | 0                | 0            | 0                                        |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [ciclo-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [endloop-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [Interrompi \_ comp-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | 0                                        |
| [Breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [Call-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz Predator-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | 0                                        |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Predator-vs](callnz-pred---vs.md))                             | 0                | -1           | 0                                        |
| [setp \_ comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | 0                                        |



 

### <a name="nesting-depth"></a>Profondità di annidamento

Profondità di annidamento consente di definire il numero di istruzioni che possono essere chiamate tra loro. Ogni tipo di istruzione ha uno o più limiti di annidamento:



| Tipo di istruzione  | Massimo                                                                              |
|-------------------|--------------------------------------------------------------------------------------|
| Annidamento statico    | Limitato solo dal numero di flussi statici                                                |
| Annidamento dinamico   | 0 o 24, vedere D3DCAPS9. VS20Caps.DynamicFlowControlDepth                               |
| annidamento ciclo/Rep  | da 1 a 4, vedere D3DCAPS9. VS20Caps.StaticFlowControlDepth                                 |
| annidamento delle chiamate      | da 1 a 4, vedere D3DCAPS9. VS20Caps. StaticFlowControlDepth (indipendente dal limite del ciclo/Rep) |
| Numero di flussi statici | 16                                                                                   |



 

## <a name="depth-count-per-instruction-for-vs_2_sw"></a>Conteggio profondità per istruzione per vs \_ 2 \_ SW

Ogni istruzione viene conteggiata in base a uno o più limiti di profondità di nidificazione. Questa tabella mostra il numero di profondità che ogni istruzione aggiunge o sottrae dalla profondità esistente:



| Istruzione                              | Annidamento statico                       | Annidamento dinamico                                                           | annidamento ciclo/Rep | annidamento delle chiamate | Numero di flussi statici |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Se bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | n/d               |
| [Se \_ comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | n/d               |
| [Se prede-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | n/d               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | n/d               |
| [endif-vs](endif---vs.md)             | -1 ([se bool-vs](if-bool---vs.md)) | -1 ([se prede-vs](if-pred---vs.md) o [if \_ comp-vs](if-comp---vs.md)) | 0                | 0            | n/d               |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | n/d               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | n/d               |
| [ciclo-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | n/d               |
| [endloop-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | n/d               |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | n/d               |
| [Interrompi \_ comp-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | n/d               |
| [Breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | n/d               |
| [Call-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz Predator-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/d               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Predator-vs](callnz-pred---vs.md))                             | 0                | -1           | n/d               |
| [setp \_ comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | n/d               |



 

### <a name="nesting-depth"></a>Profondità di annidamento

Profondità di annidamento consente di definire il numero di istruzioni che possono essere chiamate tra loro. Ogni tipo di istruzione ha uno o più limiti di annidamento:



| Tipo di istruzione  | Massimo  |
|-------------------|----------|
| Annidamento statico    | 24       |
| Annidamento dinamico   | 24       |
| annidamento ciclo/Rep  | 4        |
| annidamento delle chiamate      | 4        |
| Numero di flussi statici | Nessun limite |



 

## <a name="depth-count-per-instruction-for-vs_3_0"></a>Conteggio profondità per istruzione per vs \_ 3 \_ 0

Ogni istruzione viene conteggiata in base a uno o più limiti di profondità di nidificazione. Questa tabella mostra il numero di profondità che ogni istruzione aggiunge o sottrae dalla profondità esistente:



| Istruzione                              | Annidamento statico                       | Annidamento dinamico                                                           | annidamento ciclo/Rep | annidamento delle chiamate | Numero di flussi statici |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Se bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | n/d               |
| [Se \_ comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | n/d               |
| [Se prede-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | n/d               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | n/d               |
| [endif-vs](endif---vs.md)             | -1 ([se bool-vs](if-bool---vs.md)) | -1 ([se prede-vs](if-pred---vs.md) o [if \_ comp-vs](if-comp---vs.md)) | 0                | 0            | n/d               |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | n/d               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | n/d               |
| [ciclo-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | n/d               |
| [endloop-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | n/d               |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | n/d               |
| [Interrompi \_ comp-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | n/d               |
| [Breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | n/d               |
| [Call-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz Predator-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/d               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Predator-vs](callnz-pred---vs.md))                             | 0                | -1           | n/d               |
| [setp \_ comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | n/d               |



 

### <a name="nesting-depth"></a>Profondità di annidamento

Profondità di annidamento consente di definire il numero di istruzioni che possono essere chiamate tra loro. Ogni tipo di istruzione ha uno o più limiti di annidamento:



| Tipo di istruzione  | Massimo  |
|-------------------|----------|
| Annidamento statico    | 24       |
| Annidamento dinamico   | 24       |
| annidamento ciclo/Rep  | 4        |
| annidamento delle chiamate      | 4        |
| Numero di flussi statici | Nessun limite |



 

## <a name="depth-count-per-instruction-for-vs_3_sw"></a>Conteggio profondità per istruzione per vs \_ 3 \_ SW

Ogni istruzione viene conteggiata in base a uno o più limiti di profondità di nidificazione. Questa tabella mostra il numero di profondità che ogni istruzione aggiunge o sottrae dalla profondità esistente:



| Istruzione                              | Annidamento statico                       | Annidamento dinamico                                                           | annidamento ciclo/Rep | annidamento delle chiamate | Numero di flussi statici |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Se bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | n/d               |
| [Se \_ comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | n/d               |
| [Se prede-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | n/d               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | n/d               |
| [endif-vs](endif---vs.md)             | -1 ([se bool-vs](if-bool---vs.md)) | -1 ([se prede-vs](if-pred---vs.md) o [if \_ comp-vs](if-comp---vs.md)) | 0                | 0            | n/d               |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | n/d               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | n/d               |
| [ciclo-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | n/d               |
| [endloop-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | n/d               |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | n/d               |
| [Interrompi \_ comp-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | n/d               |
| [Breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | n/d               |
| [Call-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz Predator-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/d               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Predator-vs](callnz-pred---vs.md))                             | 0                | -1           | n/d               |
| [setp \_ comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | n/d               |



 

### <a name="nesting-depth"></a>Profondità di annidamento

Profondità di annidamento consente di definire il numero di istruzioni che possono essere chiamate tra loro. Ogni tipo di istruzione ha uno o più limiti di annidamento:



| Tipo di istruzione  | Massimo  |
|-------------------|----------|
| Annidamento statico    | 24       |
| Annidamento dinamico   | 24       |
| annidamento ciclo/Rep  | 4        |
| annidamento delle chiamate      | 4        |
| Numero di flussi statici | Nessun limite |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




