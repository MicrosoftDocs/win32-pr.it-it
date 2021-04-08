---
title: Notifiche del joystick
description: Notifiche del joystick
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- joystick, notifiche
- joystick, messaggi
- joystick acquisiti
- joystick scollegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046704"
---
# <a name="joystick-notifications"></a><span data-ttu-id="da054-107">Notifiche del joystick</span><span class="sxs-lookup"><span data-stu-id="da054-107">Joystick Notifications</span></span>

<span data-ttu-id="da054-108">È possibile acquisire i messaggi Direct joystick da inviare a una funzione tramite la funzione [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) .</span><span class="sxs-lookup"><span data-stu-id="da054-108">You can capture direct joystick messages to be sent to a function by using the [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) function.</span></span> <span data-ttu-id="da054-109">Una sola applicazione alla volta può acquisire messaggi da un joystick, ma è possibile eseguire query sul joystick da un'altra applicazione usando la funzione [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) o [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .</span><span class="sxs-lookup"><span data-stu-id="da054-109">Only one application at a time can capture messages from a joystick, but you can query the joystick from another application by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) or [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

> [!Note]  
> <span data-ttu-id="da054-110">Un messaggio di joystick può non riuscire a raggiungere l'applicazione che ha acquisito il joystick se una seconda applicazione usa **joyGetPos** o **joyGetPosEx** per eseguire una query sul joystick approssimativamente nello stesso momento in cui viene inviato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="da054-110">A joystick message can fail to reach the application that captured the joystick if a second application uses **joyGetPos** or **joyGetPosEx** to query the joystick at approximately the same time that the message is sent.</span></span> <span data-ttu-id="da054-111">In questo caso, la seconda applicazione potrebbe intercettare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="da054-111">In this case, the second application could intercept the message.</span></span>

 

<span data-ttu-id="da054-112">Se si desidera acquisire messaggi da due joystick collegati al sistema, usare due volte [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) , una volta per ogni joystick.</span><span class="sxs-lookup"><span data-stu-id="da054-112">If you want to capture messages from two joysticks attached to the system, use [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) twice, once for each joystick.</span></span> <span data-ttu-id="da054-113">La finestra riceve messaggi distinti e distinti per ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da054-113">Your window receives separate and distinct messages for each device.</span></span>

<span data-ttu-id="da054-114">È possibile rilasciare un joystick acquisito usando la funzione [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) .</span><span class="sxs-lookup"><span data-stu-id="da054-114">You can release a captured joystick by using the [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) function.</span></span> <span data-ttu-id="da054-115">Se un'applicazione non rilascia il joystick prima di terminare, il joystick viene rilasciato automaticamente poco dopo la distruzione della finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="da054-115">If an application does not release the joystick before ending, the joystick is automatically released shortly after the capture window is destroyed.</span></span>

<span data-ttu-id="da054-116">Non è possibile acquisire un joystick scollegato.</span><span class="sxs-lookup"><span data-stu-id="da054-116">You cannot capture an unplugged joystick.</span></span> <span data-ttu-id="da054-117">La funzione **joySetCapture** restituisce JOYERR \_ scollegata se il dispositivo specificato viene scollegato.</span><span class="sxs-lookup"><span data-stu-id="da054-117">The **joySetCapture** function returns JOYERR\_UNPLUGGED if the specified device is unplugged.</span></span>

 

 