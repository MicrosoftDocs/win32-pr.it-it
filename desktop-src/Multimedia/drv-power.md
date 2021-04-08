---
title: Messaggio DRV_POWER (mmsystem. h)
description: Notifica al driver che la potenza del dispositivo viene attivata o disattivata.
ms.assetid: b3bbd16a-5b90-4127-a1dd-f2ddfd918f0a
keywords:
- DRV_POWER messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_POWER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8113b7fe544bf36a35b6e516c7a98ae71082577d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964915"
---
# <a name="drv_power-message"></a><span data-ttu-id="03f6e-104">\_Messaggio di alimentazione DRV</span><span class="sxs-lookup"><span data-stu-id="03f6e-104">DRV\_POWER message</span></span>

<span data-ttu-id="03f6e-105">Notifica al driver che la potenza del dispositivo viene attivata o disattivata.</span><span class="sxs-lookup"><span data-stu-id="03f6e-105">Notifies the driver that power to the device is being turned on or off.</span></span>

## <a name="parameters"></a><span data-ttu-id="03f6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="03f6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03f6e-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="03f6e-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="03f6e-108">Identificatore del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="03f6e-108">Identifier of the installable driver.</span></span> <span data-ttu-id="03f6e-109">Si tratta dello stesso valore restituito in precedenza dal driver dal messaggio [**\_ aperto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="03f6e-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="03f6e-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="03f6e-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="03f6e-111">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="03f6e-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03f6e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03f6e-112">Return Value</span></span>

<span data-ttu-id="03f6e-113">Restituisce un valore diverso da zero in caso di esito positivo o zero.</span><span class="sxs-lookup"><span data-stu-id="03f6e-113">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="03f6e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="03f6e-114">Remarks</span></span>

<span data-ttu-id="03f6e-115">I parametri *lParam1* e *lParam2* non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="03f6e-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="03f6e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03f6e-116">Requirements</span></span>



| <span data-ttu-id="03f6e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="03f6e-117">Requirement</span></span> | <span data-ttu-id="03f6e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="03f6e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03f6e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03f6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="03f6e-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03f6e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="03f6e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03f6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="03f6e-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03f6e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="03f6e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03f6e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="03f6e-124"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03f6e-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f6e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03f6e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f6e-126">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="03f6e-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="03f6e-127">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="03f6e-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





