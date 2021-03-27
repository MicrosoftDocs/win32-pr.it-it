---
title: cut_stream (SM5-ASM)
description: Istruzione Geometry shader che completa la topologia primitiva corrente nel flusso specificato, se è stato generato un vertice e avvia una nuova topologia del tipo dichiarato da Geometry shader in quel flusso.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398212"
---
# <a name="cut_stream-sm5---asm"></a>Taglia \_ flusso (SM5-ASM)

Istruzione Geometry shader che completa la topologia primitiva corrente nel flusso specificato, se è stato generato un vertice e avvia una nuova topologia del tipo dichiarato da Geometry shader in quel flusso.



| Taglia \_ streamIndex di flusso |
|-------------------------|



 



| Elemento                                                                                                               | Descrizione                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[nell' \] indice del flusso.<br/> |



 

## <a name="remarks"></a>Commenti

Quando questa istruzione viene eseguita, tutte le topologie emesse in precedenza dalla chiamata geometry shader sono state completate. Se non sono stati generati vertici sufficienti per la topologia primitiva precedente, vengono eliminati. Poiché le uniche topologie di output disponibili per il geometry shader sono LineStrip e TriangleStrip, non ci sono mai vertici rimanenti.

*streamIndex* deve essere un valore immediato \[ 0.. 3 \] per un flusso dichiarato.

Dopo che la topologia precedente è stata completata, questa istruzione determina l'inizio di una nuova topologia, usando la topologia dichiarata come output per il geometry shader.

### <a name="restrictions"></a>Restrizioni

-   Questa istruzione si applica solo a geometry shader.
-   il **Cut \_ Stream** può comparire un numero qualsiasi di volte nello shader Geometry, incluso all'interno del controllo di flusso.
-   Se il geometry shader termina e i vertici sono stati emessi, la topologia che compila viene completata, come se fosse stata eseguita un'istruzione **Cut \_ Stream** come ultima istruzione.
-   Se i flussi non sono stati dichiarati, è necessario usare [Cut](cut--sm4---asm-.md) anziché **Cut \_ Stream**.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

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

 

 





