---
title: Determinazione e modifica della posizione corrente
description: Determinazione e modifica della posizione corrente
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- MCIWndGetStart (macro)
- MCIWndGetEnd (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471398"
---
# <a name="determining-and-changing-the-current-position"></a><span data-ttu-id="0f6de-105">Determinazione e modifica della posizione corrente</span><span class="sxs-lookup"><span data-stu-id="0f6de-105">Determining and Changing the Current Position</span></span>

<span data-ttu-id="0f6de-106">Quando un file o un dispositivo è associato a una finestra MCIWnd, la posizione di riproduzione viene inizialmente impostata all'inizio del contenuto, indipendentemente dal tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="0f6de-106">When a file or device is associated with an MCIWnd window, the playback position is initially set at the start of the content, regardless of the media type.</span></span> <span data-ttu-id="0f6de-107">Durante la riproduzione, la posizione di riproduzione viene spostata in modo lineare tramite il contenuto e, se la riproduzione non viene interrotta, raggiunge la fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="0f6de-107">During playback, the playback position moves linearly through the content and, if playback is uninterrupted, eventually reaches the end of the content.</span></span> <span data-ttu-id="0f6de-108">Se si verifica un'interruzione, la posizione di riproduzione corrente è la posizione in cui la riproduzione è stata interrotta o sospesa.</span><span class="sxs-lookup"><span data-stu-id="0f6de-108">If an interruption occurs, the current playback position is the location at which playback was stopped or paused.</span></span>

<span data-ttu-id="0f6de-109">È possibile recuperare i percorsi per l'inizio e la fine del contenuto usando le macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) e [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .</span><span class="sxs-lookup"><span data-stu-id="0f6de-109">You can retrieve the locations for the beginning and end of the content by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros.</span></span> <span data-ttu-id="0f6de-110">È possibile determinare la lunghezza del contenuto sottraendo il valore restituito da **MCIWndGetStart** dal valore restituito da **MCIWndGetEnd** o usando la macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .</span><span class="sxs-lookup"><span data-stu-id="0f6de-110">You can determine the length of the content by subtracting the value returned by **MCIWndGetStart** from the value returned by **MCIWndGetEnd**, or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span> <span data-ttu-id="0f6de-111">È possibile recuperare la posizione di riproduzione corrente usando la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) oppure è possibile recuperare la posizione di riproduzione come stringa con terminazione null usando la macro [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .</span><span class="sxs-lookup"><span data-stu-id="0f6de-111">You can retrieve the current playback position by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) macro, or you can retrieve the playback position as a null-terminated string by using the [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>

<span data-ttu-id="0f6de-112">Per modificare la posizione di riproduzione corrente, usare le macro [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)e [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) .</span><span class="sxs-lookup"><span data-stu-id="0f6de-112">To change the current playback position, use the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend), and [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) macros.</span></span> <span data-ttu-id="0f6de-113">È possibile spostare la posizione di riproduzione all'inizio del contenuto utilizzando **MCIWndHome** o alla fine del contenuto utilizzando **MCIWndEnd**.</span><span class="sxs-lookup"><span data-stu-id="0f6de-113">You can move the playback position to the start of the content by using **MCIWndHome** or to the end of the content by using **MCIWndEnd**.</span></span> <span data-ttu-id="0f6de-114">Usare **MCIWndSeek** per spostare la posizione di riproduzione in qualsiasi posizione nel contenuto.</span><span class="sxs-lookup"><span data-stu-id="0f6de-114">Use **MCIWndSeek** to move the playback position to any location in the content.</span></span>

<span data-ttu-id="0f6de-115">È anche possibile esaminare il contenuto usando la macro [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) .</span><span class="sxs-lookup"><span data-stu-id="0f6de-115">You can also step through the content by using the [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) macro.</span></span> <span data-ttu-id="0f6de-116">A partire dalla posizione di riproduzione corrente, questa macro sposta la posizione di riproduzione avanti o indietro in base a un incremento specificato.</span><span class="sxs-lookup"><span data-stu-id="0f6de-116">Beginning from the current playback position, this macro moves the playback position forward or backward by a specified increment.</span></span>

> [!Note]  
> <span data-ttu-id="0f6de-117">Le unità usate per specificare la posizione variano tra i diversi tipi di supporti e dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0f6de-117">The units used to specify position vary among the different media types and devices.</span></span> <span data-ttu-id="0f6de-118">Ad esempio, la posizione di riproduzione per i file AVI usati dal dispositivo MCIAVI viene misurata in frame; la posizione di riproduzione per i file audio CD, waveform e audio e MIDI è misurata in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0f6de-118">For example, the playback position for AVI files used by the MCIAVI device is measured in frames; the playback position for CD audio, waveform-audio, and MIDI files is measured in milliseconds.</span></span>

 

<span data-ttu-id="0f6de-119">I dispositivi per altri tipi di supporti e dispositivi di terze parti potrebbero usare altre unità.</span><span class="sxs-lookup"><span data-stu-id="0f6de-119">Devices for other media types and third-party devices might use other units.</span></span> <span data-ttu-id="0f6de-120">Per informazioni su come determinare queste unità, vedere [miglioramenti della riproduzione](playback-enhancements.md).</span><span class="sxs-lookup"><span data-stu-id="0f6de-120">For information about determining these units, see [Playback Enhancements](playback-enhancements.md).</span></span>

 

 




