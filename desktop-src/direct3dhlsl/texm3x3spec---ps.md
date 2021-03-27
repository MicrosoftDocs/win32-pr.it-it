---
title: texm3x3spec-PS
description: Esegue una moltiplicazione della matrice 3x3 e usa il risultato per eseguire una ricerca di trama. Questa operazione può essere utilizzata per la reflection speculare e il mapping dell'ambiente. texm3x3spec deve essere usato in combinazione con due istruzioni texm3x3pad-PS.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d872a5f9ebf716142fb5bc506edb77bb0b66850a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398226"
---
# <a name="texm3x3spec---ps"></a>texm3x3spec-PS

Esegue una moltiplicazione della matrice 3x3 e usa il risultato per eseguire una ricerca di trama. Questa operazione può essere utilizzata per la reflection speculare e il mapping dell'ambiente. texm3x3spec deve essere usato in combinazione con due istruzioni [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Sintassi



| texm3x3spec DST, src0, src1 |
|-----------------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 e src1 sono registri di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3spec           | x    | x    | x    |      |      |      |       |      |       |



 

Questa istruzione esegue la riga finale di una matrice 3x3 moltiplicata, usa il vettore risultante come vettore normale per riflettere un vettore di occhi, quindi usa il vettore riflesso per eseguire una ricerca di trama. Lo shader legge il vettore degli occhi da un registro costante. La moltiplicazione della matrice 3x3 è in genere utile per orientare un vettore normale allo spazio tangente corretto per la superficie di cui viene eseguito il rendering.

La matrice 3x3 è costituita dalle coordinate di trama della terza fase della trama e dalle due fasi di trama precedenti. Il vettore di Reflection post risultante (u, v, w) viene usato per campionare la trama sulla fase di trama finale. Qualsiasi trama assegnata alle due fasi di trama precedenti viene ignorata.

Questa istruzione deve essere utilizzata con due istruzioni texm3x3pad. I registri di trama devono usare la sequenza seguente.


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



La prima istruzione texm3x3pad esegue la prima riga dell'istruzione Multiply per<sup>Find u.</sup>

u<sup>'</sup> = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

La seconda istruzione texm3x3pad esegue la seconda riga della moltiplicazione per trovare la<sup>v.</sup>

v<sup>'</sup> = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L'istruzione texm3x3spec esegue la terza riga del moltiplicatore per<sup>trovare w.</sup>

w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L'istruzione texm3x3spec esegue quindi un calcolo della reflection.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* n-E

dove il normale N viene fornito da

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

e il vettore di raggio E viene fornito dal registro delle costanti

E = c \# (qualsiasi registro costante--C0, C1, C2 e così via--può essere usato)

Infine, l'istruzione texm3x3spec Samples t (m + 2) with (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) e archivia il risultato in t (m + 2).

t (m + 2)<sub>RGBA</sub> = TextureSample (fase m + 2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) come coordinate

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di shader con le mappe di trama e le fasi di trama identificate.


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



Questo esempio richiede la seguente configurazione della fase di trama.

-   Alla fase 0 viene assegnata una mappa di trama con dati normali. Questa operazione viene spesso definita mappa Bump. I dati sono normali (XYZ) per ogni Texel. Le coordinate di trama nella fase n definiscono la posizione in cui eseguire il campionamento della mappa normale.
-   Il set di coordinate di trama m viene assegnato alla riga 1 della matrice 3x3. Qualsiasi trama assegnata alla fase m viene ignorata.
-   Il set di coordinate di trama m + 1 viene assegnato alla riga 2 della matrice 3x3. Qualsiasi trama assegnata alla fase m + 1 viene ignorata.
-   Il set di coordinate di trama m + 2 viene assegnato alla riga 3 della matrice 3x3. Alla fase m + 2 viene assegnata una mappa di trama del volume o del cubo. La trama fornisce dati di colore (RGBA).
-   Il vettore di raggio E viene fornito da un registro costante E = c \# .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




