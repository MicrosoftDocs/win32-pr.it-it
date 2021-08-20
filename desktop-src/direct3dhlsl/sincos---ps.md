---
title: sincos - ps
description: Calcola il seno e il coseno, in radianti. | sincos - ps
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 95f61c3a1cfc15f699e0e637dce8d58b9517ffe58ef36e529ec297661bff6a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671571"
---
# <a name="sincos---ps"></a>sincos - ps

Calcola il seno e il coseno, in radianti.

## <a name="syntax"></a>Sintassi

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 e ps \_ 2 \_ x



| sincos dst. {x\|y\|xy}, src0. {x\|y\|z\|w}, src1, src2 |
|------------------------------------------------------|



 

Dove:

-   dst è il registro di destinazione e deve essere un registro [temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). Il registro di destinazione deve avere esattamente una delle tre maschere seguenti: .x \| .y \| .xy.
-   src0 è un registro di origine che fornisce l'angolo di input, che deve essere all'interno \[ di -pi greco, +pi \] greco. {x \| y \| z \| w} è lo swizzle di replica richiesto.
-   src1 e src2 sono registri di origine e devono essere due registri [costanti float](dx9-graphics-reference-asm-ps-registers-constant-float.md)diversi (c \# ). I valori di src1 e src2 devono corrispondere rispettivamente a quello delle macro [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) e [**D3DSINCOSCONST2.**](/windows/desktop/direct3d9/d3dsincosconst2)

### <a name="ps_3_0"></a>ps \_ 3 \_ 0



| sincos dst. {x\|y\|xy}, src0. {x\|y\|z\|w} |
|------------------------------------------|



 

Dove:

-   dst è un registro di destinazione e deve essere un registro [temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). Il registro di destinazione deve avere esattamente una delle tre maschere seguenti: .x \| .y \| .xy.
-   src0 è un registro di origine che fornisce l'angolo di input, che deve essere all'interno \[ di -pi greco, +pi \] greco. {x \| y \| z \| w} è lo swizzle di replica richiesto.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Sincos                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 e ps \_ 2 \_ x

Per ps 2 0 e ps 2 x, i sinco possono essere usati con la predicazione, ma con una restrizione al giretto del registro predicati (p0): è consentita solo la replica dello \_ \_ \_ \_ swizzle (.x [](dx9-graphics-reference-asm-ps-registers-predicate.md) \| .y \| .z \| .w).

Per ps 2 0 e ps 2 x, l'istruzione funziona come segue (V = il valore scalare da \_ \_ \_ \_ src0 con uno swizzle di replica):

-   Se la maschera di scrittura è .x:
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è .y:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è xy:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

Per ps \_ 3 \_ 0, i sinco possono essere usati con la predicazione senza alcuna restrizione. Vedere [Registro predicati](dx9-graphics-reference-asm-ps-registers-predicate.md).

Per ps 3 0, l'istruzione funziona come segue (V = valore scalare da \_ \_ src0 con uno swizzle di replica):

-   Se la maschera di scrittura è .x:
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è .y:
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se la maschera di scrittura è xy:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

L'applicazione può eseguire il mapping di un angolo arbitrario (in radianti) all'intervallo \[ -pi greco, +pi greco \] usando lo pseudocodice shader seguente:


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
