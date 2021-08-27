---
title: dcl_indexRange (sm4 - asm)
description: dcl \_ indexRange (sm4 - asm)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6fe587c3a5cfeae21b5da09a2dd79b67b82bc0c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472067"
---
# <a name="dcl_indexrange-sm4---asm"></a>dcl \_ indexRange (sm4 - asm)

Dichiara un intervallo di registri a cui sarà possibile accedere tramite indice (un numero intero calcolato nello shader).



| dcl \_ indexRange *minRegisterM*, *maxRegisterN* |
|------------------------------------------------|



 




| Elemento | Descrizione | 
|------|-------------|
| <span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em><br /> | [in] Primo registro a cui accedere in base all'indice. <br /><ul><li><em>minRegister</em> è <strong>v</strong> per un vertice o pixel shader di input o <strong>o per</strong> un registro di output vertex shader.</li><li><em>M</em> è un numero intero che indica il numero di registro.</li></ul> | 
| <span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br /> | [in] Ultimo registro a cui accedere in base all'indice. Lo stesso formato di <em>minRegister,</em> ad eccezione <em>di N,</em> è il numero di registro.<br /> | 




 

A tutti i registri si applicano le restrizioni seguenti:

-   I registri min e max devono essere dello stesso tipo e avere le stesse maschere dei componenti (se le maschere sono dichiarate).
-   Un registro può avere più intervalli di indici, purché non si sovrappongano.
-   Il numero di registro minimo deve essere minore del numero massimo di registri.
-   Un registro di indice non può contenere [un valore di sistema](dx-graphics-hlsl-semantics.md).
-   L'indicizzazione di un registro all'esterno della dichiarazione di indice massimo produce risultati non definiti.

I registri di input pixel shader devono usare la stessa modalità di interpolazione. pixel shader i registri di output non sono indicizzabili.

Un registro di input geometry shader ha due dimensioni (asse vertice, asse degli attributi); L'intervallo di indici si applica solo all'asse degli attributi perché l'asse dei vertici è sempre completamente indicizzabile.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader nel linguaggio di assembly usando Shader Model 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





