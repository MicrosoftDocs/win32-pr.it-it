---
description: Una curva regolare è un set di pixel evidenziati in una visualizzazione raster (o punti in una pagina stampata) che definiscono il perimetro (o parte del perimetro) di una sezione conica.
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: Curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e694edeb535dbc7dbd4191a5a2b0b44556b810e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880317"
---
# <a name="curves"></a>Curve

Una curva regolare è un set di pixel evidenziati in una visualizzazione raster (o punti in una pagina stampata) che definiscono il perimetro (o parte del perimetro) di una sezione conica. Una curva irregolare è un set di pixel che definiscono una curva che non si adatta al perimetro di una sezione conica. Il punto finale è escluso dalla curva così come è escluso da una riga.

Quando un'applicazione chiama una delle funzioni di disegno della curva, GDI suddivide la curva in una serie di segmenti di linea discreti di dimensioni molto ridotte. Dopo aver determinato gli endpoint (punto iniziale e punto finale) per ognuno di questi segmenti di linea, GDI determina quali pixel (o punti) definiscono ogni riga applicando il relativo DDA.

Un'applicazione può creare un'ellisse o una parte di un'ellisse chiamando la funzione [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) . Questa funzione disegna la curva all'interno del perimetro di un rettangolo invisibile denominato rettangolo di delimitazione. La dimensione dell'ellisse è specificata da due radiali invisibili che si estendono dal centro del rettangolo ai lati del rettangolo. Nella figura seguente viene illustrato un arco (parte di un'ellisse) tracciato utilizzando la funzione **Arc** .

![diagramma che mostra un arco che rappresenta tre trimestri di un cerchio completo](images/cslcv-03.png)

Quando si chiama la funzione [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) , un'applicazione specifica le coordinate del rettangolo di delimitazione e delle radiali. L'illustrazione precedente Mostra il rettangolo e le radiali con linee tratteggiate mentre l'arco effettivo è stato disegnato usando una linea continua.

Quando si disegna l'arco di un altro oggetto, l'applicazione può chiamare le funzioni [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) e [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) per controllare la direzione (in senso orario o antiorario) in cui viene disegnato l'oggetto. La direzione predefinita per disegnare archi e altri oggetti è in senso antiorario.

Oltre a disegnare ellissi o parti di ellissi, le applicazioni possono disegnare curve irregolari denominate curve di Bézier. Una *curva di Bézier* è una curva irregolare la cui curvatura è definita da quattro punti di controllo (P1, P2, P3 e P4). I punti di controllo P1 e P4 definiscono i punti iniziale e finale della curva e i punti di controllo P2 e P3 definiscono la forma della curva contrassegnando i punti in cui la curva inverte l'orientamento, come illustrato nel diagramma seguente.

![illustrazione che mostra due curve di Bézier, ognuna tra un punto iniziale e un punto finale e l'altra con due punti di controllo](images/cslcv-04.png)

Un'applicazione può creare curve irregolari chiamando la funzione [**polibezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) , fornendo i punti di controllo appropriati.

 

 



