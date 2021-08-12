---
title: texdepth - ps
description: Calcolare i valori di profondità da usare nel test di confronto del buffer di profondità per questo pixel.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f39135c34c07a9a20f03c9ebc979647733884b37680ef07b9bc666b882052690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284175"
---
# <a name="texdepth---ps"></a>texdepth - ps

Calcolare i valori di profondità da usare nel test di confronto del buffer di profondità per questo pixel.

## <a name="syntax"></a>Sintassi



| texdepth dst |
|--------------|



 

dove

-   dst è il registro di destinazione.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdepth              |      |      |      | x    |      |      |       |      |       |



 

Questa istruzione usa r5.r/r5.g nel test di confronto del buffer di profondità per questo pixel. I dati nei canali blu e alfa vengono ignorati. Se r5.g = 0, il risultato di r5.r/r5.g = 1,0.

Il registro temporaneo r5 è l'unico registro che questa istruzione può usare.

Dopo l'esecuzione di questa istruzione, il registro temporaneo r5 non è disponibile per un uso aggiuntivo nello shader.

Quando si esegue il multicampionamento, l'uso di questa istruzione elimina la maggior parte dei vantaggi del buffer di profondità con risoluzione più elevata. Poiché il pixel shader viene eseguito una volta per pixel, per ognuno dei test di confronto della profondità subpixel verrà usato il valore di profondità singolo restituito da [texm3x2depth - ps](texm3x2depth---ps.md) o texdepth.

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di uso di texdepth.


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




