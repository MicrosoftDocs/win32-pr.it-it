---
description: È possibile utilizzare la funzione GetGlyphOutline per recuperare il contorno di un glifo da un tipo di carattere TrueType.
ms.assetid: 9b255dfa-3c1d-4707-927d-a2d5f4117f6a
title: Recupero di strutture di caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638193632d4992dfb53f29a3dfe66a858b3e1fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978314"
---
# <a name="retrieving-character-outlines"></a>Recupero di strutture di caratteri

È possibile utilizzare la funzione [GetGlyphOutline](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea) per recuperare il contorno di un glifo da un tipo di carattere TrueType. Il contorno del glifo restituito dalla funzione [**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) è per un glifo dotato di griglia. Un glifo fornito da griglia è stato modificato in modo che l'immagine bitmap sia conforme al più vicino possibile alla progettazione originale del glifo. Se l'applicazione richiede un contorno di glifo non modificato, richiedere il contorno del glifo per un carattere in un tipo di carattere la cui dimensione è uguale alle unità em del tipo di carattere. Per creare un tipo di carattere con questa dimensione, impostare il membro **lfHeight** della struttura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) sul valore negativo del membro **ntmSizeEM** della struttura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .

[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) restituisce il contorno come bitmap o come una serie di polilinee e spline. Quando un'applicazione recupera un contorno di glifo come una serie di polilinee e spline, le informazioni vengono restituite in una struttura [TTPOLYGONHEADER](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) seguita da tutte le strutture [TTPOLYCURVE](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) necessarie per descrivere il glifo. Tutti i punti vengono restituiti come strutture [POINTFX](/windows/win32/api/wingdi/ns-wingdi-pointfx) e rappresentano posizioni assolute, non spostamenti relativi. Il punto iniziale specificato dal membro **pfxStart** della struttura [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) è il punto in cui inizia il contorno di un contorno. Le strutture [**TTPOLYCURVE**](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) che seguono possono essere record polilinea o record spline.

Per eseguire il rendering di una struttura di caratteri TrueType, è necessario usare sia la polilinea che i record spline. Il sistema è in grado di eseguire facilmente le polilinee e le spline. Ogni record di polilinea e spline contiene il maggior numero possibile di punti sequenziali, per ridurre al minimo il numero di record restituiti.

Il punto iniziale specificato nella struttura [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) è sempre sul contorno dell'icona. Il punto specificato funge da punto iniziale e finale per il contorno.

In questa sezione vengono fornite informazioni sui seguenti argomenti.

-   [Record polilinea](polyline-records.md)
-   [Record spline](spline-records.md)

 

 
