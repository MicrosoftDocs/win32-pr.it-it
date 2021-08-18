---
description: Un'ellisse è una curva chiusa definita da due punti fissi (f1 e f2 ) in modo che la somma delle distanze (d1 +d2 ) da qualsiasi punto della curva ai due punti fissi sia costante.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: Informazioni sui puntini di sospensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0892bfd2a8aa6fad43d18ead65eb92d260150ab31ca9057177c33af2cb8d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888552"
---
# <a name="about-ellipses"></a>Informazioni sui puntini di sospensione

Un'ellisse è una curva chiusa definita da due punti fissi (f1 e f2 ) in modo che la somma delle distanze (d1 +d2 ) da qualsiasi punto della curva ai due punti fissi sia costante. Nella figura seguente viene illustrata un'ellisse disegnata usando la [**funzione Ellipse.**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)

![Figura che mostra un'ellisse, due punti fissi, due distanze e un rettangolo di delimitazione](images/csfsh-01.png)

Quando si [**chiama Ellipse,**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)un'applicazione fornisce le coordinate degli angoli superiore sinistro e inferiore destro del rettangolo di delimitazione dell'ellisse. Un *rettangolo di delimitazione* è il rettangolo più piccolo che circonda completamente l'ellisse. Quando il sistema disegna l'ellisse, esclude i lati destro e inferiore se non è impostata alcuna trasformazione globale. Pertanto, per qualsiasi rettangolo che misura x unità di larghezza per unità y alto, l'ellisse associata misura x1 unità di larghezza per y1 unità di altezza. Se l'applicazione imposta una trasformazione globale chiamando la [**funzione SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) o [**ModifyWorldTransform,**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) il sistema include i lati destro e inferiore.

 

 



