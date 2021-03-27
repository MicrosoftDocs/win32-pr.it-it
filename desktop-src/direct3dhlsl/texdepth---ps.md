---
title: texdepth-PS
description: Calcola i valori di profondità da usare nel test di confronto del buffer di profondità per questo pixel.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857754"
---
# <a name="texdepth---ps"></a>texdepth-PS

Calcola i valori di profondità da usare nel test di confronto del buffer di profondità per questo pixel.

## <a name="syntax"></a>Sintassi



| texdepth DST |
|--------------|



 

dove

-   DST è il registro di destinazione.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdepth              |      |      |      | x    |      |      |       |      |       |



 

Questa istruzione USA R5. r/R5. g nel test di confronto del buffer di profondità per questo pixel. I dati nei canali blu e alfa vengono ignorati. Se R5. g = 0, il risultato di R5. r/R5. g = 1,0.

Il registro temporaneo R5 è l'unico registro che questa istruzione può utilizzare.

Dopo l'esecuzione di questa istruzione, il registro temporaneo R5 non è disponibile per un uso aggiuntivo nello shader.

Quando si esegue il campionamento multiplo, l'utilizzo di questa istruzione Elimina la maggior parte del vantaggio del buffer di profondità di risoluzione superiore. Poiché il pixel shader viene eseguito una volta per ogni pixel, viene usato il valore di profondità singola restituito da [texm3x2depth-PS](texm3x2depth---ps.md) o texdepth per ogni test di confronto di profondità dei sottopixel.

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio che usa texdepth.


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

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




