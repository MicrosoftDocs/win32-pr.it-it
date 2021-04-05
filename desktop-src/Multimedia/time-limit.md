---
title: Limite di tempo
description: Limite di tempo
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Struttura CAPTUREPARMS
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Struttura CAPTUREPARMS
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714440"
---
# <a name="time-limit"></a><span data-ttu-id="f28d5-109">Limite di tempo</span><span class="sxs-lookup"><span data-stu-id="f28d5-109">Time Limit</span></span>

<span data-ttu-id="f28d5-110">È possibile limitare la durata di un'operazione di acquisizione usando i membri **fLimitEnabled** e **WTimeLimit** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="f28d5-110">You can limit the duration of a capture operation by using the **fLimitEnabled** and **wTimeLimit** members of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="f28d5-111">Il membro **fLimitEnabled** indica se l'operazione di acquisizione deve essere temporizzata, mentre **wTimeLimit** specifica la durata massima dell'operazione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f28d5-111">The **fLimitEnabled** member indicates whether the capture operation is to be timed, while **wTimeLimit** specifies the maximum duration of the capture operation.</span></span>

<span data-ttu-id="f28d5-112">È possibile recuperare i valori per **fLimitEnabled** e **wTimeLimit** usando il messaggio di [**installazione della sequenza di WM \_ Cap \_ \_ \_ Get**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="f28d5-112">You can retrieve the values for **fLimitEnabled** and **wTimeLimit** by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="f28d5-113">È possibile abilitare un timer per l'operazione di acquisizione specificando **true** come valore di **fLimitEnabled** oppure è possibile impostare la durata dell'operazione di acquisizione specificando un valore, in secondi, per **wTimeLimit**.</span><span class="sxs-lookup"><span data-stu-id="f28d5-113">You can enable a timer for the capture operation by specifying **TRUE** as the value of **fLimitEnabled**, or you can set the duration of the capture operation by specifying a value, in seconds, for **wTimeLimit**.</span></span> <span data-ttu-id="f28d5-114">Dopo aver impostato questi membri, inviare la struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) aggiornata alla finestra di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_ del set**](wm-cap-set-sequence-setup.md) di test WM (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="f28d5-114">After you set these members, send the updated [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="f28d5-115">Il valore predefinito di **fLimitEnabled** è **false**.</span><span class="sxs-lookup"><span data-stu-id="f28d5-115">The default value of **fLimitEnabled** is **FALSE**.</span></span>

 

 




