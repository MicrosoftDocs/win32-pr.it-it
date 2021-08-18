---
title: switch (sm4 - asm)
description: Trasferisce il controllo a un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39cb304c1ccf59c188a4e1f20f2b136897d833c80d6eb67cb0eb683d628ab9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724352"
---
# <a name="switch-sm4---asm"></a>switch (sm4 - asm)

Trasferisce il controllo a un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.



| switch src0.selected \_ component |
|---------------------------------|



 



| Elemento                                                            | Descrizione                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Selettore per l'istruzione switch.<br/> |



 

## <a name="remarks"></a>Commenti

Un costrutto **switch** endswitch si comporta esattamente come un costrutto switch nel linguaggio C, con l'eccezione seguente: per le istruzioni predefinite del case / [](endswitch--sm4---asm-.md) D3D11  che passano all'impostazione predefinita case successiva senza un'interruzione non possono contenere [](case--sm4---asm-.md) / [](default--sm4---asm-.md)  /  codice. [](break--sm4---asm-.md) È consentito che più **istruzioni case,** inclusa **quella** predefinita, vengano visualizzate in sequenza, condividendo lo stesso blocco di codice.

La condizione deve essere un componente registro a 32 bit o una quantità immediata. Il confronto di uguaglianza è bit per bit (integer).

Come per qualsiasi istruzione Shader in D3D11, l'hardware può implementare direttamente o meno il **costrutto switch.**

**Le istruzioni switch** possono essere annidate. Ogni **blocco switch** viene conteggiato come livello 1 rispetto al limite di profondità di annidamento del controllo di flusso di 64 per subroutine e main, indipendentemente dal numero di istruzioni **case.** Il compilatore HLSL non genererà subroutine che superano questo limite. Il comportamento delle istruzioni del flusso di controllo oltre i 64 livelli di profondità per subroutine non è definito.

Nell'esempio seguente viene illustrato come utilizzare questa istruzione.

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
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

 

 





