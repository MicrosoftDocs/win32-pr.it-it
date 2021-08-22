---
title: swapc (sm5 - asm)
description: Esegue uno scambio condizionale per componente dei valori tra due registri di input.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d09d52bd497c7819500c11c4464907e4a7854bb305ed0e31d53b897ba4cf7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486261"
---
# <a name="swapc-sm5---asm"></a>swapc (sm5 - asm)

Esegue uno scambio condizionale per componente dei valori tra due registri di input.



| swapc dest0 \[ \] .mask, dest1 \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle, \] src2 \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                               | Descrizione                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[in Registra con maschere di scrittura \] arbitrarie nonempty. Deve essere diverso da *dest1*.<br/> |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[in Registra con maschere di scrittura \] arbitrarie nonempty. Deve essere diverso da *dest0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[in \] Fornisce 4 condizioni. Un valore intero diverso da zero indica **true.** <br/>               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[in \] Uno dei valori da scambiare.<br/>                                              |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/>    | \[in \] Uno dei valori da scambiare.<br/>                                              |



 

## <a name="remarks"></a>Commenti

La codifica di questa istruzione tenta di esprimere in modo compatto più scambi condizionali paralleli di scalari in due registri a 4 componenti, con una minore flessibilità nella disposizione delle coppie di numeri coinvolte nello scambio.

La scelta di register e value per *src0,* *src1* e *src2* non è vincolata in alcun modo, ad [esempio movc](movc--sm4---asm-.md).

La semantica di questa istruzione può essere descritta dalle operazioni equivalenti con **l'istruzione movc.** Il caso peggiore è illustrato nell'esempio seguente, assicurando che i registri di destinazione non siano aggiornati fino alla fine.

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

È possibile scegliere come affrontare l'attività, se non direttamente. Ad esempio, lo stesso effetto può essere ottenuto da una sequenza di un massimo di 4 semplici scambi condizionali scalari o, come sopra, da due istruzioni **movc** vettoriali, oltre a un sovraccarico per assicurarsi che i valori di origine non siano clobbered dalle operazioni precedenti durante l'espansione.

Usare questa istruzione per l'ordinamento.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





