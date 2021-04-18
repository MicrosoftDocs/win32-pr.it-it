---
title: Riproduzione di cicli (audio Waveform)
description: Riproduzione di cicli (audio Waveform)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- audio della forma d'onda, suoni di loop
- waveform-interfaccia audio, loop suoni
- audio della forma d'onda, riproduzione a cicli
- waveform-interfaccia audio, riproduzione a ciclo
- loop della forma d'onda-suoni audio
- esecuzione del loop della forma d'onda-riproduzione audio
- waveOutWrite (funzione)
- waveOutBreakLoop (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334032"
---
# <a name="looping-playback"></a><span data-ttu-id="3b106-111">Riproduzione di cicli</span><span class="sxs-lookup"><span data-stu-id="3b106-111">Looping Playback</span></span>

<span data-ttu-id="3b106-112">Il ciclo di un suono è controllato dai membri **dwLoops** e **DwFlags** nelle strutture [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) passate al dispositivo con la funzione [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) .</span><span class="sxs-lookup"><span data-stu-id="3b106-112">Looping a sound is controlled by the **dwLoops** and **dwFlags** members in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structures passed to the device with the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> <span data-ttu-id="3b106-113">Usare i flag **WHDR \_ BEGINLOOP** e **WHDR \_ EndLoop** nel membro **dwFlags** per specificare i blocchi di dati iniziali e finali per il ciclo.</span><span class="sxs-lookup"><span data-stu-id="3b106-113">Use the **WHDR\_BEGINLOOP** and **WHDR\_ENDLOOP** flags in the **dwFlags** member to specify the beginning and ending data blocks for looping.</span></span>

<span data-ttu-id="3b106-114">Per eseguire il ciclo di un singolo blocco di dati, specificare entrambi i flag per lo stesso blocco.</span><span class="sxs-lookup"><span data-stu-id="3b106-114">To loop a single data block, specify both flags for the same block.</span></span> <span data-ttu-id="3b106-115">Per specificare il numero di cicli, usare il membro **dwLoops** nella struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) per il primo blocco del ciclo.</span><span class="sxs-lookup"><span data-stu-id="3b106-115">To specify the number of loops, use the **dwLoops** member in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure for the first block in the loop.</span></span>

<span data-ttu-id="3b106-116">È possibile chiamare la funzione [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) per arrestare un suono di ciclo.</span><span class="sxs-lookup"><span data-stu-id="3b106-116">You can call the [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) function to stop a looping sound.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b106-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b106-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b106-118">Riproduzione di file di Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="3b106-118">Playing Waveform-Audio Files</span></span>](playing-waveform-audio-files.md)
</dt> </dl>

 

 
