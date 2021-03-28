---
title: Cut (SM4-ASM)
description: Istruzione Geometry shader che completa la topologia primitiva corrente (se sono stati generati vertici) e avvia una nuova topologia del tipo dichiarato da Geometry shader.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c462d2f4dc2e0c6b4076f577610c93794e890af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976327"
---
# <a name="cut-sm4---asm"></a>Cut (SM4-ASM)

Istruzione Geometry shader che completa la topologia primitiva corrente (se sono stati generati vertici) e avvia una nuova topologia del tipo dichiarato da Geometry shader.



| tagliare |
|-----|



 

## <a name="remarks"></a>Commenti

Quando si esegue il **Cut** , la prima cosa che si verifica è che tutte le topologie generate in precedenza dalla chiamata geometry shader siano state completate. Se non sono stati generati vertici sufficienti per la topologia primitiva precedente, vengono eliminati. Poiché le uniche topologie di output disponibili per il geometry shader sono LineStrip e TriangleStrip, non ci sono mai vertici rimanenti al momento dell' **interruzione**.

Dopo che la topologia precedente è stata completata, **Cut** causa l'inizio di una nuova topologia, usando la topologia dichiarata come output di Geometry shader.

## <a name="restrictions"></a>Restrizioni

-   L'istruzione **Cut** si applica solo a geometry shader.
-   il **taglio** può apparire un numero qualsiasi di volte nello shader Geometry, incluso all'interno del controllo di flusso.
-   Se il geometry shader termina e i vertici sono stati emessi, la topologia che compila viene completata, come se fosse stato eseguito un **taglio** come ultima istruzione.
-   Se i flussi sono stati dichiarati, è necessario usare [Cut \_ Stream](cut-stream---sm5---asm-.md) anziché **Cut**.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




