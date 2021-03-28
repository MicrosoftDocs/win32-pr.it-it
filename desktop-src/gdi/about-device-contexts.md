---
description: L'indipendenza del dispositivo è una delle funzionalità principali di Microsoft Windows.
ms.assetid: f2a4c4cf-55e9-4129-8067-256552af49d2
title: Informazioni sui contesti di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b686ec8b48492658f19531cb42161c043f178d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130359"
---
# <a name="about-device-contexts"></a>Informazioni sui contesti di dispositivo

L'indipendenza del dispositivo è una delle funzionalità principali di Microsoft Windows. Le applicazioni possono creare e stampare l'output su un'ampia gamma di dispositivi. Il software che supporta questa indipendenza dal dispositivo è contenuto in due librerie a collegamento dinamico. Il primo, Gdi.dll, viene definito GDI (Graphics Device Interface); il secondo viene definito driver di dispositivo. Il nome del secondo dipende dal dispositivo in cui l'applicazione disegna l'output. Se, ad esempio, l'applicazione disegna l'output nell'area client della finestra in una visualizzazione VGA, questa libreria è Vga.dll; Se l'applicazione stampa l'output in una stampante Epson FX-80, questa libreria è Epson9.dll.

Un'applicazione deve informare GDI per caricare un driver di dispositivo specifico e, una volta caricato il driver, per preparare il dispositivo per le operazioni di disegno, ad esempio la selezione di un colore e una larghezza della linea, un motivo e un colore per il pennello, un carattere tipografico, un'area di ridimensionamento e così via. Queste attività vengono eseguite tramite la creazione e la gestione di un contesto di dispositivo (DC). Un controller di dominio è una struttura che definisce un set di oggetti grafici e i relativi attributi associati e le modalità grafiche che interessano l'output. Gli oggetti grafici includono una penna per il disegno a linee, un pennello per il disegno e il riempimento, una bitmap per la copia o lo scorrimento di parti dello schermo, una tavolozza per la definizione del set di colori disponibili, un'area per il ritaglio e altre operazioni e un percorso per le operazioni di disegno e disegno. A differenza della maggior parte delle strutture, un'applicazione non ha mai accesso diretto al controller di dominio; ma opera sulla struttura indirettamente chiamando diverse funzioni.

In questa panoramica vengono fornite informazioni sui seguenti argomenti:

-   [Oggetti grafici](graphic-objects.md)
-   [Modalità grafica](graphic-modes.md)
-   [Tipi di contesto di dispositivo](device-context-types.md)
-   [Operazioni di contesto del dispositivo](device-context-operations.md)
-   [Funzioni di contesto di dispositivo abilitate per ICM](icm-enabled-device-context-functions.md)

Un concetto importante è il layout di un controller di dominio o di una finestra, che descrive l'ordine in cui vengono rivelati gli oggetti e il testo GDI (da sinistra a destra o da destra a sinistra). Per ulteriori informazioni, vedere "layout della finestra e mirroring" nelle [**funzionalità della finestra**](../winmsg/window-features.md) e funzioni [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) e [**selayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout) .

 

 
