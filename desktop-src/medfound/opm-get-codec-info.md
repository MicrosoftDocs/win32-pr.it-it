---
description: Ottiene il valore di Merit di un codec hardware.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226522"
---
# <a name="opm_get_codec_info"></a><span data-ttu-id="ce54f-103">\_informazioni sul \_ codec di Get di OPM \_</span><span class="sxs-lookup"><span data-stu-id="ce54f-103">OPM\_GET\_CODEC\_INFO</span></span>

<span data-ttu-id="ce54f-104">Ottiene il valore di Merit di un codec hardware.</span><span class="sxs-lookup"><span data-stu-id="ce54f-104">Gets the merit value of a hardware codec.</span></span>



| <span data-ttu-id="ce54f-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce54f-105">Requirement</span></span> | <span data-ttu-id="ce54f-106">Valore</span><span class="sxs-lookup"><span data-stu-id="ce54f-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce54f-107">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="ce54f-107">Request GUID</span></span> | <span data-ttu-id="ce54f-108">**\_informazioni sul \_ codec di Get di OPM \_**</span><span class="sxs-lookup"><span data-stu-id="ce54f-108">**OPM\_GET\_CODEC\_INFO**</span></span>                                                                 |
| <span data-ttu-id="ce54f-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="ce54f-109">Input data</span></span>   | <span data-ttu-id="ce54f-110">Una struttura di [**\_ parametri di \_ \_ informazioni \_ sul codec Get di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)</span><span class="sxs-lookup"><span data-stu-id="ce54f-110">An [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure</span></span>   |
| <span data-ttu-id="ce54f-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="ce54f-111">Return data</span></span>  | <span data-ttu-id="ce54f-112">Struttura [**di \_ \_ \_ \_ informazioni sul codec Get di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)</span><span class="sxs-lookup"><span data-stu-id="ce54f-112">An [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ce54f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce54f-113">Remarks</span></span>

<span data-ttu-id="ce54f-114">Sebbene questo comando usi l'interfaccia di [Output Protection Manager](output-protection-manager.md) (OPM), si applica solo a codificatori e decodificatori hardware.</span><span class="sxs-lookup"><span data-stu-id="ce54f-114">Although this command uses the [Output Protection Manager](output-protection-manager.md) (OPM) interface, it applies only to hardware encoders and decoders.</span></span> <span data-ttu-id="ce54f-115">Non si applica ai dispositivi di output video.</span><span class="sxs-lookup"><span data-stu-id="ce54f-115">It does not apply to video output devices.</span></span>

<span data-ttu-id="ce54f-116">In genere, non usare direttamente questo comando.</span><span class="sxs-lookup"><span data-stu-id="ce54f-116">Generally, you should not use this command directly.</span></span> <span data-ttu-id="ce54f-117">Per ottenere il valore di Merit per un codec hardware, chiamare la funzione [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .</span><span class="sxs-lookup"><span data-stu-id="ce54f-117">To get the merit value for a hardware codec, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span> <span data-ttu-id="ce54f-118">Questa funzione esegue tutte le chiamate OPM necessarie per inviare il comando **OPM \_ get \_ codec \_ info** .</span><span class="sxs-lookup"><span data-stu-id="ce54f-118">This function performs all of the OPM calls needed to send the **OPM\_GET\_CODEC\_INFO** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce54f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce54f-119">Requirements</span></span>



| <span data-ttu-id="ce54f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce54f-120">Requirement</span></span> | <span data-ttu-id="ce54f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ce54f-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ce54f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce54f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce54f-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ce54f-123">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ce54f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce54f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce54f-125">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce54f-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ce54f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce54f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce54f-127"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce54f-127"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce54f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce54f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce54f-129">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="ce54f-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> <dt>

[<span data-ttu-id="ce54f-130">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="ce54f-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="ce54f-131">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="ce54f-131">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




