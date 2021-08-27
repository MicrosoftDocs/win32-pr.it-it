---
title: cut_stream (sm5 - asm)
description: Istruzione geometry shader che completa la topologia primitiva corrente nel flusso specificato, se sono stati generati vertici, e avvia una nuova topologia del tipo dichiarato dallo shader geometry in tale flusso.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c019785d121bfb504b447456ad2376deb9c9c63357621513f42dcdf09351f465
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025021"
---
# <a name="cut_stream-sm5---asm"></a>cut \_ stream (sm5 - asm)

Istruzione geometry shader che completa la topologia primitiva corrente nel flusso specificato, se sono stati generati vertici, e avvia una nuova topologia del tipo dichiarato dallo shader geometry in tale flusso.



| stream \_ cutIndex |
|-------------------------|



 



| Elemento                                                                                                               | Descrizione                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[\]nell'indice del flusso.<br/> |



 

## <a name="remarks"></a>Commenti

Quando questa istruzione viene eseguita, qualsiasi topologia emessa in precedenza dalla chiamata geometry shader viene completata. Se non sono stati generati vertici sufficienti per la topologia primitiva precedente, vengono eliminati. Poiché le uniche topologie di output disponibili per lo shader geometry sono pointlist, linestrip e trianglestrip, non sono mai presenti vertici rimanenti.

*streamIndex* deve essere un valore immediato \[ 0..3 \] per un flusso dichiarato.

Al termine della topologia precedente, se presente, questa istruzione determina l'avvio di una nuova topologia, usando la topologia dichiarata come output per lo shader geometry.

### <a name="restrictions"></a>Restrizioni

-   Questa istruzione si applica solo allo shader geometry.
-   **Il \_ flusso di** taglio può essere visualizzato in qualsiasi numero di volte nello shader geometry, incluso il controllo di flusso.
-   Se il geometry shader termina e i vertici sono stati generati, la topologia che stanno creando viene completata, come se fosse stata eseguita un'istruzione **cut \_ stream** come ultima istruzione.
-   Se i flussi non sono stati dichiarati, è necessario usare [cut](cut--sm4---asm-.md) anziché **cut \_ stream**.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





