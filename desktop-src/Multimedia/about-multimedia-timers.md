---
title: Informazioni sui timer multimediali
description: Informazioni sui timer multimediali
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows Multimedia, timer
- Multimedia, timer
- input multimediale, timer
- timer multimediali, informazioni
- timer, informazioni
- timer multimediali, eventi di pianificazione
- timer, eventi di pianificazione
- pianificazione degli eventi del timer
- temporizzazione ad alta risoluzione
- Funzione setimer
- CreateWaitableTimer (funzione)
- Messaggi di WM_TIMER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046681"
---
# <a name="about-multimedia-timers"></a><span data-ttu-id="2eebb-115">Informazioni sui timer multimediali</span><span class="sxs-lookup"><span data-stu-id="2eebb-115">About Multimedia Timers</span></span>

<span data-ttu-id="2eebb-116">I servizi timer multimediali consentono alle applicazioni di pianificare gli eventi del timer con la massima risoluzione (o accuratezza) possibile per la piattaforma hardware.</span><span class="sxs-lookup"><span data-stu-id="2eebb-116">Multimedia timer services allow applications to schedule timer events with the greatest resolution (or accuracy) possible for the hardware platform.</span></span> <span data-ttu-id="2eebb-117">Questi servizi timer multimediali consentono di pianificare gli eventi del timer a una risoluzione superiore rispetto ad altri servizi timer.</span><span class="sxs-lookup"><span data-stu-id="2eebb-117">These multimedia timer services allow you to schedule timer events at a higher resolution than other timer services.</span></span>

<span data-ttu-id="2eebb-118">Questi servizi timer sono utili per le applicazioni che richiedono tempi di risoluzione elevata.</span><span class="sxs-lookup"><span data-stu-id="2eebb-118">These timer services are useful for applications that demand high-resolution timing.</span></span> <span data-ttu-id="2eebb-119">Ad esempio, un sequencer MIDI richiede un timer ad alta risoluzione, perché deve mantenere la velocità degli eventi MIDI entro una risoluzione di 1 millisecondo.</span><span class="sxs-lookup"><span data-stu-id="2eebb-119">For example, a MIDI sequencer requires a high-resolution timer because it must maintain the pace of MIDI events within a resolution of 1 millisecond.</span></span>

<span data-ttu-id="2eebb-120">Le applicazioni che non usano la temporizzazione ad alta risoluzione devono usare la funzione [setimer](/windows/win32/api/winuser/nf-winuser-settimer) anziché i servizi timer multimediali.</span><span class="sxs-lookup"><span data-stu-id="2eebb-120">Applications that do not use high-resolution timing should use the [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) function instead of multimedia timer services.</span></span> <span data-ttu-id="2eebb-121">I servizi timer forniti da **setimer** inviano messaggi del [ \_ timer WM](../winmsg/wm-timer.md) a una coda di messaggi, mentre i servizi timer multimediali chiamano una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="2eebb-121">The timer services provided by **SetTimer** post [WM\_TIMER](../winmsg/wm-timer.md) messages to a message queue, while the multimedia timer services call a callback function.</span></span> <span data-ttu-id="2eebb-122">Le applicazioni che vogliono un timer in attesa devono usare la funzione [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) .</span><span class="sxs-lookup"><span data-stu-id="2eebb-122">Applications that want a waitable timer should use the [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) function.</span></span>

 

 