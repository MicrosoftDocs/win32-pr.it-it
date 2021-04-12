---
title: Fornire aggiornamenti sullo stato
description: Fornire aggiornamenti sullo stato
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- MCIWndSetActiveTimer (macro)
- MCIWndSetInactiveTimer (macro)
- MCIWndGetActiveTimer (macro)
- MCIWndGetInactiveTimer (macro)
- MCIWndSetTimers (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395826"
---
# <a name="providing-status-updates"></a><span data-ttu-id="9df46-108">Fornire aggiornamenti sullo stato</span><span class="sxs-lookup"><span data-stu-id="9df46-108">Providing Status Updates</span></span>

<span data-ttu-id="9df46-109">MCIWnd usa i timer per aggiornare periodicamente le informazioni nella barra del titolo della finestra e nella barra di scorrimento e per inviare messaggi di notifica alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="9df46-109">MCIWnd uses timers to periodically update information in the window title bar and scroll bar, and to send notification messages to the parent window.</span></span> <span data-ttu-id="9df46-110">Un timer controlla il periodo di aggiornamento della finestra MCIWnd attiva e un secondo timer controlla il periodo di aggiornamento per le finestre MCIWnd che sono inattive.</span><span class="sxs-lookup"><span data-stu-id="9df46-110">One timer controls the update period of the active MCIWnd window, and a second timer controls the update period for MCIWnd windows that are inactive.</span></span> <span data-ttu-id="9df46-111">L'applicazione può utilizzare le macro del timer MCIWnd per recuperare le impostazioni correnti del timer e per modificare i periodi di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="9df46-111">Your application can use the MCIWnd timer macros to retrieve the current timer settings and to adjust the update periods.</span></span>

<span data-ttu-id="9df46-112">È possibile impostare il periodo di aggiornamento utilizzato dal timer della finestra attiva utilizzando la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="9df46-112">You can set the update period used by the active window timer by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span> <span data-ttu-id="9df46-113">Questa macro imposta il periodo usato da MCIWnd per aggiornare il controllo TrackBar, per aggiornare la posizione di riproduzione indicata nella barra del titolo della finestra e per notificare alla finestra padre che il supporto è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="9df46-113">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window title bar, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="9df46-114">È possibile recuperare il periodo di aggiornamento corrente utilizzato dal timer della finestra attiva utilizzando la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="9df46-114">You can retrieve the current update period used by the active window timer by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span> <span data-ttu-id="9df46-115">Il periodo di aggiornamento predefinito per il timer della finestra attiva è pari a 500 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="9df46-115">The default update period for the active window timer is 500 milliseconds.</span></span>

<span data-ttu-id="9df46-116">È possibile impostare il periodo di aggiornamento utilizzato dal timer della finestra inattiva utilizzando la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="9df46-116">You can set the update period used by the inactive window timer by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span> <span data-ttu-id="9df46-117">Questa macro imposta il periodo usato da MCIWnd per aggiornare il controllo TrackBar, per aggiornare la posizione di riproduzione indicata nella didascalia della finestra e per notificare alla finestra padre che il supporto è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="9df46-117">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window caption, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="9df46-118">È possibile recuperare il periodo di aggiornamento corrente utilizzato dal timer della finestra inattiva utilizzando la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="9df46-118">You can retrieve the current update period used by the inactive window timer by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span> <span data-ttu-id="9df46-119">Il periodo di aggiornamento predefinito per il timer della finestra inattiva è pari a 2000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="9df46-119">The default update period for the inactive window timer is 2000 milliseconds.</span></span>

<span data-ttu-id="9df46-120">L'applicazione può impostare contemporaneamente il periodo di aggiornamento per entrambi i timer usando la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .</span><span class="sxs-lookup"><span data-stu-id="9df46-120">Your application can simultaneously set the update period for both timers by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span> <span data-ttu-id="9df46-121">Lo spazio di archiviazione per il valore del periodo di aggiornamento è limitato a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="9df46-121">The storage for the value of the update period is limited to 16 bits.</span></span> <span data-ttu-id="9df46-122">Se è necessaria una quantità maggiore per uno dei due periodi di aggiornamento, impostare i timer singolarmente.</span><span class="sxs-lookup"><span data-stu-id="9df46-122">If a larger quantity for either update period is needed, set the timers individually.</span></span>

 

 




