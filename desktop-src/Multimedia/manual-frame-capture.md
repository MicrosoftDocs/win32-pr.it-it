---
title: Acquisizione frame manuale
description: Acquisizione frame manuale
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- Messaggio WM_CAP_SINGLE_FRAME_OPEN
- Messaggio WM_CAP_SINGLE_FRAME
- Messaggio WM_CAP_SINGLE_FRAME_CLOSE
- capCaptureSingleFrameOpen (macro)
- capCaptureSingleFrame (macro)
- capCaptureSingleFrameClose (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26899032d8e81be437e8f29acf36f0a37703c560
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855866"
---
# <a name="manual-frame-capture"></a><span data-ttu-id="9f6a0-109">Acquisizione frame manuale</span><span class="sxs-lookup"><span data-stu-id="9f6a0-109">Manual Frame Capture</span></span>

<span data-ttu-id="9f6a0-110">Se si desidera specificare singolarmente i frame da acquisire in un flusso video, è possibile controllare la sequenza usando i messaggi [**WM \_ Cap \_ Single \_ frame \_ Open**](wm-cap-single-frame-open.md), [**WM \_ Cap \_ Single \_ frame**](wm-cap-single-frame.md)e [**WM \_ Cap Single \_ \_ frame \_ Close**](wm-cap-single-frame-close.md) (oppure le macro [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)e [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) ).</span><span class="sxs-lookup"><span data-stu-id="9f6a0-110">If you want to individually specify the frames to capture in a video stream, you can control the sequence by using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md), [**WM\_CAP\_SINGLE\_FRAME**](wm-cap-single-frame.md), and [**WM\_CAP\_SINGLE\_FRAME\_CLOSE**](wm-cap-single-frame-close.md) messages (or the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe), and [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macros).</span></span> <span data-ttu-id="9f6a0-111">In genere, questi messaggi vengono usati per creare animazioni aggiungendo singoli frame al file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9f6a0-111">Typically, these messages are used to create animation by appending individual frames to the capture file.</span></span> <span data-ttu-id="9f6a0-112">\_ \_ \_ Il singolo frame aperto WM Cap \_ apre un file per un'operazione di acquisizione basata manualmente.</span><span class="sxs-lookup"><span data-stu-id="9f6a0-112">WM\_CAP\_SINGLE\_FRAME\_OPEN opens a file for a manually driven capture operation.</span></span> <span data-ttu-id="9f6a0-113">\_ \_ Il singolo frame WM Cap \_ acquisisce un singolo frame e lo aggiunge al file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9f6a0-113">WM\_CAP\_SINGLE\_FRAME captures an individual frame and appends it to the capture file.</span></span> <span data-ttu-id="9f6a0-114">\_ \_ \_ La chiusura del singolo frame WM Cap \_ chiude il file usato per l'acquisizione manuale dei frame.</span><span class="sxs-lookup"><span data-stu-id="9f6a0-114">WM\_CAP\_SINGLE\_FRAME\_CLOSE closes the file used for manual frame capture.</span></span>

> [!Note]  
> <span data-ttu-id="9f6a0-115">Questo metodo di acquisizione non supporta l'acquisizione audio simultanea con acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="9f6a0-115">This capture method does not support simultaneous audio capture with video capture.</span></span>

 

 

 




