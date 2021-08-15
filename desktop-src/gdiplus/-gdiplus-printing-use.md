---
description: Con alcune piccole modifiche al codice, è possibile inviare l Windows GDI+ output a una stampante anziché a uno schermo.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Stampa (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f5807c976ef3224bc4b66afc0bb8637d79d725f12cbdebd3199d9710ae529a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885082"
---
# <a name="printing-gdi"></a>Stampa (GDI+)

Con alcune piccole modifiche al codice, è possibile inviare l Windows GDI+ output a una stampante anziché a uno schermo. Per disegnare su una stampante, ottenere un handle del contesto di dispositivo per la stampante e passare tale handle a un [**costruttore Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Inserire i GDI+ di disegno tra le chiamate [a StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) [ed EndDoc.](/windows/win32/api/wingdi/nf-wingdi-enddoc)

Gli argomenti seguenti descrivono l'GDI+'output alle stampanti in modo più dettagliato:

-   [Invio di un output GDI+ a una stampante](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Visualizzazione di una finestra di dialogo Stampa](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Ottimizzazione della stampa fornendo un handle di stampante](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



