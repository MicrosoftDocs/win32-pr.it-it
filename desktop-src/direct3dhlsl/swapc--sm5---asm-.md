---
title: swapc (SM5-ASM)
description: Esegue uno scambio condizionale per componente dei valori tra due registri di input.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d2ee674a1cb1067594b0e96c739ff8df73b152
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993088"
---
# <a name="swapc-sm5---asm"></a>swapc (SM5-ASM)

Esegue uno scambio condizionale per componente dei valori tra due registri di input.



| swapc dest0 \[ . mask \] , DesT1 \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                               | Descrizione                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[in \] registra con maschere di scrittura non vuote arbitrarie. Deve essere diverso da *DesT1*.<br/> |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[in \] registra con maschere di scrittura non vuote arbitrarie. Deve essere diverso da *dest0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[in \] fornisce 4 condizioni. Un valore integer diverso da zero indica **true**. <br/>               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[in \] uno dei valori da scambiare.<br/>                                              |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/>    | \[in \] uno dei valori da scambiare.<br/>                                              |



 

## <a name="remarks"></a>Commenti

La codifica di questa istruzione tenta di esprimere in modo compatto più scambi condizionali paralleli di scalari tra i registri dei componenti 2 4, con una minore flessibilità nella disposizione delle coppie di numeri interessati dallo scambio.

La scelta del registro e del valore per *src0*, *src1* e *src2* non è vincolata in alcun modo, ad esempio [MOVC](movc--sm4---asm-.md).

La semantica di questa istruzione può essere descritta dalle operazioni equivalenti con l'istruzione **MOVC** . Il caso peggiore è illustrato nell'esempio seguente, assicurandosi che i registri di destinazione non vengano aggiornati fino alla fine.

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

È possibile scegliere come affrontare l'attività, se non direttamente. Ad esempio, lo stesso effetto può essere ottenuto da una sequenza di un massimo di quattro scambi condizionali semplici scalari, o come sopra, due istruzioni **MOVC** vettoriali, oltre a qualsiasi overhead per assicurarsi che i valori di origine non vengano compromessi dalle operazioni precedenti durante l'espansione.

Usare questa istruzione per l'ordinamento.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





