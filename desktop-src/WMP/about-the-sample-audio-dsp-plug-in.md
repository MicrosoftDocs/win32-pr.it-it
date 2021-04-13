---
title: Informazioni sul plug-in audio DSP di esempio
description: Informazioni sul plug-in audio DSP di esempio
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- Plug-in di Windows Media Player, esempi
- plug-in, esempi
- plug-in di elaborazione dei segnali digitali, esempi
- Plug-in DSP, esempi
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, esempi di audio
- Plug-in DSP, esempi di audio
- esempi, plug-in DSP
- plug-in audio DSP, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edc3a5860c0c52837bfece16d2e709bf16d836d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330111"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="1e08d-113">Informazioni sul plug-in audio DSP di esempio</span><span class="sxs-lookup"><span data-stu-id="1e08d-113">About the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="1e08d-114">Il plug-in audio DSP di esempio fornisce una semplice implementazione di elaborazione che ridimensiona l'ampiezza dell'audio in base a un fattore fornito dall'utente nella pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1e08d-114">The sample audio DSP plug-in provides a simple processing implementation that scales the amplitude of the audio by a factor provided by the user in the property page.</span></span> <span data-ttu-id="1e08d-115">Il plug-in accetta valori compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="1e08d-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="1e08d-116">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="1e08d-116">The default value is 1.</span></span> <span data-ttu-id="1e08d-117">Il valore 1 non ha alcun effetto sul suono; altri fattori di scala sono moltiplicatori per gli esempi audio.</span><span class="sxs-lookup"><span data-stu-id="1e08d-117">A value of 1 has no effect upon the sound; other scale factors are multipliers for the audio samples.</span></span> <span data-ttu-id="1e08d-118">Ad esempio, un valore di 0,5 comporterebbe una riduzione di 6 decibel nel volume.</span><span class="sxs-lookup"><span data-stu-id="1e08d-118">For instance, a value of .5 would result in a 6 decibel decrease in volume.</span></span> <span data-ttu-id="1e08d-119">Il valore zero restituisce il silenzio.</span><span class="sxs-lookup"><span data-stu-id="1e08d-119">A value of zero results in silence.</span></span>

<span data-ttu-id="1e08d-120">Il plug-in audio DSP di esempio funziona con audio stereo o mono PCM.</span><span class="sxs-lookup"><span data-stu-id="1e08d-120">The sample audio DSP plug-in works with stereo or mono PCM audio.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e08d-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e08d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e08d-122">**Creazione di un plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="1e08d-122">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




