---
description: Le tavolozze di mezzitoni sono progettate per essere usate ogni volta che la modalità di adattamento di un contesto di dispositivo è impostata su mezzitoni.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Tavolozza mezzitoni e regolazione colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528339"
---
# <a name="halftone-palette-and-color-adjustment"></a>Tavolozza mezzitoni e regolazione colore

Le tavolozze di mezzitoni sono progettate per essere usate ogni volta che la modalità di adattamento di un contesto di dispositivo è impostata su mezzitoni. Un'applicazione crea una tavolozza di mezzitoni usando la funzione [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) . L'applicazione deve selezionare e realizzare questa tavolozza nel contesto di dispositivo prima di chiamare la funzione [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) o [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .

Il sistema regola automaticamente il colore di input delle bitmap di origine ogni volta che le applicazioni chiamano le funzioni [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) e [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) e la modalità di adattamento di un contesto di dispositivo è impostata su mezzitoni. Queste regolazioni dei colori influiscono su determinati attributi dell'immagine, ad esempio contrasto e luminosità. Un'applicazione può impostare i valori di regolazione del colore tramite la funzione [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) . L'applicazione può recuperare i valori di regolazione del colore per il contesto di dispositivo specificato tramite la funzione [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .

 

 



