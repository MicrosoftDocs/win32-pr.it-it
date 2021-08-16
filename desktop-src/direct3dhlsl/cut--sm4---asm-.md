---
title: cut (sm4 - asm)
description: Istruzione Geometry Shader che completa la topologia primitiva corrente (se sono stati generati vertici) e avvia una nuova topologia del tipo dichiarato da Geometry Shader.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34357c05cdd9506ec480d5021db5b330971de9fce7fd70ce9909658be9bb8c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908825"
---
# <a name="cut-sm4---asm"></a>cut (sm4 - asm)

Istruzione Geometry Shader che completa la topologia primitiva corrente (se sono stati generati vertici) e avvia una nuova topologia del tipo dichiarato da Geometry Shader.



| Tagliare |
|-----|



 

## <a name="remarks"></a>Commenti

Quando **si** esegue cut, la prima cosa che accade è che qualsiasi topologia emessa in precedenza dalla chiamata geometry shader viene completata. Se non sono stati generati vertici sufficienti per la topologia primitiva precedente, vengono eliminati. Poiché le uniche topologie di output disponibili per Geometry Shader sono pointlist, linestrip e trianglestrip, non ci sono mai vertici rimanenti al momento del **taglio.**

Dopo aver completato la topologia precedente, se **presente,** il taglio causa l'avvio di una nuova topologia, usando la topologia dichiarata come output geometry shader.

## <a name="restrictions"></a>Restrizioni

-   **L'istruzione** cut si applica solo allo shader Geometry.
-   **Cut** può essere visualizzato un numero qualsiasi di volte in Geometry Shader, incluso il controllo di flusso.
-   Se geometry shader termina e i vertici sono stati generati, la topologia  che stanno compilando viene completata, come se fosse stato eseguito un taglio come ultima istruzione.
-   Se i flussi sono stati dichiarati, è necessario usare [ \_ cut stream](cut-stream---sm5---asm-.md) anziché **cut.**

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




