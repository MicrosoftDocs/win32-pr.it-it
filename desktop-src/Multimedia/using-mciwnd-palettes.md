---
title: Uso di tavolozze MCIWnd
description: Uso di tavolozze MCIWnd
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- MCIWndGetPalette (macro)
- MCIWndSetPalette (macro)
- MCIWndRealize (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963051"
---
# <a name="using-mciwnd-palettes"></a>Uso di tavolozze MCIWnd

La riproduzione di clip video con una profondità di colore a 8 bit (capacità di 256 colori) richiede una tavolozza per definire i colori utilizzati. In alcuni casi, la tavolozza inclusa in un clip video non è la tavolozza più appropriata da usare durante la riproduzione. In questo caso, MCIWnd offre tre modi per gestire le tavolozze per la riproduzione:

-   Recuperare un handle per la tavolozza associata a una finestra MCIWnd usando la macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) . La tavolozza non è necessariamente associata esclusivamente alla finestra MCIWnd. Altre applicazioni possono accedere e persino invalidare l'handle della tavolozza. Di conseguenza, l'applicazione deve prevedere l'utilizzo globale della tavolozza e, al termine della tavolozza, non dovrebbe liberarlo.
-   Specificare una nuova tavolozza da usare con il clip video associato a una finestra MCIWnd usando la macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .
-   Realizzare la tavolozza associata a una finestra MCIWnd nella tavolozza di sistema usando la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) . Questa macro chiama la funzione [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) con la tavolozza associata alla finestra MCIWnd. Se i gestori di messaggi dell'applicazione [**per \_ WM PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) chiamano solo **RealizePalette** o **MCIWndRealize**, è necessario inviare tali messaggi a MCIWnd se non vengono gestiti da soli.

> [!Note]  
> Quando un clip video con profondità di colore a 8 bit viene caricato nella finestra MCIWnd, la tavolozza inclusa con tale clip sostituisce la tavolozza associata alla finestra MCIWnd.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramenti della riproduzione](playback-enhancements.md)
</dt> </dl>

 

 