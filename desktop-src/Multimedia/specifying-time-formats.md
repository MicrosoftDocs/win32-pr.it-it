---
title: Specifica di formati di ora
description: Specifica di formati di ora
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- MCIWndGetTimeFormat (macro)
- MCIWndSetTimeFormat (macro)
- MCIWndUseTime (macro)
- MCIWndUseFrames (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330060"
---
# <a name="specifying-time-formats"></a><span data-ttu-id="ef1c8-107">Specifica di formati di ora</span><span class="sxs-lookup"><span data-stu-id="ef1c8-107">Specifying Time Formats</span></span>

<span data-ttu-id="ef1c8-108">I tipi di dati multimediali possono in genere utilizzare il tempo per identificare posizioni significative all'interno del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-108">Multimedia data types typically can use time to identify significant positions within their content.</span></span> <span data-ttu-id="ef1c8-109">I formati di ora comuni sono millisecondi, tracce e frame; Esistono anche altri formati di tempo meno comuni, ad esempio SMPTE (Society of Motion Picture e Television Engineers) 24.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-109">Common time formats are milliseconds, tracks, and frames; other less common time formats, such as SMPTE (Society of Motion Picture and Television Engineers) 24, also exist.</span></span> <span data-ttu-id="ef1c8-110">Time è il formato e il sistema di riferimento per i dati audio della forma d'onda, MIDI e CD.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-110">Time is the format and reference system for waveform-audio, MIDI, and CD audio data.</span></span> <span data-ttu-id="ef1c8-111">Il video supporta il tempo anche se viene registrato come sequenza di frame (flusso) che in genere viene riprodotta a una velocità specifica.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-111">Video supports time even though it is recorded as a sequence of frames (stream) that is typically played at a specific speed.</span></span> <span data-ttu-id="ef1c8-112">Sono disponibili diverse macro per la designazione del formato ora.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-112">Several macros are available for designating time format.</span></span>

<span data-ttu-id="ef1c8-113">È possibile recuperare il formato dell'ora corrente per un file o un dispositivo usando la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="ef1c8-113">You can retrieve the current time format for a file or device by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span> <span data-ttu-id="ef1c8-114">È possibile modificare il formato dell'ora corrente con qualsiasi altro formato di ora supportato da un dispositivo usando la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="ef1c8-114">You can change the current time format to any other time format supported by a device by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span> <span data-ttu-id="ef1c8-115">In alternativa, è possibile impostare il formato dell'ora su millisecondi o frame usando le macro [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) o [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) .</span><span class="sxs-lookup"><span data-stu-id="ef1c8-115">Or you can the set the time format to milliseconds or frames by using the [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) or [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) macros.</span></span>

> [!Note]  
> <span data-ttu-id="ef1c8-116">I formati non continui, ad esempio Tracks e SMPTE, possono causare un comportamento anomalo della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-116">Noncontinuous formats, such as tracks and SMPTE, can cause the toolbar to behave erratically.</span></span> <span data-ttu-id="ef1c8-117">Per questi formati temporali, potrebbe essere necessario disattivare la barra degli strumenti specificando lo \_ stile della finestra NOPLAYBAR di MCIWNDF durante la creazione di una finestra di MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-117">For these time formats, you might want to turn off the toolbar by specifying the MCIWNDF\_NOPLAYBAR window style when creating an MCIWnd window.</span></span>

 

 

 




