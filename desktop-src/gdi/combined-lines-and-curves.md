---
description: Oltre a tracciare linee o curve, le applicazioni possono disegnare combinazioni di output di linee e curve chiamando una singola funzione. Ad esempio, un'applicazione può tracciare il contorno di un grafico a torta chiamando la funzione AngleArc.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Linee e curve combinate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978735"
---
# <a name="combined-lines-and-curves"></a>Linee e curve combinate

Oltre a tracciare linee o curve, le applicazioni possono disegnare combinazioni di output di linee e curve chiamando una singola funzione. Ad esempio, un'applicazione può tracciare il contorno di un grafico a torta chiamando la funzione [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .

La funzione [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) disegna un arco lungo il perimetro di un cerchio e disegna una linea che connette il punto iniziale dell'arco al centro del cerchio. Oltre a usare la funzione **AngleArc** , un'applicazione può combinare anche l'output a curva linea e irregolare usando la funzione di [**politraccia**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) .

 

 



