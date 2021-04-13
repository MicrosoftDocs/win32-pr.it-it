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
# <a name="printing-gdi"></a><span data-ttu-id="01b2e-103">Stampa (GDI+)</span><span class="sxs-lookup"><span data-stu-id="01b2e-103">Printing (GDI+)</span></span>

<span data-ttu-id="01b2e-104">Con alcune modifiche minime al codice, è possibile inviare l'output di Windows GDI+ a una stampante anziché a una schermata.</span><span class="sxs-lookup"><span data-stu-id="01b2e-104">With a few minor adjustments to your code, you can send Windows GDI+ output to a printer rather than to a screen.</span></span> <span data-ttu-id="01b2e-105">Per creare una stampante, ottenere un handle del contesto di dispositivo per la stampante e passare tale handle a un costruttore di [**grafica**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="01b2e-105">To draw on a printer, obtain a device context handle for the printer and pass that handle to a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="01b2e-106">Inserire i comandi di disegno GDI+ tra le chiamate a [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) e [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="01b2e-106">Place your GDI+ drawing commands in between calls to [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="01b2e-107">Gli argomenti seguenti illustrano l'invio di output GDI+ alle stampanti in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="01b2e-107">The following topics cover sending GDI+ output to printers in more detail:</span></span>

-   [<span data-ttu-id="01b2e-108">Invio di un output GDI+ a una stampante</span><span class="sxs-lookup"><span data-stu-id="01b2e-108">Sending GDI+ Output to a Printer</span></span>](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [<span data-ttu-id="01b2e-109">Visualizzazione di una finestra di dialogo Stampa</span><span class="sxs-lookup"><span data-stu-id="01b2e-109">Displaying a Print Dialog Box</span></span>](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [<span data-ttu-id="01b2e-110">Ottimizzazione della stampa fornendo un handle di stampante</span><span class="sxs-lookup"><span data-stu-id="01b2e-110">Optimizing Printing by Providing a Printer Handle</span></span>](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



