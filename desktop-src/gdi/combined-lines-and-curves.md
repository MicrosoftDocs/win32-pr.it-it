---
description: Oltre a disegnare linee o curve, le applicazioni possono disegnare combinazioni di output di linee e curve chiamando una singola funzione. Ad esempio, un'applicazione può disegnare la struttura di un grafico a torta chiamando la funzione AngleArc.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Linee e curve combinate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1939b863bfacf2176f15c950b48c8b7c91cc43e7b6b4d4c58ac08e1760c4cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105720"
---
# <a name="combined-lines-and-curves"></a>Linee e curve combinate

Oltre a disegnare linee o curve, le applicazioni possono disegnare combinazioni di output di linee e curve chiamando una singola funzione. Ad esempio, un'applicazione può disegnare la struttura di un grafico a torta chiamando la [**funzione AngleArc.**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)

La [**funzione AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) disegna un arco lungo il perimetro di un cerchio e disegna una linea che connette il punto iniziale dell'arco al centro del cerchio. Oltre a usare la funzione **AngleArc,** un'applicazione può anche combinare l'output della linea e della curva irregolare usando la [**funzione PolyDraw.**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)

 

 



