---
title: dcl_maxOutputVertexCount (sm4 - asm)
description: dcl \_ maxOutputVertexCount (sm4 - asm)
ms.assetid: 91eb2dfc-f4ff-4f23-9cb4-ec5fdb676157
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ba7783575ac5782c63bc1ec3ca5f56f6ffe9a1bc7483f3f01ccbcf8adac5e23f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068521"
---
# <a name="dcl_maxoutputvertexcount-sm4---asm"></a>dcl \_ maxOutputVertexCount (sm4 - asm)

Dichiara il numero massimo di vertici che possono essere restituiti da un geometry shader.



| dcl \_ maxOutputVertexCount *count* |
|-----------------------------------|



 



| Elemento                                                               | Descrizione                                                             |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="count"></span><span id="COUNT"></span>*Conteggio*<br/> | \[in \] un intero senza segno a 32 bit compreso tra 1 e n inclusi.<br/> |



 

Un geometry shader può ottenere un massimo di 1024 valori a 32 bit. Questo valore massimo include le dimensioni dei dati di input e le dimensioni dei dati creati dallo shader.

Ecco alcune limitazioni:

-   Se il numero di vertici viene raggiunto prima del completamento dell'esecuzione dello shader geometry, lo shader termina.
-   Uno shader geometrico può raggiungere la fine del programma prima dell'output di tutti i vertici. Questo è perfettamente legale.
-   Se si esegue il debug di un geometry shader, è possibile indicare il numero di vertici generati contando il numero di istruzioni di creazione generate.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. Non è possibile creare uno shader in linguaggio assembly usando il modello shader 4.

## <a name="example"></a>Esempio

Di seguito sono riportati alcuni esempi.

Si supponga che i dati di input siano di posizione (.xyzw) e colore (.rgb). Ogni componente utilizza un byte. dati 7 byte, il numero massimo di vertici che lo shader può generare sarebbe 1024 / (4 + 3) = 146.


```
dcl_maxOutputVertexCount 146
```



Si supponga che lo shader geometrico crei 32 vettori a 4 componenti. Il numero massimo di vertici che lo shader può generare è 1024 / (32 \* 4) = 8.


```
dcl_maxOutputVertexCount 8
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

 

 





