---
description: Il sistema gestisce automaticamente il disegno in un contesto di dispositivo (DC) che si estende su più di un monitor, anche quando i monitoraggi hanno profondità dei colori differenti.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Disegno su più monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754343"
---
# <a name="painting-on-multiple-display-monitors"></a><span data-ttu-id="626ab-103">Disegno su più monitor di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="626ab-103">Painting on Multiple Display Monitors</span></span>

<span data-ttu-id="626ab-104">Il sistema gestisce automaticamente il disegno in un contesto di dispositivo (DC) che si estende su più di un monitor, anche quando i monitoraggi hanno profondità dei colori differenti.</span><span class="sxs-lookup"><span data-stu-id="626ab-104">The system automatically handles painting into a device context (DC) that spans more than one monitor, even when the monitors have different color depths.</span></span> <span data-ttu-id="626ab-105">In genere, questo produce risultati ottimali, ma potrebbe non essere ottimale.</span><span class="sxs-lookup"><span data-stu-id="626ab-105">Usually this produces good results, but it may not be optimal.</span></span> <span data-ttu-id="626ab-106">Ad esempio, una finestra su due monitoraggi di profondità dei colori notevolmente diverse potrebbe avere una resa dei colori scadente.</span><span class="sxs-lookup"><span data-stu-id="626ab-106">For example, a window on two monitors of vastly different color depths could have poor color rendition.</span></span> <span data-ttu-id="626ab-107">Inoltre, i monitoraggi con la stessa profondità di colore possono avere un esempio di colore systemper diverso, i colori possono essere codificati con numeri di bit diversi o essere posizionati in posizioni diverse nel valore di colore di un pixel.</span><span class="sxs-lookup"><span data-stu-id="626ab-107">Also, monitors with the same color depth may have different color formatsfor example, colors could be encoded with different numbers of bits, or be located in different places in a pixel's color value.</span></span>

<span data-ttu-id="626ab-108">Per ottenere risultati ottimali per ognuno dei monitoraggi in un controller di dominio che si estende su più di una visualizzazione, chiamare [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) per enumerare i monitoraggi che intersecano il controller di dominio e disegnare l'area di intersezione in ognuno di essi separatamente in base agli attributi di visualizzazione per il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="626ab-108">To get the best results for each of the monitors in a DC that spans more than one display, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) to enumerate the monitors that intersect your DC and paint the intersecting area in each of them separately according to the display attributes for that monitor.</span></span> <span data-ttu-id="626ab-109">Vedere l'esempio in [disegnare in un controller di dominio che si estende su più schermi](painting-on-a-dc-that-spans-multiple-displays.md).</span><span class="sxs-lookup"><span data-stu-id="626ab-109">See the example in [Painting on a DC That Spans Multiple Displays](painting-on-a-dc-that-spans-multiple-displays.md).</span></span>

<span data-ttu-id="626ab-110">Se si esegue tutto il disegno nel codice di **disegno \_ WM** e se il codice **\_ di disegno WM** gestisce tutte le varie modalità video, sarà possibile inserire il codice di disegno **\_ WM** nel **MonitorEnumProc** di [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) con solo alcune modifiche.</span><span class="sxs-lookup"><span data-stu-id="626ab-110">If you do all of your drawing in your **WM\_PAINT** code and if your **WM\_PAINT** code handles all of the various video modes, then you should be able to place your **WM\_PAINT** code in the **MonitorEnumProc** of [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) with only a few modifications.</span></span>

 

 



