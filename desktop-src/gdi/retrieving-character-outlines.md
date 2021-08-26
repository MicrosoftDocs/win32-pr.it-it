---
description: È possibile usare la funzione GetGlyphOutline per recuperare la struttura di un glifo da un tipo di carattere TrueType.
ms.assetid: 9b255dfa-3c1d-4707-927d-a2d5f4117f6a
title: Recupero di contorni di caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3db9b9200f665088096fdecbffc12866668d093c0c4d5ddb4a1612153873e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092651"
---
# <a name="retrieving-character-outlines"></a>Recupero di contorni di caratteri

È possibile usare la [funzione GetGlyphOutline](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea) per recuperare la struttura di un glifo da un tipo di carattere TrueType. Il contorno del glifo restituito dalla [**funzione GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) è per un glifo con griglia. Un glifo montato sulla griglia è stato modificato in modo che l'immagine bitmap sia il più possibile conforme alla progettazione originale del glifo. Se l'applicazione richiede un contorno glifo non modificato, richiedere il contorno del glifo per un carattere in un tipo di carattere le cui dimensioni sono uguali alle unità em del tipo di carattere. Per creare un tipo di carattere con queste dimensioni, impostare il membro **lfHeight** della struttura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) sul valore negativo del valore del membro **ntmSizeEM** della struttura [NEWTEXTMETRIC.](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)

[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) restituisce il contorno come bitmap o come una serie di polilinee e spline. Quando un'applicazione recupera un contorno del glifo come una serie di polilinee e spline, le informazioni vengono restituite in una struttura [TTPOLYGONHEADER](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) seguita da tutte le strutture [TTPOLYCURVE](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) necessarie per descrivere il glifo. Tutti i punti vengono restituiti [come strutture POINTFX](/windows/win32/api/wingdi/ns-wingdi-pointfx) e rappresentano le posizioni assolute, non gli spostamenti relativi. Il punto iniziale specificato dal **membro pfxStart** della struttura [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) è il punto in cui inizia la struttura per un contorno. Le [**strutture TTPOLYCURVE**](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) che seguono possono essere record polilinea o record spline.

Per eseguire il rendering di un contorno di caratteri TrueType, è necessario usare sia la polilinea che i record spline. Il sistema può eseguire facilmente il rendering di polilinee e spline. Ogni record di polilinea e spline contiene il maggior numero possibile di punti sequenziali, per ridurre al minimo il numero di record restituiti.

Il punto iniziale specificato nella [**struttura TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) è sempre sulla struttura del glifo. Il punto specificato funge da punto iniziale e finale per il contorno.

In questa sezione vengono fornite informazioni sugli argomenti seguenti.

-   [Record di polilinea](polyline-records.md)
-   [Record spline](spline-records.md)

 

 
