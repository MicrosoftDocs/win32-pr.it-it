---
title: Per trovare i numeri di flusso e i numeri di output
description: Per trovare i numeri di flusso e i numeri di output
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- ASF (Advanced Systems Format), numeri di flusso
- ASF (formato avanzato dei sistemi), creazione di numeri
- ASF (Advanced Systems Format), ricerca dei numeri di output
- ASF (Advanced Systems Format), ricerca dei numeri di output
- lettori sincroni, numeri di flusso
- lettori sincroni, ricerca di numeri di output
- flussi, ricerca di numeri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723463"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a><span data-ttu-id="bdcc8-110">Per trovare i numeri di flusso e i numeri di output</span><span class="sxs-lookup"><span data-stu-id="bdcc8-110">To Find Stream Numbers and Output Numbers</span></span>

<span data-ttu-id="bdcc8-111">Il lettore sincrono supporta il cambio più semplificato tra i numeri di flusso e di output per la riproduzione rispetto al Reader asincrono.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-111">The synchronous reader supports more simplified switching between stream and output numbers for playback than the asynchronous reader.</span></span> <span data-ttu-id="bdcc8-112">È quindi più importante riuscire a individuare i numeri di flusso che corrispondono ai numeri di output o viceversa.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-112">It is therefore more important to be able to find which stream numbers equate to which output numbers, or the other way around.</span></span>

<span data-ttu-id="bdcc8-113">Per trovare il numero di output corrispondente a un numero di flusso, chiamare [**IWMSyncReader:: GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span><span class="sxs-lookup"><span data-stu-id="bdcc8-113">To find the output number that corresponds to a stream number, call [**IWMSyncReader::GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span></span>

<span data-ttu-id="bdcc8-114">Per trovare il numero di flusso che corrisponde a un numero di output, chiamare [ **IWMSyncReader:: GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span><span class="sxs-lookup"><span data-stu-id="bdcc8-114">To find the stream number that corresponds to an output number, call [**IWMSyncReader::GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdcc8-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bdcc8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdcc8-116">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="bdcc8-116">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="bdcc8-117">**Input, flussi e output**</span><span class="sxs-lookup"><span data-stu-id="bdcc8-117">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="bdcc8-118">**Lettura di file con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="bdcc8-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




