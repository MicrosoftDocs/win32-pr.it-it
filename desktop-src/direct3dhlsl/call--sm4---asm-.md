---
title: call (sm4 - asm)
description: Chiama una subroutine contrassegnata da dove viene visualizzata l'etichetta l\ nel programma.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c55ce1c0005014928c006e29c9d7d08c3cadc3d11fee870ea1c9fa39df514fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516654"
---
# <a name="call-sm4---asm"></a>call (sm4 - asm)

Chiama una subroutine contrassegnata da dove viene visualizzata **\# l'etichetta** nel programma.



| call l\# |
|----------|



 



| Elemento                                                       | Descrizione                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span id="l_"></span><span id="L_"></span>*L\#*<br/> | \[in \] Etichetta della subroutine.<br/> |



 

## <a name="remarks"></a>Commenti

Quando viene [rilevato un ret,](ret--sm4---asm-.md) restituire l'esecuzione all'istruzione dopo questa chiamata.

Per praticità, il formato del token contiene l'offset dell'etichetta corrispondente nello shader.

Nell'esempio seguente viene illustrata l'istruzione di chiamata .


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a>Restrizioni

-   Le subroutine possono annidare 32 deep.
-   Lo stack di indirizzi mittente viene gestito in modo trasparente dall'implementazione di .
-   Se sono già presenti 32 voci nello  stack di indirizzi mittente e viene emessa una chiamata, la chiamata viene ignorata.
-   Non è disponibile alcun stack di parametri automatico. L'applicazione può usare una matrice di registri temporanei indicizzabili (x \# \[ \] ) per implementare manualmente uno stack. Tuttavia, gli indirizzi restituiti delle chiamate subroutine non sono visibili e sono ortogonali per qualsiasi gestione manuale dello stack eseguita dall'applicazione.
-   L'indicizzazione del *parametro l \#* non è consentita.
-   La ricorsione non è consentita.

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

 

 





