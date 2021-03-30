---
description: Quasi tutte le applicazioni utilizzano la schermata per visualizzare i dati modificati.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: Informazioni su disegno e disegno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993861"
---
# <a name="about-painting-and-drawing"></a>Informazioni su disegno e disegno

Quasi tutte le applicazioni utilizzano la schermata per visualizzare i dati modificati. Un'applicazione disegna immagini, disegna figure e scrive testo in modo che l'utente possa visualizzare i dati durante la creazione, la modifica e la stampa. Microsoft Windows offre un supporto avanzato per la progettazione e il disegno, ma, a causa della natura dei sistemi operativi multitasking, le applicazioni devono collaborare tra loro durante l'accesso allo schermo.

Per garantire il funzionamento corretto e cooperativo di tutte le applicazioni, il sistema gestisce tutti gli output sullo schermo. Le applicazioni utilizzano Windows come dispositivo di output primario anziché con la schermata stessa. Il sistema consente di visualizzare i contesti di dispositivo che corrispondono in modo univoco alle finestre. Le applicazioni usano i contesti di dispositivo di visualizzazione per indirizzare l'output alle finestre specificate. Il disegno in una finestra (indirizzando l'output) impedisce a un'applicazione di interferire con l'output di altre applicazioni e consente alle applicazioni di coesistere l'uno con l'altro sfruttando al tempo stesso tutte le funzionalità grafiche del sistema.

-   [Quando creare un oggetto in una finestra](when-to-draw-in-a-window.md)
-   [Messaggio di \_ disegno WM](the-wm-paint-message.md)
-   [Disegno senza il messaggio di disegno WM \_](drawing-without-the-wm-paint-message.md)
-   [Sistema di coordinate finestra](window-coordinate-system.md)
-   [Aree della finestra](window-regions.md)
-   [Sfondo finestra](window-background.md)
-   [Finestre ridotte a icona](minimized-windows.md)
-   [Finestre ridimensionate](resized-windows.md)
-   [Area non client](nonclient-area.md)
-   [Area di aggiornamento della finestra figlio](child-window-update-region.md)
-   [Dispositivi di visualizzazione](display-devices.md)
-   [Blocco aggiornamento finestra](window-update-lock.md)
-   [Rettangolo di delimitazione accumulato](accumulated-bounding-rectangle.md)

 

 



