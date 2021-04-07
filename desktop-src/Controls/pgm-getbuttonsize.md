---
title: Messaggio PGM_GETBUTTONSIZE (COMmctrl. h)
description: Recupera le dimensioni correnti del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro GetButtonSize del cercapersone.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- Controlli di Windows Message PGM_GETBUTTONSIZE
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048553"
---
# <a name="pgm_getbuttonsize-message"></a><span data-ttu-id="5f9f2-105">\_Messaggio GETBUTTONSIZE PGM</span><span class="sxs-lookup"><span data-stu-id="5f9f2-105">PGM\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="5f9f2-106">Recupera le dimensioni correnti del pulsante per il controllo pager.</span><span class="sxs-lookup"><span data-stu-id="5f9f2-106">Retrieves the current button size for the pager control.</span></span> <span data-ttu-id="5f9f2-107">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetButtonSize del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) .</span><span class="sxs-lookup"><span data-stu-id="5f9f2-107">You can send this message explicitly or use the [**Pager\_GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f9f2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f9f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f9f2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f9f2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5f9f2-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5f9f2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5f9f2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f9f2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5f9f2-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5f9f2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f9f2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f9f2-113">Return value</span></span>

<span data-ttu-id="5f9f2-114">Restituisce un valore INT che contiene la dimensione corrente del pulsante, in pixel.</span><span class="sxs-lookup"><span data-stu-id="5f9f2-114">Returns an INT value that contains the current button size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f9f2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f9f2-115">Requirements</span></span>



| <span data-ttu-id="5f9f2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f9f2-116">Requirement</span></span> | <span data-ttu-id="5f9f2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5f9f2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9f2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f9f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5f9f2-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f9f2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f9f2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f9f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5f9f2-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5f9f2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f9f2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f9f2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f9f2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f9f2-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f9f2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f9f2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f9f2-125">**\_SETBUTTONSIZE PGM**</span><span class="sxs-lookup"><span data-stu-id="5f9f2-125">**PGM\_SETBUTTONSIZE**</span></span>](pgm-setbuttonsize.md)
</dt> </dl>

 

 





