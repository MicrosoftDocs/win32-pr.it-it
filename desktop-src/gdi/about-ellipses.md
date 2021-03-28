---
description: Un'ellisse è una curva chiusa definita da due punti fissi (F1 e F2), in modo che la somma delle distanze (D1 + D2) da qualsiasi punto sulla curva ai due punti fissi sia costante.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: Informazioni sugli ellissi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c6b2774da9886e25d3e1dcca7c701b034e7b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564752"
---
# <a name="about-ellipses"></a>Informazioni sugli ellissi

Un'ellisse è una curva chiusa definita da due punti fissi (F1 e F2), in modo che la somma delle distanze (D1 + D2) da qualsiasi punto sulla curva ai due punti fissi sia costante. La figura seguente mostra un'ellisse disegnata usando la funzione [**ellisse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) .

![illustrazione che mostra un'ellisse, due punti fissi, due distanze e un rettangolo di delimitazione](images/csfsh-01.png)

Quando si chiama [**ellisse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), un'applicazione fornisce le coordinate degli angoli superiore sinistro e inferiore destro del rettangolo di delimitazione dell'ellisse. Un *rettangolo di delimitazione* è il rettangolo più piccolo che circonda completamente l'ellisse. Quando il sistema disegna l'ellisse, esclude i lati destro e inferiore se non è impostata alcuna trasformazione mondiale. Pertanto, per qualsiasi rettangolo che misuri x unità di larghezza per unità y elevate, l'ellisse associata misura X1 unità di larghezza per Y1 unità di altezza. Se l'applicazione imposta una trasformazione globale chiamando la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) o [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , il sistema include i lati destro e inferiore.

 

 



