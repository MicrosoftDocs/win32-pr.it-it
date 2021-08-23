---
description: Le modifiche alla tavolozza del sistema per il dispositivo di visualizzazione possono avere effetti notevoli e talvolta indesiderati sui colori usati nelle finestre sul desktop.
ms.assetid: 9c470b6f-c0d3-462e-9649-1f39b06bd543
title: Messaggi della tavolozza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a82c5ae2727e9f687f5f7fb628279b7832e896991f703225beec075a6630133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558441"
---
# <a name="palette-messages"></a>Messaggi della tavolozza

Le modifiche alla tavolozza del sistema per il dispositivo di visualizzazione possono avere effetti notevoli e talvolta indesiderati sui colori usati nelle finestre sul desktop. Per ridurre al minimo l'impatto di queste modifiche, il sistema fornisce un set di messaggi che consentono alle applicazioni di gestire le tavolozze logiche garantendo al tempo stesso che i colori nella finestra attiva siano il più vicini possibile ai colori destinati.

Il sistema invia un [**messaggio WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) a una finestra di primo livello o sovrapposta subito prima di attivare la finestra. Questo messaggio offre a un'applicazione la possibilità di selezionare e realizzare la tavolozza logica in modo che riceva il mapping migliore possibile dei colori per la tavolozza logica. Quando l'applicazione riceve il messaggio, deve usare le funzioni [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette), [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) per selezionare e realizzare la tavolozza logica. In questo modo il sistema aggiorna i colori nella tavolozza di sistema in modo che i colori corrispondano al maggior numero possibile di colori nella tavolozza logica.

Quando un'applicazione causa modifiche alla tavolozza di sistema in seguito alla realizzazione della tavolozza logica, il sistema invia un messaggio [**WM \_ PALETTECHANGED**](wm-palettechanged.md) a tutte le finestre sovrapposte e di primo livello. Questo messaggio offre alle applicazioni la possibilità di aggiornare i colori nelle aree client delle finestre, sostituendo i colori modificati con colori più corrispondenti ai colori destinati. Un'applicazione che riceve il messaggio **WM \_ PALETTECHANGED** deve usare [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) per reimpostare le tavolozze logiche associate a tutte le finestre inattive e quindi aggiornare i colori nell'area client per ogni finestra inattiva usando la [**funzione UpdateColors.**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) Questa tecnica non garantisce il maggior numero di corrispondenze esatte dei colori; tuttavia garantisce che i colori nella tavolozza logica siano mappati a colori ragionevoli nella tavolozza di sistema.

> [!Note]  
> Per evitare la creazione di un ciclo infinito, un'applicazione non deve mai realizzare la tavolozza per la finestra il cui handle corrisponde all'handle passato nel parametro *wParam* del [**messaggio WM \_ PALETTECHANGED.**](wm-palettechanged.md)

 

La [**funzione UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) aggiorna in genere un'area client di una finestra inattiva più velocemente rispetto al ridisegno dell'area. Tuttavia, poiché UpdateColors esegue la **traslazione** dei colori in base al colore di ogni pixel prima della modifica della tavolozza di sistema, ogni chiamata a questa funzione comporta la perdita di una certa accuratezza del colore. Ciò significa **che UpdateColors non** può essere usato per aggiornare i colori quando la finestra diventa attiva. In questi casi, l'applicazione deve ridisegnare l'area client.

Il sistema può inviare il [**messaggio WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) quando vengono apportate modifiche alla tavolozza logica. Inoltre, il sistema può inviare il messaggio [**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md) a tutte le finestre di primo livello e sovrapposte quando la tavolozza di sistema sta per cambiare.

 

 



