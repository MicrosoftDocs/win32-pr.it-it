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
# <a name="application-defined-mapping-modes"></a>Modalità di mapping Application-Defined

\_ \_ Per le modalità di mapping specifiche dell'applicazione vengono fornite le due modalità di mapping definite dall'applicazione, ovvero il filtro di base per il filtro di base e il anisotropico mm. La \_ modalità con filtro di tipo di filtro in mm garantisce che le unità logiche nella direzione x e nella direzione y siano uguali, mentre la modalità ANISOTROPICO mm \_ consente di variare le unità. Un CAD o un'applicazione di disegno può trarre vantaggio dalla modalità di mapping del filtro di base dei dispositivi MM \_ , ma potrebbe essere necessario specificare unità logiche che corrispondano agli incrementi sulla scala di un tecnico (1/64 pollice). Queste unità sarebbero difficili da ottenere con le modalità di mapping predefinite (MM \_ HIENGLISH o mm \_ HIMETRIC). Tuttavia, possono essere facilmente ottenute selezionando la modalità di \_ filtro di base (anisotropico \_ ) mm. Nell'esempio seguente viene illustrato come impostare le unità logiche su 1/64 pollice:


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



