---
description: Oltre all'area di aggiornamento, ogni finestra dispone di un'area visibile che definisce la parte della finestra visibile all'utente.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Aree della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057922"
---
# <a name="window-regions"></a><span data-ttu-id="46480-103">Aree della finestra</span><span class="sxs-lookup"><span data-stu-id="46480-103">Window Regions</span></span>

<span data-ttu-id="46480-104">Oltre all'area di aggiornamento, ogni finestra dispone di un' *area visibile* che definisce la parte della finestra visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="46480-104">In addition to the update region, every window has a *visible region* that defines the window portion visible to the user.</span></span> <span data-ttu-id="46480-105">Il sistema modifica l'area visibile per la finestra ogni volta che la finestra viene modificata o quando un'altra finestra viene spostata in modo da nascondere o esporre una parte della finestra.</span><span class="sxs-lookup"><span data-stu-id="46480-105">The system changes the visible region for the window whenever the window changes size or whenever another window is moved such that it obscures or exposes a portion of the window.</span></span> <span data-ttu-id="46480-106">Le applicazioni non possono modificare direttamente l'area visibile, ma il sistema usa automaticamente l'area visibile per creare l'area di ridimensionamento per qualsiasi contesto di periferica di visualizzazione recuperato per la finestra.</span><span class="sxs-lookup"><span data-stu-id="46480-106">Applications cannot change the visible region directly, but the system automatically uses the visible region to create the clipping region for any display device context retrieved for the window.</span></span>

<span data-ttu-id="46480-107">L' *area di visualizzazione* determina la posizione in cui il sistema consente il disegno.</span><span class="sxs-lookup"><span data-stu-id="46480-107">The *clipping region* determines where the system permits drawing.</span></span> <span data-ttu-id="46480-108">Quando l'applicazione recupera un contesto di dispositivo di visualizzazione usando la funzione [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , il sistema imposta l'area di ridimensionamento per il contesto di dispositivo sull'intersezione tra l'area visibile e l'area di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="46480-108">When the application retrieves a display device context using the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function, the system sets the clipping region for the device context to the intersection of the visible region and the update region.</span></span> <span data-ttu-id="46480-109">Le applicazioni possono modificare l'area di visualizzazione utilizzando funzioni come [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) e [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), per limitare ulteriormente il disegno a una parte specifica dell'area di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="46480-109">Applications can change the clipping region by using functions such as [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) and [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), to further limit drawing to a particular portion of the update area.</span></span>

<span data-ttu-id="46480-110">Gli \_ stili WS CLIPCHILDREN e WS \_ CLIPSIBLINGS specificano ulteriormente il modo in cui il sistema calcola l'area visibile per una finestra.</span><span class="sxs-lookup"><span data-stu-id="46480-110">The WS\_CLIPCHILDREN and WS\_CLIPSIBLINGS styles further specify how the system calculates the visible region for a window.</span></span> <span data-ttu-id="46480-111">Se una finestra ha uno o entrambi gli stili, l'area visibile esclude qualsiasi finestra figlio o Windows di pari livello (Windows con la stessa finestra padre).</span><span class="sxs-lookup"><span data-stu-id="46480-111">If a window has one or both of these styles, the visible region excludes any child window or sibling windows (windows having the same parent window).</span></span> <span data-ttu-id="46480-112">Pertanto, il disegno che altrimenti sarebbe intruso in queste finestre verrà sempre ritagliato.</span><span class="sxs-lookup"><span data-stu-id="46480-112">Therefore, drawing that would otherwise intrude in these windows will always be clipped.</span></span>

 

 



