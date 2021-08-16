---
description: Le funzioni seguenti vengono usate per creare, modificare o disegnare tracciati.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: Funzioni path (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700298056ac595b0e9208c0b8535d7a3d2e822e048e4c656d0b4501947764533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759427"
---
# <a name="path-functions-windows-gdi"></a>Funzioni path (Windows GDI)

Le funzioni seguenti vengono usate per creare, modificare o disegnare tracciati.



| Funzione                                       | Descrizione                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPath**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | Chiude ed elimina tutti i percorsi nel contesto di dispositivo specificato.                                                                                                   |
| [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | Apre una parentesi di percorso nel contesto di dispositivo specificato.                                                                                                            |
| [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | Chiude una figura aperta in un percorso.                                                                                                                                 |
| [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | Chiude una parentesi di percorso e seleziona il percorso definito dalla parentesi nel contesto di dispositivo specificato.                                                             |
| [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | Chiude tutte le figure aperte nel percorso corrente e riempie l'interno del tracciato usando il pennello corrente e la modalità di riempimento poligono.                                   |
| [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | Trasforma tutte le curve nel tracciato selezionato nel contesto di dispositivo corrente, trasformando ogni curva in una sequenza di linee.                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | Recupera il limite di miter per il contesto di dispositivo specificato.                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | Recupera le coordinate che definiscono gli endpoint delle linee e i punti di controllo delle curve presenti nel percorso selezionato nel contesto di dispositivo specificato. |
| [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | Crea un'area dal percorso selezionato nel contesto di dispositivo specificato.                                                                               |
| [**SetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | Imposta il limite per la lunghezza dei join di miter per il contesto di dispositivo specificato.                                                                                   |
| [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | Chiude tutte le figure aperte in un tracciato, traccia il contorno del tracciato usando la penna corrente e riempie l'area interna usando il pennello corrente.                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | Esegue il rendering del percorso specificato usando la penna corrente.                                                                                                             |
| [**WidenPath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | Ridefinisce il tracciato corrente come area che verrebbe disegnata se il tracciato fosse stato tracciato usando la penna attualmente selezionata nel contesto di dispositivo specificato.            |



 

 

 



