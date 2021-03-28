---
description: Prima di disegnare, il sistema deve preparare il dispositivo di visualizzazione per le operazioni di disegno.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Dispositivi di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978658"
---
# <a name="display-devices"></a><span data-ttu-id="3e962-103">Dispositivi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="3e962-103">Display Devices</span></span>

<span data-ttu-id="3e962-104">Prima di disegnare, il sistema deve preparare il dispositivo di visualizzazione per le operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="3e962-104">Before painting, the system must prepare the display device for drawing operations.</span></span> <span data-ttu-id="3e962-105">Un contesto di dispositivo di visualizzazione definisce un set di oggetti grafici e i relativi attributi associati, nonché le modalità grafiche che interessano l'output.</span><span class="sxs-lookup"><span data-stu-id="3e962-105">A display device context defines a set of graphic objects and their associated attributes, and the graphic modes that affect output.</span></span> <span data-ttu-id="3e962-106">Il sistema prepara ogni contesto di dispositivo di visualizzazione per l'output in una finestra, impostando gli oggetti, i colori e le modalità di disegno per la finestra anziché il dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3e962-106">The system prepares each display device context for output to a window, setting the drawing objects, colors, and modes for the window instead of the display device.</span></span> <span data-ttu-id="3e962-107">Quando l'applicazione fornisce il contesto del dispositivo di visualizzazione tramite le chiamate alle funzioni GDI, GDI USA le informazioni nel contesto per generare l'output nella finestra specificata senza intrusioni in altre finestre o altre parti dello schermo.</span><span class="sxs-lookup"><span data-stu-id="3e962-107">When the application supplies the display device context through calls to GDI functions, GDI uses the information in the context to generate output in the specified window without intruding on other windows or other parts of the screen.</span></span>

<span data-ttu-id="3e962-108">Il sistema offre cinque tipi di contesti di dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3e962-108">The system provides five kinds of display device contexts.</span></span>



| <span data-ttu-id="3e962-109">Type</span><span class="sxs-lookup"><span data-stu-id="3e962-109">Type</span></span>                                           | <span data-ttu-id="3e962-110">Significato</span><span class="sxs-lookup"><span data-stu-id="3e962-110">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e962-111">comune</span><span class="sxs-lookup"><span data-stu-id="3e962-111">common</span></span>](common-display-device-contexts.md)   | <span data-ttu-id="3e962-112">Consente il disegno nell'area client di una finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="3e962-112">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="3e962-113">class</span><span class="sxs-lookup"><span data-stu-id="3e962-113">class</span></span>](class-display-device-contexts.md)     | <span data-ttu-id="3e962-114">Consente il disegno nell'area client di una finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="3e962-114">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="3e962-115">parent</span><span class="sxs-lookup"><span data-stu-id="3e962-115">parent</span></span>](parent-display-device-contexts.md)   | <span data-ttu-id="3e962-116">Consente di disegnare in un punto qualsiasi della finestra.</span><span class="sxs-lookup"><span data-stu-id="3e962-116">Permits drawing anywhere in the window.</span></span> <span data-ttu-id="3e962-117">Sebbene il contesto di dispositivo padre consenta anche il disegno nella finestra padre, non è destinato a essere utilizzato in questo modo.</span><span class="sxs-lookup"><span data-stu-id="3e962-117">Although the parent device context also permits drawing in the parent window, it is not intended to be used in this way.</span></span> |
| [<span data-ttu-id="3e962-118">privata</span><span class="sxs-lookup"><span data-stu-id="3e962-118">private</span></span>](private-display-device-contexts.md) | <span data-ttu-id="3e962-119">Consente il disegno nell'area client di una finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="3e962-119">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="3e962-120">finestra</span><span class="sxs-lookup"><span data-stu-id="3e962-120">window</span></span>](window-display-device-contexts.md)   | <span data-ttu-id="3e962-121">Consente di disegnare in un punto qualsiasi della finestra.</span><span class="sxs-lookup"><span data-stu-id="3e962-121">Permits drawing anywhere in the window.</span></span>                                                                                                                          |



 

<span data-ttu-id="3e962-122">Il sistema fornisce un contesto di dispositivo comune, di classe, padre o privato a una finestra in base al tipo di contesto del dispositivo di visualizzazione specificato nello stile della classe di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="3e962-122">The system supplies a common, class, parent, or private device context to a window based on the type of display device context specified in that window's class style.</span></span> <span data-ttu-id="3e962-123">Il sistema fornisce un contesto di dispositivo finestra solo quando l'applicazione ne richiede esplicitamente uno, ad esempio chiamando la funzione [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) .</span><span class="sxs-lookup"><span data-stu-id="3e962-123">The system supplies a window device context only when the application explicitly requests one for example, by calling the [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function.</span></span> <span data-ttu-id="3e962-124">In tutti i casi, un'applicazione può usare la funzione [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) per determinare la finestra attualmente rappresentata da un controller di dominio di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3e962-124">In all cases, an application can use the [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) function to determine which window a display DC currently represents.</span></span>

<span data-ttu-id="3e962-125">In questa sezione vengono fornite informazioni sui seguenti argomenti.</span><span class="sxs-lookup"><span data-stu-id="3e962-125">This section provides information on the following topics.</span></span>

-   [<span data-ttu-id="3e962-126">Visualizza la cache del contesto del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3e962-126">Display Device Context Cache</span></span>](display-device-context-cache.md)
-   [<span data-ttu-id="3e962-127">Visualizzare le impostazioni predefinite del contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="3e962-127">Display Device Context Defaults</span></span>](display-device-context-defaults.md)
-   [<span data-ttu-id="3e962-128">Contesti di dispositivo di visualizzazione comuni</span><span class="sxs-lookup"><span data-stu-id="3e962-128">Common Display Device Contexts</span></span>](common-display-device-contexts.md)
-   [<span data-ttu-id="3e962-129">Contesti di dispositivo di visualizzazione privati</span><span class="sxs-lookup"><span data-stu-id="3e962-129">Private Display Device Contexts</span></span>](private-display-device-contexts.md)
-   [<span data-ttu-id="3e962-130">Contesti dispositivo di visualizzazione padre</span><span class="sxs-lookup"><span data-stu-id="3e962-130">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)
-   [<span data-ttu-id="3e962-131">Classe Visualizza contesti di dispositivo</span><span class="sxs-lookup"><span data-stu-id="3e962-131">Class Display Device Contexts</span></span>](class-display-device-contexts.md)
-   [<span data-ttu-id="3e962-132">Visualizzazione dei contesti di dispositivo della finestra</span><span class="sxs-lookup"><span data-stu-id="3e962-132">Window Display Device Contexts</span></span>](window-display-device-contexts.md)
-   [<span data-ttu-id="3e962-133">Contesti dispositivo di visualizzazione padre</span><span class="sxs-lookup"><span data-stu-id="3e962-133">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)

 

 



