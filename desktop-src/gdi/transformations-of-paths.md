---
description: I percorsi vengono definiti usando unità logiche e trasformazioni correnti.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Trasformazioni di percorsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7561cc1544a49555eaad4d58cf06d29a4763b6cd40528452c68cea551c99af34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889001"
---
# <a name="transformations-of-paths"></a>Trasformazioni di percorsi

I percorsi vengono definiti usando unità logiche e trasformazioni correnti. Se è stata [**chiamata la funzione SetWorldTransform,**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) le unità logiche sono unità del mondo. In caso contrario, le unità logiche sono unità di pagina. Un'applicazione può usare le trasformazioni del mondo per ridimensionare, ruotare, traslare, traslare e riflettere le linee e le curve di Bézier che definiscono un tracciato.

> [!Note]  
> Una trasformazione globale all'interno di una parentesi di percorso influisce solo sulle linee e le curve disegnate dopo l'impostazione della trasformazione. Non avrà alcun effetto sulle linee e sulle curve disegnate prima dell'impostazione. Per una descrizione della trasformazione globale, vedere [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).

 

Un'applicazione può anche usare [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per delineare la forma della penna usata per delineare un tracciato se la penna è geometrica. Per una descrizione delle penne [geometriche, vedere Penn](pens.md).

 

 



