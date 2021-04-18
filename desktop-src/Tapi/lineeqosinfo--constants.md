---
description: Queste costanti vengono utilizzate da un TSP per identificare il risultato di una richiesta QoS (Quality of Service).
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: Costanti LINEEQOSINFO_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331594"
---
# <a name="lineeqosinfo_-constants"></a><span data-ttu-id="38fba-103">\_Costanti LINEEQOSINFO</span><span class="sxs-lookup"><span data-stu-id="38fba-103">LINEEQOSINFO\_ Constants</span></span>

<span data-ttu-id="38fba-104">Queste costanti vengono utilizzate da un TSP per identificare il risultato di una richiesta QoS (Quality of Service).</span><span class="sxs-lookup"><span data-stu-id="38fba-104">These constants are used by a TSP to identify the result of a QoS (Quality of Service) request.</span></span>

<dl> <dt>

<span data-ttu-id="38fba-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**\_NOQOS LINEEQOSINFO**</span><span class="sxs-lookup"><span data-stu-id="38fba-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO\_NOQOS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="38fba-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38fba-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="38fba-107">QoS non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="38fba-107">QoS is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38fba-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**\_ADMISSIONFAILURE LINEEQOSINFO**</span><span class="sxs-lookup"><span data-stu-id="38fba-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO\_ADMISSIONFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="38fba-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="38fba-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="38fba-110">Non è stato possibile soddisfare la richiesta QoS.</span><span class="sxs-lookup"><span data-stu-id="38fba-110">The QoS request could not be met.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38fba-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**\_POLICYFAILURE LINEEQOSINFO**</span><span class="sxs-lookup"><span data-stu-id="38fba-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO\_POLICYFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="38fba-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="38fba-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="38fba-113">Il tipo di QoS richiesto non è supportato.</span><span class="sxs-lookup"><span data-stu-id="38fba-113">The type of QoS requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38fba-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**\_errore generico LINEEQOSINFO**</span><span class="sxs-lookup"><span data-stu-id="38fba-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO\_GENERICERROR**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="38fba-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="38fba-115">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="38fba-116">Errore QoS non specificato.</span><span class="sxs-lookup"><span data-stu-id="38fba-116">Unspecified QoS error.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38fba-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38fba-117">Requirements</span></span>



| <span data-ttu-id="38fba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="38fba-118">Requirement</span></span> | <span data-ttu-id="38fba-119">Valore</span><span class="sxs-lookup"><span data-stu-id="38fba-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="38fba-120">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="38fba-120">TAPI version</span></span><br/> | <span data-ttu-id="38fba-121">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="38fba-121">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="38fba-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38fba-122">Header</span></span><br/>       | <dl> <span data-ttu-id="38fba-123"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="38fba-123"><dt>Tspi.h</dt></span></span> </dl> |



 

 




