---
title: texm3x3tex - ps
description: Esegue una moltiplicazione di matrice 3x3 e usa il risultato per eseguire una ricerca trame. texm3x3tex deve essere usato con due istruzioni texm3x3pad - ps.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a40c78fddadde5d58186f9a1ebb01f4d021620862f9d3534e535842a848a2e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787560"
---
# <a name="texm3x3tex---ps"></a>texm3x3tex - ps

Esegue una moltiplicazione di matrice 3x3 e usa il risultato per eseguire una ricerca trame. texm3x3tex deve essere usato con due [istruzioni texm3x3pad - ps.](texm3x3pad---ps.md)

## <a name="syntax"></a>Sintassi



| texm3x3tex dst, src |
|---------------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3tex            | x    | x    | x    |      |      |      |       |      |       |



 

Questa istruzione viene usata come finale di tre istruzioni che rappresentano un'operazione di moltiplicazione di matrice 3x3, seguita da una ricerca trame. La matrice 3x3 è costituita da coordinate di trama della terza fase della trama e delle due fasi di trama precedenti. Il vettore a tre componenti risultante (u,v,w) viene usato per campionare la trama nella fase 3. Qualsiasi trama assegnata alle due fasi di trama precedenti viene ignorata. La moltiplicazione di matrice 3x3 è in genere utile per orientare un vettore normale nello spazio tangente corretto per la superficie di cui viene eseguito il rendering.

Questa istruzione deve essere usata con l'istruzione texm3x3pad. I registri di trama devono usare la sequenza seguente.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



Di seguito sono fornite informazioni più dettagliate sul modo in cui viene eseguita la moltiplicazione 3x3.

La prima istruzione texm3x3pad esegue la prima riga della moltiplicazione per trovare u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

La seconda istruzione texm3x3pad esegue la seconda riga della moltiplicazione per trovare v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

L'istruzione texm3x3spec esegue la terza riga della moltiplicazione per trovare w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Infine,<sup>l'istruzione</sup>texm3x3tex esempi t(m+2) con (u<sup>'</sup>,v<sup>',w</sup>' ) e archivia il risultato in t(m+2).

t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> usando (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) come coordinate.

## <a name="examples"></a>Esempio

Ecco un esempio di shader con le mappe di trama identificate e le fasi della trama identificate.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



Questo esempio richiede la configurazione della fase di trama seguente.

-   Alla fase 0 viene assegnata una mappa trame con dati normali. Questa mappa viene spesso definita mappa di rilievo. I dati sono normali (XYZ) per ogni texel. Il set di coordinate di trama 0 definisce come campionare questa mappa normale.
-   Il set di coordinate di trama 1 viene assegnato alla riga 1 della matrice 3x3. Qualsiasi trama assegnata alla fase 1 viene ignorata.
-   Il set di coordinate di trama 2 viene assegnato alla riga 2 della matrice 3x3. Qualsiasi trama assegnata alla fase 2 viene ignorata.
-   Il set di coordinate di trama 3 viene assegnato alla riga 3 della matrice 3x3. Una trama di volume o cubo deve essere impostata sulla fase 3 per la ricerca da parte del vettore 3D trasformato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




