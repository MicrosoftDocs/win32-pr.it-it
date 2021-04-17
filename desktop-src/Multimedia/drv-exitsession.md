---
title: Messaggio DRV_EXITSESSION (mmsystem. h)
description: Notifica al driver che Windows sta preparando la chiusura. Il driver deve prepararsi per la chiusura.
ms.assetid: 8d200d64-b89b-47f1-ad21-ab86987efa4b
keywords:
- DRV_EXITSESSION messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_EXITSESSION
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236da457541af2d594bc708caf5b5ed07e58cc04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479150"
---
# <a name="drv_exitsession-message"></a><span data-ttu-id="f7a4d-105">\_Messaggio EXITSESSION DRV</span><span class="sxs-lookup"><span data-stu-id="f7a4d-105">DRV\_EXITSESSION message</span></span>

<span data-ttu-id="f7a4d-106">Notifica al driver che Windows sta preparando la chiusura.</span><span class="sxs-lookup"><span data-stu-id="f7a4d-106">Notifies the driver that Windows is preparing to exit.</span></span> <span data-ttu-id="f7a4d-107">Il driver deve prepararsi per la chiusura.</span><span class="sxs-lookup"><span data-stu-id="f7a4d-107">The driver should prepare for termination.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7a4d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7a4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7a4d-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="f7a4d-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="f7a4d-110">Identificatore del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="f7a4d-110">Identifier of the installable driver.</span></span> <span data-ttu-id="f7a4d-111">Si tratta dello stesso valore restituito in precedenza dal driver dal messaggio [**\_ aperto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="f7a4d-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="f7a4d-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="f7a4d-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="f7a4d-113">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="f7a4d-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7a4d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7a4d-114">Return Value</span></span>

<span data-ttu-id="f7a4d-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f7a4d-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7a4d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7a4d-116">Remarks</span></span>

<span data-ttu-id="f7a4d-117">I parametri *lParam1* e *lParam2* non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="f7a4d-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7a4d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7a4d-118">Requirements</span></span>



| <span data-ttu-id="f7a4d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7a4d-119">Requirement</span></span> | <span data-ttu-id="f7a4d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f7a4d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a4d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7a4d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f7a4d-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7a4d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f7a4d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7a4d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f7a4d-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7a4d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f7a4d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7a4d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7a4d-126"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7a4d-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7a4d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7a4d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a4d-128">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="f7a4d-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="f7a4d-129">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="f7a4d-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





