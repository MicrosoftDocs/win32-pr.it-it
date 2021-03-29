---
title: Informazioni di riferimento su ASM shader
description: Gli shader guidano la pipeline grafica programmabile.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2019
ms.locfileid: "104976543"
---
# <a name="asm-shader-reference"></a>Informazioni di riferimento su ASM shader

Gli shader guidano la pipeline grafica programmabile.

## <a name="vertex-shader-reference"></a>Riferimento vertex shader

-   [vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-1-1.md)
-   [vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-2-0.md)
-   [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md)
-   [vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-3-0.md)

[Differenze tra vertex shader](dx9-graphics-reference-asm-vs-differences.md) riepiloga le differenze tra le versioni di vertex shader.

## <a name="pixel-shader-reference"></a>Riferimento a pixel shader

-   [PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-1-x.md)
-   [PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-2-0.md)
-   [PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-2-x.md)
-   [PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-3-0.md)

[Differenze pixel shader](dx9-graphics-reference-asm-ps-differences.md) riepiloga le differenze tra pixel shader versioni.

## <a name="shader-model-4-and-5-reference"></a>Riferimento al modello Shader 4 e 5

Le sezioni assembly [Shader Model 4 assembly](dx-graphics-hlsl-sm4-asm.md) e [Shader Model 5](shader-model-5-assembly--directx-hlsl-.md) sono descritte le istruzioni supportate dal modello Shader 4 e 5.

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a>Comportamento dei registri costanti negli shader degli assembly

Esistono due modi per impostare i registri costanti in un assembly shader:

-   Dichiarare una costante dello shader nel codice assembly usando una delle istruzioni def \* .
-   Usare uno dei metodi dell' \* \* \* API set ShaderConstant \* .

### <a name="direct3d-9-shader-constants"></a>Costanti shader Direct3D 9

In Direct3D 9 la durata delle costanti definite in un dato shader è confinata solo all'esecuzione di tale shader (e non è sottoponibile a override). Le costanti definite in Direct3D 9 non hanno effetti collaterali al di fuori dello shader.

Di seguito è riportato un esempio di utilizzo di Direct3D 9:


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



In Direct3D 9 la chiamata a Get \* \* \* ShaderConstant \* recupererà solo i valori costanti impostati tramite set \* \* \* ShaderConstant \* .

### <a name="direct3d-8-shader-constants"></a>Costanti shader Direct3D 8

Questo comportamento è diverso in Direct3D 8. x.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



In Direct3D 8. x set \* \* \* ShaderConstant viene applicato immediatamente. Si consideri lo scenario indicato di seguito.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



Il risultato indesiderato è che l'ordine in cui gli shader sono impostati potrebbe influire sul comportamento osservato dei singoli shader.

## <a name="shader-driver-model-requirements"></a>Requisiti del modello di driver shader

Le interfacce Direct3D 9 sono limitate ai driver DDI (Device Driver Interface) che sono a livello di DirectX 7 e versioni successive. Per controllare il livello di DDI, eseguire lo [strumento di diagnostica DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) ed esaminare il file di testo salvato.

Per riferimento, le interfacce Direct3D 8 funzionano solo su driver DDI con estensione DirectX 6 e versioni successive.

## <a name="shader-binary-format"></a>Formato binario dello shader

Il layout bit per bit del flusso di istruzioni dello shader è definito in D3d9types. h. Se si desidera progettare il proprio compilatore shader o gli strumenti di costruzione e si desiderano ulteriori informazioni sul flusso di token shader, fare riferimento a Direct3D 9 Driver Development Kit (DDK).

## <a name="c-like-shader-language"></a>Linguaggio shader simile a C

Vedere informazioni di [riferimento su HLSL](dx-graphics-hlsl-reference.md) per sperimentare un linguaggio di shader simile a C.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento per HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




