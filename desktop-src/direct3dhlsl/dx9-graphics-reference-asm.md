---
title: Informazioni di riferimento su Asm Shader
description: Gli shader guidano la pipeline di grafica programmabile.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9dbeb680b7131581b3891e59bb6bd2db0d6e5c19eb6279c47b83d22f01b5000e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119545"
---
# <a name="asm-shader-reference"></a>Informazioni di riferimento su Asm Shader

Gli shader guidano la pipeline di grafica programmabile.

## <a name="vertex-shader-reference"></a>Informazioni di riferimento sul vertex shader

-   [vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-1-1.md)
-   [vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-2-0.md)
-   [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md)
-   [vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-3-0.md)

[Differenze vertex shader riepiloga](dx9-graphics-reference-asm-vs-differences.md) le differenze tra le versioni di vertex shader.

## <a name="pixel-shader-reference"></a>Informazioni di riferimento sui pixel shader

-   [ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4](dx9-graphics-reference-asm-ps-1-x.md)
-   [ps \_ 2 \_ 0](dx9-graphics-reference-asm-ps-2-0.md)
-   [ps \_ 2 \_ x](dx9-graphics-reference-asm-ps-2-x.md)
-   [ps \_ 3 \_ 0](dx9-graphics-reference-asm-ps-3-0.md)

[Differenze dei pixel shader](dx9-graphics-reference-asm-ps-differences.md) riepiloga le differenze tra pixel shader versioni.

## <a name="shader-model-4-and-5-reference"></a>Informazioni di riferimento sul modello shader 4 e 5

Le [sezioni Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) e Shader Model [5 Assembly](shader-model-5-assembly--directx-hlsl-.md) descrivono le istruzioni supportate dal modello shader 4 e 5.

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a>Comportamento dei registri costanti negli shader di assembly

Esistono due modi per impostare i registri costanti in un assembly shader:

-   Dichiarare una costante shader nel codice dell'assembly usando una delle istruzioni \* def.
-   Usare uno dei metodi dell'API Set \* \* \* ShaderConstant. \*

### <a name="direct3d-9-shader-constants"></a>Costanti dello shader Direct3D 9

In Direct3D 9 la durata delle costanti definite in un determinato shader è limitata solo all'esecuzione di tale shader (ed è non sottoponibile a override). Le costanti definite in Direct3D 9 non hanno effetti collaterali all'esterno dello shader.

Ecco un esempio di uso di Direct3D 9:


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



In Direct3D 9, la chiamata a Get ShaderConstant recupererà solo i valori \* \* \* costanti impostati tramite \* Set \* \* \* ShaderConstant. \*

### <a name="direct3d-8-shader-constants"></a>Costanti dello shader Direct3D 8

Questo comportamento è diverso in Direct3D 8.x.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



In Direct3D 8.x Set \* \* \* ShaderConstant ha effetto immediato. Si consideri lo scenario indicato di seguito.


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



Il risultato indesiderato è che l'ordine in cui vengono impostati gli shader può influire sul comportamento osservato dei singoli shader.

## <a name="shader-driver-model-requirements"></a>Requisiti del modello di driver shader

Le interfacce Direct3D 9 sono limitate ai driver DDI (Device Driver Interface) di livello DirectX 7 e superiori. Per controllare il livello DDI, eseguire lo [strumento di diagnostica DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) ed esaminare il file di testo salvato.

Per riferimento, le interfacce Direct3D 8 funzionano solo su driver DDI di livello DirectX 6 e superiori.

## <a name="shader-binary-format"></a>Formato binario shader

Il layout bit per bit del flusso di istruzioni shader è definito in D3d9types.h. Se si vogliono progettare strumenti di compilazione o compilatore shader personalizzati e si vogliono altre informazioni sul flusso del token shader, vedere Direct3D 9 Driver Development Kit (DDK).

## <a name="c-like-shader-language"></a>Linguaggio shader simile a C

Vedere [Informazioni di riferimento su HLSL](dx-graphics-hlsl-reference.md) per sperimentare un linguaggio shader simile a C.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento per HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




