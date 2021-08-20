---
title: texdp3 - ps
description: Esegue un prodotto punto a tre componenti tra i dati nel numero del registro trame e il set di coordinate della trama corrispondente al numero del registro di destinazione.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e39f2682aac7741af304269b0584f3552158b2f83596c7fd55f1c83948d09f0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788201"
---
# <a name="texdp3---ps"></a>texdp3 - ps

Esegue un prodotto punto a tre componenti tra i dati nel numero del registro trame e il set di coordinate della trama corrispondente al numero del registro di destinazione.

## <a name="syntax"></a>Sintassi



| texdp3 dst, src |
|-----------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
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



Di seguito sono fornite informazioni più dettagliate sul modo in cui viene ottenuto il prodotto dot.

L'istruzione texdp3 esegue un prodotto dot a tre componenti e lo replica in tutti e quattro i canali di colore.

t(m)<sub>RGBA</sub> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




