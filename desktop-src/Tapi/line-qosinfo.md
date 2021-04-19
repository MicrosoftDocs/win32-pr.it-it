---
description: Il messaggio QOSINFO della riga TSPI \_ fa sì che TAPI generi un evento QoS. Per ulteriori informazioni, vedere ITQOSEvent.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Messaggio LINE_QOSINFO (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328910"
---
# <a name="line_qosinfo-message"></a><span data-ttu-id="5d799-104">\_Messaggio linea QOSINFO</span><span class="sxs-lookup"><span data-stu-id="5d799-104">LINE\_QOSINFO message</span></span>

<span data-ttu-id="5d799-105">Il messaggio **\_ QOSINFO della riga** TSPI fa sì che TAPI generi un evento QoS.</span><span class="sxs-lookup"><span data-stu-id="5d799-105">The TSPI **LINE\_QOSINFO** message causes TAPI to fire a QOS event.</span></span> <span data-ttu-id="5d799-106">Per ulteriori informazioni, vedere [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) .</span><span class="sxs-lookup"><span data-stu-id="5d799-106">See [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) for additional information.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="5d799-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d799-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d799-108">*htLine*</span><span class="sxs-lookup"><span data-stu-id="5d799-108">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="5d799-109">Handle TAPI per la riga.</span><span class="sxs-lookup"><span data-stu-id="5d799-109">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="5d799-110">*htCall*</span><span class="sxs-lookup"><span data-stu-id="5d799-110">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="5d799-111">Handle TAPI per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d799-111">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="5d799-112">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="5d799-112">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="5d799-113">RIGA del valore \_ QOSINFO.</span><span class="sxs-lookup"><span data-stu-id="5d799-113">The value LINE\_QOSINFO.</span></span>

</dd> <dt>

<span data-ttu-id="5d799-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5d799-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="5d799-115">Membro dell'enumeratore [**di \_ eventi QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) che identifica il tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="5d799-115">A member of the [**QOS\_EVENT**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) enumerator that identifies the type of event.</span></span>

</dd> <dt>

<span data-ttu-id="5d799-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5d799-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="5d799-117">Costante del [tipo di supporto](./tapiprotocol--constants.md) che identifica il supporto della chiamata associata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="5d799-117">A [media type](./tapiprotocol--constants.md) constant that identifies the media of the call associated with this event.</span></span>

</dd> <dt>

<span data-ttu-id="5d799-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="5d799-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="5d799-119">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5d799-119">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d799-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d799-120">Requirements</span></span>



| <span data-ttu-id="5d799-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d799-121">Requirement</span></span> | <span data-ttu-id="5d799-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5d799-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5d799-123">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5d799-123">TAPI version</span></span><br/> | <span data-ttu-id="5d799-124">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="5d799-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="5d799-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d799-125">Header</span></span><br/>       | <dl> <span data-ttu-id="5d799-126"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d799-126"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d799-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d799-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d799-128">**\_evento QoS**</span><span class="sxs-lookup"><span data-stu-id="5d799-128">**QOS\_EVENT**</span></span>](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[<span data-ttu-id="5d799-129">**ITQOSEvent**</span><span class="sxs-lookup"><span data-stu-id="5d799-129">**ITQOSEvent**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

