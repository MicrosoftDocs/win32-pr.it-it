---
description: "\\_ \\_ Per le modalità di mapping specifiche dell'applicazione vengono fornite le due modalità di mapping definite dall'applicazione, ovvero il filtro di base per il filtro di base e il anisotropico mm."
ms.assetid: c4c4e352-63fc-4e97-a218-a1b7deac02e8
title: Modalità di mapping Application-Defined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d800a3ce631ebffeef8223fc53ec505c10cb69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994136"
---
# <a name="application-defined-mapping-modes"></a><span data-ttu-id="6e63f-103">Modalità di mapping Application-Defined</span><span class="sxs-lookup"><span data-stu-id="6e63f-103">Application-Defined Mapping Modes</span></span>

<span data-ttu-id="6e63f-104">\_ \_ Per le modalità di mapping specifiche dell'applicazione vengono fornite le due modalità di mapping definite dall'applicazione, ovvero il filtro di base per il filtro di base e il anisotropico mm.</span><span class="sxs-lookup"><span data-stu-id="6e63f-104">The two application-defined mapping modes (MM\_ISOTROPIC and MM\_ANISOTROPIC) are provided for application-specific mapping modes.</span></span> <span data-ttu-id="6e63f-105">La \_ modalità con filtro di tipo di filtro in mm garantisce che le unità logiche nella direzione x e nella direzione y siano uguali, mentre la modalità ANISOTROPICO mm \_ consente di variare le unità.</span><span class="sxs-lookup"><span data-stu-id="6e63f-105">The MM\_ISOTROPIC mode guarantees that logical units in the x-direction and in the y-direction are equal, while the MM\_ANISOTROPIC mode allows the units to differ.</span></span> <span data-ttu-id="6e63f-106">Un CAD o un'applicazione di disegno può trarre vantaggio dalla modalità di mapping del filtro di base dei dispositivi MM \_ , ma potrebbe essere necessario specificare unità logiche che corrispondano agli incrementi sulla scala di un tecnico (1/64 pollice).</span><span class="sxs-lookup"><span data-stu-id="6e63f-106">A CAD or drawing application can benefit from the MM\_ISOTROPIC mapping mode but may need to specify logical units that correspond to the increments on an engineer's scale (1/64 inch).</span></span> <span data-ttu-id="6e63f-107">Queste unità sarebbero difficili da ottenere con le modalità di mapping predefinite (MM \_ HIENGLISH o mm \_ HIMETRIC). Tuttavia, possono essere facilmente ottenute selezionando la modalità di \_ filtro di base (anisotropico \_ ) mm.</span><span class="sxs-lookup"><span data-stu-id="6e63f-107">These units would be difficult to obtain with the predefined mapping modes (MM\_HIENGLISH or MM\_HIMETRIC); however, they can easily be obtained by selecting the MM\_ISOTROPIC (or MM\_ANISOTROPIC) mode.</span></span> <span data-ttu-id="6e63f-108">Nell'esempio seguente viene illustrato come impostare le unità logiche su 1/64 pollice:</span><span class="sxs-lookup"><span data-stu-id="6e63f-108">The following example shows how to set logical units to 1/64 inch:</span></span>


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



