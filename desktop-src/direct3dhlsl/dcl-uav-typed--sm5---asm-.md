---
title: dcl_uav_typed (sm5 - asm)
description: Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'uso da parte di uno shader. | dcl_uav_typed (sm5 - asm)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec321389f8c8296bda8ccd1eba947b5ba38adc80c94b3c8c0685b069fcdafbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950581"
---
# <a name="dcl_uav_typed-sm5---asm"></a>dcl \_ uav \_ typed (sm5 - asm)

Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'uso da parte di uno shader.



| dcl \_ uav \_ typed \[ \_ glc \] dstUAV, dimension, type |
|--------------------------------------------------|



 



| Elemento                                                                                           | Descrizione                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[\]nell'UAV.<br/>                                                                        |
| <span id="dimension"></span><span id="DIMENSION"></span>*Dimensione*<br/>                 | \[in \] specifica il numero di dimensioni fornite nelle istruzioni che accedono all'UAV.<br/> |
| <span id="type"></span><span id="TYPE"></span>*digitare*<br/>                                | \[in \] Tipo dell'UAV.<br/>                                                            |



 

## <a name="remarks"></a>Commenti

*dstUAV è* un registro u dichiarato come riferimento a un oggetto UnorderedAccessView che deve essere associato allo \# slot UAV \# nell'API.

La dimensione deve essere buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray o Texture3D. Indica il numero di dimensioni fornite da qualsiasi istruzione che accede all'UAV: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) o 3 (Texture2DArray, Texture3D).

Il tipo è {UNORM,SNORM,UINT,SINT,FLOAT}. Le operazioni eseguite con l'u dichiarato devono essere compatibili con il tipo dichiarato qui e anche l'UAV associato allo \# slot deve avere lo stesso \# tipo.

Il \_ flag glc è l'acronimo di "globally coherent". L'assenza di glc indica che l'UAV viene dichiarato solo come "coerente del gruppo" nello shader di calcolo o "coerente localmente" in una singola pixel shader \_ chiamata.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché gli UAV sono disponibili in tutte le fasi dello shader per Direct3D 11.1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11.1, disponibile a partire da Windows 8.



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

> [!Note]  
> Questa istruzione non è supportata in compute shader 4.x.

 

## <a name="minimum-shader-model"></a>Modello di shader minimo

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

 

 





