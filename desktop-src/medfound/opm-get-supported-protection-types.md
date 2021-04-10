---
description: Restituisce l'elenco dei meccanismi di protezione supportati dal connettore.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc79b33673e34d00914b84165d915baa0d8f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966985"
---
# <a name="opm_get_supported_protection_types"></a><span data-ttu-id="02d00-103">OPM \_ ottenere \_ i \_ tipi di protezione supportati \_</span><span class="sxs-lookup"><span data-stu-id="02d00-103">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>

<span data-ttu-id="02d00-104">Restituisce l'elenco dei meccanismi di protezione supportati dal connettore.</span><span class="sxs-lookup"><span data-stu-id="02d00-104">Returns the list of protection mechanisms that are supported by the connector.</span></span>



| <span data-ttu-id="02d00-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="02d00-105">Requirement</span></span> | <span data-ttu-id="02d00-106">Valore</span><span class="sxs-lookup"><span data-stu-id="02d00-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="02d00-107">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="02d00-107">Request GUID</span></span> | <span data-ttu-id="02d00-108">OPM \_ ottenere \_ i \_ tipi di protezione supportati \_</span><span class="sxs-lookup"><span data-stu-id="02d00-108">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>                                      |
| <span data-ttu-id="02d00-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="02d00-109">Input data</span></span>   | <span data-ttu-id="02d00-110">nessuno</span><span class="sxs-lookup"><span data-stu-id="02d00-110">None</span></span>                                                                        |
| <span data-ttu-id="02d00-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="02d00-111">Return data</span></span>  | <span data-ttu-id="02d00-112">Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="02d00-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="02d00-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="02d00-113">Remarks</span></span>

<span data-ttu-id="02d00-114">I meccanismi di protezione vengono restituiti nel membro **ulInformation** della struttura [**di \_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="02d00-114">The protection mechanisms are returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="02d00-115">Il valore è **un operatore OR** bit per bit di flag di [tipo protezione OPM](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="02d00-115">The value is a bitwise **OR** of [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span>

<span data-ttu-id="02d00-116">Questa query equivale alla \_ query DXVA COPPQueryProtectionType utilizzata in Certified Output Protocol (Copp).</span><span class="sxs-lookup"><span data-stu-id="02d00-116">This query is equivalent to the DXVA\_COPPQueryProtectionType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="02d00-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02d00-117">Requirements</span></span>



| <span data-ttu-id="02d00-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="02d00-118">Requirement</span></span> | <span data-ttu-id="02d00-119">Valore</span><span class="sxs-lookup"><span data-stu-id="02d00-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="02d00-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02d00-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02d00-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02d00-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="02d00-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02d00-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02d00-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="02d00-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="02d00-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02d00-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="02d00-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="02d00-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02d00-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02d00-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d00-127">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="02d00-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="02d00-128">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="02d00-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="02d00-129">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="02d00-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




