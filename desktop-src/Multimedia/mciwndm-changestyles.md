---
title: Messaggio di MCIWNDM_CHANGESTYLES (VFW. h)
description: Il \_ messaggio MCIWNDM CHANGESTYLES modifica gli stili utilizzati dalla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndChangeStyles.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301170"
---
# <a name="mciwndm_changestyles-message"></a><span data-ttu-id="25cdd-105">\_Messaggio MCIWNDM CHANGESTYLES</span><span class="sxs-lookup"><span data-stu-id="25cdd-105">MCIWNDM\_CHANGESTYLES message</span></span>

<span data-ttu-id="25cdd-106">Il messaggio **MCIWNDM \_ CHANGESTYLES** modifica gli stili utilizzati dalla finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="25cdd-106">The **MCIWNDM\_CHANGESTYLES** message changes the styles used by the MCIWnd window.</span></span> <span data-ttu-id="25cdd-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) .</span><span class="sxs-lookup"><span data-stu-id="25cdd-107">You can send this message explicitly or by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro.</span></span>


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a><span data-ttu-id="25cdd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="25cdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25cdd-109"><span id="mask"></span><span id="MASK"></span>*maschera*</span><span class="sxs-lookup"><span data-stu-id="25cdd-109"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="25cdd-110">Maschera che identifica gli stili che possono cambiare.</span><span class="sxs-lookup"><span data-stu-id="25cdd-110">Mask that identifies the styles that can change.</span></span> <span data-ttu-id="25cdd-111">Questa maschera rappresenta l'operatore OR bit per bit di tutti gli stili che saranno consentiti per la modifica.</span><span class="sxs-lookup"><span data-stu-id="25cdd-111">This mask is the bitwise OR operator of all styles that will be permitted to change.</span></span>

</dd> <dt>

<span data-ttu-id="25cdd-112"><span id="value"></span><span id="VALUE"></span>*valore*</span><span class="sxs-lookup"><span data-stu-id="25cdd-112"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="25cdd-113">Nuove impostazioni di stile per la finestra.</span><span class="sxs-lookup"><span data-stu-id="25cdd-113">New style settings for the window.</span></span> <span data-ttu-id="25cdd-114">Specificare zero per questo parametro per disattivare tutti gli stili identificati nella maschera.</span><span class="sxs-lookup"><span data-stu-id="25cdd-114">Specify zero for this parameter to turn off all styles identified in the mask.</span></span> <span data-ttu-id="25cdd-115">Per un elenco degli stili disponibili, vedere la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="25cdd-115">For a list of the available styles, see the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25cdd-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25cdd-116">Return Value</span></span>

<span data-ttu-id="25cdd-117">Restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="25cdd-117">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="25cdd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25cdd-118">Requirements</span></span>



| <span data-ttu-id="25cdd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="25cdd-119">Requirement</span></span> | <span data-ttu-id="25cdd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="25cdd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="25cdd-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25cdd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="25cdd-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25cdd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="25cdd-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25cdd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="25cdd-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25cdd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="25cdd-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25cdd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="25cdd-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="25cdd-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25cdd-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25cdd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25cdd-128">**MCIWndCreate**</span><span class="sxs-lookup"><span data-stu-id="25cdd-128">**MCIWndCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[<span data-ttu-id="25cdd-129">**MCIWndChangeStyles**</span><span class="sxs-lookup"><span data-stu-id="25cdd-129">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





