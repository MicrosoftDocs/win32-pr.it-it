---
title: chiamata (SM4-ASM)
description: Chiama una subroutine contrassegnata da dove l'etichetta l \ appare nel programma.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719399"
---
# <a name="call-sm4---asm"></a>chiamata (SM4-ASM)

Chiama una subroutine contrassegnata da dove viene visualizzata l'etichetta **l \#** nel programma.



| chiama l\# |
|----------|



 



| Elemento                                                       | Descrizione                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span id="l_"></span><span id="L_"></span>*l\#*<br/> | \[nell' \] etichetta della subroutine.<br/> |



 

## <a name="remarks"></a>Commenti

Quando viene rilevata una [ret](ret--sm4---asm-.md) , restituisce l'esecuzione all'istruzione dopo questa chiamata.

Il formato del token contiene l'offset dell'etichetta corrispondente nello shader per praticità.

Nell'esempio seguente viene illustrata l'istruzione Call.


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

-   Le subroutine possono annidare 32 a fondo.
-   Lo stack degli indirizzi restituiti viene gestito in modo trasparente dall'implementazione di.
-   Se sono già presenti 32 voci nello stack di indirizzi restituiti e viene eseguita una **chiamata** , la chiamata viene ignorata.
-   Nessun stack di parametri automatico. L'applicazione può usare una matrice di registro temporanea indicizzabile (x \# \[ \] ) per implementare manualmente uno stack. Tuttavia, gli indirizzi restituiti della chiamata subroutine non sono visibili e sono ortogonali a qualsiasi gestione dello stack manuale eseguita dall'applicazione.
-   L'indicizzazione del parametro *l \#* non è consentita.
-   La ricorsione non è consentita.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 





