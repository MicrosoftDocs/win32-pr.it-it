---
description: Le tavolozze dei mezzitoni devono essere usate ogni volta che la modalità di estensione di un contesto di dispositivo è impostata su HALFTONE.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Tavolozza dei mezzitoni e regolazione del colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be13f780dc5496173ffb4ddb990a96f7dbe462223e41e8a48d4a58329451277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761005"
---
# <a name="halftone-palette-and-color-adjustment"></a>Tavolozza dei mezzitoni e regolazione del colore

Le tavolozze dei mezzitoni devono essere usate ogni volta che la modalità di estensione di un contesto di dispositivo è impostata su HALFTONE. Un'applicazione crea una tavolozza dei mezzitoni usando la [**funzione CreateHalftonePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) L'applicazione deve selezionare e realizzare questo riquadro nel contesto di dispositivo prima di chiamare la [**funzione StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) [**o StretchDIBits.**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

Il sistema regola automaticamente il colore di input delle bitmap di origine ogni volta che le applicazioni chiamano le funzioni [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) e [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) e la modalità di estensione di un contesto di dispositivo è impostata su HALFTONE. Queste regolazioni del colore influiscono su determinati attributi dell'immagine, ad esempio il contrasto e la luminosità. Un'applicazione può impostare i valori di regolazione del colore usando la [**funzione SetColorAdjustment.**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) L'applicazione può recuperare i valori di regolazione del colore per il contesto di dispositivo specificato usando la [**funzione GetColorAdjustment.**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment)

 

 



