---
title: Riferimento al joystick
description: Riferimento al joystick
ms.assetid: c2ad092f-a0c5-4e28-ada7-227dc52c3c83
keywords:
- Windows Multimedia, riferimento al joystick
- Multimedia, riferimento al joystick
- input multimediale, riferimento al joystick
- joystick, riferimento
- informazioni di riferimento per i joystick, informazioni
- riferimento al joystick, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242f3fb21f9da9b1853ae8e9e7f694b9ad3bf711
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872370"
---
# <a name="joystick-reference"></a><span data-ttu-id="e10a3-109">Riferimento al joystick</span><span class="sxs-lookup"><span data-stu-id="e10a3-109">Joystick Reference</span></span>

<span data-ttu-id="e10a3-110">In questa sezione vengono descritte le funzioni, le strutture e i messaggi associati ai joystick.</span><span class="sxs-lookup"><span data-stu-id="e10a3-110">This section describes the functions, structures, and messages associated with joysticks.</span></span> <span data-ttu-id="e10a3-111">Gli elementi vengono raggruppati come segue:</span><span class="sxs-lookup"><span data-stu-id="e10a3-111">The elements are grouped as follows:</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="e10a3-112">Funzionalità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e10a3-112">Device Capabilities</span></span>

-   [<span data-ttu-id="e10a3-113">**joyGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="e10a3-113">**joyGetDevCaps**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps)
-   [<span data-ttu-id="e10a3-114">**joyGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="e10a3-114">**joyGetNumDevs**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs)
-   [<span data-ttu-id="e10a3-115">**JOYCAPS**</span><span class="sxs-lookup"><span data-stu-id="e10a3-115">**JOYCAPS**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joycaps)

## <a name="querying-a-joystick"></a><span data-ttu-id="e10a3-116">Esecuzione di query su un joystick</span><span class="sxs-lookup"><span data-stu-id="e10a3-116">Querying a Joystick</span></span>

-   [<span data-ttu-id="e10a3-117">**joyConfigChanged**</span><span class="sxs-lookup"><span data-stu-id="e10a3-117">**joyConfigChanged**</span></span>](/windows/desktop/api/joystickapi/nf-joystickapi-joyconfigchanged)
-   [<span data-ttu-id="e10a3-118">**joyGetPos**</span><span class="sxs-lookup"><span data-stu-id="e10a3-118">**joyGetPos**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos)
-   [<span data-ttu-id="e10a3-119">**joyGetPosEx**</span><span class="sxs-lookup"><span data-stu-id="e10a3-119">**joyGetPosEx**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex)
-   [<span data-ttu-id="e10a3-120">**JOYINFO**</span><span class="sxs-lookup"><span data-stu-id="e10a3-120">**JOYINFO**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfo)
-   [<span data-ttu-id="e10a3-121">**JOYINFOEX**</span><span class="sxs-lookup"><span data-stu-id="e10a3-121">**JOYINFOEX**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfoex)

## <a name="capturing-a-joystick"></a><span data-ttu-id="e10a3-122">Acquisizione di un joystick</span><span class="sxs-lookup"><span data-stu-id="e10a3-122">Capturing a Joystick</span></span>

-   [<span data-ttu-id="e10a3-123">**joyGetThreshold**</span><span class="sxs-lookup"><span data-stu-id="e10a3-123">**joyGetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetthreshold)
-   [<span data-ttu-id="e10a3-124">**joyReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="e10a3-124">**joyReleaseCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture)
-   [<span data-ttu-id="e10a3-125">**joySetCapture**</span><span class="sxs-lookup"><span data-stu-id="e10a3-125">**joySetCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture)
-   [<span data-ttu-id="e10a3-126">**joySetThreshold**</span><span class="sxs-lookup"><span data-stu-id="e10a3-126">**joySetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold)
-   [<span data-ttu-id="e10a3-127">**\_JOY1BUTTONDOWN mm**</span><span class="sxs-lookup"><span data-stu-id="e10a3-127">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md)
-   [<span data-ttu-id="e10a3-128">**\_JOY1BUTTONUP mm**</span><span class="sxs-lookup"><span data-stu-id="e10a3-128">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)
-   [<span data-ttu-id="e10a3-129">**\_JOY1MOVE mm**</span><span class="sxs-lookup"><span data-stu-id="e10a3-129">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)
-   [<span data-ttu-id="e10a3-130">**\_JOY1ZMOVE mm**</span><span class="sxs-lookup"><span data-stu-id="e10a3-130">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)
-   [<span data-ttu-id="e10a3-131">**\_JOY2BUTTONDOWN mm**</span><span class="sxs-lookup"><span data-stu-id="e10a3-131">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md)
-   [<span data-ttu-id="e10a3-132">**\_JOY2BUTTONUP mm**</span><span class="sxs-lookup"><span data-stu-id="e10a3-132">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)
-   [<span data-ttu-id="e10a3-133">**\_JOY2MOVE mm**</span><span class="sxs-lookup"><span data-stu-id="e10a3-133">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)
-   [<span data-ttu-id="e10a3-134">**\_JOY2ZMOVE mm**</span><span class="sxs-lookup"><span data-stu-id="e10a3-134">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)

## <a name="related-topics"></a><span data-ttu-id="e10a3-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e10a3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e10a3-136">Joystick</span><span class="sxs-lookup"><span data-stu-id="e10a3-136">Joysticks</span></span>](joysticks.md)
</dt> </dl>

 

 