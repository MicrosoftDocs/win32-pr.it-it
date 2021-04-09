---
description: Esegue una query se un connettore DVI (Digital Video Interface) supporta la versione DVI 1,1 o successiva.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049657"
---
# <a name="opm_get_dvi_characteristics"></a><span data-ttu-id="4afee-103">\_caratteristiche di Get \_ DVI \_ per OPM</span><span class="sxs-lookup"><span data-stu-id="4afee-103">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>

<span data-ttu-id="4afee-104">Esegue una query se un connettore DVI (Digital Video Interface) supporta la versione DVI 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="4afee-104">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>



| <span data-ttu-id="4afee-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="4afee-105">Requirement</span></span> | <span data-ttu-id="4afee-106">Valore</span><span class="sxs-lookup"><span data-stu-id="4afee-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="4afee-107">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="4afee-107">Request GUID</span></span> | <span data-ttu-id="4afee-108">\_caratteristiche di Get \_ DVI \_ per OPM</span><span class="sxs-lookup"><span data-stu-id="4afee-108">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>                                              |
| <span data-ttu-id="4afee-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="4afee-109">Input data</span></span>   | <span data-ttu-id="4afee-110">nessuno</span><span class="sxs-lookup"><span data-stu-id="4afee-110">None</span></span>                                                                        |
| <span data-ttu-id="4afee-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="4afee-111">Return data</span></span>  | <span data-ttu-id="4afee-112">Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="4afee-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4afee-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4afee-113">Remarks</span></span>

<span data-ttu-id="4afee-114">Se la query ha esito positivo, il membro **ulInformation** della struttura di [**\_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4afee-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains one of the following values.</span></span>



| <span data-ttu-id="4afee-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4afee-115">Value</span></span>                                     | <span data-ttu-id="4afee-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4afee-116">Description</span></span>               |
|-------------------------------------------|---------------------------|
| <span data-ttu-id="4afee-117">Caratteristica di OPM \_ DVI \_ \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4afee-117">OPM\_DVI\_CHARACTERISTIC\_1\_0</span></span>            | <span data-ttu-id="4afee-118">Versione 1,0 di DVI.</span><span class="sxs-lookup"><span data-stu-id="4afee-118">DVI version 1.0.</span></span>          |
| <span data-ttu-id="4afee-119">Caratteristiche di OPM \_ DVI \_ \_ 1 \_ 1 \_ o versione \_ successiva</span><span class="sxs-lookup"><span data-stu-id="4afee-119">OPM\_DVI\_CHARACTERISTIC\_1\_1\_OR\_ABOVE</span></span> | <span data-ttu-id="4afee-120">DVI versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="4afee-120">DVI version 1.1 or later.</span></span> |



 

<span data-ttu-id="4afee-121">Questa query è supportata solo quando il tipo di connettore fisico è il tipo di connettore OPM \_ \_ \_ DVI.</span><span class="sxs-lookup"><span data-stu-id="4afee-121">This query is supported only when the physical connector type is OPM\_CONNECTOR\_TYPE\_DVI.</span></span> <span data-ttu-id="4afee-122">Per ottenere il tipo di connettore, inviare la query del [**\_ tipo di \_ connettore \_ OPM Get**](opm-get-connector-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4afee-122">To get the connector type, send the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) query.</span></span>

## <a name="requirements"></a><span data-ttu-id="4afee-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4afee-123">Requirements</span></span>



| <span data-ttu-id="4afee-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4afee-124">Requirement</span></span> | <span data-ttu-id="4afee-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4afee-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4afee-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4afee-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4afee-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4afee-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4afee-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4afee-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4afee-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4afee-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4afee-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4afee-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4afee-131"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4afee-131"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4afee-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4afee-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4afee-133">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="4afee-133">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="4afee-134">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="4afee-134">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




