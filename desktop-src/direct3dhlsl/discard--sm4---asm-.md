---
title: Ignora (SM4-ASM)
description: Contrassegnare in modo condizionale i risultati del pixel shader da scartare al raggiungimento della fine del programma.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956069"
---
# <a name="discard-sm4---asm"></a>Ignora (SM4-ASM)

Contrassegnare in modo condizionale i risultati del pixel shader da scartare al raggiungimento della fine del programma.



| Ignora { \_ z \|\_NZ} src0. Select ( \_ componente) |
|-------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] valore che determina se annullare il pixel corrente in fase di elaborazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione contrassegna il pixel corrente come terminato, continuando l'esecuzione, in modo che altri pixel in esecuzione in parallelo possano ottenere i derivati, se necessario. Anche se l'esecuzione continua, tutte le scritture di output di pixel shader prima o dopo l'istruzione di **eliminazione** vengono scartate.

Per **scarto \_ z**, se tutti i bit in *src0. Select \_ Component* sono pari a zero, il pixel viene ignorato.

Per **scarto \_ NZ**, se i bit nel *\_ componente src0. Select* sono diversi da zero, il pixel viene ignorato.

Inoltre, l'istruzione di **eliminazione** può essere presente all'interno di qualsiasi costrutto di controllo di flusso.

È possibile che in uno shader siano presenti più istruzioni di **eliminazione** e, in caso di esecuzione, il pixel viene terminato.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





