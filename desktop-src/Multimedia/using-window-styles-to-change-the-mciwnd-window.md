---
title: Uso degli stili della finestra per modificare la finestra MCIWnd
description: Uso degli stili della finestra per modificare la finestra MCIWnd
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- MCIWndCreate (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299672"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a><span data-ttu-id="13b6b-104">Uso degli stili della finestra per modificare la finestra MCIWnd</span><span class="sxs-lookup"><span data-stu-id="13b6b-104">Using Window Styles to Change the MCIWnd Window</span></span>

<span data-ttu-id="13b6b-105">Come con qualsiasi finestra, è possibile modificare l'aspetto e il comportamento di una finestra MCIWnd scegliendo tra gli stili standard della finestra specificati con la funzione [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="13b6b-105">As with any window, you can change the appearance and behavior of an MCIWnd window by choosing from the standard window styles specified with the [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="13b6b-106">Inoltre, è possibile scegliere tra diversi altri stili di finestra specifici per le finestre di MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="13b6b-106">In addition, you can choose from several other window styles that are specific to MCIWnd windows.</span></span> <span data-ttu-id="13b6b-107">Con questi stili, l'applicazione può modificare le finestre MCIWnd nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="13b6b-107">With these styles, your application can change these MCIWnd windows in the following ways:</span></span>

-   <span data-ttu-id="13b6b-108">Modificare le dimensioni della finestra.</span><span class="sxs-lookup"><span data-stu-id="13b6b-108">Change window size.</span></span>
-   <span data-ttu-id="13b6b-109">Nascondere o visualizzare i controlli.</span><span class="sxs-lookup"><span data-stu-id="13b6b-109">Hide or display controls.</span></span>
-   <span data-ttu-id="13b6b-110">Invia messaggi di notifica.</span><span class="sxs-lookup"><span data-stu-id="13b6b-110">Issue notification messages.</span></span>
-   <span data-ttu-id="13b6b-111">Visualizzare le informazioni nella barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="13b6b-111">Display information in the title bar.</span></span>

<span data-ttu-id="13b6b-112">Per impostare gli stili della finestra, è possibile specificarli nella funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) oppure usare la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) per modificare lo stile di una finestra di MCIWnd esistente.</span><span class="sxs-lookup"><span data-stu-id="13b6b-112">You can set window styles by specifying them in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function, or you can use the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro to change the style of an existing MCIWnd window.</span></span> <span data-ttu-id="13b6b-113">È anche possibile eseguire una query su una finestra MCIWnd per gli stili correnti usando la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .</span><span class="sxs-lookup"><span data-stu-id="13b6b-113">You can also query an MCIWnd window for its current styles by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>

<span data-ttu-id="13b6b-114">Per un elenco degli stili della finestra specifici di MCIWnd, vedere [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="13b6b-114">For a list of the MCIWnd-specific window styles, see [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span>

 

 