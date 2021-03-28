---
title: texm3x3-PS
description: Esegue una moltiplicazione di matrice 3x3 quando viene usata insieme a due istruzioni texm3x3pad-PS.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976354"
---
# <a name="texm3x3---ps"></a>texm3x3-PS

Esegue una moltiplicazione di matrice 3x3 quando viene usata insieme a due istruzioni [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Sintassi



| texm3x3 DST, src |
|------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3               |      | x    | x    |      |      |      |       |      |       |



 

Questa istruzione è identica a quella dell'istruzione [texm3x3tex-PS](texm3x3tex---ps.md) , senza la ricerca della trama.

Questa istruzione viene usata come finale di tre istruzioni che rappresentano un'operazione di moltiplicazione della matrice 3x3. La matrice 3x3 è costituita dalle coordinate di trama della terza fase della trama e dalle due fasi di trama precedenti. Qualsiasi trama assegnata a una qualsiasi delle tre fasi della trama viene ignorata.

Questa istruzione deve essere utilizzata con due istruzioni texm3x3pad. I registri di trama devono seguire la sequenza seguente.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



Di seguito sono riportati altri dettagli su come viene eseguita la moltiplicazione 3x3.

La prima istruzione texm3x3pad esegue la prima riga dell'istruzione Multiply per<sup>Find u.</sup>

u<sup>'</sup> = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

La seconda istruzione texm3x3pad esegue la seconda riga della moltiplicazione per trovare la<sup>v.</sup>

v<sup>'</sup> = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L'istruzione texm3x3tex esegue la terza riga del moltiplicatore per<sup>trovare w.</sup>

w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Posizionare il risultato della moltiplicazione della matrice nel registro di destinazione.

t (m + 2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




