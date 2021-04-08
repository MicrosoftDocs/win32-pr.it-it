---
title: Messaggio DRV_LOAD (mmsystem. h)
description: Notifica al driver che è stato caricato. Il driver deve verificare che siano presenti hardware e driver di supporto necessari per il corretto funzionamento.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- DRV_LOAD messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964917"
---
# <a name="drv_load-message"></a><span data-ttu-id="a279d-105">\_Messaggio di caricamento DRV</span><span class="sxs-lookup"><span data-stu-id="a279d-105">DRV\_LOAD message</span></span>

<span data-ttu-id="a279d-106">Notifica al driver che è stato caricato.</span><span class="sxs-lookup"><span data-stu-id="a279d-106">Notifies the driver that it has been loaded.</span></span> <span data-ttu-id="a279d-107">Il driver deve verificare che siano presenti hardware e driver di supporto necessari per il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="a279d-107">The driver should make sure that any hardware and supporting drivers it needs to function properly are present.</span></span>

## <a name="parameters"></a><span data-ttu-id="a279d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a279d-108">Parameters</span></span>

<span data-ttu-id="a279d-109">Il parametro *hdrvr* è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="a279d-109">The *hdrvr* parameter is always zero.</span></span> <span data-ttu-id="a279d-110">I parametri *dwDriverId*, *lParam1* e *lParam2* non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="a279d-110">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="a279d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a279d-111">Return Value</span></span>

<span data-ttu-id="a279d-112">Restituisce un valore diverso da zero in caso di esito positivo o zero.</span><span class="sxs-lookup"><span data-stu-id="a279d-112">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a279d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a279d-113">Remarks</span></span>

<span data-ttu-id="a279d-114">Il messaggio di **\_ caricamento DRV** è sempre il primo messaggio ricevuto da un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a279d-114">The **DRV\_LOAD** message is always the first message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="a279d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a279d-115">Requirements</span></span>



| <span data-ttu-id="a279d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a279d-116">Requirement</span></span> | <span data-ttu-id="a279d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a279d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a279d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a279d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a279d-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a279d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a279d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a279d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a279d-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a279d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a279d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a279d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a279d-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a279d-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a279d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a279d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a279d-125">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="a279d-125">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="a279d-126">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="a279d-126">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





