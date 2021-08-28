---
title: dcl_function_table (sm5 - asm)
description: Dichiarare una tabella di funzioni.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549653ee7316a664b628d5cdc692c091bdf042ad24e89b983c0fd3aac8a67ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490891"
---
# <a name="dcl_function_table-sm5---asm"></a>Tabella delle funzioni dcl \_ \_ (sm5 - asm)

Dichiarare una tabella di funzioni.



| dcl \_ function table ft = \_ \# {fb \# , fb , \# ...} |
|-----------------------------------------------|



 



| Elemento                                                      | Descrizione                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span id="ft"></span><span id="FT"></span>*Ft*<br/> | \[in \] Voci della tabella della funzione.<br/> |



 

## <a name="remarks"></a>Commenti

Questa funzione dichiara una tabella di funzioni come set di corpi di funzione dichiarati in precedenza.

È simile a una vtable C++, ad eccezione del fatto che è presente una voce per ogni sito di chiamata per un'interfaccia anziché per ogni metodo.

Non esiste alcun limite al numero di corpi di funzione che possono essere elencati in una tabella di funzioni.

È possibile fare riferimento più volte a un determinato corpo della funzione fb in una o più tabelle di funzioni, in modo da \# condividere il codice comune.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





