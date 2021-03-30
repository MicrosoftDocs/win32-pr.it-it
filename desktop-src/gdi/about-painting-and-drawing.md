---
description: Quasi tutte le applicazioni utilizzano la schermata per visualizzare i dati modificati.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: Informazioni su disegno e disegno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993861"
---
# <a name="about-painting-and-drawing"></a><span data-ttu-id="8491f-103">Informazioni su disegno e disegno</span><span class="sxs-lookup"><span data-stu-id="8491f-103">About Painting and Drawing</span></span>

<span data-ttu-id="8491f-104">Quasi tutte le applicazioni utilizzano la schermata per visualizzare i dati modificati.</span><span class="sxs-lookup"><span data-stu-id="8491f-104">Nearly all applications use the screen to display the data they manipulate.</span></span> <span data-ttu-id="8491f-105">Un'applicazione disegna immagini, disegna figure e scrive testo in modo che l'utente possa visualizzare i dati durante la creazione, la modifica e la stampa.</span><span class="sxs-lookup"><span data-stu-id="8491f-105">An application paints images, draws figures, and writes text so that the user can view data as it is created, edited, and printed.</span></span> <span data-ttu-id="8491f-106">Microsoft Windows offre un supporto avanzato per la progettazione e il disegno, ma, a causa della natura dei sistemi operativi multitasking, le applicazioni devono collaborare tra loro durante l'accesso allo schermo.</span><span class="sxs-lookup"><span data-stu-id="8491f-106">Microsoft Windows provides rich support for painting and drawing, but, because of the nature of multitasking operating systems, applications must cooperate with one another when accessing the screen.</span></span>

<span data-ttu-id="8491f-107">Per garantire il funzionamento corretto e cooperativo di tutte le applicazioni, il sistema gestisce tutti gli output sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="8491f-107">To keep all applications functioning smoothly and cooperatively, the system manages all output to the screen.</span></span> <span data-ttu-id="8491f-108">Le applicazioni utilizzano Windows come dispositivo di output primario anziché con la schermata stessa.</span><span class="sxs-lookup"><span data-stu-id="8491f-108">Applications use windows as their primary output device rather than the screen itself.</span></span> <span data-ttu-id="8491f-109">Il sistema consente di visualizzare i contesti di dispositivo che corrispondono in modo univoco alle finestre.</span><span class="sxs-lookup"><span data-stu-id="8491f-109">The system supplies display device contexts that uniquely correspond to the windows.</span></span> <span data-ttu-id="8491f-110">Le applicazioni usano i contesti di dispositivo di visualizzazione per indirizzare l'output alle finestre specificate.</span><span class="sxs-lookup"><span data-stu-id="8491f-110">Applications use display device contexts to direct their output to the specified windows.</span></span> <span data-ttu-id="8491f-111">Il disegno in una finestra (indirizzando l'output) impedisce a un'applicazione di interferire con l'output di altre applicazioni e consente alle applicazioni di coesistere l'uno con l'altro sfruttando al tempo stesso tutte le funzionalità grafiche del sistema.</span><span class="sxs-lookup"><span data-stu-id="8491f-111">Drawing in a window (directing output to it) prevents an application from interfering with the output of other applications and allows applications to coexist with one another while still taking full advantage of the graphics capabilities of the system.</span></span>

-   [<span data-ttu-id="8491f-112">Quando creare un oggetto in una finestra</span><span class="sxs-lookup"><span data-stu-id="8491f-112">When to Draw in a Window</span></span>](when-to-draw-in-a-window.md)
-   [<span data-ttu-id="8491f-113">Messaggio di \_ disegno WM</span><span class="sxs-lookup"><span data-stu-id="8491f-113">The WM\_PAINT Message</span></span>](the-wm-paint-message.md)
-   [<span data-ttu-id="8491f-114">Disegno senza il messaggio di disegno WM \_</span><span class="sxs-lookup"><span data-stu-id="8491f-114">Drawing Without the WM\_PAINT Message</span></span>](drawing-without-the-wm-paint-message.md)
-   [<span data-ttu-id="8491f-115">Sistema di coordinate finestra</span><span class="sxs-lookup"><span data-stu-id="8491f-115">Window Coordinate System</span></span>](window-coordinate-system.md)
-   [<span data-ttu-id="8491f-116">Aree della finestra</span><span class="sxs-lookup"><span data-stu-id="8491f-116">Window Regions</span></span>](window-regions.md)
-   [<span data-ttu-id="8491f-117">Sfondo finestra</span><span class="sxs-lookup"><span data-stu-id="8491f-117">Window Background</span></span>](window-background.md)
-   [<span data-ttu-id="8491f-118">Finestre ridotte a icona</span><span class="sxs-lookup"><span data-stu-id="8491f-118">Minimized Windows</span></span>](minimized-windows.md)
-   [<span data-ttu-id="8491f-119">Finestre ridimensionate</span><span class="sxs-lookup"><span data-stu-id="8491f-119">Resized Windows</span></span>](resized-windows.md)
-   [<span data-ttu-id="8491f-120">Area non client</span><span class="sxs-lookup"><span data-stu-id="8491f-120">Nonclient Area</span></span>](nonclient-area.md)
-   [<span data-ttu-id="8491f-121">Area di aggiornamento della finestra figlio</span><span class="sxs-lookup"><span data-stu-id="8491f-121">Child Window Update Region</span></span>](child-window-update-region.md)
-   [<span data-ttu-id="8491f-122">Dispositivi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="8491f-122">Display Devices</span></span>](display-devices.md)
-   [<span data-ttu-id="8491f-123">Blocco aggiornamento finestra</span><span class="sxs-lookup"><span data-stu-id="8491f-123">Window Update Lock</span></span>](window-update-lock.md)
-   [<span data-ttu-id="8491f-124">Rettangolo di delimitazione accumulato</span><span class="sxs-lookup"><span data-stu-id="8491f-124">Accumulated Bounding Rectangle</span></span>](accumulated-bounding-rectangle.md)

 

 



