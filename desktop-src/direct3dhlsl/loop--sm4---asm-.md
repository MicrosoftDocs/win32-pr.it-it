---
title: loop (sm4 - asm)
description: Specifica un ciclo che esegue l'iterazione fino a quando non viene rilevata un'istruzione di interruzione.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dfc3090e71c1101e2c2748924de24f5443363ede76b86130cf63c3a319c76ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043769"
---
# <a name="loop-sm4---asm"></a>loop (sm4 - asm)

Specifica un ciclo che esegue l'iterazione fino a quando non viene rilevata un'istruzione di interruzione.



| loop |
|------|



 

## <a name="remarks"></a>Commenti

**Il** ciclo può eseguire un'iterazione illimitata, anche se l'esecuzione complessiva dello shader può essere forzata a terminare dopo l'esecuzione di alcune istruzioni.

Flow blocchi di controllo possono nidificare fino a 64 deep per subroutine e main. Il compilatore HLSL non genererà subroutine che superano questo limite. Il comportamento delle istruzioni del flusso di controllo oltre i 64 livelli di profondità per subroutine non è definito.

Il formato del token contiene l'offset [dell'istruzione endloop](endloop--sm4---asm-.md) corrispondente nello shader per praticità.

Nell'esempio seguente viene illustrato come usare l'istruzione del ciclo .

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 




