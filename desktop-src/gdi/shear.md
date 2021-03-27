---
description: Alcune applicazioni forniscono funzionalità che consentono di disegnare oggetti di taglio nell'area client.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Taglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232551"
---
# <a name="shear"></a>Taglio

Alcune applicazioni forniscono funzionalità che consentono di disegnare oggetti di taglio nell'area client. Le applicazioni che usano le funzionalità di taglio usano la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare i valori appropriati nella trasformazione spazio globale nella pagina. Questa funzione [**riceve un puntatore a una struttura che**](/windows/win32/api/wingdi/ns-wingdi-xform) contiene i valori appropriati. I membri eM12 e eM21 di l'oggetto di controllo di stato specificano rispettivamente le costanti di proporzionalità orizzontale e verticale.

Sono disponibili due componenti per la *trasformazione di taglio*. Il primo modifica le linee verticali in un oggetto; il secondo modifica le linee orizzontali. Nell'illustrazione seguente viene mostrato un rettangolo di 20 unità, con tranciatura orizzontale quando viene copiato dallo spazio globale allo spazio della pagina.

![illustrazione che mostra un rettangolo nello spazio globale e un trapeziod nello spazio della pagina](images/cstrn-13.png)

Una cesoia orizzontale può essere rappresentata dall'algoritmo seguente:

``` syntax
x' = x + (Sx * y) 
```

dove x è la coordinata x originale, SX è la costante di proporzionalità e x ' è il risultato della trasformazione di taglio.

Una cesoia verticale può essere rappresentata dall'algoritmo seguente:

``` syntax
y' = y + (Sy * x) 
```

dove y è la coordinata y originale, Sy è la costante di proporzionalità e y è il risultato della trasformazione di taglio.

Le trasformazioni orizzontali e a taglio verticale possono essere combinate in una singola operazione usando una matrice 2 per 2.

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

La matrice 2 per 2 che ha prodotto la distorsione contiene i valori seguenti:

``` syntax
|1    1| 
|0    1| 
```

 

 



