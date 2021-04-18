---
title: Messaggio DRV_CLOSE (mmsystem. h)
description: Indica al driver di chiudere l'istanza di specificata. Se non sono aperte altre istanze, il driver deve prepararsi per la versione successiva dalla memoria.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- DRV_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a205b7e6edb4a427b0e80d32cc711d9bf2b052c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302634"
---
# <a name="drv_close-message"></a><span data-ttu-id="a2aa0-105">\_Messaggio di chiusura DRV</span><span class="sxs-lookup"><span data-stu-id="a2aa0-105">DRV\_CLOSE message</span></span>

<span data-ttu-id="a2aa0-106">Indica al driver di chiudere l'istanza di specificata.</span><span class="sxs-lookup"><span data-stu-id="a2aa0-106">Directs the driver to close the given instance.</span></span> <span data-ttu-id="a2aa0-107">Se non sono aperte altre istanze, il driver deve prepararsi per la versione successiva dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="a2aa0-107">If no other instances are open, the driver should prepare for subsequent release from memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2aa0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2aa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2aa0-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="a2aa0-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="a2aa0-110">Identificatore del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="a2aa0-110">Identifier of the installable driver.</span></span> <span data-ttu-id="a2aa0-111">Si tratta dello stesso valore restituito in precedenza dal driver dal messaggio [**\_ aperto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="a2aa0-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="a2aa0-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="a2aa0-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="a2aa0-113">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="a2aa0-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="a2aa0-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a2aa0-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a2aa0-115">valore a 32 bit specificato come parametro *lParam1* in una chiamata alla funzione **DriverClose** .</span><span class="sxs-lookup"><span data-stu-id="a2aa0-115">32-bit value specified as the *lParam1* parameter in a call to the **DriverClose** function.</span></span>

</dd> <dt>

<span data-ttu-id="a2aa0-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a2aa0-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a2aa0-117">valore a 32 bit specificato come parametro *lParam2* in una chiamata alla funzione **DriverClose** .</span><span class="sxs-lookup"><span data-stu-id="a2aa0-117">32-bit value specified as the *lParam2* parameter in a call to the **DriverClose** function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2aa0-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2aa0-118">Return Value</span></span>

<span data-ttu-id="a2aa0-119">Restituisce un valore diverso da zero in caso di esito positivo o zero.</span><span class="sxs-lookup"><span data-stu-id="a2aa0-119">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2aa0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2aa0-120">Requirements</span></span>



| <span data-ttu-id="a2aa0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2aa0-121">Requirement</span></span> | <span data-ttu-id="a2aa0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a2aa0-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2aa0-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2aa0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2aa0-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a2aa0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a2aa0-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2aa0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2aa0-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a2aa0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a2aa0-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2aa0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2aa0-128"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2aa0-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2aa0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2aa0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2aa0-130">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="a2aa0-130">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="a2aa0-131">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="a2aa0-131">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





