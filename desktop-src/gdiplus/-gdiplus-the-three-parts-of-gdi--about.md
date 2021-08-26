---
description: 'I servizi di Windows GDI+ rientrano nelle tre ampie categorie seguenti:'
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: Le tre parti di GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5547702ca98cce86ace0f672b7aeed2dc8fc0ecee63534aaa15fac05bdcb024b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014651"
---
# <a name="the-three-parts-of-gdi"></a>Le tre parti di GDI+

I servizi di Windows GDI+ rientrano nelle tre ampie categorie seguenti:

-   [grafica vettoriale bidimensionale](#2-d-vector-graphics)
-   [Creazione delle immagini](#imaging)
-   [Tipografia](#typography)

## <a name="2-d-vector-graphics"></a>grafica vettoriale bidimensionale

La grafica vettoriale prevede il disegno di primitive (ad esempio linee, curve e figure) specificate da set di punti in un sistema di coordinate. Ad esempio, una linea retta può essere specificata dai due endpoint e un rettangolo può essere specificato da un punto che indica la posizione dell'angolo superiore sinistro e una coppia di numeri che ne specifica larghezza e altezza. Un percorso semplice può essere specificato da una matrice di punti da collegare tramite linee rette. Una spline di Bézier è una curva sofisticata specificata da quattro punti di controllo.

GDI+ classi che archiviano informazioni sulle primitive stesse, classi che archiviano informazioni sulla modalità di disegno delle primitive e classi che ese tracciano effettivamente il disegno. Ad esempio, la **classe Rect** archivia la posizione e le dimensioni di un rettangolo. La **classe Pen** archivia informazioni sul colore della linea, lo spessore della linea e lo stile della linea. e la **classe Graphics** include metodi per disegnare linee, rettangoli, tracciati e altre figure. Sono anche disponibili diverse **classi Brush** che archiviano informazioni sul modo in cui figure e tracciati chiusi devono essere riempiti con colori o motivi.

## <a name="imaging"></a>Creazione delle immagini

Alcuni tipi di immagini sono difficili o impossibili da visualizzare con le tecniche di grafica vettoriale. Ad esempio, le immagini sui pulsanti della barra degli strumenti e le immagini visualizzate come icone sarebbero difficili da specificare come raccolte di linee e curve. Una fotografia digitale ad alta risoluzione di uno stadio di baseball gremito sarebbe ancora più difficile da creare con tecniche vettoriali. Le immagini di questo tipo vengono archiviate come bitmap, matrici di numeri che rappresentano i colori dei singoli punti sullo schermo. Le strutture di dati che archiviano informazioni sulle bitmap tendono a essere più complesse rispetto a quelle necessarie per la grafica vettoriale, quindi esistono diverse classi in GDI+ dedicate a questo scopo. Un esempio di questa classe è **CachedBitmap,** che viene usato per archiviare una bitmap in memoria per un accesso e una visualizzazione veloci.

## <a name="typography"></a>Tipografia

La tipografia riguarda la visualizzazione del testo in un'ampia gamma di tipi di carattere, dimensioni e stili. GDI+ offre una notevole quantità di supporto per questa attività complessa. Una delle nuove funzionalità di GDI+ è l'antialiasing subpixel, che offre un aspetto più uniforme del testo sottoposto a rendering su uno schermo LCD.

 

 



