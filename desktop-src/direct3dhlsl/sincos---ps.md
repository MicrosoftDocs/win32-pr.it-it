---
title: SinCos-PS
description: Calcola il seno e il coseno, in radianti. | SinCos-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995541"
---
# <a name="sincos---ps"></a>SinCos-PS

Calcola il seno e il coseno, in radianti.

## <a name="syntax"></a>Sintassi

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 e PS \_ 2 \_ x



| SinCos DST. x|y|XY}, src0. x|y|z|w}, src1, src2 |
|------------------------------------------------------|



 

Dove:

-   DST è il registro di destinazione e deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). Il registro di destinazione deve avere esattamente una delle tre maschere seguenti:. x \| . y \| . XY.
-   src0 è un registro di origine che fornisce l'angolo di input, che deve essere compreso tra \[ -pi, + pi \] . {x \| y \| z \| w} è la replica obbligatoria Swizzle.
-   src1 e src2 sono registri di origine e devono essere due diversi registri [float costanti](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ). I valori di src1 e src2 devono corrispondere rispettivamente alle macro [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) e [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) .

### <a name="ps_3_0"></a>PS \_ 3 \_ 0



| SinCos DST. x|y|XY}, src0. x|y|z|w |
|------------------------------------------|



 

Dove:

-   DST è un registro di destinazione e deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). Il registro di destinazione deve avere esattamente una delle tre maschere seguenti:. x \| . y \| . XY.
-   src0 è un registro di origine che fornisce l'angolo di input, che deve essere compreso tra \[ -pi, + pi \] . {x \| y \| z \| w} è la replica obbligatoria Swizzle.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| SinCos                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 e PS \_ 2 \_ x

Per PS \_ 2 \_ 0 e PS \_ 2 \_ x, è possibile usare SinCos con predicazione, ma con una restrizione a swizzle del [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0): è consentita solo la replica di swizzle (. x \| . y \| . z \| . w).

Per PS \_ 2 \_ 0 e PS \_ 2 \_ x, l'istruzione opera nel modo seguente (V = valore scalare da src0 con un swizzle di replica):

-   Se la maschera di scrittura è. x:
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è. y:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è. XY:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

Per PS \_ 3 \_ 0, è possibile usare SinCos con predicazione senza alcuna restrizione. Vedere [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).

Per PS \_ 3 \_ 0, l'istruzione funziona nel modo seguente (V = valore scalare da src0 con un swizzle di replica):

-   Se la maschera di scrittura è. x:
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è. y:
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è. XY:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
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

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
