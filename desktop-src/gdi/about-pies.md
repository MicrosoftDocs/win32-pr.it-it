---
description: Una torta è un'area delimitata dall'intersezione di una curva di ellisse e due radiali. Nella figura seguente viene illustrato un grafico a torta creato utilizzando la funzione Pie.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Informazioni su torte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2184276fc208827ddac82fd7f4cacec3ddb20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049738"
---
# <a name="about-pies"></a>Informazioni su torte

Una *torta* è un'area delimitata dall'intersezione di una curva di ellisse e due radiali. Nella figura seguente viene illustrato un grafico a torta creato utilizzando la funzione [**Pie**](/windows/desktop/api/Wingdi/nf-wingdi-pie) .

![illustrazione che mostra un'ellisse con una torta ombreggiata](images/csfsh-03.png)

Quando si chiama [**torta**](/windows/win32/api/wingdi/nf-wingdi-pie), un'applicazione fornisce le coordinate degli angoli superiore sinistro e inferiore destro del rettangolo di delimitazione dell'ellisse, nonché le coordinate di due punti che definiscono due radiali.

Quando il sistema disegna la parte curva della torta, usa la direzione di arco corrente per il contesto di dispositivo specificato. La direzione di arco predefinita è in senso antiorario. Un'applicazione può reimpostare la direzione dell'arco chiamando la funzione [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .

 

 
