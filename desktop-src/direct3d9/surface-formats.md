---
description: In Direct3D tutte le immagini bidimensionali (2D) sono rappresentate da un intervallo lineare di memoria denominato superficie.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Formati surface (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e54b6bf4573243e170f089a72d7d5c69e31c81a536703d764694d43f2dc33cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291498"
---
# <a name="surface-formats-direct3d-9"></a>Formati surface (Direct3D 9)

In Direct3D tutte le immagini bidimensionali (2D) sono rappresentate da un intervallo lineare di memoria denominato superficie. Una superficie può essere pensata come una matrice 2D in cui ogni elemento contiene un valore di colore che rappresenta una piccola sezione dell'immagine, denominata pixel. Il livello di dettaglio di un'immagine è definito sia dal numero di pixel necessari per rappresentare l'immagine sia dal numero di bit necessari per lo spettro dei colori dell'immagine. Ad esempio, un'immagine di 800 pixel di larghezza per 600 pixel di altezza con 32 bit di colore per ogni pixel (scritta come 800x600x32) sarà più dettagliata rispetto a un'immagine di 640 pixel di larghezza per 480 pixel di altezza con 16 bit di colore per ogni pixel (scritta come 640x480x16). Analogamente, l'immagine più dettagliata richiederà una superficie più grande per archiviare i dati. Per un'immagine 800x600x32, le dimensioni della matrice della superficie saranno 800x600 e ogni elemento contenerà un valore a 32 bit per rappresentare il colore.

Tutte le superfici hanno una dimensione e archiviano un numero specifico di bit che rappresentano il colore. I bit che rappresentano il colore sono separati in singoli elementi di colore: rosso, verde e blu. In Direct3D tutti gli elementi di colore sono definiti dal [tipo enumerato D3DFORMAT.](d3dformat.md) Un formato di colore Direct3D è suddiviso nel numero di bye riservati per ogni colore. Ad esempio, un formato di colore a 16 bit in Direct3D è definito come D3DFMT R5G6B5, dove 5 bit sono riservati per il rosso (R), 6 bit per il verde (G) e 5 bit per il blu \_ (B).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 



