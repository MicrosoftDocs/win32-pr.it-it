---
title: Buffer video
description: Buffer video
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712583"
---
# <a name="video-buffers"></a><span data-ttu-id="f1abe-107">Buffer video</span><span class="sxs-lookup"><span data-stu-id="f1abe-107">Video Buffers</span></span>

<span data-ttu-id="f1abe-108">I buffer usati con l'acquisizione video si trovano nell'heap di memoria.</span><span class="sxs-lookup"><span data-stu-id="f1abe-108">The buffers used with video capture reside in the memory heap.</span></span> <span data-ttu-id="f1abe-109">Il numero di buffer utilizzati in un'operazione di acquisizione può variare e dipende dal valore del membro **wNumVideoRequested** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) e della memoria di sistema disponibile.</span><span class="sxs-lookup"><span data-stu-id="f1abe-109">The number of buffers used in a capture operation can vary and depend on the value of the **wNumVideoRequested** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure and available system memory.</span></span>

<span data-ttu-id="f1abe-110">È possibile recuperare il valore corrente dei buffer video richiesti usando il messaggio di [**\_ installazione della \_ \_ sequenza \_ WM Cap Get**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="f1abe-110">You can retrieve the current value of requested video buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="f1abe-111">Il numero di buffer video corrente richiesto viene archiviato nel membro **wNumVideoRequested** della struttura **CAPTUREPARMS** .</span><span class="sxs-lookup"><span data-stu-id="f1abe-111">The current requested number of video buffers is stored in the **wNumVideoRequested** member of the **CAPTUREPARMS** structure.</span></span> <span data-ttu-id="f1abe-112">È possibile richiedere la posizione e il numero di buffer aggiornando questo membro, quindi inviando la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_ del set**](wm-cap-set-sequence-setup.md) di test WM (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="f1abe-112">You can request the placement and number of buffers by updating this member, and then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

 

 




