---
description: Una torta è un'area delimitata dall'intersezione di una curva ellisse e di due radiali. La figura seguente mostra una torta disegnata usando la funzione Pie.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Informazioni sulle pie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e447e313a3088bbf9a72c790115fb3bb25770017cf13ce7922685fd18ccfe671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966461"
---
# <a name="about-pies"></a>Informazioni sulle pie

Una *torta è* un'area delimitata dall'intersezione di una curva ellisse e di due radiali. La figura seguente mostra una torta disegnata usando la [**funzione Pie.**](/windows/desktop/api/Wingdi/nf-wingdi-pie)

![Figura che mostra un'ellisse con una torta ombreggiata](images/csfsh-03.png)

Quando si chiama [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), un'applicazione fornisce le coordinate degli angoli superiore sinistro e inferiore destro del rettangolo di delimitazione dell'ellisse, nonché le coordinate di due punti che definiscono due radiali.

Quando il sistema disegna la parte curva della torta, usa la direzione dell'arco corrente per il contesto di dispositivo specificato. La direzione predefinita dell'arco è in senso antiorario. Un'applicazione può reimpostare la direzione dell'arco chiamando la [**funzione SetArcDirection.**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection)

 

 
