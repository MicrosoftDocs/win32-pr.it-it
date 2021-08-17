---
title: dcl_temps (sm4 - asm)
description: dcl \_ temps (sm4 - asm)
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6426caff8ecd347ce8233f15df6b914a53c647ae79fb50a530b531e9207bf1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726809"
---
# <a name="dcl_temps-sm4---asm"></a>dcl \_ temps (sm4 - asm)

Dichiara i registri temporanei.



| dcl \_ temps N |
|--------------|



 



| Elemento                                                   | Descrizione                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[in \] Numero di registri temporanei.<br/> |



 

Ogni registro ha spazio per un valore a quattro componenti a 32 bit. Il numero totale di registri temporanei [e indicizzabili-temporanei](dcl-indexabletemp.md) deve essere minore o uguale a 4096.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. Non è possibile creare uno shader in linguaggio assembly usando il modello shader 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_temps 10; // Declare r0-r9
```



## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





