---
title: texm3x3tex-PS
description: Esegue una moltiplicazione della matrice 3x3 e usa il risultato per eseguire una ricerca di trama. texm3x3tex deve essere usato con due istruzioni texm3x3pad-PS.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398314"
---
# <a name="texm3x3tex---ps"></a>texm3x3tex-PS

Esegue una moltiplicazione della matrice 3x3 e usa il risultato per eseguire una ricerca di trama. texm3x3tex deve essere usato con due istruzioni [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Sintassi



| texm3x3tex DST, src |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3tex            | x    | x    | x    |      |      |      |       |      |       |



 

Questa istruzione viene usata come finale di tre istruzioni che rappresentano un'operazione di moltiplicazione della matrice 3x3, seguita da una ricerca di trama. La matrice 3x3 è costituita dalle coordinate di trama della terza fase della trama e dalle due fasi di trama precedenti. Il vettore a tre componenti risultante (u, v, w) viene usato per campionare la trama nella fase 3. Qualsiasi trama assegnata alle due fasi di trama precedenti viene ignorata. La moltiplicazione della matrice 3x3 è in genere utile per orientare un vettore normale allo spazio tangente corretto per la superficie di cui viene eseguito il rendering.

Questa istruzione deve essere utilizzata con l'istruzione texm3x3pad. I registri di trama devono usare la sequenza seguente.


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



Di seguito sono riportati altri dettagli su come viene eseguita la moltiplicazione 3x3.

La prima istruzione texm3x3pad esegue la prima riga dell'istruzione Multiply per<sup>Find u.</sup>

u<sup>'</sup> = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

La seconda istruzione texm3x3pad esegue la seconda riga della moltiplicazione per trovare la<sup>v.</sup>

v<sup>'</sup> = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L'istruzione texm3x3spec esegue la terza riga del moltiplicatore per<sup>trovare w.</sup>

w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Infine, l'istruzione texm3x3tex Samples t (m + 2) with (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) e archivia il risultato in t (m + 2).

t (m + 2)<sub>RGBA</sub> = TextureSample (stage m + 2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) come coordinates.

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di shader con le mappe di trama identificate e le fasi di trama identificate.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



Questo esempio richiede la seguente configurazione della fase di trama.

-   Alla fase 0 viene assegnata una mappa di trama con dati normali. Questa operazione viene spesso definita mappa Bump. I dati sono normali (XYZ) per ogni Texel. Il set di coordinate di trama 0 definisce come campionare questa mappa normale.
-   Il set di coordinate di trama 1 viene assegnato alla riga 1 della matrice 3x3. Qualsiasi trama assegnata alla fase 1 viene ignorata.
-   Il set 2 della coordinata di trama viene assegnato alla riga 2 della matrice 3x3. Qualsiasi trama assegnata alla fase 2 viene ignorata.
-   Il set di coordinate di trama 3 viene assegnato alla riga 3 della matrice 3x3. È necessario impostare una trama del volume o del cubo sulla fase 3 per la ricerca tramite il vettore 3D trasformato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




