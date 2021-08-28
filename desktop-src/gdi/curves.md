---
description: Una curva regolare è un set di pixel evidenziati su uno schermo raster (o punti su una pagina stampata) che definiscono il perimetro (o parte del perimetro) di una sezione conica.
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: Curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed6b7c0f6ad03a9ebe16dcffe85694397f6127ff15c2d9d3a9e68f79257a0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452241"
---
# <a name="curves"></a>Curve

Una curva regolare è un set di pixel evidenziati su uno schermo raster (o punti su una pagina stampata) che definiscono il perimetro (o parte del perimetro) di una sezione conica. Una curva irregolare è un set di pixel che definiscono una curva che non rientra nel perimetro di una sezione conica. Il punto finale viene escluso da una curva così come viene escluso da una linea.

Quando un'applicazione chiama una delle funzioni di disegno della curva, GDI suddivide la curva in un numero di segmenti di linea discreti estremamente piccoli. Dopo aver determinato gli endpoint (punto iniziale e punto finale) per ognuno di questi segmenti di linea, GDI determina quali pixel (o punti) definiscono ogni linea applicando il relativo DDA.

Un'applicazione può disegnare un'ellisse o una parte di un'ellisse chiamando la [**funzione**](/windows/desktop/api/Wingdi/nf-wingdi-arc) Arc. Questa funzione disegna la curva all'interno del perimetro di un rettangolo invisibile denominato rettangolo di delimitazione. Le dimensioni dell'ellisse vengono specificate da due radiali invisibili che si estendono dal centro del rettangolo ai lati del rettangolo. La figura seguente mostra un arco (parte di un'ellisse) disegnato usando la **funzione Arc.**

![diagramma che mostra un arco che rappresenta i tre trimestri di un cerchio completo](images/cslcv-03.png)

Quando si chiama [**la funzione Arc,**](/windows/desktop/api/Wingdi/nf-wingdi-arc) un'applicazione specifica le coordinate del rettangolo di delimitazione e dei radiali. La figura precedente mostra il rettangolo e i radiali con linee tratteggiate mentre l'arco effettivo è stato disegnato usando una linea continua.

Quando si disegna l'arco di un altro oggetto, l'applicazione può chiamare le funzioni [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) e [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) per controllare la direzione (in senso orario o in senso antiorario) in cui viene disegnato l'oggetto. La direzione predefinita per il disegno di archi e altri oggetti è in senso antiorario.

Oltre a disegnare ellissi o parti di puntini di sospensione, le applicazioni possono disegnare curve irregolari denominate curve di Bézier. Una *curva di Bézier* è una curva irregolare la cui curvatura è definita da quattro punti di controllo (p1, p2, p3 e p4). I punti di controllo p1 e p4 definiscono i punti iniziale e finale della curva, mentre i punti di controllo p2 e p3 definiscono la forma della curva contrassegnando i punti in cui la curva inverte l'orientamento, come illustrato nel diagramma seguente.

![Figura che mostra due curve di Bézier, ognuna tra un punto iniziale e un punto finale e ognuna con due punti di controllo](images/cslcv-04.png)

Un'applicazione può disegnare curve irregolari chiamando la [**funzione PolyBezier,**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) fornendo i punti di controllo appropriati.

 

 



