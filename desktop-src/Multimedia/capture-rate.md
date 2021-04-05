---
title: Velocità di acquisizione
description: Velocità di acquisizione
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Struttura CAPTUREPARMS
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93be9e94f5f9085d25c6ad85a30b115d13349169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044715"
---
# <a name="capture-rate"></a><span data-ttu-id="f06c5-108">Velocità di acquisizione</span><span class="sxs-lookup"><span data-stu-id="f06c5-108">Capture Rate</span></span>

<span data-ttu-id="f06c5-109">La velocità di acquisizione è il numero di frame acquisiti ogni secondo di una sessione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f06c5-109">The capture rate is the number of frames that are captured each second of a capture session.</span></span> <span data-ttu-id="f06c5-110">È possibile recuperare la velocità di acquisizione corrente usando il messaggio di [**\_ \_ \_ \_ installazione della sequenza WM Cap**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="f06c5-110">You can retrieve the current capture rate by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="f06c5-111">La velocità di acquisizione corrente è archiviata nel membro **dwRequestMicroSecPerFrame** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="f06c5-111">The current capture rate is stored in the **dwRequestMicroSecPerFrame** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="f06c5-112">È possibile impostare la velocità di acquisizione specificando il numero di microsecondi tra i frame successivi come valore di questo membro, quindi inviando la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_ di serie WM CAP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="f06c5-112">You can set the capture rate by specifying the number of microseconds between successive frames as the value of this member, then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="f06c5-113">Il valore predefinito di **dwRequestMicroSecPerFrame** è 66667, che corrisponde a 15 fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="f06c5-113">The default value of **dwRequestMicroSecPerFrame** is 66667, which corresponds to 15 frames per second.</span></span>

 

 




