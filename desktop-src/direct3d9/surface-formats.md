---
description: In Direct3D tutte le immagini bidimensionali (2D) sono rappresentate da una gamma lineare di memoria denominata superficie.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Formati di superficie (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124812"
---
# <a name="surface-formats-direct3d-9"></a>Formati di superficie (Direct3D 9)

In Direct3D tutte le immagini bidimensionali (2D) sono rappresentate da una gamma lineare di memoria denominata superficie. Una superficie può essere considerata come una matrice 2D in cui ogni elemento include un valore di colore che rappresenta una piccola sezione dell'immagine, detta pixel. Il livello di dettaglio di un'immagine viene definito sia dal numero di pixel necessari per rappresentare l'immagine che dal numero di bit necessari per lo spettro di colore dell'immagine. Ad esempio, un'immagine di 800 pixel di larghezza per 600 pixel di altezza con 32 bit di colore per ogni pixel (scritta come 800x600x32) sarà più dettagliata di un'immagine con una larghezza di 640 pixel in larghezza per 480 pixel di altezza con 16 bit di colore per ogni pixel (scritto come 640x480x16). Analogamente, l'immagine più dettagliata richiederà una superficie più ampia per archiviare i dati. Per un'immagine 800x600x32, le dimensioni della matrice della superficie saranno 800x600 e ogni elemento manterrà un valore a 32 bit per rappresentare il colore.

Tutte le superfici hanno una dimensione e archiviano un numero specifico di bit che rappresentano il colore. I bit che rappresentano il colore sono separati in singoli elementi di colore: rosso, verde e blu. In Direct3D tutti gli elementi di colore sono definiti dal tipo enumerato [D3DFORMAT](d3dformat.md) . Un formato di colore Direct3D viene suddiviso nel numero di addii riservati per ogni colore. Un formato di colore a 16 bit in Direct3D, ad esempio, è definito come D3DFMT \_ R5G6B5, dove 5 bit sono riservati per rosso (R), 6 bit per il verde (G) e 5 bit per il blu (B).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 



