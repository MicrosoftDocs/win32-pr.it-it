---
description: Restituisce l'identificatore univoco del monitoraggio associato a questo output del video.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309057"
---
# <a name="opm_get_output_id"></a><span data-ttu-id="39c79-103">\_ID di \_ output \_ Get di OPM</span><span class="sxs-lookup"><span data-stu-id="39c79-103">OPM\_GET\_OUTPUT\_ID</span></span>

<span data-ttu-id="39c79-104">Restituisce l'identificatore univoco del monitoraggio associato a questo output del video.</span><span class="sxs-lookup"><span data-stu-id="39c79-104">Returns the unique identifier of the monitor associated with this video output.</span></span>



| <span data-ttu-id="39c79-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c79-105">Requirement</span></span> | <span data-ttu-id="39c79-106">Valore</span><span class="sxs-lookup"><span data-stu-id="39c79-106">Value</span></span> |
|--------------|------------------------------------------------------------------|
| <span data-ttu-id="39c79-107">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="39c79-107">Request GUID</span></span> | <span data-ttu-id="39c79-108">\_ID di \_ output \_ Get di OPM</span><span class="sxs-lookup"><span data-stu-id="39c79-108">OPM\_GET\_OUTPUT\_ID</span></span>                                             |
| <span data-ttu-id="39c79-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="39c79-109">Input data</span></span>   | <span data-ttu-id="39c79-110">nessuno</span><span class="sxs-lookup"><span data-stu-id="39c79-110">None</span></span>                                                             |
| <span data-ttu-id="39c79-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="39c79-111">Return data</span></span>  | <span data-ttu-id="39c79-112">Struttura [**\_ \_ \_ dei dati dell'ID di output di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)</span><span class="sxs-lookup"><span data-stu-id="39c79-112">An [**OPM\_OUTPUT\_ID\_DATA**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="39c79-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="39c79-113">Remarks</span></span>

<span data-ttu-id="39c79-114">Il driver video assegna un identificatore univoco a ogni monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="39c79-114">The video driver assigns a unique identifier to each monitor.</span></span> <span data-ttu-id="39c79-115">Questa query restituisce l'identificatore per il monitoraggio associato al puntatore [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) corrente.</span><span class="sxs-lookup"><span data-stu-id="39c79-115">This query returns the identifier for the monitor that is associated with the current [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c79-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39c79-116">Requirements</span></span>



| <span data-ttu-id="39c79-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c79-117">Requirement</span></span> | <span data-ttu-id="39c79-118">Valore</span><span class="sxs-lookup"><span data-stu-id="39c79-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39c79-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39c79-119">Minimum supported client</span></span><br/> | <span data-ttu-id="39c79-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39c79-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="39c79-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39c79-121">Minimum supported server</span></span><br/> | <span data-ttu-id="39c79-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="39c79-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="39c79-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39c79-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c79-124"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c79-124"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c79-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39c79-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c79-126">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="39c79-126">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="39c79-127">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="39c79-127">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




