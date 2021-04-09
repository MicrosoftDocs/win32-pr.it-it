---
title: Misurazione della qualità dei video
description: Misurazione della qualità dei video
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044640"
---
# <a name="measuring-video-quality"></a><span data-ttu-id="835d2-107">Misurazione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="835d2-107">Measuring Video Quality</span></span>

<span data-ttu-id="835d2-108">Un modo per misurare la qualità dei video consiste nel limitare il numero di frame acquisiti eliminati durante l'operazione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="835d2-108">One way to measure video quality is to limit the number of captured frames dropped during the capture operation.</span></span> <span data-ttu-id="835d2-109">Al termine dell'acquisizione del flusso, il valore della qualità viene confrontato con il rapporto tra i frame eliminati e il totale dei frame.</span><span class="sxs-lookup"><span data-stu-id="835d2-109">When streaming capture has finished, the quality value is compared with the ratio of dropped frames to total frames.</span></span> <span data-ttu-id="835d2-110">Se la percentuale di frame eliminati è maggiore del valore del membro **wPercentDropForError** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) , AVICap Invia un messaggio di errore alla funzione di callback degli errori, se installata.</span><span class="sxs-lookup"><span data-stu-id="835d2-110">If the percentage of dropped frames is greater than the value of the **wPercentDropForError** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure, AVICap sends an error message to the error callback function if it is installed.</span></span>

<span data-ttu-id="835d2-111">È possibile recuperare il limite corrente di frame eliminati (espresso come percentuale) usando il messaggio di [**\_ installazione della \_ \_ sequenza \_ WM Cap Get**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="835d2-111">You can retrieve the current limit of dropped frames (expressed as a percentage) by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="835d2-112">È possibile impostare un nuovo limite specificando una percentuale come valore del membro **wPercentDropForError** della struttura **CAPTUREPARMS** e quindi inviando la struttura aggiornata alla finestra di acquisizione usando il messaggio di installazione della [**\_ sequenza del \_ set \_ \_ di estremità WM**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="835d2-112">You can set a new limit by specifying a percentage as the value of the **wPercentDropForError** member of the **CAPTUREPARMS** structure, and then sending the updated structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="835d2-113">Il valore predefinito di **wPercentDropForError** è 10%.</span><span class="sxs-lookup"><span data-stu-id="835d2-113">The default value of **wPercentDropForError** is 10 percent.</span></span>

 

 




