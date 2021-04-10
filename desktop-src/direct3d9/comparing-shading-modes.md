---
description: In modalità ombreggiatura piatta, la piramide seguente viene visualizzata con un bordo acuto tra i visi adiacenti. In modalità ombreggiatura Gouraud, tuttavia, i valori di ombreggiatura vengono interpolati sul bordo e l'aspetto finale è una superficie curva.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Confronto tra modalità di ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127778"
---
# <a name="comparing-shading-modes-direct3d-9"></a>Confronto tra modalità di ombreggiatura (Direct3D 9)

In modalità ombreggiatura piatta, la piramide seguente viene visualizzata con un bordo acuto tra i visi adiacenti. In modalità ombreggiatura Gouraud, tuttavia, i valori di ombreggiatura vengono interpolati sul bordo e l'aspetto finale è una superficie curva.

![illustrazione di una piramide con spigoli acuti e frecce che puntano alle normali del volto](images/shade2.png)

Gouraud ombreggiatura illumina le superfici piane in maniera più realistica dell'ombreggiatura semplice. Una faccia in modalità ombreggiatura piatta è un colore uniforme, ma l'ombreggiatura Gouraud consente di rientrare in modo più corretto in una faccia. Questo effetto è particolarmente ovvio se è presente un'origine punto vicina.

L'ombreggiatura Gouraud smussa i bordi acuti tra i poligoni visibili con ombreggiatura piatta. Tuttavia, può produrre bande Mach, che sono bande di colore o luce che non sono mescolate in modo uniforme tra poligoni adiacenti. L'applicazione può ridurre l'aspetto delle bande Mach aumentando il numero di poligoni in un oggetto, aumentando la risoluzione dello schermo o aumentando la profondità di colore dell'applicazione.

L'ombreggiatura di Gouraud può non riuscire ad alcuni dettagli. Nella figura seguente, ad esempio, un oggetto Spotlight è completamente contenuto all'interno di una superficie poligonale.

![illustrazione di un oggetto Spotlight in una superficie poligonale](images/gouraud.png)

In questo caso, l'ombreggiatura Gouraud, che interpola tra i vertici, potrebbe non essere completamente in evidenza; viene eseguito il rendering della faccia come se il Spotlight non esistesse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ombreggiatura](shading.md)
</dt> </dl>

 

 



