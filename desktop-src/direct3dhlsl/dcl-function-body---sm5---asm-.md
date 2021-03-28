---
title: dcl_function_body (SM5-ASM)
description: Dichiarare il corpo di una funzione.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117229"
---
# <a name="dcl_function_body-sm5---asm"></a>\_corpo della funzione DCL \_ (SM5-ASM)

Dichiarare il corpo di una funzione.



| \_corpo della funzione DCL \_ FB\# |
|--------------------------|



 



| Elemento                                                          | Descrizione                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="fb_"></span><span id="FB_"></span>*FB\#*<br/> | \[nell' \] etichetta della posizione in cui verrà visualizzata la funzione.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione dichiara un corpo della funzione univoco il cui codice verrà visualizzato in un secondo momento nel programma in corrispondenza dell'etichetta FB \# .

I corpi delle funzioni vengono usati nelle dichiarazioni di tabella di funzione. Per altre informazioni, vedere [ \_ \_ tabella delle funzioni DCL](dcl-function-table---sm5---asm-.md).

In Hull shader e Domain shader, in cui sono presenti più fasi (fase del punto di controllo, fase della divisione e fase di join), tutti i corpi delle funzioni (etichetta FB \# ) vengono visualizzati dopo tutte le fasi, anziché essere raggruppati per fase.

Non esiste alcun limite al numero di corpi delle funzioni che possono essere presenti.

Questa istruzione si applica alle fasi dello shader seguenti:



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



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





