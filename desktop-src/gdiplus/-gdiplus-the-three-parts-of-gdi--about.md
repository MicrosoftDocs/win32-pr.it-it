---
description: 'I servizi di Windows GDI+ rientrano nelle tre categorie generali seguenti:'
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: Le tre parti di GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2021260e9fe3b3d927131c2ba1856aeed0ed07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994181"
---
# <a name="the-three-parts-of-gdi"></a>Le tre parti di GDI+

I servizi di Windows GDI+ rientrano nelle tre categorie generali seguenti:

-   [grafica vettoriale bidimensionale](#2-d-vector-graphics)
-   [Creazione delle immagini](#imaging)
-   [Tipografia](#typography)

## <a name="2-d-vector-graphics"></a>grafica vettoriale bidimensionale

La grafica vettoriale comporta il disegno di primitive, ad esempio linee, curve e figure, specificate da set di punti in un sistema di coordinate. Ad esempio, è possibile specificare una linea retta dai relativi due endpoint e un rettangolo può essere specificato da un punto che fornisce la posizione dell'angolo superiore sinistro e una coppia di numeri che ne assegna la larghezza e l'altezza. Un percorso semplice può essere specificato da una matrice di punti da connettere tramite linee rette. Una spline di Bézier è una curva sofisticata specificata da quattro punti di controllo.

GDI+ fornisce classi che archiviano informazioni sulle primitive stesse, classi in cui vengono archiviate le informazioni sulla modalità di disegno delle primitive e le classi che eseguono effettivamente il disegno. Ad esempio, la classe **Rect** archivia la posizione e le dimensioni di un rettangolo. la classe **Pen** archivia le informazioni sul colore della linea, lo spessore della linea e lo stile della linea; e la classe **Graphics** dispone di metodi per disegnare linee, rettangoli, percorsi e altre figure. Sono inoltre disponibili diverse classi di **pennelli** in cui vengono archiviate le informazioni sulla modalità di riempimento delle figure e dei percorsi chiusi con i colori o i modelli.

## <a name="imaging"></a>Creazione delle immagini

Alcuni tipi di immagini sono difficili o impossibili da visualizzare con le tecniche di grafica vettoriale. Ad esempio, le immagini sui pulsanti della barra degli strumenti e le immagini visualizzate come icone sarebbero difficili da specificare come raccolte di linee e curve. Una fotografia digitale ad alta risoluzione di uno stadio di baseball affollato sarebbe ancora più difficile da creare con le tecniche vettoriali. Le immagini di questo tipo vengono archiviate come bitmap, matrici di numeri che rappresentano i colori dei singoli punti sullo schermo. Le strutture di dati che archiviano informazioni sulle bitmap tendono a essere più complesse rispetto a quelle richieste per la grafica vettoriale, quindi sono disponibili diverse classi in GDI+ dedicate a questo scopo. Un esempio di tale classe è **CachedBitmap**, che viene usato per archiviare una bitmap in memoria per l'accesso e la visualizzazione rapidi.

## <a name="typography"></a>Tipografia

La tipografia è interessata alla visualizzazione del testo in un'ampia gamma di tipi di carattere, dimensioni e stili. GDI+ offre una notevole quantità di supporto per questa attività complessa. Una delle nuove funzionalità di GDI+ è l'anti-aliasing dei subpixel, che fornisce un aspetto più uniforme del testo visualizzato sullo schermo LCD.

 

 



