---
title: Uso di controlli TrackBar
description: In questa sezione vengono forniti dettagli ed esempi di implementazione per i controlli TrackBar.
ms.assetid: 28078f3e-a3d1-4bb5-96c6-2191ff9f8d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d667a495dce918bdcfcf0391638eef8a3c6e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710021"
---
# <a name="using-trackbar-controls"></a><span data-ttu-id="c6030-103">Uso di controlli TrackBar</span><span class="sxs-lookup"><span data-stu-id="c6030-103">Using Trackbar Controls</span></span>

<span data-ttu-id="c6030-104">In questa sezione vengono forniti dettagli ed esempi di implementazione per i controlli TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c6030-104">This section provides implementation details and examples for Trackbar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c6030-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c6030-105">In this section</span></span>



| <span data-ttu-id="c6030-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="c6030-106">Topic</span></span>                                                                                                  | <span data-ttu-id="c6030-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6030-107">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6030-108">Come creare un TrackBar</span><span class="sxs-lookup"><span data-stu-id="c6030-108">How to Create a Trackbar</span></span>](create-a-trackbar.md)<br/>                                           | <span data-ttu-id="c6030-109">Quando viene creato il TrackBar, viene inizializzato sia l'intervallo che l'intervallo di selezione.</span><span class="sxs-lookup"><span data-stu-id="c6030-109">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="c6030-110">Anche le dimensioni della pagina sono impostate in questo momento.</span><span class="sxs-lookup"><span data-stu-id="c6030-110">The page size is also set at this time.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="c6030-111">Come elaborare i messaggi di notifica TrackBar</span><span class="sxs-lookup"><span data-stu-id="c6030-111">How to Process Trackbar Notification Messages</span></span>](process-trackbar-notification-messages.md)<br/> | <span data-ttu-id="c6030-112">I TrackBar inviano notifiche alla finestra padre delle azioni dell'utente inviando il messaggio padre a [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="c6030-112">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="c6030-113">Come limitare lo spostamento del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="c6030-113">How to Limit Slider Movement</span></span>](limit-slider-movement.md)<br/>                                   | <span data-ttu-id="c6030-114">Come descritto in [informazioni sui controlli TrackBar](trackbar-controls.md), è possibile impostare parte dell'intervallo TrackBar come intervallo di selezione.</span><span class="sxs-lookup"><span data-stu-id="c6030-114">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="c6030-115">Uno degli scopi di un intervallo di selezione potrebbe essere quello di limitare lo spostamento del dispositivo di scorrimento, facendo in modo che alcune parti dell'intervallo completo non superino i limiti.</span><span class="sxs-lookup"><span data-stu-id="c6030-115">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span> <br/> |
| [<span data-ttu-id="c6030-116">Come usare le finestre di Buddy</span><span class="sxs-lookup"><span data-stu-id="c6030-116">How to Use Buddy Windows</span></span>](use-buddy-windows.md)<br/>                                           | <span data-ttu-id="c6030-117">Impostando altri controlli come finestre Buddy per un TrackBar, è possibile posizionare automaticamente tali controlli alle estremità del TrackBar come etichette.</span><span class="sxs-lookup"><span data-stu-id="c6030-117">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span><br/>                                                                                                                          |



 

 

 





