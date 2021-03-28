---
title: fcall (SM5-ASM)
description: Chiamata di funzione dell'interfaccia.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398290"
---
# <a name="fcall-sm5---asm"></a>fcall (SM5-ASM)

Chiamata di funzione dell'interfaccia.



| fcall FP \# \[ arrayIndex \] \[ chiamata\] |
|--------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*FP\#*<br/>                                                  | \[nel \] puntatore a funzione.<br/>                                                                                                                                                                                                                                                                    |
| <span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*<br/> | \[in \] facoltativo. Specifica un offset nella matrice del puntatore a funzione. Questo parametro deve essere un valore letterale Unsigned Integer se FP \# non è stato dichiarato come indicizzabile. In caso contrario, arrayIndex può essere del formato letterale base + offset da un registro shader. Ad esempio, fcall FP1 \[ R1. w + 0 \] \[ 0 \] .<br/> |
| <span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*chiamata*<br/>     | \[in \] facoltativo. Un valore letterale Unsigned Integer offset nella tabella della funzione selezionata, selezionando un corpo della funzione FB \# da eseguire. <br/>                                                                                                                                                                |



 

## <a name="remarks"></a>Commenti

*FP \#* \[  \] \[ arrayIndex \] viene risolto in una particolare tabella di funzioni, selezionata dall'API al di fuori dello shader dalle opzioni della tabella di funzioni elencate nella dichiarazione di *FP \#*.

La somma di \# in *FP \#* e *arrayIndex* consente di selezionare la tabella function. Se, ad esempio, un'interfaccia viene dichiarata come 4PQ \[ 4 \] \[ 3 \] (dimensione della matrice 4), i **fcall** seguenti sono equivalenti: fcall 4PQ \[ 2 \] \[ 3 \] e FP5 \[ 1 \] \[ 3 \] , perché 4 + 2 = 5 + 1.

### <a name="restrictions"></a>Restrizioni

-   Se *arrayIndex* usa l'indicizzazione dinamica, il comportamento non è definito se *arrayIndex* diverge sulle chiamate shader adiacenti, che potrebbero essere in esecuzione in contemporanea. Il compilatore HLSL tenterà di non consentire questo caso.

    Le chiamate adiacenti possono essere inattive a causa del controllo di flusso, perché non interrompe l'esecuzione del contemporanea.

-   Se *FP \#*  +  *arrayIndex* specifica un indice fuori limite, il comportamento non è definito.
-   Per i casi non definiti descritti, significa che il comportamento del dispositivo D3D corrente diventa non definito, inclusa la possibilità di perdita del dispositivo. Tuttavia, non sarà possibile accedere alla memoria esterna al dispositivo D3D corrente o eseguirla come codice.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





