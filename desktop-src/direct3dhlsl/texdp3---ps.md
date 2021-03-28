---
title: texdp3-PS
description: Esegue un prodotto punto a tre componenti tra i dati nel numero di registro della trama e il set di coordinate di trama corrispondente al numero di registro di destinazione.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64cc14ee66123ea3e25941579b9838977a753174
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335452"
---
# <a name="texdp3---ps"></a>texdp3-PS

Esegue un prodotto punto a tre componenti tra i dati nel numero di registro della trama e il set di coordinate di trama corrispondente al numero di registro di destinazione.

## <a name="syntax"></a>Sintassi



| texdp3 DST, src |
|-----------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3                |      | x    | x    |      |      |      |       |      |       |



 

I registri di trama devono usare la sequenza seguente.


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



Di seguito sono riportate informazioni più dettagliate sul modo in cui viene eseguito il prodotto punto.

L'istruzione texdp3 esegue un prodotto punto a tre componenti e lo replica in tutti e quattro i canali colori.

t (m)<sub>RGBA</sub> = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




