---
description: L'indipendenza dei dispositivi è una delle principali funzionalità di Microsoft Windows.
ms.assetid: f2a4c4cf-55e9-4129-8067-256552af49d2
title: Informazioni sui contesti di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9439e3091b3138917e24ab4a49ff89c21a1e1b53480d4a138bd2bbad3288fcd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105876"
---
# <a name="about-device-contexts"></a>Informazioni sui contesti di dispositivo

L'indipendenza dei dispositivi è una delle principali funzionalità di Microsoft Windows. Le applicazioni possono disegnare e stampare l'output su un'ampia gamma di dispositivi. Il software che supporta questa indipendenza dei dispositivi è contenuto in due librerie a collegamento dinamico. Il primo, Gdi.dll, viene definito GDI (Graphics Device Interface). il secondo è detto driver di dispositivo. Il nome del secondo dipende dal dispositivo in cui l'applicazione disegna l'output. Ad esempio, se l'applicazione disegna l'output nell'area client della relativa finestra su una visualizzazione VGA, questa libreria viene Vga.dll; se l'applicazione stampa l'output su una stampante Epson FX-80, questa libreria è Epson9.dll.

Un'applicazione deve informare GDI di caricare un driver di dispositivo specifico e, dopo il caricamento del driver, preparare il dispositivo per le operazioni di disegno, ad esempio la selezione di un colore e di una larghezza della linea, un motivo e un colore del pennello, un carattere tipografico del carattere, un'area di ritaglio e così via. Queste attività vengono eseguite creando e mantenendo un contesto di dispositivo (DC). Un controller di dominio è una struttura che definisce un set di oggetti grafici e i relativi attributi associati e le modalità grafiche che influiscono sull'output. Gli oggetti grafici includono una penna per il disegno di linee, un pennello per disegnare e riempire, una bitmap per la copia o lo scorrimento di parti dello schermo, una tavolozza per la definizione del set di colori disponibili, un'area per il ritaglio e altre operazioni e un tracciato per le operazioni di disegno e disegno. A differenza della maggior parte delle strutture, un'applicazione non ha mai accesso diretto al controller di dominio; ma opera indirettamente sulla struttura chiamando varie funzioni.

In questa panoramica vengono fornite informazioni sugli argomenti seguenti:

-   [Oggetti grafici](graphic-objects.md)
-   [Modalità grafica](graphic-modes.md)
-   [Tipi di contesto di dispositivo](device-context-types.md)
-   [Operazioni del contesto di dispositivo](device-context-operations.md)
-   [ICM del contesto di dispositivo abilitate per l'uso](icm-enabled-device-context-functions.md)

Un concetto importante è il layout di un controller di dominio o di una finestra, che descrive l'ordine in cui vengono rivelati gli oggetti GDI e il testo (da sinistra a destra o da destra a sinistra). Per altre informazioni, vedere "Layout e mirroring della finestra" in [**Funzionalità delle**](../winmsg/window-features.md) finestre e le [**funzioni GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) [**e SetLayout.**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)

 

 
