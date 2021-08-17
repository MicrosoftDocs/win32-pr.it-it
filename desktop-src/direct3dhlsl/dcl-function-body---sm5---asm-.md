---
title: dcl_function_body (sm5 - asm)
description: Dichiarare il corpo di una funzione.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339e7f5d7edb91f4f3405b328286a9ae32a8108efdaafaba1f212870be7ff8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727235"
---
# <a name="dcl_function_body-sm5---asm"></a>Corpo della funzione dcl \_ \_ (sm5 - asm)

Dichiarare il corpo di una funzione.



| Corpo della funzione dcl \_ \_ fb\# |
|--------------------------|



 



| Elemento                                                          | Descrizione                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="fb_"></span><span id="FB_"></span>*Fb\#*<br/> | \[in \] Etichetta della posizione in cui verrà visualizzata la funzione.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione dichiara un corpo di funzione univoco il cui codice verrà visualizzato più avanti nel programma in corrispondenza dell'etichetta fb \# .

I corpi delle funzioni vengono usati nelle dichiarazioni di tabella delle funzioni. Per altre informazioni, vedere [dcl \_ function \_ table](dcl-function-table---sm5---asm-.md).

Nello shader hull e nello shader di dominio, in cui sono presenti più fasi (fase del punto di controllo, fase fork e fase di join), tutti i corpi funzione (etichetta fb ) vengono visualizzati dopo tutte le fasi, anziché essere raggruppati per \# fase.

Non esiste alcun limite al numero di corpi funzione che possono essere presenti.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





