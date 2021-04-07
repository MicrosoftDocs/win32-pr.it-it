---
title: Messaggio DRV_REMOVE (mmsystem. h)
description: Notifica al driver che sta per essere rimosso dal sistema. Quando un driver riceve questo messaggio, è necessario rimuovere tutte le sezioni create nel registro di sistema.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- DRV_REMOVE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfc94d648f83e618a20323ed7bbe3694616bc06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048745"
---
# <a name="drv_remove-message"></a><span data-ttu-id="a4000-105">DRV- \_ Rimuovi messaggio</span><span class="sxs-lookup"><span data-stu-id="a4000-105">DRV\_REMOVE message</span></span>

<span data-ttu-id="a4000-106">Notifica al driver che sta per essere rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="a4000-106">Notifies the driver that it is about to be removed from the system.</span></span> <span data-ttu-id="a4000-107">Quando un driver riceve questo messaggio, è necessario rimuovere tutte le sezioni create nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a4000-107">When a driver receives this message, it should remove any sections it created in the registry.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4000-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4000-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4000-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="a4000-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="a4000-110">Identificatore del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="a4000-110">Identifier of the installable driver.</span></span> <span data-ttu-id="a4000-111">Si tratta dello stesso valore restituito in precedenza dal driver dal messaggio [**\_ aperto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="a4000-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="a4000-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="a4000-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="a4000-113">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="a4000-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4000-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4000-114">Return Value</span></span>

<span data-ttu-id="a4000-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a4000-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4000-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4000-116">Remarks</span></span>

<span data-ttu-id="a4000-117">I parametri *lParam1* e *lParam2* non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="a4000-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4000-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4000-118">Requirements</span></span>



| <span data-ttu-id="a4000-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4000-119">Requirement</span></span> | <span data-ttu-id="a4000-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a4000-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4000-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4000-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a4000-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a4000-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a4000-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4000-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a4000-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a4000-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a4000-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4000-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4000-126"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4000-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4000-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4000-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4000-128">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="a4000-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="a4000-129">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="a4000-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





