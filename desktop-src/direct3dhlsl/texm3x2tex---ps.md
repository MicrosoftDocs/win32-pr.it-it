---
title: texm3x2tex-PS
description: Esegue la riga finale di una matrice 3x2 moltiplicata e utilizza il risultato per eseguire una ricerca di trama. texm3x2tex deve essere usato in combinazione con l'istruzione texm3x2pad-PS.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993093"
---
# <a name="texm3x2tex---ps"></a>texm3x2tex-PS

Esegue la riga finale di una matrice 3x2 moltiplicata e utilizza il risultato per eseguire una ricerca di trama. texm3x2tex deve essere usato in combinazione con l'istruzione [texm3x2pad-PS](texm3x2pad---ps.md) .

## <a name="syntax"></a>Sintassi



| texm3x2tex DST, src |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2tex            | x    | x    | x    |      |      |      |       |      |       |



 

L'istruzione viene utilizzata come una delle due istruzioni che rappresentano un'operazione di moltiplicazione della matrice 3x2. Questa istruzione deve essere usata con l'istruzione [texm3x2pad-PS](texm3x2pad---ps.md) .

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



Ecco altri dettagli sul modo in cui viene eseguita la moltiplicazione 3x2.

L'istruzione texm3x2pad esegue la prima riga dell'istruzione Multiply per<sup>Find u.</sup>

u<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (fase m)<sub>UVW</sub>

L'istruzione texm3x2tex esegue la seconda riga della moltiplicazione per trovare la<sup>v.</sup>

v<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (stage m + 1)<sub>UVW</sub>

L'istruzione texm3x2tex esegue il campionamento della trama sulla fase (m + 1) con (u<sup>'</sup>, v<sup>'</sup>) e archivia il risultato in t (m + 1).

t (m + 1)<sub>RGB</sub> = TextureSample (stage m + 1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) As coordinates

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di shader con le mappe di trama e le fasi di trama identificate.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



Questo esempio richiede le seguenti trame nelle fasi di trama seguenti.

-   La fase 0 accetta una mappa con i dati di perturbazione (x, y, z).
-   La fase 1 include le coordinate di trama. Non è necessaria alcuna trama nella fase della trama.
-   La fase 2 include entrambe le coordinate di trama e un set di trame 2D in quella fase della trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




