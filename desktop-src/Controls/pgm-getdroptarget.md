---
title: Messaggio PGM_GETDROPTARGET (COMmctrl. h)
description: Recupera un puntatore all'interfaccia IDropTarget del controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro GetDropTarget del cercapersone.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- Controlli di Windows Message PGM_GETDROPTARGET
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477897"
---
# <a name="pgm_getdroptarget-message"></a><span data-ttu-id="41be0-105">\_Messaggio GETDROPTARGET PGM</span><span class="sxs-lookup"><span data-stu-id="41be0-105">PGM\_GETDROPTARGET message</span></span>

<span data-ttu-id="41be0-106">Recupera un puntatore all'interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) del controllo pager.</span><span class="sxs-lookup"><span data-stu-id="41be0-106">Retrieves a pager control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span> <span data-ttu-id="41be0-107">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetDropTarget del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="41be0-107">You can send this message explicitly or use the [**Pager\_GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="41be0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="41be0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41be0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41be0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="41be0-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="41be0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="41be0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41be0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41be0-112">Puntatore a un puntatore [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) che riceve il puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="41be0-112">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="41be0-113">È responsabilità del chiamante chiamare il [**rilascio**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su questo puntatore quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="41be0-113">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41be0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41be0-114">Return value</span></span>

<span data-ttu-id="41be0-115">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="41be0-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="41be0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41be0-116">Requirements</span></span>



| <span data-ttu-id="41be0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="41be0-117">Requirement</span></span> | <span data-ttu-id="41be0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="41be0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41be0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41be0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="41be0-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41be0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41be0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41be0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="41be0-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41be0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41be0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41be0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="41be0-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41be0-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

