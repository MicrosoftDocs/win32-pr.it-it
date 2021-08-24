---
title: callc (sm4 - asm)
description: Chiama in modo condizionale una subroutine contrassegnata da dove viene visualizzata l'etichetta l\ nel programma.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb751b57a09704a2fec7a9c3afb69362873e3a1d2b43091efd984f67623188a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727161"
---
# <a name="callc-sm4---asm"></a>callc (sm4 - asm)

Chiama in modo condizionale una subroutine contrassegnata da dove viene visualizzata **l'etichetta \#** nel programma.



| callc{ \_ z\|\_nz} src0.select \_ component, l\# |
|----------------------------------------------|



 



| Elemento                                                            | Descrizione                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componente in cui testare la condizione.<br/> |
| <span id="l_"></span><span id="L_"></span>*L\#*<br/>      | \[in \] Etichetta della subroutine.<br/>                  |



 

## <a name="remarks"></a>Commenti

Quando viene [rilevato un ret,](ret--sm4---asm-.md) restituire l'esecuzione all'istruzione dopo questa chiamata.

Per praticità, il formato del token contiene l'offset dell'etichetta corrispondente nello shader.

Nell'esempio seguente viene illustrata l'istruzione di chiamata .


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret

```



### <a name="restrictions"></a>Restrizioni

-   Le subroutine possono annidare 32 livelli di profondità.
-   Lo stack di indirizzi mittente viene gestito in modo trasparente dall'implementazione di .
-   Se sono già presenti 32 voci nello  stack di indirizzi mittente e viene emessa una chiamata, la chiamata viene ignorata.
-   Non è disponibile alcun stack di parametri automatico. L'applicazione può usare una matrice di registri temporanei indicizzabili (x \# \[ \] ) per implementare manualmente uno stack. Tuttavia, gli indirizzi restituiti delle chiamate subroutine non sono visibili e sono ortogonali per qualsiasi gestione manuale dello stack eseguita dall'applicazione.
-   L'indicizzazione del *parametro l \#* non è consentita.
-   Il registro a 32 bit fornito da *src0* viene testato a livello di bit. Se un bit è diverso da zero, **callc \_ nz** eseguirà la chiamata. Se tutti i bit sono zero, **callc \_ z** eseguirà la chiamata.
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

 

 





