---
title: Messaggio DRV_QUERYCONFIGURE (mmsystem. h)
description: Indica al driver di specificare se supporta la configurazione personalizzata.
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- DRV_QUERYCONFIGURE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_QUERYCONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66780106fdd42364d247db534a838842f25dc16a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225232"
---
# <a name="drv_queryconfigure-message"></a><span data-ttu-id="ce863-104">\_Messaggio QUERYCONFIGURE DRV</span><span class="sxs-lookup"><span data-stu-id="ce863-104">DRV\_QUERYCONFIGURE message</span></span>

<span data-ttu-id="ce863-105">Indica al driver di specificare se supporta la configurazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ce863-105">Directs the driver to specify whether it supports custom configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce863-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce863-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce863-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="ce863-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="ce863-108">Identificatore del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="ce863-108">Identifier of the installable driver.</span></span> <span data-ttu-id="ce863-109">Si tratta dello stesso valore restituito in precedenza dal driver dal messaggio [**\_ aperto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="ce863-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="ce863-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="ce863-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="ce863-111">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="ce863-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce863-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce863-112">Return Value</span></span>

<span data-ttu-id="ce863-113">Restituisce un valore diverso da zero se il driver è in grado di visualizzare una finestra di dialogo di configurazione o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ce863-113">Returns a nonzero value if the driver can display a configuration dialog box or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce863-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce863-114">Remarks</span></span>

<span data-ttu-id="ce863-115">I parametri *lParam1* e *lParam2* non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="ce863-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce863-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce863-116">Requirements</span></span>



| <span data-ttu-id="ce863-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce863-117">Requirement</span></span> | <span data-ttu-id="ce863-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ce863-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce863-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce863-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ce863-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce863-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ce863-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce863-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ce863-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce863-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ce863-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce863-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce863-124"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce863-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce863-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce863-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce863-126">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="ce863-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="ce863-127">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="ce863-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





