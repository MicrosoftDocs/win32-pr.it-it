---
title: discard (sm4 - asm)
description: Contrassegnare in modo condizionale i risultati di Pixel Shader da eliminare quando viene raggiunta la fine del programma.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6b5744ee8cf8d2953247711d95fe5d5ec6f96c36c700e1a38ce4e0cb1e1ff5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986601"
---
# <a name="discard-sm4---asm"></a>discard (sm4 - asm)

Contrassegnare in modo condizionale i risultati di Pixel Shader da eliminare quando viene raggiunta la fine del programma.



| discard{ \_ z\|\_nz} src0.select \_ component |
|-------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Valore che determina se eliminare il pixel corrente in fase di elaborazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione contrassegna il pixel corrente come terminato, continuando l'esecuzione, in modo che altri pixel in esecuzione in parallelo possano ottenere derivati, se necessario. Anche se l'esecuzione continua, tutte le scritture di output pixel shader prima o dopo l'istruzione **discard** vengono eliminate.

Per **discard \_ z**, se tutti i bit nel *componente src0.select \_* sono pari a zero, il pixel viene eliminato.

Per **discard \_ nz**, se i bit nel *componente \_ src0.select* sono diversi da zero, il pixel viene eliminato.

Inoltre, **l'istruzione discard** può essere presente all'interno di qualsiasi costrutto di controllo di flusso.

In **uno** shader possono essere presenti più istruzioni discard e, se vengono eseguite, il pixel viene terminato.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





