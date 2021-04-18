---
title: Impostazioni acquisizione video
description: Impostazioni acquisizione video
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Struttura CAPTUREPARMS
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297895"
---
# <a name="video-capture-settings"></a><span data-ttu-id="96332-108">Impostazioni acquisizione video</span><span class="sxs-lookup"><span data-stu-id="96332-108">Video Capture Settings</span></span>

<span data-ttu-id="96332-109">La struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) contiene i parametri di controllo per l'acquisizione video di streaming.</span><span class="sxs-lookup"><span data-stu-id="96332-109">The [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure contains the control parameters for streaming video capture.</span></span> <span data-ttu-id="96332-110">Questa struttura controlla diversi aspetti del processo di acquisizione e consente di eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="96332-110">This structure controls several aspects of the capture process, and allows you to perform the following tasks:</span></span>

-   <span data-ttu-id="96332-111">Specificare la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="96332-111">Specify the frame rate.</span></span>
-   <span data-ttu-id="96332-112">Consente di specificare il numero di buffer video allocati.</span><span class="sxs-lookup"><span data-stu-id="96332-112">Specify the number of allocated video buffers.</span></span>
-   <span data-ttu-id="96332-113">Disabilitare e abilitare l'acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="96332-113">Disable and enable audio capture.</span></span>
-   <span data-ttu-id="96332-114">Specificare l'intervallo di tempo per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="96332-114">Specify the time interval for the capture.</span></span>
-   <span data-ttu-id="96332-115">Specificare se durante l'acquisizione viene usato un dispositivo MCI (VCR o videodisco).</span><span class="sxs-lookup"><span data-stu-id="96332-115">Specify whether an MCI device (VCR or videodisc) is used during capture.</span></span>
-   <span data-ttu-id="96332-116">Consente di specificare il controllo della tastiera o del mouse per lo streaming finale.</span><span class="sxs-lookup"><span data-stu-id="96332-116">Specify keyboard or mouse control for ending streaming.</span></span>
-   <span data-ttu-id="96332-117">Consente di specificare il tipo di media video applicato durante l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="96332-117">Specify the type of video averaging applied during capture.</span></span>

<span data-ttu-id="96332-118">È possibile recuperare le impostazioni di acquisizione correnti all'interno della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) inviando il messaggio di [**\_ \_ \_ \_ configurazione della sequenza WM CAP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ) a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="96332-118">You can retrieve the current capture settings within the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure by sending the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro) to a capture window.</span></span> <span data-ttu-id="96332-119">È possibile impostare una o più impostazioni di acquisizione correnti aggiornando i membri appropriati della struttura **CAPTUREPARMS** e quindi inviando il messaggio di [**\_ \_ \_ \_ installazione sequenza di WM Cap**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ) e **CAPTUREPARMS** a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="96332-119">You can set one or more current capture settings by updating the appropriate members of the **CAPTUREPARMS** structure and then sending the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro) and **CAPTUREPARMS** to a capture window.</span></span>

 

 




