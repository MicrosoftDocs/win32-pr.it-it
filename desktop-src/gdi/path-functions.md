---
description: Le funzioni seguenti vengono utilizzate per creare, modificare o tracciare percorsi.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: Funzioni Path (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab85e52392b3e600877f8f5adac08d5de77e873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978447"
---
# <a name="path-functions-windows-gdi"></a>Funzioni Path (Windows GDI)

Le funzioni seguenti vengono utilizzate per creare, modificare o tracciare percorsi.



| Funzione                                       | Descrizione                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPath**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | Chiude ed Elimina tutti i percorsi nel contesto di dispositivo specificato.                                                                                                   |
| [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | Apre una parentesi del percorso nel contesto di dispositivo specificato.                                                                                                            |
| [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | Chiude una figura aperta in un percorso.                                                                                                                                 |
| [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | Chiude una parentesi del percorso e seleziona il percorso definito dalla parentesi nel contesto di dispositivo specificato.                                                             |
| [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | Chiude tutte le figure aperte nel percorso corrente e riempie l'area interna del percorso utilizzando il pennello corrente e la modalità di riempimento del poligono.                                   |
| [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | Trasforma le curve nel percorso selezionato nel contesto di dispositivo corrente (DC), trasformando ciascuna curva in una sequenza di righe.                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | Recupera il limite di smussatura per il contesto di dispositivo specificato.                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | Recupera le coordinate che definiscono gli endpoint delle linee e i punti di controllo delle curve trovate nel percorso selezionato nel contesto di dispositivo specificato. |
| [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | Crea un'area dal percorso selezionato nel contesto di dispositivo specificato.                                                                               |
| [**SetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | Imposta il limite per la lunghezza dei join degli angoli smussati per il contesto di dispositivo specificato.                                                                                   |
| [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | Chiude tutte le figure aperte in un percorso, traccia il contorno del tracciato utilizzando la penna corrente e riempie l'interno utilizzando il pennello corrente.                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | Esegue il rendering del percorso specificato utilizzando la penna corrente.                                                                                                             |
| [**WidenPath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | Ridefinisce il percorso corrente come area da disegnare se il tracciato è stato tracciato utilizzando la penna attualmente selezionata nel contesto di dispositivo specificato.            |



 

 

 



