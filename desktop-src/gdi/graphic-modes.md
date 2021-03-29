---
description: Windows supporta cinque modalità grafiche che consentono a un'applicazione di specificare la modalità di combinazione dei colori, il modo in cui viene visualizzato l'output, la modalità di ridimensionamento dell'output e così via. Queste modalità, archiviate in un controller di dominio, sono descritte nella tabella seguente.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Modalità grafica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528344"
---
# <a name="graphic-modes"></a>Modalità grafica

Windows supporta cinque modalità grafiche che consentono a un'applicazione di specificare la modalità di combinazione dei colori, il modo in cui viene visualizzato l'output, la modalità di ridimensionamento dell'output e così via. Queste modalità, archiviate in un controller di dominio, sono descritte nella tabella seguente.



| Modalità grafica | Descrizione                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| Sfondo    | Definisce la modalità di combinazione dei colori di sfondo con la finestra o i colori dello schermo esistenti per le operazioni bitmap e di testo.              |
| Disegno       | Definisce il modo in cui i colori di primo piano vengono combinati con i colori della finestra o dello schermo esistenti per operazioni di penna, pennello, bitmap e testo. |
| Mapping       | Definisce il modo in cui viene eseguito il mapping dell'output della grafica da uno spazio logico o globale alla finestra, alla schermata o alla stampante.             |
| Riempimento poligono  | Definisce la modalità di utilizzo del modello di pennello per riempire l'area interna delle aree complesse.                                             |
| L'estensione    | Definisce il modo in cui i colori bitmap vengono combinati con i colori della finestra o dello schermo esistenti quando la bitmap viene compressa (o ridotta).  |



 

Come avviene con gli oggetti grafici, il sistema Inizializza un controller di dominio con le modalità grafiche predefinite. Un'applicazione può recuperare ed esaminare queste modalità predefinite chiamando le funzioni seguenti.



| Modalità grafica | Funzione                                       |
|---------------|------------------------------------------------|
| Sfondo    | [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| Disegno       | [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| Mapping       | [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| Riempimento poligono  | [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| L'estensione    | [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

Un'applicazione può modificare le modalità predefinite chiamando una delle funzioni seguenti.



| Modalità grafica | Funzione                                       |
|---------------|------------------------------------------------|
| Sfondo    | [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| Disegno       | [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| Mapping       | [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| Riempimento poligono  | [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| L'estensione    | [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



