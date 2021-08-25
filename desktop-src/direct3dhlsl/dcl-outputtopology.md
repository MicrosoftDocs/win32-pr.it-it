---
title: dcl_outputTopology (sm4 - asm)
description: dcl \_ outputTopology (sm4 - asm)
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6a3b46dc226a85593a17b02118ed52088ed75d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471997"
---
# <a name="dcl_outputtopology-sm4---asm"></a>dcl \_ outputTopology (sm4 - asm)

Dichiara i dati di output geometry-shader del tipo primitivo.



| dcl \_ outputTopology *Type* |
|----------------------------|



 




| Elemento | Descrizione | 
|------|-------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Digitare</em><br /> | [in] Topologia primitiva di output, che è uno dei valori seguenti: <br /><ul><li><em>elenco di punti</em></li><li><em>linestrip</em></li><li><em>trianglestrip</em></li></ul> | 




 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader nel linguaggio di assembly usando Shader Model 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_outputTopology trianglestrip
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

 

 





