---
description: Restituisce il tipo di connettore fisico dell'output del video.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226521"
---
# <a name="opm_get_connector_type"></a><span data-ttu-id="710c6-103">\_tipo di \_ connettore OPM Get \_</span><span class="sxs-lookup"><span data-stu-id="710c6-103">OPM\_GET\_CONNECTOR\_TYPE</span></span>

<span data-ttu-id="710c6-104">Restituisce il tipo di connettore fisico dell'output del video.</span><span class="sxs-lookup"><span data-stu-id="710c6-104">Returns the physical connector type of the video output.</span></span>



| <span data-ttu-id="710c6-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="710c6-105">Requirement</span></span> | <span data-ttu-id="710c6-106">Valore</span><span class="sxs-lookup"><span data-stu-id="710c6-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="710c6-107">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="710c6-107">Request GUID</span></span> | <span data-ttu-id="710c6-108">\_tipo di \_ connettore OPM Get \_</span><span class="sxs-lookup"><span data-stu-id="710c6-108">OPM\_GET\_CONNECTOR\_TYPE</span></span>                                                   |
| <span data-ttu-id="710c6-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="710c6-109">Input data</span></span>   | <span data-ttu-id="710c6-110">nessuno</span><span class="sxs-lookup"><span data-stu-id="710c6-110">None</span></span>                                                                        |
| <span data-ttu-id="710c6-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="710c6-111">Return data</span></span>  | <span data-ttu-id="710c6-112">Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="710c6-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="710c6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="710c6-113">Remarks</span></span>

<span data-ttu-id="710c6-114">Il tipo di connettore viene restituito nel membro **ulInformation** della struttura [**di \_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="710c6-114">The connector type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="710c6-115">Il valore di **ulInformation** è uguale a uno dei tipi di connettore elencati nei [**flag di tipo del connettore OPM**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="710c6-115">The value of **ulInformation** is equal to one of the connector types listed in [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="710c6-116">In modalità di emulazione COPP, il tipo di connettore può essere combinato con il flag **interno del tipo di connettore di OPM \_ Copp \_ compatibile \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="710c6-116">In COPP emulation mode, the connector type might be combined with the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="710c6-117">Usare un operatore **and** bit per bit per estrarre il tipo di connettore:</span><span class="sxs-lookup"><span data-stu-id="710c6-117">Use a bitwise **AND** to extract the connector type:</span></span>

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

<span data-ttu-id="710c6-118">Le applicazioni devono ignorare il flag **\_ interno del \_ \_ \_ tipo \_ di connettore con compatibilità OPM Copp** .</span><span class="sxs-lookup"><span data-stu-id="710c6-118">Applications should ignore the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="710c6-119">Per ulteriori informazioni, vedere la sezione Osservazioni dei [**flag del tipo di connettore OPM**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="710c6-119">For more information, see the Remarks section of [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="710c6-120">Questa query equivale alla \_ query DXVA COPPQueryConnectorType utilizzata in Certified Output Protocol (Copp).</span><span class="sxs-lookup"><span data-stu-id="710c6-120">This query is equivalent to the DXVA\_COPPQueryConnectorType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="710c6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="710c6-121">Requirements</span></span>



| <span data-ttu-id="710c6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="710c6-122">Requirement</span></span> | <span data-ttu-id="710c6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="710c6-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="710c6-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="710c6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="710c6-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="710c6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="710c6-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="710c6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="710c6-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="710c6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="710c6-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="710c6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="710c6-129"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="710c6-129"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="710c6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="710c6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="710c6-131">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="710c6-131">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="710c6-132">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="710c6-132">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="710c6-133">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="710c6-133">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




