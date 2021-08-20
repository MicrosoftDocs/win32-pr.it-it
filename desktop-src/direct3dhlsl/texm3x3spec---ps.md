---
title: texm3x3spec - ps
description: Esegue una moltiplicazione di matrice 3x3 e usa il risultato per eseguire una ricerca trame. Può essere usato per la reflection speculare e il mapping dell'ambiente. texm3x3spec deve essere usato insieme a due istruzioni texm3x3pad - ps.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b5fcef771d6d06a1691d5c5e953b76b1c445c7c8df7b2da37b8b4220bef2b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485431"
---
# <a name="texm3x3spec---ps"></a>texm3x3spec - ps

Esegue una moltiplicazione di matrice 3x3 e usa il risultato per eseguire una ricerca trame. Può essere usato per la reflection speculare e il mapping dell'ambiente. texm3x3spec deve essere usato insieme a due [istruzioni texm3x3pad - ps.](texm3x3pad---ps.md)

## <a name="syntax"></a>Sintassi



| texm3x3spec dst, src0, src1 |
|-----------------------------|



 

dove

-   dst è il registro di destinazione.
-   src0 e src1 sono registri di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3spec           | x    | x    | x    |      |      |      |       |      |       |



 

Questa istruzione esegue la riga finale di una moltiplicazione di matrice 3x3, usa il vettore risultante come vettore normale per riflettere un vettore di raggio oculare e quindi usa il vettore riflesso per eseguire una ricerca della trama. Lo shader legge il vettore del raggio oculare da un registro costante. La moltiplicazione della matrice 3x3 è in genere utile per orientare un vettore normale nello spazio tangente corretto per la superficie di cui viene eseguito il rendering.

La matrice 3x3 è costituita da coordinate di trama della terza fase della trama e delle due fasi di trama precedenti. Il vettore di post reflection risultante (u,v,w) viene usato per campionare la trama nella fase finale della trama. Qualsiasi trama assegnata alle due fasi precedenti della trama viene ignorata.

Questa istruzione deve essere usata con due istruzioni texm3x3pad. I registri di trama devono usare la sequenza seguente.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



La prima istruzione texm3x3pad esegue la prima riga della moltiplicazione per trovare u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

La seconda istruzione texm3x3pad esegue la seconda riga della moltiplicazione per trovare v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

L'istruzione texm3x3spec esegue la terza riga della moltiplicazione per trovare w<sup>'.</sup>

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

L'istruzione texm3x3spec esegue quindi un calcolo di reflection.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (N \* E)/(N \* N) \] \* N - E

dove la normale N viene data da

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

e il vettore di raggio oculare E viene fornito dal registro costante

E = c (è possibile usare qualsiasi registro \# costante-- c0, c1, c2 e così via)

Infine, l'istruzione texm3x3spec campita t(m+2) con (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) e archivia il risultato in t(m+2).

t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates

## <a name="examples"></a>Esempio

Ecco un esempio di shader con le mappe di trama e le fasi della trama identificate.


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



Questo esempio richiede la configurazione della fase di trama seguente.

-   Alla fase 0 viene assegnata una mappa di trama con dati normali. Questa mappa viene spesso definita mappa di rilievo. I dati sono normali (XYZ) per ogni texel. Le coordinate di trama nella fase n definiscono dove campionare questa mappa normale.
-   Il set di coordinate della trama m viene assegnato alla riga 1 della matrice 3x3. Qualsiasi trama assegnata alla fase m viene ignorata.
-   Il set di coordinate della trama m+1 viene assegnato alla riga 2 della matrice 3x3. Qualsiasi trama assegnata alla fase m+1 viene ignorata.
-   Il set di coordinate della trama m+2 viene assegnato alla riga 3 della matrice 3x3. Alla fase m+2 viene assegnata una mappa di trama di volume o cubo. La trama fornisce dati di colore (RGBA).
-   Il vettore di raggio oculare E viene fornito da un registro costante E = c \# .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




