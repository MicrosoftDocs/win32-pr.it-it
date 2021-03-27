---
description: Un poligono è una forma riempita con lati dritti.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Informazioni sui poligoni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049737"
---
# <a name="about-polygons"></a>Informazioni sui poligoni

Un *poligono* è una forma riempita con lati dritti. I lati di un poligono vengono disegnati usando la penna corrente. Quando il sistema compila un poligono, usa il pennello corrente e la modalità di riempimento del poligono corrente. Le due modalità di riempimento, alternative (impostazione predefinita) e Winding, determinano se le aree all'interno di un poligono complesso vengono riempite o lasciate non verniciate. Un'applicazione può selezionare una delle due modalità chiamando la funzione [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . Per ulteriori informazioni sulle modalità di riempimento poligono, vedere [Regions](regions.md).

La figura seguente mostra un poligono disegnato usando [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).

![illustrazione di un poligono nella forma di una stella a cinque punte](images/csfsh-04.png)

Oltre a disegnare un singolo poligono usando [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), un'applicazione può disegnare più poligoni usando la funzione [**polipolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) .

 

 
