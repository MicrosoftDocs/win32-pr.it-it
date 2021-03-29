---
description: È possibile utilizzare il \_ messaggio di disegno WM per eseguire il disegno necessario per la visualizzazione delle informazioni.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Uso del messaggio WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77246e04effc74de8158aef9bfc4aaf27471c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227140"
---
# <a name="using-the-wm_paint-message"></a><span data-ttu-id="5b0ef-103">Uso del \_ messaggio di disegno WM</span><span class="sxs-lookup"><span data-stu-id="5b0ef-103">Using the WM\_PAINT Message</span></span>

<span data-ttu-id="5b0ef-104">È possibile utilizzare il [**messaggio \_ di disegno WM**](wm-paint.md) per eseguire il disegno necessario per la visualizzazione delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="5b0ef-104">You can use the [**WM\_PAINT**](wm-paint.md) message to carry out the drawing necessary for displaying information.</span></span> <span data-ttu-id="5b0ef-105">Poiché il sistema invia \_ messaggi di disegno WM all'applicazione quando è necessario aggiornare la finestra o quando si richiede in modo esplicito un aggiornamento, è possibile consolidare il codice per il disegno nella routine della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5b0ef-105">Because the system sends WM\_PAINT messages to your application when your window must be updated or when you explicitly request an update, you can consolidate the code for drawing in your application's window procedure.</span></span> <span data-ttu-id="5b0ef-106">È quindi possibile usare questo codice ogni volta che l'applicazione deve creare informazioni nuove o esistenti.</span><span class="sxs-lookup"><span data-stu-id="5b0ef-106">You can then use this code whenever your application must draw either new or existing information.</span></span>

<span data-ttu-id="5b0ef-107">Le sezioni seguenti illustrano diversi modi per usare il \_ messaggio di disegno WM per disegnare in una finestra:</span><span class="sxs-lookup"><span data-stu-id="5b0ef-107">The following sections show a variety of ways to use the WM\_PAINT message to draw in a window:</span></span>

-   [<span data-ttu-id="5b0ef-108">Disegno nell'area client</span><span class="sxs-lookup"><span data-stu-id="5b0ef-108">Drawing in the Client Area</span></span>](drawing-in-the-client-area.md)
-   [<span data-ttu-id="5b0ef-109">Ridisegno dell'intera area client</span><span class="sxs-lookup"><span data-stu-id="5b0ef-109">Redrawing the Entire Client Area</span></span>](redrawing-the-entire-client-area.md)
-   [<span data-ttu-id="5b0ef-110">Ridisegno nell'area di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5b0ef-110">Redrawing in the Update Region</span></span>](redrawing-in-the-update-region.md)
-   [<span data-ttu-id="5b0ef-111">Invalidare l'area client</span><span class="sxs-lookup"><span data-stu-id="5b0ef-111">Invalidating the Client Area</span></span>](invalidating-the-client-area.md)
-   [<span data-ttu-id="5b0ef-112">Disegno di una finestra ridotta a icona</span><span class="sxs-lookup"><span data-stu-id="5b0ef-112">Drawing a Minimized Window</span></span>](drawing-a-minimized-window.md)
-   [<span data-ttu-id="5b0ef-113">Disegno di uno sfondo personalizzato della finestra</span><span class="sxs-lookup"><span data-stu-id="5b0ef-113">Drawing a Custom Window Background</span></span>](drawing-a-custom-window-background.md)

 

 



