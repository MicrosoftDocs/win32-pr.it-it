---
title: texm3x3 - ps
description: Esegue una moltiplicazione di matrice 3x3 se usata in combinazione con due istruzioni texm3x3pad - ps.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 17030bb99eb472b5cffe53474eb04c30159e5e30ffb2d219f1ac47dfce9da205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787734"
---
# <a name="texm3x3---ps"></a>texm3x3 - ps

Esegue una moltiplicazione di matrice 3x3 se usata in combinazione con due [istruzioni texm3x3pad - ps.](texm3x3pad---ps.md)

## <a name="syntax"></a>Sintassi



| texm3x3 dst, src |
|------------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3               |      | x    | x    |      |      |      |       |      |       |



 

Questa istruzione è uguale all'istruzione [texm3x3tex - ps,](texm3x3tex---ps.md) senza la ricerca della trama.

Questa istruzione viene usata come ultima di tre istruzioni che rappresentano un'operazione di moltiplicazione di matrice 3x3. La matrice 3x3 è costituita dalle coordinate della trama della terza fase della trama e dalle due fasi di trama precedenti. Qualsiasi trama assegnata a una delle tre fasi della trama viene ignorata.

Questa istruzione deve essere usata con due istruzioni texm3x3pad. I registri di trama devono seguire la sequenza seguente.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



Ecco altri dettagli su come viene eseguita la moltiplicazione 3x3.

La prima istruzione texm3x3pad esegue la prima riga della moltiplicazione per trovare u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

La seconda istruzione texm3x3pad esegue la seconda riga della moltiplicazione per trovare v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

L'istruzione texm3x3tex esegue la terza riga della moltiplicazione per trovare w<sup>'.</sup>

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Inserire il risultato della moltiplicazione della matrice nel registro di destinazione.

t(m+2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




