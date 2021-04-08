---
title: Messaggio DRV_FREE (mmsystem. h)
description: Notifica al driver che è stata rimossa dalla memoria. Il driver deve liberare memoria e altre risorse di sistema allocate.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- DRV_FREE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964919"
---
# <a name="drv_free-message"></a><span data-ttu-id="651ba-105">\_Messaggio privo di DRV</span><span class="sxs-lookup"><span data-stu-id="651ba-105">DRV\_FREE message</span></span>

<span data-ttu-id="651ba-106">Notifica al driver che è stata rimossa dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="651ba-106">Notifies the driver that it is being removed from memory.</span></span> <span data-ttu-id="651ba-107">Il driver deve liberare memoria e altre risorse di sistema allocate.</span><span class="sxs-lookup"><span data-stu-id="651ba-107">The driver should free any memory and other system resources that it has allocated.</span></span>

## <a name="parameters"></a><span data-ttu-id="651ba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="651ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="651ba-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="651ba-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="651ba-110">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="651ba-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="651ba-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="651ba-111">Return Value</span></span>

<span data-ttu-id="651ba-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="651ba-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="651ba-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="651ba-113">Remarks</span></span>

<span data-ttu-id="651ba-114">I parametri *dwDriverId*, *lParam1* e *lParam2* non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="651ba-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="651ba-115">Il messaggio **drv \_ Free** è sempre l'ultimo messaggio ricevuto da un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="651ba-115">The **DRV\_FREE** message is always the last message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="651ba-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="651ba-116">Requirements</span></span>



| <span data-ttu-id="651ba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="651ba-117">Requirement</span></span> | <span data-ttu-id="651ba-118">Valore</span><span class="sxs-lookup"><span data-stu-id="651ba-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="651ba-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="651ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="651ba-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="651ba-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="651ba-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="651ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="651ba-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="651ba-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="651ba-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="651ba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="651ba-124"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="651ba-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="651ba-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="651ba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="651ba-126">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="651ba-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="651ba-127">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="651ba-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





