---
description: Restituisce il tipo di bus di I/O usato dall'output del video.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309059"
---
# <a name="opm_get_adapter_bus_type"></a><span data-ttu-id="61a54-103">\_tipo di \_ bus di adapter \_ \_ per OPM Get</span><span class="sxs-lookup"><span data-stu-id="61a54-103">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>

<span data-ttu-id="61a54-104">Restituisce il tipo di bus di I/O usato dall'output del video.</span><span class="sxs-lookup"><span data-stu-id="61a54-104">Returns the type of I/O bus used by the video output.</span></span>



| <span data-ttu-id="61a54-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a54-105">Requirement</span></span> | <span data-ttu-id="61a54-106">Valore</span><span class="sxs-lookup"><span data-stu-id="61a54-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="61a54-107">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="61a54-107">Request GUID</span></span> | <span data-ttu-id="61a54-108">\_tipo di \_ bus di adapter \_ \_ per OPM Get</span><span class="sxs-lookup"><span data-stu-id="61a54-108">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>                                                |
| <span data-ttu-id="61a54-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="61a54-109">Input data</span></span>   | <span data-ttu-id="61a54-110">nessuno</span><span class="sxs-lookup"><span data-stu-id="61a54-110">None</span></span>                                                                        |
| <span data-ttu-id="61a54-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="61a54-111">Return data</span></span>  | <span data-ttu-id="61a54-112">Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="61a54-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="61a54-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="61a54-113">Remarks</span></span>

<span data-ttu-id="61a54-114">Il tipo di bus viene restituito nel membro **ulInformation** della struttura [**di \_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="61a54-114">The bus type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="61a54-115">Il valore è **un operatore OR** bit per bit di flag di [**tipo bus OPM**](opm-bus-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="61a54-115">The value is a bitwise **OR** of [**OPM Bus Type Flags**](opm-bus-type-flags.md).</span></span>

<span data-ttu-id="61a54-116">Questa query equivale alla \_ query DXVA COPPQueryBusData utilizzata in Certified Output Protocol (Copp).</span><span class="sxs-lookup"><span data-stu-id="61a54-116">This query is equivalent to the DXVA\_COPPQueryBusData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="61a54-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61a54-117">Requirements</span></span>



| <span data-ttu-id="61a54-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a54-118">Requirement</span></span> | <span data-ttu-id="61a54-119">Valore</span><span class="sxs-lookup"><span data-stu-id="61a54-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="61a54-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61a54-120">Minimum supported client</span></span><br/> | <span data-ttu-id="61a54-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61a54-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="61a54-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61a54-122">Minimum supported server</span></span><br/> | <span data-ttu-id="61a54-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61a54-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="61a54-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61a54-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="61a54-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="61a54-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61a54-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61a54-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a54-127">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="61a54-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="61a54-128">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="61a54-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="61a54-129">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="61a54-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




