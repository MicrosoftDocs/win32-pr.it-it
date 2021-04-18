---
title: Messaggio WM_DPICHANGED_AFTERPARENT (winuser. h)
description: Per le finestre di primo livello di per monitor V2, questo messaggio viene inviato a tutti gli HWND nell'albero HWDN figlio della finestra in cui è in corso una modifica del valore DPI. | Messaggio WM_DPICHANGED_AFTERPARENT (winuser. h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- Messaggio WM_DPICHANGED_AFTERPARENT alto DPI
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321921"
---
# <a name="wm_dpichanged_afterparent-message"></a><span data-ttu-id="ebc74-105">\_ \_ Messaggio AFTERPARENT di WM DPICHANGED</span><span class="sxs-lookup"><span data-stu-id="ebc74-105">WM\_DPICHANGED\_AFTERPARENT message</span></span>

<span data-ttu-id="ebc74-106">Per le finestre di primo livello di per [Monitor V2](dpi-awareness-context.md) , questo messaggio viene inviato a tutti gli HWND nell'albero HWDN figlio della finestra in cui è in corso una modifica del valore dpi.</span><span class="sxs-lookup"><span data-stu-id="ebc74-106">For [Per Monitor v2](dpi-awareness-context.md) top-level windows, this message is sent to all HWNDs in the child HWDN tree of the window that is undergoing a DPI change.</span></span> <span data-ttu-id="ebc74-107">Questo messaggio si verifica dopo che la finestra di primo livello riceve [**WM \_ DPICHANGED**](wm-dpichanged.md)e attraversa l'albero figlio dall'alto verso il basso.</span><span class="sxs-lookup"><span data-stu-id="ebc74-107">This message occurs after the top-level window receives [**WM\_DPICHANGED**](wm-dpichanged.md), and traverses the child tree from the top down.</span></span>


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a><span data-ttu-id="ebc74-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebc74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebc74-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebc74-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebc74-110">Questo valore non è utilizzato e sarà zero.</span><span class="sxs-lookup"><span data-stu-id="ebc74-110">This value is unused and will be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ebc74-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebc74-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebc74-112">Questo valore non è utilizzato e sarà zero.</span><span class="sxs-lookup"><span data-stu-id="ebc74-112">This value is unused and will be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebc74-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebc74-113">Return value</span></span>

<span data-ttu-id="ebc74-114">Questo valore non è utilizzato e viene ignorato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ebc74-114">This value is unused and ignored by the system.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebc74-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebc74-115">Remarks</span></span>

<span data-ttu-id="ebc74-116">Non esiste alcuna gestione predefinita del messaggio in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="ebc74-116">There is no default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="ebc74-117">Questo messaggio viene inviato solo quando la finestra di primo livello ha un contesto di riconoscimento DPI di PMv2.</span><span class="sxs-lookup"><span data-stu-id="ebc74-117">This message is only sent when the top-level window has a DPI awareness context of PMv2.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebc74-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebc74-118">Requirements</span></span>



| <span data-ttu-id="ebc74-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebc74-119">Requirement</span></span> | <span data-ttu-id="ebc74-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ebc74-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc74-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebc74-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ebc74-122">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebc74-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ebc74-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebc74-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ebc74-124">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="ebc74-124">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ebc74-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebc74-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebc74-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebc74-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebc74-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebc74-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc74-128">**\_DPICHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="ebc74-128">**WM\_DPICHANGED**</span></span>](wm-dpichanged.md)
</dt> <dt>

[<span data-ttu-id="ebc74-129">**\_BEFOREPARENT DPICHANGED \_ WM**</span><span class="sxs-lookup"><span data-stu-id="ebc74-129">**WM\_DPICHANGED\_BEFOREPARENT**</span></span>](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

