---
title: DoProcessOutput nel plug-in di video DSP di esempio
description: DoProcessOutput nel plug-in di video DSP di esempio
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Plug-in di Windows Media Player, video DSP
- plug-in, video DSP
- plug-in per l'elaborazione di segnali digitali, DoProcessOutput
- Plug-in DSP, DoProcessOutput
- plug-in DSP video, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bc844890930209a1c6007213d3c466f0cd15b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297877"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a><span data-ttu-id="ccb37-108">DoProcessOutput nel plug-in di video DSP di esempio</span><span class="sxs-lookup"><span data-stu-id="ccb37-108">DoProcessOutput in the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="ccb37-109">Poiché un plug-in video DSP supporta in genere diversi formati video, è opportuno separare il codice di implementazione dell'elaborazione in una funzione separata per ogni formato.</span><span class="sxs-lookup"><span data-stu-id="ccb37-109">Because a video DSP plug-in typically supports several video formats, it is convenient to separate the processing implementation code into a separate function for each format.</span></span> <span data-ttu-id="ccb37-110">Ciò significa che l'implementazione di **DoProcessOutput** per i plug-in di video DSP è relativamente semplice.</span><span class="sxs-lookup"><span data-stu-id="ccb37-110">This means that the implementation of **DoProcessOutput** for video DSP plug-ins is relatively simple.</span></span>

<span data-ttu-id="ccb37-111">L'implementazione nel plug-in di esempio verifica innanzitutto se l'utente ha abilitato il plug-in.</span><span class="sxs-lookup"><span data-stu-id="ccb37-111">The implementation in the sample plug-in first tests whether the user has enabled the plug-in.</span></span> <span data-ttu-id="ccb37-112">Se il plug-in è disabilitato, il codice copia i dati forniti nel buffer di input nel buffer di output senza modificarli, come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="ccb37-112">If the plug-in is disabled, the code copies the data provided in the input buffer to the output buffer without changing it, as the following code demonstrates:</span></span>


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



<span data-ttu-id="ccb37-113">Se il plug-in è abilitato, il codice esegue semplicemente una serie di controlli sul membro del **sottotipo** di Media Type di input per determinare il formato video corrente.</span><span class="sxs-lookup"><span data-stu-id="ccb37-113">If the plug-in is enabled, the code simply performs a series of checks on the input media type **subtype** member to determine the current video format.</span></span> <span data-ttu-id="ccb37-114">Quando viene trovata una corrispondenza, il codice chiama la funzione di elaborazione appropriata.</span><span class="sxs-lookup"><span data-stu-id="ccb37-114">When a match is found, the code calls the appropriate processing function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccb37-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ccb37-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccb37-116">**Implementazione di un plug-in video DSP**</span><span class="sxs-lookup"><span data-stu-id="ccb37-116">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




