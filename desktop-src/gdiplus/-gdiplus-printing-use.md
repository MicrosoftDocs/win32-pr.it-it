---
description: Con alcune modifiche minime al codice, è possibile inviare l'output di Windows GDI+ a una stampante anziché a una schermata.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Stampa (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b60010bcb63c553a96c5d70826f3fe0d3d4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978954"
---
# <a name="printing-gdi"></a>Stampa (GDI+)

Con alcune modifiche minime al codice, è possibile inviare l'output di Windows GDI+ a una stampante anziché a una schermata. Per creare una stampante, ottenere un handle del contesto di dispositivo per la stampante e passare tale handle a un costruttore di [**grafica**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Inserire i comandi di disegno GDI+ tra le chiamate a [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) e [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).

Gli argomenti seguenti illustrano l'invio di output GDI+ alle stampanti in modo più dettagliato:

-   [Invio di un output GDI+ a una stampante](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Visualizzazione di una finestra di dialogo Stampa](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Ottimizzazione della stampa fornendo un handle di stampante](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



