---
title: sincos - vs
description: Calcola il seno e il coseno, in radianti. | sincos - vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e132e0070b8fb1e6629fe6dab46fd3801a7e8989637b60602500bc1c66a2f87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905960"
---
# <a name="sincos---vs"></a>sincos - vs

Calcola il seno e il coseno, in radianti.

## <a name="syntax"></a>Sintassi

### <a name="vs_2_0-and-vs_2_x"></a>vs \_ 2 \_ 0 e vs \_ 2 \_ x



| sincos dst. {x\|y\|xy}, src0. {x\|y\|z\|w}, src1, src2 |
|------------------------------------------------------|



 

Dove:

-   dst è il registro di destinazione e deve essere un [registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). Il registro di destinazione deve avere esattamente una delle tre maschere seguenti: .x \| .y \| .xy.
-   src0 è un registro di origine che fornisce l'angolo di input, che deve essere all'interno di \[ -pi greco, +pi \] greco. {x \| y \| z \| w} è lo swizzle di replica richiesto.
-   src1 e src2 sono registri di origine e devono essere due diversi [Registri costanti float](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c \# ). I valori di src1 e src2 devono corrispondere rispettivamente alle macro [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) e [**D3DSINCOSCONST2.**](/windows/desktop/direct3d9/d3dsincosconst2)

### <a name="vs_3_0"></a>vs \_ 3 \_ 0



| sincos dst. {x\|y\|xy}, src0. {x\|y\|z\|w} |
|------------------------------------------|



 

Dove:

-   dst è un registro di destinazione e deve essere un [registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). Il registro di destinazione deve avere esattamente una delle tre maschere seguenti: .x \| .y \| .xy.
-   src0 è un registro di origine che fornisce l'angolo di input, che deve essere all'interno di \[ -pi greco, +pi \] greco. {x \| y \| z \| w} è lo swizzle di replica richiesto.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Sincos                 |      | x    | x    | x     | x    | x     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a>vs \_ 2 \_ 0 e vs \_ 2 \_ x Osservazioni

Per le versioni 2 0 e 2 x, i sinco possono essere usati con la predicazione, ma con una restrizione per lo swizzle del registro predicato (p0): è consentita solo la replica dello \_ \_ \_ \_ swizzle (.x [](dx9-graphics-reference-asm-vs-registers-predicate.md) \| .y \| .z \| .w).

Per vs \_ 2 0 e vs 2 x, l'istruzione funziona come segue: (V = valore scalare da src0 con uno \_ \_ \_ swizzle di replica):

-   Se la maschera di scrittura è .x:
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è .y:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è xy:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a>vs \_ 3 \_ 0 Osservazioni

Per la \_ versione 3 \_ 0, i sinco possono essere usati con la predicazione senza alcuna restrizione. Vedere [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).

Per vs 3 0, l'istruzione funziona come segue: (V = valore scalare da \_ \_ src0 con uno swizzle di replica)

-   Se la maschera di scrittura è .x:
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è .y:
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è xy:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

L'applicazione può eseguire il mapping di un angolo arbitrario (in radianti) all'intervallo \[ -pi greco, +pi \] greco usando lo pseudocodice shader seguente:


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
