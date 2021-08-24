---
title: emit_stream (sm5 - asm)
description: Emettere un vertice in un flusso specificato.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e90bfb72862abeccc8a9411904a7b42f77c933cc4c87af189d6557596389c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562701"
---
# <a name="emit_stream-sm5---asm"></a>emit \_ stream (sm5 - asm)

Emettere un vertice in un flusso specificato.



| emettere \_ un flusso streamIndex |
|--------------------------|



 



| Elemento                                                                                                               | Descrizione                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[in \] Indice del flusso.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione fa sì che tutti i registri o dichiarati per il flusso specificato siano letti dal \# geometry shader per generare un vertice. Afer l'emissione, tutti i dati in tutti i registri di output per tutti i flussi diventano non inizializzati, non solo il flusso emesso.

*streamIndex* deve essere un valore immediato \[ 0..3 \] per un flusso dichiarato.

Quando vengono **\_ emesse** più chiamate di flusso di emissione, vengono generate primitive.

### <a name="restrictions"></a>Restrizioni

-   **Il \_ flusso di** creazione può essere visualizzato un numero qualsiasi di volte in uno shader geometry, incluso il controllo di flusso.
-   Se i flussi non sono stati dichiarati, è necessario usare [emit](emit--sm4---asm-.md) anziché **emettere \_ il flusso**.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





