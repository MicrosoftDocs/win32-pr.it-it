---
title: Riferimento al mixer audio
description: Riferimento al mixer audio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- audio multimediale, mixer audio
- audio, mixer audio
- audio multimediale, riferimento al mixer
- audio, riferimento al mixer
- mixer audio, informazioni di riferimento
- mixer, riferimento
- informazioni di riferimento per i mixer audio, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223857"
---
# <a name="audio-mixer-reference"></a><span data-ttu-id="cdede-110">Riferimento al mixer audio</span><span class="sxs-lookup"><span data-stu-id="cdede-110">Audio Mixer Reference</span></span>

<span data-ttu-id="cdede-111">In questa sezione vengono descritte le funzioni, le strutture e i messaggi associati a mixer audio.</span><span class="sxs-lookup"><span data-stu-id="cdede-111">This section describes the functions, structures, and messages associated with audio mixers.</span></span> <span data-ttu-id="cdede-112">Questi elementi vengono raggruppati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="cdede-112">These elements are grouped as follows.</span></span>

## <a name="querying-devices"></a><span data-ttu-id="cdede-113">Esecuzione di query sui dispositivi</span><span class="sxs-lookup"><span data-stu-id="cdede-113">Querying Devices</span></span>

-   [<span data-ttu-id="cdede-114">**MIXERCAPS**</span><span class="sxs-lookup"><span data-stu-id="cdede-114">**MIXERCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [<span data-ttu-id="cdede-115">**mixerGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="cdede-115">**mixerGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [<span data-ttu-id="cdede-116">**mixerGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="cdede-116">**mixerGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a><span data-ttu-id="cdede-117">Apertura e chiusura</span><span class="sxs-lookup"><span data-stu-id="cdede-117">Opening and Closing</span></span>

-   [<span data-ttu-id="cdede-118">**mixerClose**</span><span class="sxs-lookup"><span data-stu-id="cdede-118">**mixerClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [<span data-ttu-id="cdede-119">**mixerOpen**</span><span class="sxs-lookup"><span data-stu-id="cdede-119">**mixerOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a><span data-ttu-id="cdede-120">Recupero degli identificatori del mixer</span><span class="sxs-lookup"><span data-stu-id="cdede-120">Retrieving Mixer Identifiers</span></span>

-   [<span data-ttu-id="cdede-121">**mixerGetID**</span><span class="sxs-lookup"><span data-stu-id="cdede-121">**mixerGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a><span data-ttu-id="cdede-122">Recupero di controlli linea</span><span class="sxs-lookup"><span data-stu-id="cdede-122">Retrieving Line Controls</span></span>

-   [<span data-ttu-id="cdede-123">**MIXERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="cdede-123">**MIXERCONTROL**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [<span data-ttu-id="cdede-124">**mixerGetLineControls**</span><span class="sxs-lookup"><span data-stu-id="cdede-124">**mixerGetLineControls**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [<span data-ttu-id="cdede-125">**MIXERLINECONTROLS**</span><span class="sxs-lookup"><span data-stu-id="cdede-125">**MIXERLINECONTROLS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a><span data-ttu-id="cdede-126">Modifica degli attributi del controllo</span><span class="sxs-lookup"><span data-stu-id="cdede-126">Changing Control Attributes</span></span>

-   [<span data-ttu-id="cdede-127">**MIXERCONTROLDETAILS**</span><span class="sxs-lookup"><span data-stu-id="cdede-127">**MIXERCONTROLDETAILS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   <span data-ttu-id="cdede-128">[**MIXERCONTROLDETAILS ( \_ booleano)**](/previous-versions//dd757295(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cdede-128">[**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85))</span></span>
-   <span data-ttu-id="cdede-129">[**\_LISTTEXT MIXERCONTROLDETAILS**](/previous-versions//dd757296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cdede-129">[**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span></span>
-   <span data-ttu-id="cdede-130">[**MIXERCONTROLDETAILS \_ firmato**](/previous-versions//dd757297(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cdede-130">[**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85))</span></span>
-   <span data-ttu-id="cdede-131">[**MIXERCONTROLDETAILS \_ senza segno**](/previous-versions//dd757298(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cdede-131">[**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85))</span></span>
-   [<span data-ttu-id="cdede-132">**mixerGetControlDetails**</span><span class="sxs-lookup"><span data-stu-id="cdede-132">**mixerGetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [<span data-ttu-id="cdede-133">**mixerSetControlDetails**</span><span class="sxs-lookup"><span data-stu-id="cdede-133">**mixerSetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a><span data-ttu-id="cdede-134">Recupero delle informazioni sulla riga</span><span class="sxs-lookup"><span data-stu-id="cdede-134">Retrieving Line Information</span></span>

-   [<span data-ttu-id="cdede-135">**mixerGetLineInfo**</span><span class="sxs-lookup"><span data-stu-id="cdede-135">**mixerGetLineInfo**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [<span data-ttu-id="cdede-136">**MIXERLINE**</span><span class="sxs-lookup"><span data-stu-id="cdede-136">**MIXERLINE**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [<span data-ttu-id="cdede-137">**\_ \_ modifica controllo MIXM \_ mm**</span><span class="sxs-lookup"><span data-stu-id="cdede-137">**MM\_MIXM\_CONTROL\_CHANGE**</span></span>](mm-mixm-control-change.md)
-   [<span data-ttu-id="cdede-138">**\_ \_ modifica riga MIXM \_ mm**</span><span class="sxs-lookup"><span data-stu-id="cdede-138">**MM\_MIXM\_LINE\_CHANGE**</span></span>](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a><span data-ttu-id="cdede-139">Invio di messaggi di User-Defined</span><span class="sxs-lookup"><span data-stu-id="cdede-139">Sending User-Defined Messages</span></span>

-   [<span data-ttu-id="cdede-140">**mixerMessage**</span><span class="sxs-lookup"><span data-stu-id="cdede-140">**mixerMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a><span data-ttu-id="cdede-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cdede-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdede-142">Riferimento al mixer audio</span><span class="sxs-lookup"><span data-stu-id="cdede-142">Audio Mixer Reference</span></span>](audio-mixer-reference.md)
</dt> </dl>

 

 