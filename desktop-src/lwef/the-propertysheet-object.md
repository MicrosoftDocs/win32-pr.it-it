---
title: Oggetto PropertySheet
description: Oggetto PropertySheet
ms.assetid: 9d15d198-a4fe-4c05-a7be-0807a179cd9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ae4ded2625440ba34170df605b60287f105800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116792"
---
# <a name="the-propertysheet-object"></a>Oggetto PropertySheet

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

L'oggetto [**PropertySheet**](https://www.bing.com/search?q=**PropertySheet**) fornisce diverse proprietà che è possibile usare se si vuole modificare il carattere relativo alla finestra delle proprietà di Microsoft Agent, nota anche come finestra Opzioni carattere avanzate.

-   [**Altezza**](height-property-pso.md)
-   [**Sinistra**](left-property-pso.md)
-   [**Page**](page-property.md)
-   [**In alto**](top-property-pso.md)
-   [**Visible**](visible-property.md)
-   [**Larghezza**](width-property-pso.md)

Se si esegue una query sulle proprietà [**Height**](height-property-pso.md), [**Left**](left-property-pso.md), [**Top**](top-property-pso.md)e [**Width**](width-property-pso.md) prima che la finestra delle proprietà venga mai visualizzata, i relativi valori vengono restituiti come zero (0). Una volta visualizzate, queste proprietà restituiscono l'ultima posizione e le dimensioni della finestra (rispetto alla risoluzione dello schermo corrente).

 

 




