---
description: Specifica le informazioni sul segnale video, oltre al livello di protezione.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527876"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a><span data-ttu-id="3fd92-103">il \_ set \_ di OPM ACP \_ e la \_ \_ segnalazione CGMSA</span><span class="sxs-lookup"><span data-stu-id="3fd92-103">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="3fd92-104">Specifica le informazioni sul segnale video, oltre al livello di protezione.</span><span class="sxs-lookup"><span data-stu-id="3fd92-104">Specifies information about the video signal, other than the protection level.</span></span>



| <span data-ttu-id="3fd92-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd92-105">Requirement</span></span> | <span data-ttu-id="3fd92-106">Valore</span><span class="sxs-lookup"><span data-stu-id="3fd92-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd92-107">GUID comando</span><span class="sxs-lookup"><span data-stu-id="3fd92-107">Command GUID</span></span> | <span data-ttu-id="3fd92-108">il \_ set \_ di OPM ACP \_ e la \_ \_ segnalazione CGMSA</span><span class="sxs-lookup"><span data-stu-id="3fd92-108">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                                                |
| <span data-ttu-id="3fd92-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="3fd92-109">Input data</span></span>   | <span data-ttu-id="3fd92-110">Struttura [**di \_ \_ parametri di \_ \_ \_ segnalazione \_ ACP e CGMSA di un set OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters)</span><span class="sxs-lookup"><span data-stu-id="3fd92-110">An [**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3fd92-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fd92-111">Remarks</span></span>

<span data-ttu-id="3fd92-112">Questo comando equivale al \_ comando DXVA COPPSetSignaling usato in Certified Output Protocol (Copp).</span><span class="sxs-lookup"><span data-stu-id="3fd92-112">This command is equivalent to the DXVA\_COPPSetSignaling command used in Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="3fd92-113">Per CGMS-A, determinati standard di protezione richiedono che il segnale televisivo includa informazioni all'interno degli stessi pacchetti di forma d'onda VBI dei bit CGMS-A.</span><span class="sxs-lookup"><span data-stu-id="3fd92-113">For CGMS-A, certain protection standards require that the television signal contain information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="3fd92-114">Tra le altre cose, queste informazioni includono le proporzioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="3fd92-114">Among other things, this information includes the picture aspect ratio.</span></span> <span data-ttu-id="3fd92-115">I televisori potrebbero non essere visualizzati correttamente se le informazioni sulle proporzioni non sono coerenti con il flusso video.</span><span class="sxs-lookup"><span data-stu-id="3fd92-115">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="3fd92-116">L'applicazione può utilizzare questo comando per specificare le proporzioni in modo che il driver di grafica possa generare i pacchetti VBI corretti.</span><span class="sxs-lookup"><span data-stu-id="3fd92-116">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd92-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fd92-117">Requirements</span></span>



| <span data-ttu-id="3fd92-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd92-118">Requirement</span></span> | <span data-ttu-id="3fd92-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3fd92-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd92-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fd92-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd92-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fd92-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3fd92-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fd92-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd92-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3fd92-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3fd92-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fd92-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd92-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd92-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd92-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fd92-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd92-127">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="3fd92-127">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="3fd92-128">Comandi di OPM</span><span class="sxs-lookup"><span data-stu-id="3fd92-128">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




