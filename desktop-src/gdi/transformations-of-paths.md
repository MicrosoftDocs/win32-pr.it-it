---
description: I percorsi vengono definiti usando le unità logiche e le trasformazioni correnti.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Trasformazioni di percorsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980295"
---
# <a name="transformations-of-paths"></a>Trasformazioni di percorsi

I percorsi vengono definiti usando le unità logiche e le trasformazioni correnti. Se è stata chiamata la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) , le unità logiche sono unità internazionali. in caso contrario, le unità logiche sono unità di pagina. Un'applicazione può usare le trasformazioni globali per ridimensionare, ruotare, tagliare, tradurre e riflettere le linee e le curve di Bézier che definiscono un percorso.

> [!Note]  
> Una trasformazione globale all'interno di una parentesi del percorso influiscono solo sulle linee e sulle curve disegnate dopo l'impostazione della trasformazione. Non avrà alcun effetto su tali linee e curve disegnate prima di essere impostate. Per una descrizione della trasformazione globale, vedere [spazi di coordinate e trasformazioni](coordinate-spaces-and-transformations.md).

 

Un'applicazione può anche usare [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per delineare la forma della penna usata per delineare un percorso se la penna è una penna geometrica. Per una descrizione delle penne geometriche, vedere [penne](pens.md).

 

 



