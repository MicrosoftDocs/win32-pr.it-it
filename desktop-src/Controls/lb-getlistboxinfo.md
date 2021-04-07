---
title: Messaggio LB_GETLISTBOXINFO (winuser. h)
description: Ottiene il numero di elementi per colonna in una casella di riepilogo specificata.
ms.assetid: 925bebd9-2563-4892-a7d7-73d4ef012b42
keywords:
- Controlli di Windows Message LB_GETLISTBOXINFO
topic_type:
- apiref
api_name:
- LB_GETLISTBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f49f96e3f12b1c21e81e8b5358e174e576d07f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048261"
---
# <a name="lb_getlistboxinfo-message"></a><span data-ttu-id="2e86e-104">\_Messaggio GETLISTBOXINFO lb</span><span class="sxs-lookup"><span data-stu-id="2e86e-104">LB\_GETLISTBOXINFO message</span></span>

<span data-ttu-id="2e86e-105">Ottiene il numero di elementi per colonna in una casella di riepilogo specificata.</span><span class="sxs-lookup"><span data-stu-id="2e86e-105">Gets the number of items per column in a specified list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e86e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e86e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e86e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e86e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e86e-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2e86e-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2e86e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e86e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e86e-110">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2e86e-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e86e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e86e-111">Return value</span></span>

<span data-ttu-id="2e86e-112">Il valore restituito è il numero di elementi per colonna.</span><span class="sxs-lookup"><span data-stu-id="2e86e-112">The return value is the number of items per column.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e86e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e86e-113">Remarks</span></span>

<span data-ttu-id="2e86e-114">Questo messaggio è equivalente a [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).</span><span class="sxs-lookup"><span data-stu-id="2e86e-114">This message is equivalent to [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e86e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e86e-115">Requirements</span></span>



| <span data-ttu-id="2e86e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e86e-116">Requirement</span></span> | <span data-ttu-id="2e86e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2e86e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e86e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e86e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2e86e-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e86e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2e86e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e86e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2e86e-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e86e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e86e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e86e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e86e-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e86e-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e86e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e86e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e86e-125">**GetListBoxInfo**</span><span class="sxs-lookup"><span data-stu-id="2e86e-125">**GetListBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo)
</dt> </dl>

 

 





