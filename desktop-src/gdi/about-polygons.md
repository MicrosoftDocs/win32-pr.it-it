---
description: Un poligono è una forma piena con lati rette.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Informazioni sui poligoni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0d28bd915237991294f6579448ca08785481f374814f0ed5840f77ee9f813c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966441"
---
# <a name="about-polygons"></a>Informazioni sui poligoni

Un *poligono* è una forma piena con lati rette. I lati di un poligono vengono disegnati usando la penna corrente. Quando il sistema riempie un poligono, usa il pennello corrente e la modalità di riempimento poligono corrente. Le due modalità di riempimento, alternate (impostazione predefinita) e winding, determinano se le aree all'interno di un poligono complesso sono riempite o non ridisegnate. Un'applicazione può selezionare una delle due modalità chiamando la [**funzione SetPolyFillMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) Per altre informazioni sulle modalità di riempimento poligono, vedere [Aree.](regions.md)

La figura seguente mostra un poligono disegnato usando [**Polygon.**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)

![illustrazione di un poligono nella forma di una stella a cinque punte](images/csfsh-04.png)

Oltre a disegnare un singolo poligono usando [**Polygon,**](/windows/win32/api/wingdi/nf-wingdi-polygon)un'applicazione può disegnare più poligoni usando la [**funzione PolyPolygon.**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)

 

 
