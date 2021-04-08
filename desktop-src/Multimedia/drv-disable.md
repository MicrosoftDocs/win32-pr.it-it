---
title: Messaggio DRV_DISABLE (mmsystem. h)
description: Disabilita il driver. Il driver deve inserire il dispositivo corrispondente, se presente, in uno stato inattivo e terminare eventuali funzioni di callback o thread.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964920"
---
# <a name="drv_disable-message"></a><span data-ttu-id="29195-105">\_Messaggio di disabilitazione DRV</span><span class="sxs-lookup"><span data-stu-id="29195-105">DRV\_DISABLE message</span></span>

<span data-ttu-id="29195-106">Disabilita il driver.</span><span class="sxs-lookup"><span data-stu-id="29195-106">Disables the driver.</span></span> <span data-ttu-id="29195-107">Il driver deve inserire il dispositivo corrispondente, se presente, in uno stato inattivo e terminare eventuali funzioni di callback o thread.</span><span class="sxs-lookup"><span data-stu-id="29195-107">The driver should place the corresponding device, if any, in an inactive state and terminate any callback functions or threads.</span></span>

## <a name="parameters"></a><span data-ttu-id="29195-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="29195-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29195-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="29195-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="29195-110">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="29195-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29195-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29195-111">Return Value</span></span>

<span data-ttu-id="29195-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="29195-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29195-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="29195-113">Remarks</span></span>

<span data-ttu-id="29195-114">I parametri *dwDriverId*, *lParam1* e *lParam2* non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="29195-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="29195-115">Dopo la disabilitazione del driver, il sistema invia in genere al driver un messaggio [**drv \_ libero**](drv-free.md) prima di rimuovere il driver dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="29195-115">After disabling the driver, the system typically sends the driver a [**DRV\_FREE**](drv-free.md) message before removing the driver from memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="29195-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29195-116">Requirements</span></span>



| <span data-ttu-id="29195-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="29195-117">Requirement</span></span> | <span data-ttu-id="29195-118">Valore</span><span class="sxs-lookup"><span data-stu-id="29195-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29195-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29195-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29195-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="29195-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="29195-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29195-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29195-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="29195-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="29195-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29195-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="29195-124"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29195-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29195-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29195-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29195-126">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="29195-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="29195-127">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="29195-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





