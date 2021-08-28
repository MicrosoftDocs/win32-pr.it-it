---
description: Windows supporta cinque modalità grafiche che consentono a un'applicazione di specificare come vengono misti i colori, dove viene visualizzato l'output, come viene ridimensionato l'output e così via. Queste modalità, archiviate in un controller di dominio, sono descritte nella tabella seguente.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Modalità grafica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c36461935c8279e38e09afe9f7802e2f758d1cf45380beaa16d1911f4ed965f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558771"
---
# <a name="graphic-modes"></a>Modalità grafica

Windows supporta cinque modalità grafiche che consentono a un'applicazione di specificare come vengono misti i colori, dove viene visualizzato l'output, come viene ridimensionato l'output e così via. Queste modalità, archiviate in un controller di dominio, sono descritte nella tabella seguente.



| Modalità grafica | Descrizione                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| Sfondo    | Definisce il modo in cui i colori di sfondo vengono misti con i colori della finestra o dello schermo esistenti per le operazioni bitmap e di testo.              |
| Disegno       | Definisce il modo in cui i colori in primo piano vengono misti con i colori della finestra o dello schermo esistenti per le operazioni su penna, pennello, bitmap e testo. |
| Mapping       | Definisce la modalità di mapping dell'output grafico dallo spazio logico (o mondo) alla finestra, allo schermo o alla carta della stampante.             |
| Riempimento poligono  | Definisce il modo in cui il motivo del pennello viene usato per riempire l'interno di aree complesse.                                             |
| Stretching    | Definisce il modo in cui i colori bitmap vengono misti con i colori della finestra o dello schermo esistenti quando la bitmap viene compressa (o ridotta).  |



 

Come per gli oggetti grafici, il sistema inizializza un controller di dominio con le modalità grafiche predefinite. Un'applicazione può recuperare ed esaminare queste modalità predefinite chiamando le funzioni seguenti.



| Modalità grafica | Funzione                                       |
|---------------|------------------------------------------------|
| Sfondo    | [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| Disegno       | [**Get PIÙ2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| Mapping       | [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| Riempimento poligono  | [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| Stretching    | [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

Un'applicazione può modificare le modalità predefinite chiamando una delle funzioni seguenti.



| Modalità grafica | Funzione                                       |
|---------------|------------------------------------------------|
| Sfondo    | [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| Disegno       | [**Set UNAN2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| Mapping       | [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| Riempimento poligono  | [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| Stretching    | [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



