---
description: Un rettangolo è un poligono a quattro lati i cui lati opposti sono paralleli e di lunghezza uguale.
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: Disegno di rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880294"
---
# <a name="drawing-rectangles"></a>Disegno di rettangoli

Un rettangolo è un poligono a quattro lati i cui lati opposti sono paralleli e di lunghezza uguale. Sebbene un'applicazione possa creare un rettangolo chiamando la funzione [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) , fornendo le coordinate di ogni angolo, la funzione [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) fornisce un metodo più semplice. Questa funzione richiede solo le coordinate per gli angoli superiore sinistro e inferiore destro. Quando un'applicazione chiama la funzione [**Rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) , il sistema disegna il rettangolo, esclusi i lati destro e inferiore se non è impostata alcuna trasformazione globale per il contesto di dispositivo specificato.

Se è stata impostata una trasformazione globale tramite la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) o [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , il sistema include i bordi destro e inferiore.

Oltre a disegnare un rettangolo tradizionale, è possibile disegnare rettangoli con angoli arrotondati. Per la funzione [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) è necessario che l'applicazione fornisca le coordinate degli angoli inferiore sinistro e superiore destro, nonché la larghezza e l'altezza dell'ellisse utilizzata per arrotondare ogni angolo.

Per modificare i rettangoli, le applicazioni possono utilizzare le funzioni seguenti.



| Funzione                         | Descrizione                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [**FillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | Ridisegna l'interno di un rettangolo.                              |
| [**FrameRect**](/windows/desktop/api/Winuser/nf-winuser-framerect)   | Ridisegnato i lati di un rettangolo.                                  |
| [**InvertRect**](/windows/desktop/api/Winuser/nf-winuser-invertrect) | Inverte i colori visualizzati all'interno di un rettangolo. |



 

 

 
