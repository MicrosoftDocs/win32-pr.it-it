---
title: dcl_maxOutputVertexCount (SM4-ASM)
description: '\_maxOutputVertexCount DCL (SM4-ASM)'
ms.assetid: 91eb2dfc-f4ff-4f23-9cb4-ec5fdb676157
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31a09788b2f407673f57dad8a71792a5b02b7613
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993224"
---
# <a name="dcl_maxoutputvertexcount-sm4---asm"></a>\_maxOutputVertexCount DCL (SM4-ASM)

Dichiara il numero massimo di vertici che possono essere restituiti da un geometry shader.



| \_ *conteggio* maxOutputVertexCount DCL |
|-----------------------------------|



 



| Elemento                                                               | Descrizione                                                             |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="count"></span><span id="COUNT"></span>*conteggio*<br/> | \[in \] una Unsigned Integer a 32 bit compresa tra 1 e n, inclusi.<br/> |



 

Un geometry shader può restituire un massimo di valori a 1024 32 bit. Questo valore massimo include le dimensioni dei dati di input e le dimensioni dei dati creati dallo shader.

Di seguito sono riportate alcune limitazioni:

-   Se viene raggiunto il numero di vertici prima del completamento dell'esecuzione del geometry shader, lo shader termina.
-   Un geometry shader può raggiungere la fine del programma prima di eseguire l'output di tutti i vertici; Questo è perfettamente valido.
-   Se si esegue il debug di un geometry shader, è possibile indicare il numero di vertici generati contando il numero di istruzioni Emit generate.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Di seguito sono riportati alcuni esempi.

Si supponga che i dati di input siano composti da position (. xyzw) e color (. RGB). Ogni componente utilizza un byte; dato 7 byte, il numero massimo di vertici che lo shader può generare è 1024/(4 + 3) = 146.


```
dcl_maxOutputVertexCount 146
```



Si supponga che il geometry shader crei vettori di componenti 32 4. Il numero massimo di vertici che lo shader può generare è 1024/(32 \* 4) = 8.


```
dcl_maxOutputVertexCount 8
```



## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





