---
title: Modifica del volume di Audio-Devices ausiliari
description: Modifica del volume di Audio-Devices ausiliari
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- audio Waveform, modifica del volume del dispositivo audio ausiliario
- modifica del volume del dispositivo audio ausiliario
- audio ausiliario, modifica del volume del dispositivo
- interfaccia audio ausiliaria
- dispositivi audio ausiliari, modifica del volume
- audio ausiliario, interfaccia
- audio ausiliario, dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727319"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a><span data-ttu-id="e5d10-110">Modifica del volume di Audio-Devices ausiliari</span><span class="sxs-lookup"><span data-stu-id="e5d10-110">Changing the Volume of Auxiliary Audio-Devices</span></span>

<span data-ttu-id="e5d10-111">Windows fornisce le funzioni seguenti per eseguire query e impostare il volume per i dispositivi audio ausiliari.</span><span class="sxs-lookup"><span data-stu-id="e5d10-111">Windows provides the following functions to query and set the volume for auxiliary audio devices.</span></span>



| <span data-ttu-id="e5d10-112">Funzione</span><span class="sxs-lookup"><span data-stu-id="e5d10-112">Function</span></span>                             | <span data-ttu-id="e5d10-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5d10-113">Description</span></span>                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="e5d10-114">**auxGetVolume**</span><span class="sxs-lookup"><span data-stu-id="e5d10-114">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | <span data-ttu-id="e5d10-115">Recupera l'impostazione corrente del volume del dispositivo di output ausiliario specificato.</span><span class="sxs-lookup"><span data-stu-id="e5d10-115">Retrieves the current volume setting of the specified auxiliary output device.</span></span> |
| [<span data-ttu-id="e5d10-116">**auxSetVolume**</span><span class="sxs-lookup"><span data-stu-id="e5d10-116">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | <span data-ttu-id="e5d10-117">Imposta il volume del dispositivo di output ausiliario specificato.</span><span class="sxs-lookup"><span data-stu-id="e5d10-117">Sets the volume of the specified auxiliary output device.</span></span>                      |



 

<span data-ttu-id="e5d10-118">Non tutti i dispositivi audio ausiliari supportano le modifiche del volume.</span><span class="sxs-lookup"><span data-stu-id="e5d10-118">Not all auxiliary audio devices support volume changes.</span></span> <span data-ttu-id="e5d10-119">Alcuni dispositivi sono in grado di supportare singole modifiche dei volumi nei canali sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="e5d10-119">Some devices can support individual volume changes on both the left and the right channels.</span></span>

<span data-ttu-id="e5d10-120">Il volume viene specificato in un valore di parola doppia, come per le funzioni di controllo del volume Waveform-Audio e MIDI.</span><span class="sxs-lookup"><span data-stu-id="e5d10-120">Volume is specified in a doubleword value, as with the waveform-audio and MIDI volume-control functions.</span></span> <span data-ttu-id="e5d10-121">Quando il formato audio è stereo, i 16 bit superiori specificano il volume relativo del canale destro e i 16 bit inferiori specificano il volume relativo del canale sinistro.</span><span class="sxs-lookup"><span data-stu-id="e5d10-121">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="e5d10-122">Per i dispositivi che non supportano il controllo del volume del canale sinistro e destro, i 16 bit inferiori specificano il livello del volume e i 16 bit superiori vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="e5d10-122">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="e5d10-123">I valori a livello di volume variano da 0x0 (silenzioso) a 0xFFFF (volume massimo) e vengono interpretati come logaritmicamente.</span><span class="sxs-lookup"><span data-stu-id="e5d10-123">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="e5d10-124">L'aumento del volume percepito è lo stesso quando si aumenta il livello di volume da 0x5000 a 0x6000, come da 0x4000 a 0x5000.</span><span class="sxs-lookup"><span data-stu-id="e5d10-124">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 