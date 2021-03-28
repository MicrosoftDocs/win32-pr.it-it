---
title: SinCos-vs
description: Calcola il seno e il coseno, in radianti. | SinCos-vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969236"
---
# <a name="sincos---vs"></a>SinCos-vs

Calcola il seno e il coseno, in radianti.

## <a name="syntax"></a>Sintassi

### <a name="vs_2_0-and-vs_2_x"></a>vs \_ 2 \_ 0 e vs \_ 2 \_ x



| SinCos DST. x|y|XY}, src0. x|y|z|w}, src1, src2 |
|------------------------------------------------------|



 

Dove:

-   DST è il registro di destinazione e deve essere un [registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). Il registro di destinazione deve avere esattamente una delle tre maschere seguenti:. x \| . y \| . XY.
-   src0 è un registro di origine che fornisce l'angolo di input, che deve essere compreso tra \[ -pi, + pi \] . {x \| y \| z \| w} è la replica obbligatoria Swizzle.
-   src1 e src2 sono registri di origine e devono essere due diversi registri [float costanti](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c \# ). I valori di src1 e src2 devono corrispondere rispettivamente alle macro [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) e [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) .

### <a name="vs_3_0"></a>vs \_ 3 \_ 0



| SinCos DST. x|y|XY}, src0. x|y|z|w |
|------------------------------------------|



 

Dove:

-   DST è un registro di destinazione e deve essere un [registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). Il registro di destinazione deve avere esattamente una delle tre maschere seguenti:. x \| . y \| . XY.
-   src0 è un registro di origine che fornisce l'angolo di input, che deve essere compreso tra \[ -pi, + pi \] . {x \| y \| z \| w} è la replica obbligatoria Swizzle.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| SinCos                 |      | x    | x    | x     | x    | x     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a>\_osservazioni vs 2 \_ 0 e vs \_ 2 \_ x

Per vs \_ 2 \_ 0 e vs \_ 2 \_ x, è possibile usare SinCos con predicazione, ma con una restrizione a swizzle del [registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0): è consentita solo la replica di swizzle (. x \| . y \| . z \| . w).

Per vs \_ 2 \_ 0 e vs \_ 2 \_ x, l'istruzione funziona nel modo seguente: (V = valore scalare da src0 con un swizzle di replica):

-   Se la maschera di scrittura è. x:
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è. y:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è. XY:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a>Osservazioni di vs \_ 3 \_ 0

Per vs \_ 3 \_ 0, SinCos può essere usato con predicazione senza alcuna restrizione. Vedere [registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md).

Per vs \_ 3 \_ 0, l'istruzione funziona nel modo seguente: (V = valore scalare da src0 con un swizzle di replica)

-   Se la maschera di scrittura è. x:
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è. y:
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è. XY:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

L'applicazione può eseguire il mapping di un angolo arbitrario (in radianti) all'intervallo \[ -pi, + pi greco \] usando lo pseudocodice dello shader seguente:


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
