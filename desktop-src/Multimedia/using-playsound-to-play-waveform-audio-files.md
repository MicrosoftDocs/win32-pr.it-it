---
title: Uso di PlaySound per riprodurre file di Waveform-Audio
description: Uso di PlaySound per riprodurre file di Waveform-Audio
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- audio Waveform, funzione PlaySound
- audio Waveform, riproduzione di file
- audio Waveform, estensione del nome file WAV
- Funzione PlaySound, riproduzione di file audio Waveform
- riproduzione di file audio Waveform, funzione PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d5dde46827b7892217f760c749e75e19f368f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963076"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a><span data-ttu-id="5b726-108">Uso di PlaySound per riprodurre file di Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="5b726-108">Using PlaySound to Play Waveform-Audio Files</span></span>

<span data-ttu-id="5b726-109">La maggior parte dei file audio della forma d'onda usa il. Estensione del nome file WAV.</span><span class="sxs-lookup"><span data-stu-id="5b726-109">Most waveform-audio files use the .WAV filename extension.</span></span>

<span data-ttu-id="5b726-110">L'istruzione seguente riproduce i \\ \\ campanelli. File WAV:</span><span class="sxs-lookup"><span data-stu-id="5b726-110">The following statement plays the C:\\SOUNDS\\BELLS.WAV file:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



<span data-ttu-id="5b726-111">Se il file specificato non esiste o se il file non rientra nella memoria disponibile, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) riproduce il suono di sistema predefinito.</span><span class="sxs-lookup"><span data-stu-id="5b726-111">If the specified file does not exist, or if the file does not fit into the available memory, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) plays the default system sound.</span></span> <span data-ttu-id="5b726-112">Se non è stato definito alcun suono di sistema predefinito, **PlaySound** ha esito negativo senza produrre alcun suono.</span><span class="sxs-lookup"><span data-stu-id="5b726-112">If no default system sound has been defined, **PlaySound** fails without producing any sound.</span></span> <span data-ttu-id="5b726-113">Se non si desidera riprodurre l'audio di sistema predefinito, specificare il flag SND \_ NODEFAULT, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="5b726-113">If you do not want the default system sound to play, specify the SND\_NODEFAULT flag, as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 