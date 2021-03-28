---
title: texm3x2depth-PS
description: Calcolare il valore di profondità da usare per il test di profondità per questo pixel.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976386"
---
# <a name="texm3x2depth---ps"></a>texm3x2depth-PS

Calcolare il valore di profondità da usare per il test di profondità per questo pixel.

## <a name="syntax"></a>Sintassi



| texm3x2depth DST, src |
|-----------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2depth          |      |      | x    |      |      |      |       |      |       |



 

Questa istruzione deve essere usata con l'istruzione [texm3x2pad-PS](texm3x2pad---ps.md) .

Quando si usano queste due istruzioni, i registri di trama devono usare la sequenza seguente.


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



Il calcolo della profondità viene eseguito dopo l'utilizzo di un'operazione del prodotto punto per trovare z e w. Ecco altri dettagli sul modo in cui viene eseguito il calcolo della profondità.

L'istruzione texm3x2pad calcola z.

z = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L'istruzione texm3x2depth calcola w.

w = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Calcolare la profondità e archiviare il risultato in t (m + 1).


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



La profondità calcolata è contrassegnata per essere usata nel test di profondità per il pixel, sostituendo il valore del test di profondità esistente per il pixel.

Assicurarsi di bloccare z/w nell'intervallo (0-1). Se z/w è esterno a questo intervallo, il risultato archiviato nel buffer di profondità sarà indefinito.

Dopo l'esecuzione di texm3x2depth, il registro t (m + 1) non è più disponibile per l'uso nello shader.

Quando si esegue il campionamento multiplo, l'utilizzo di questa istruzione Elimina la maggior parte del vantaggio del buffer di profondità di risoluzione superiore. Poiché il pixel shader viene eseguito una volta per pixel, viene usato il valore di profondità singola restituito da texm3x2depth o [texdepth-PS](texdepth---ps.md) per ogni test di confronto di profondità dei sottopixel.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




