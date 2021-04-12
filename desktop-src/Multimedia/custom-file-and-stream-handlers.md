---
title: Gestori di file e flussi personalizzati
description: Gestori di file e flussi personalizzati
ms.assetid: c61e0118-d405-4c1e-9ae8-ed6a145a5d6b
keywords:
- Video per Windows (VFW), gestori di file personalizzati
- Video per Windows (VFW), gestori di flussi personalizzati
- Video per Windows (VFW), gestori di file
- Video per Windows (VFW), gestori di flusso
- VFW (video per Windows), gestori di file personalizzati
- VFW (video per Windows), gestori di flussi personalizzati
- VFW (video per Windows), gestori di file
- VFW (video per Windows), gestori di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f991ac3197eb6d2f23fcd20d0d14e5f7c65e48de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471414"
---
# <a name="custom-file-and-stream-handlers"></a><span data-ttu-id="51d56-111">Gestori di file e flussi personalizzati</span><span class="sxs-lookup"><span data-stu-id="51d56-111">Custom File and Stream Handlers</span></span>

<span data-ttu-id="51d56-112">I gestori di file e flussi sono driver che forniscono interfacce coerenti a un'applicazione che controlla i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="51d56-112">File and stream handlers are drivers that provide consistent interfaces to an application that controls multimedia data.</span></span> <span data-ttu-id="51d56-113">I gestori di file e flussi inclusi nel sistema operativo utilizzano i dati audio video e di forma d'onda, archiviati in file audio-video interleaved (AVI) e Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="51d56-113">The file and stream handlers included in the operating system use video and waveform-audio data stored in audio-video interleaved (AVI) and waveform-audio files.</span></span>

<span data-ttu-id="51d56-114">È possibile scrivere gestori per consentire all'applicazione di scrivere o accedere a dati multimediali da un'altra origine, ad esempio un file usando un formato proprietario, un file AVI che è stato espanso per contenere flussi di dati aggiuntivi o un gestore che genera i propri dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="51d56-114">You can write handlers to allow your application to write or access multimedia data from another source, such as a file using a proprietary format, an AVI file that has been expanded to contain additional data streams, or a handler that generates its own multimedia data.</span></span> <span data-ttu-id="51d56-115">Se si dispone di un formato di file personalizzato per i dati AVI che si desidera utilizzare con le [funzioni e le macro avifile](avifile-functions-and-macros.md), è necessario scrivere un gestore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="51d56-115">If you have a custom file format for AVI data that you would like to use with the [AVIFile Functions and Macros](avifile-functions-and-macros.md), you need to write a custom handler.</span></span>

-   [<span data-ttu-id="51d56-116">Informazioni sui gestori di file e flussi personalizzati</span><span class="sxs-lookup"><span data-stu-id="51d56-116">About Custom File and Stream Handlers</span></span>](about-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="51d56-117">Uso di gestori di file e flussi personalizzati</span><span class="sxs-lookup"><span data-stu-id="51d56-117">Using Custom File and Stream Handlers</span></span>](using-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="51d56-118">Riferimento al gestore di file e flussi personalizzati</span><span class="sxs-lookup"><span data-stu-id="51d56-118">Custom File and Stream Handler Reference</span></span>](custom-file-and-stream-handler-reference.md)

 

 




