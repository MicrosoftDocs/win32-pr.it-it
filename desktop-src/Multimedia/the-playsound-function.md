---
title: Funzione PlaySound
description: Funzione PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- audio multimediale, funzione PlaySound
- audio, funzione PlaySound
- audio Waveform, funzione PlaySound
- PlaySound (funzione), informazioni
- sndPlaySound (funzione)
- Funzione PlaySound, confrontata con la funzione sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223537"
---
# <a name="the-playsound-function"></a><span data-ttu-id="89321-109">Funzione PlaySound</span><span class="sxs-lookup"><span data-stu-id="89321-109">The PlaySound Function</span></span>

<span data-ttu-id="89321-110">È possibile usare la funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) per riprodurre l'audio della forma d'onda se il suono si adatta alla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="89321-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play waveform audio if the sound fits into available memory.</span></span> <span data-ttu-id="89321-111">La funzione [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) offre un subset delle funzionalità di PlaySound.</span><span class="sxs-lookup"><span data-stu-id="89321-111">(The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function offers a subset of the capabilities of PlaySound.</span></span> <span data-ttu-id="89321-112">Per ottimizzare la portabilità dell'applicazione basata su Win32, usare **PlaySound**, non **sndPlaySound**.</span><span class="sxs-lookup"><span data-stu-id="89321-112">To maximize the portability of your Win32-based application, use **PlaySound**, not **sndPlaySound**.)</span></span>

<span data-ttu-id="89321-113">La funzione **PlaySound** consente di specificare un suono in uno dei tre modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="89321-113">The **PlaySound** function allows you to specify a sound in one of three ways:</span></span>

-   <span data-ttu-id="89321-114">Come avviso di sistema, usando l'alias archiviato nel file WIN.INI o nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="89321-114">As a system alert, using the alias stored in the WIN.INI file or the registry</span></span>
-   <span data-ttu-id="89321-115">Come nome file</span><span class="sxs-lookup"><span data-stu-id="89321-115">As a filename</span></span>
-   <span data-ttu-id="89321-116">Come identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="89321-116">As a resource identifier</span></span>

<span data-ttu-id="89321-117">La funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) consente di riprodurre un suono in un ciclo continuo, terminando solo quando si chiama di nuovo **PlaySound** , specificando **null** o l'identificatore audio di un altro suono per il parametro *pszSound* .</span><span class="sxs-lookup"><span data-stu-id="89321-117">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function allows you to play a sound in a continuous loop, ending only when you call **PlaySound** again, specifying either **NULL** or the sound identifier of another sound for the *pszSound* parameter.</span></span>

<span data-ttu-id="89321-118">È possibile usare **PlaySound** per riprodurre il suono in modo sincrono o asincrono e per controllare il comportamento della funzione in altri modi quando deve condividere le risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="89321-118">You can use **PlaySound** to play the sound synchronously or asynchronously, and to control the behavior of the function in other ways when it must share system resources.</span></span>

<span data-ttu-id="89321-119">Per ulteriori informazioni sull'utilizzo di PlaySound, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="89321-119">For more information about using PlaySound, see the following topics:</span></span>

-   [<span data-ttu-id="89321-120">Uso di PlaySound per riprodurre file di Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="89321-120">Using PlaySound to Play Waveform-Audio Files</span></span>](using-playsound-to-play-waveform-audio-files.md)
-   [<span data-ttu-id="89321-121">Uso di PlaySound per il ciclo di suoni</span><span class="sxs-lookup"><span data-stu-id="89321-121">Using PlaySound to Loop Sounds</span></span>](using-playsound-to-loop-sounds.md)
-   [<span data-ttu-id="89321-122">Uso di PlaySound per riprodurre suoni di sistema</span><span class="sxs-lookup"><span data-stu-id="89321-122">Using PlaySound to Play System Sounds</span></span>](using-playsound-to-play-system-sounds.md)

<span data-ttu-id="89321-123">Per altri esempi su come usare **PlaySound** nelle applicazioni basate su Win32, vedere la pagina relativa alla [riproduzione di risorse Wave](playing-wave-resources.md).</span><span class="sxs-lookup"><span data-stu-id="89321-123">For more examples of how to use **PlaySound** in your Win32-based applications, see [Playing WAVE Resources](playing-wave-resources.md).</span></span>

 

 