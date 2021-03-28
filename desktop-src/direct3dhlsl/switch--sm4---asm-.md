---
title: Switch (SM4-ASM)
description: Trasferisce il controllo a un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046088"
---
# <a name="switch-sm4---asm"></a>Switch (SM4-ASM)

Trasferisce il controllo a un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.



| cambia il componente src0. Selected \_ |
|---------------------------------|



 



| Elemento                                                            | Descrizione                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] selettore per l'istruzione switch.<br/> |



 

## <a name="remarks"></a>Commenti

Un  / costrutto Switch [endswitch](endswitch--sm4---asm-.md) si comporta esattamente come un costrutto **Switch** nel linguaggio C, con la seguente eccezione: per le istruzioni predefinite del [case](case--sm4---asm-.md)d3d11 che passano fino / [](default--sm4---asm-.md) al  / **valore predefinito** del case successivo senza [interruzioni](break--sm4---asm-.md) non possono contenere codice. È consentita la visualizzazione sequenziale di più istruzioni **case** , inclusa quella **predefinita**, che condividono lo stesso blocco di codice.

La condizione deve essere un componente di registro a 32 bit o una quantità immediata. Il confronto di uguaglianza è bit per bit (Integer).

Come per qualsiasi istruzione shader in D3D11, l'hardware può o meno implementare direttamente il costrutto **Switch** .

Le istruzioni **Switch** possono essere annidate. Ogni blocco **Switch** viene conteggiato come 1 livello rispetto al limite di profondità di nidificazione del controllo di flusso di 64 per subroutine e Main, indipendentemente dal numero di istruzioni **case** . Il compilatore HLSL non genererà subroutine che superano questo limite. Il comportamento delle istruzioni del flusso di controllo oltre 64 livelli di profondità per subroutine non è definito.

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

 

 





