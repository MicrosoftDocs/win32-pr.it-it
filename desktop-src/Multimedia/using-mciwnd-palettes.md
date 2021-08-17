---
title: Uso dei palette MCIWnd
description: Uso dei palette MCIWnd
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- Macro MCIWndGetPalette
- Macro MCIWndSetPalette
- Macro MCIWndRealize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074dece2c1dac95e24a465413cae686acea5a8e9055913bfb832341efdb12c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801120"
---
# <a name="using-mciwnd-palettes"></a>Uso dei palette MCIWnd

La riproduzione di clip video con profondità di colore a 8 bit (capacità di 256 colori) richiede una tavolozza per definire i colori usati. In alcuni casi, la tavolozza inclusa in un clip video non è la tavolozza più appropriata da usare durante la riproduzione. In questo caso, MCIWnd offre tre modi per gestire i palette per la riproduzione:

-   Recuperare un handle per il riquadro associato a una finestra MCIWnd usando la macro [**MCIWndGetPalette.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) Il riquadro non è necessariamente associato esclusivamente alla finestra MCIWnd. Altre applicazioni possono accedere e persino invalidare l'handle del riquadro. Di conseguenza, l'applicazione deve prevedere l'uso globale della tavolozza e, al termine, non deve liberarla.
-   Specificare una nuova tavolozza da usare con il clip video associato a una finestra MCIWnd usando la macro [**MCIWndSetPalette.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
-   Rendere la tavolozza associata a una finestra MCIWnd al riquadro di sistema usando la macro [**MCIWndRealize.**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) Questa macro chiama la [**funzione RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) con la tavolozza associata alla finestra MCIWnd. Se i gestori di messaggi dell'applicazione per [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) chiamano solo **RealizePalette** o **MCIWndRealize,** è necessario inoltrare questi messaggi a MCIWnd se non vengono gestiti manualmente.

> [!Note]  
> Quando un clip video con profondità di colore a 8 bit viene caricato nella finestra MCIWnd, la tavolozza inclusa in tale clip sostituisce la tavolozza associata alla finestra MCIWnd.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramenti della riproduzione](playback-enhancements.md)
</dt> </dl>

 

 