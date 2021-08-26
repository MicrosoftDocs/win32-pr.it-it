---
title: dcl_output_control_point_count (sm5 - asm)
description: Dichiara il conteggio dei punti di controllo dell'output dello hull shader.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93dc28a2af3ac50c835fa7ec38d7d344029af76a11cb2b84945dbf5009d68473
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024701"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a>Conteggio punti di controllo di output dcl \_ \_ \_ \_ (sm5 - asm)

Dichiara il conteggio dei punti di controllo dell'output dello hull shader.



| dcl \_ output control point count \_ \_ \_ N |
|--------------------------------------|



 



| Elemento                                                   | Descrizione                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[in \] Valore intero compreso tra 0 e 32 che specifica il conteggio dei punti di controllo di output.<br/> |



 

## <a name="remarks"></a>Commenti

Lo hull shader può ottenere 0 punti di controllo se non sono necessari.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo                 | Dominio | Geometria | Pixel | Calcolo |
|--------|----------------------|--------|----------|-------|---------|
|        | Sezione Dichiarazioni |        |          |       |         |



 

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

 

 





