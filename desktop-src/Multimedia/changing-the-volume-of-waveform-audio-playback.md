---
title: Modifica del volume della riproduzione Waveform-Audio
description: Modifica del volume della riproduzione Waveform-Audio
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- audio della forma d'onda, modifica del volume di riproduzione
- waveform-interfaccia audio, modifica del volume di riproduzione
- audio Waveform, volume di riproduzione
- waveform-interfaccia audio, volume di riproduzione
- modifica del volume della riproduzione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f972b5bd8e6f0d4a0d7d5964f164429c5632b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727314"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a><span data-ttu-id="5d56a-108">Modifica del volume della riproduzione Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="5d56a-108">Changing the Volume of Waveform-Audio Playback</span></span>

<span data-ttu-id="5d56a-109">Windows fornisce le funzioni seguenti per eseguire query e impostare il livello di volume dei dispositivi di output dell'audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="5d56a-109">Windows provides the following functions to query and set the volume level of waveform-audio output devices.</span></span>



| <span data-ttu-id="5d56a-110">Funzione</span><span class="sxs-lookup"><span data-stu-id="5d56a-110">Function</span></span>                                     | <span data-ttu-id="5d56a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d56a-111">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="5d56a-112">**waveOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="5d56a-112">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | <span data-ttu-id="5d56a-113">Recupera il livello del volume corrente del dispositivo di output dell'audio e della forma d'onda specificato.</span><span class="sxs-lookup"><span data-stu-id="5d56a-113">Retrieves the current volume level of the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="5d56a-114">**waveOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="5d56a-114">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | <span data-ttu-id="5d56a-115">Imposta il livello del volume del dispositivo di output dell'audio e della forma d'onda specificato.</span><span class="sxs-lookup"><span data-stu-id="5d56a-115">Sets the volume level of the specified waveform-audio output device.</span></span>              |



 

<span data-ttu-id="5d56a-116">Non tutti i dispositivi Waveform-Audio supportano le modifiche del volume.</span><span class="sxs-lookup"><span data-stu-id="5d56a-116">Not all waveform-audio devices support volume changes.</span></span> <span data-ttu-id="5d56a-117">Alcuni dispositivi supportano il controllo del volume singolo sui canali sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="5d56a-117">Some devices support individual volume control on both the left and right channels.</span></span> <span data-ttu-id="5d56a-118">Per informazioni su come determinare le funzionalità di controllo del volume dei dispositivi audio e della forma d'onda, vedere [dispositivi e tipi di dati](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="5d56a-118">For information about how to determine the volume-control capabilities of waveform-audio devices, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="5d56a-119">Alcune applicazioni consentono all'utente di controllare il volume per tutti i dispositivi audio in un sistema.</span><span class="sxs-lookup"><span data-stu-id="5d56a-119">Some applications allow the user to control the volume for all audio devices in a system.</span></span> <span data-ttu-id="5d56a-120">In molte applicazioni di questo tipo vengono utilizzati i servizi mixer audio. per ulteriori informazioni, vedere [mixer audio](audio-mixers.md). A meno che l'applicazione non sia in grado di eseguire questo tipo di controllo del volume principale, è necessario aprire un dispositivo audio prima di modificarne il volume.</span><span class="sxs-lookup"><span data-stu-id="5d56a-120">(Many applications of this type use the audio mixer services; for more information, see [Audio Mixers](audio-mixers.md).) Unless your application is capable of this kind of master volume control, you should open an audio device before changing its volume.</span></span> <span data-ttu-id="5d56a-121">È anche necessario eseguire una query sul livello del volume prima di modificarlo e ripristinare il livello del volume precedente il prima possibile.</span><span class="sxs-lookup"><span data-stu-id="5d56a-121">You should also query the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="5d56a-122">Il volume è specificato in un valore parola doppia.</span><span class="sxs-lookup"><span data-stu-id="5d56a-122">Volume is specified in a doubleword value.</span></span> <span data-ttu-id="5d56a-123">Quando il formato audio è stereo, i 16 bit superiori specificano il volume relativo del canale destro e i 16 bit inferiori specificano il volume relativo del canale sinistro.</span><span class="sxs-lookup"><span data-stu-id="5d56a-123">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="5d56a-124">Per i dispositivi che non supportano il controllo del volume del canale sinistro e destro, i 16 bit inferiori specificano il livello del volume e i 16 bit superiori vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="5d56a-124">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="5d56a-125">I valori a livello di volume variano da 0x0 (silenzioso) a 0xFFFF (volume massimo) e vengono interpretati come logaritmicamente.</span><span class="sxs-lookup"><span data-stu-id="5d56a-125">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="5d56a-126">L'aumento del volume percepito è lo stesso quando si aumenta il livello di volume da 0x5000 a 0x6000, come da 0x4000 a 0x5000.</span><span class="sxs-lookup"><span data-stu-id="5d56a-126">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 