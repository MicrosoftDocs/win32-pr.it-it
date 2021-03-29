---
description: Per creare un percorso e selezionarlo in un controller di dominio, è necessario innanzitutto definire i punti che lo descrivono.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Creazione percorso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226678"
---
# <a name="path-creation"></a>Creazione percorso

Per creare un percorso e selezionarlo in un controller di dominio, è necessario innanzitutto definire i punti che lo descrivono. Questa operazione viene eseguita chiamando la funzione [**beginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) , specificando le funzioni di disegno appropriate, quindi chiamando la funzione [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) . Questa combinazione di funzioni (**beginPath**, Drawing Functions e **EndPath**) costituisce una *parentesi del percorso*. Di seguito è riportato l'elenco delle funzioni di disegno che è possibile utilizzare.

-   [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [**Ellisse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [**Torta**](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [**Polibezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [**Polidisegni**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [**Polilinea**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [**PolylineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [**Polilinea**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [**Rettangolo**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Quando un'applicazione chiama [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), il sistema seleziona il percorso associato nel controller di dominio specificato. Se in precedenza è stato selezionato un altro percorso nel controller di dominio, il sistema elimina tale percorso senza salvarlo. Quando il sistema seleziona il percorso nel controller di dominio, un'applicazione può operare sul percorso in uno dei modi seguenti:

-   Disegnare la struttura del percorso (usando la penna corrente).
-   Disegnare l'interno del tracciato (usando il pennello corrente).
-   Disegnare la struttura e riempire la parte interna del percorso.
-   Modificare il percorso (convertendo le curve in segmenti di linea).
-   Converte il percorso in un tracciato di ritaglio.
-   Convertire il percorso in un'area.
-   Rendere flat il percorso convertendo ogni curva del tracciato in una serie di segmenti di linea.
-   Recuperare le coordinate delle linee e delle curve che compongono un percorso.

 

 



