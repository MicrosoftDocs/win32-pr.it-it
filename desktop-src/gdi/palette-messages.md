---
description: Le modifiche alla tavolozza di sistema per il dispositivo di visualizzazione possono avere effetti significativi e talvolta indesiderati sui colori usati in Windows sul desktop.
ms.assetid: 9c470b6f-c0d3-462e-9649-1f39b06bd543
title: Messaggi tavolozza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f19a5458ec89d8d9a0524fd2ec383de740c0179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978450"
---
# <a name="palette-messages"></a>Messaggi tavolozza

Le modifiche alla tavolozza di sistema per il dispositivo di visualizzazione possono avere effetti significativi e talvolta indesiderati sui colori usati in Windows sul desktop. Per ridurre al minimo l'effetto di queste modifiche, il sistema fornisce un set di messaggi che consentono alle applicazioni di gestire le tavolozze logiche garantendo al contempo che i colori nella finestra attiva siano il più vicino possibile ai colori previsti.

Il sistema invia un messaggio [**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) a una finestra di primo livello o sovrapposta appena prima di attivare la finestra. Questo messaggio fornisce a un'applicazione la possibilità di selezionare e realizzare la relativa tavolozza logica in modo che riceva il migliore mapping possibile dei colori per la tavolozza logica. Quando l'applicazione riceve il messaggio, deve usare le funzioni [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette), [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) per selezionare e realizzare la tavolozza logica. In questo modo, il sistema deve aggiornare i colori nella tavolozza di sistema in modo che i colori corrispondano a tutti i colori disponibili nella tavolozza logica.

Quando un'applicazione causa modifiche alla tavolozza di sistema in seguito alla realizzazione della tavolozza logica, il sistema invia un messaggio [**WM \_ PALETTECHANGED**](wm-palettechanged.md) a tutte le finestre di primo livello e sovrapposte. Questo messaggio offre alle applicazioni la possibilità di aggiornare i colori nelle aree client delle rispettive finestre, sostituendo i colori che sono stati modificati con colori che corrispondono maggiormente ai colori desiderati. Un'applicazione che riceve il **messaggio WM \_ PALETTECHANGED** deve usare [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) per reimpostare le tavolozze logiche associate a tutte le finestre inattive e quindi aggiornare i colori nell'area client per ogni finestra inattiva usando la funzione [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) . Questa tecnica non garantisce il maggior numero di corrispondenze esatte dei colori; Tuttavia, garantisce la mappatura dei colori della tavolozza logica ai colori ragionevoli della tavolozza di sistema.

> [!Note]  
> Per evitare di creare un ciclo infinito, un'applicazione non deve mai realizzare la tavolozza per la finestra il cui handle corrisponde all'handle passato nel parametro *wParam* del messaggio [**WM \_ PALETTECHANGED**](wm-palettechanged.md) .

 

La funzione [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) aggiorna in genere un'area client di una finestra inattiva più velocemente rispetto al ridisegno dell'area. Tuttavia, poiché **UpdateColors** esegue la conversione dei colori in base al colore di ogni pixel prima che la tavolozza di sistema venga modificata, ogni chiamata a questa funzione comporta la perdita di una certa accuratezza del colore. Ciò significa che non è possibile usare **UpdateColors** per aggiornare i colori quando la finestra diventa attiva. In questi casi, l'applicazione deve ricreare l'area client.

Il sistema può inviare il messaggio [**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) quando vengono apportate modifiche alla tavolozza logica. Inoltre, il sistema può inviare il messaggio [**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md) a tutte le finestre di primo livello e sovrapposte quando la tavolozza di sistema sta per cambiare.

 

 



