---
title: texm3x2tex - ps
description: Esegue la riga finale di una moltiplicazione di matrice 3x2 e usa il risultato per eseguire una ricerca trame. texm3x2tex deve essere usato insieme all'istruzione texm3x2pad - ps.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9653325098b05959fcbd9e7a838801652a532d936bdaebc829055b717a49096f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723019"
---
# <a name="texm3x2tex---ps"></a>texm3x2tex - ps

Esegue la riga finale di una moltiplicazione di matrice 3x2 e usa il risultato per eseguire una ricerca trame. texm3x2tex deve essere usato insieme all'istruzione [texm3x2pad - ps.](texm3x2pad---ps.md)

## <a name="syntax"></a>Sintassi



| texm3x2tex dst, src |
|---------------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2tex            | x    | x    | x    |      |      |      |       |      |       |



 

L'istruzione viene usata come una delle due istruzioni che rappresentano un'operazione di moltiplicazione di matrice 3x2. Questa istruzione deve essere usata con [l'istruzione texm3x2pad - ps.](texm3x2pad---ps.md)

Quando si usano queste due istruzioni, i registri di trama devono usare la sequenza seguente.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



Di seguito sono fornite informazioni più dettagliate sul modo in cui viene eseguita la moltiplicazione 3x2.

L'istruzione texm3x2pad esegue la prima riga della moltiplicazione per trovare u<sup>'</sup>.

u<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m)<sub>UVW</sub>

L'istruzione texm3x2tex esegue la seconda riga della moltiplicazione per trovare v<sup>'</sup>.

v<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m+1)<sub>UVW</sub>

L'istruzione texm3x2tex campione la trama sullo stage (m+1) con (u<sup>'</sup>,v<sup>'</sup>) e archivia il risultato in t(m+1).

t(m+1)<sub>RGB</sub> = TextureSample(stage m+1)<sub>RGB</sub> usando (u<sup>'</sup>, v<sup>'</sup> ) come coordinate

## <a name="examples"></a>Esempio

Ecco un esempio di shader con le mappe trame e le fasi della trama identificate.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



Questo esempio richiede le trame seguenti nelle fasi di trama seguenti.

-   La fase 0 accetta una mappa con i dati di perturbazione (x,y,z).
-   La fase 1 contiene le coordinate della trama. Nella fase della trama non è necessaria alcuna trama.
-   La fase 2 contiene sia le coordinate della trama che una trama 2D impostata in tale fase della trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




