---
title: emit_stream (SM5-ASM)
description: Creare un vertice in un flusso specificato.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398229"
---
# <a name="emit_stream-sm5---asm"></a>Emit \_ Stream (SM5-ASM)

Creare un vertice in un flusso specificato.



| genera \_ flusso streamIndex |
|--------------------------|



 



| Elemento                                                                                                               | Descrizione                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[nell' \] indice del flusso.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione causa la lettura da parte di Geometry shader di tutti i registri o dichiarati \# per il flusso specificato per generare un vertice. Dopo l'emissione, tutti i dati in tutti i registri di output per tutti i flussi diventano non inizializzati, non solo il flusso generato a.

*streamIndex* deve essere un valore immediato \[ 0.. 3 \] per un flusso dichiarato.

Quando vengono rilasciate più chiamate a **\_ flussi Emit** , vengono generate le primitive.

### <a name="restrictions"></a>Restrizioni

-   **il \_ flusso di emissione** può comparire un numero qualsiasi di volte in un geometry shader, incluso all'interno del controllo di flusso.
-   Se i flussi non sono stati dichiarati, è necessario usare [Emit](emit--sm4---asm-.md) anziché **Emit \_ Stream**.

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

 

 





