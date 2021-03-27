---
title: dcl_uav_raw (SM5-ASM)
description: Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'utilizzo da uno shader. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995453"
---
# <a name="dcl_uav_raw-sm5---asm"></a>\_RAW UAV DCL \_ (SM5-ASM)

Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'utilizzo da uno shader.



| \_ \_ \[ \_ dstUAV GLC di DCL UAV RAW \] |
|-------------------------------|



 



| Elemento                                                                                           | Descrizione                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[nel \] UAV.<br/> |



 

## <a name="remarks"></a>Commenti

*dstUAV* è un \# registro u dichiarato come riferimento a un UnorderedAccessView di un buffer, in cui il buffer viene visualizzato come una semplice matrice 1D di voci non tipizzate a 32 bit.

Le operazioni eseguite sulla memoria possono interpretare in modo implicito i dati come aventi un tipo.

Il \_ flag GLC significa "globalmente coerente". L'assenza di \_ GLC significa che il UAV viene dichiarato solo come "gruppo coerente" nel compute shader o "coerente localmente" in una singola chiamata di pixel shader.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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



 

> [!Note]  
> Questa istruzione è supportata in cs \_ 4 \_ 0 e cs \_ 4 \_ 1.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





