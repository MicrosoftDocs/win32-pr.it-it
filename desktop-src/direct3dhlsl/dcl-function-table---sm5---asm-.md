---
title: dcl_function_table (SM5-ASM)
description: Dichiarare una tabella di funzioni.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993253"
---
# <a name="dcl_function_table-sm5---asm"></a>\_tabella delle funzioni DCL \_ (SM5-ASM)

Dichiarare una tabella di funzioni.



| \_tabella della funzione DCL \_ ft \# = {FB \# , FB \# ,...} |
|-----------------------------------------------|



 



| Elemento                                                      | Descrizione                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span id="ft"></span><span id="FT"></span>*ft*<br/> | \[nelle \] voci della tabella di funzioni.<br/> |



 

## <a name="remarks"></a>Commenti

Questa funzione dichiara una tabella di funzioni come un set di corpi di funzione dichiarati in precedenza.

Si tratta di un vtable C++, ad eccezione del fatto che è presente una voce per ogni sito di chiamata per un'interfaccia anziché per ogni metodo.

Non esiste alcun limite al numero di corpi delle funzioni che possono essere elencati in una tabella di funzioni.

È possibile fare riferimento più volte a una determinata funzione del corpo della funzione \# in una o più tabelle di funzioni, come modalità di condivisione del codice comune.

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

 

 





