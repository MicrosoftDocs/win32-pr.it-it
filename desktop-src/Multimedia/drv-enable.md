---
title: Messaggio DRV_ENABLE (mmsystem. h)
description: Consente di abilitare il driver. Il driver deve inizializzare qualsiasi variabile e individuare i dispositivi con l'interfaccia di input e output (I/O).
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964922"
---
# <a name="drv_enable-message"></a><span data-ttu-id="d8ff4-105">\_Messaggio di abilitazione DRV</span><span class="sxs-lookup"><span data-stu-id="d8ff4-105">DRV\_ENABLE message</span></span>

<span data-ttu-id="d8ff4-106">Consente di abilitare il driver.</span><span class="sxs-lookup"><span data-stu-id="d8ff4-106">Enables the driver.</span></span> <span data-ttu-id="d8ff4-107">Il driver deve inizializzare qualsiasi variabile e individuare i dispositivi con l'interfaccia di input e output (I/O).</span><span class="sxs-lookup"><span data-stu-id="d8ff4-107">The driver should initialize any variables and locate devices with the input and output (I/O) interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="d8ff4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8ff4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8ff4-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="d8ff4-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="d8ff4-110">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="d8ff4-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8ff4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8ff4-111">Return Value</span></span>

<span data-ttu-id="d8ff4-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="d8ff4-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8ff4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8ff4-113">Remarks</span></span>

<span data-ttu-id="d8ff4-114">I parametri *dwDriverId*, *lParam1* e *lParam2* non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="d8ff4-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="d8ff4-115">I driver vengono considerati abilitati dal momento in cui ricevono questo messaggio finché non vengono disabilitati usando il messaggio di [**\_ disabilitazione DRV**](drv-disable.md) .</span><span class="sxs-lookup"><span data-stu-id="d8ff4-115">Drivers are considered enabled from the time they receive this message until they are disabled by using the [**DRV\_DISABLE**](drv-disable.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ff4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8ff4-116">Requirements</span></span>



| <span data-ttu-id="d8ff4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8ff4-117">Requirement</span></span> | <span data-ttu-id="d8ff4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d8ff4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ff4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8ff4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ff4-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8ff4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d8ff4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8ff4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ff4-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8ff4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d8ff4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8ff4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8ff4-124"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8ff4-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ff4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8ff4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ff4-126">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="d8ff4-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="d8ff4-127">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="d8ff4-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





