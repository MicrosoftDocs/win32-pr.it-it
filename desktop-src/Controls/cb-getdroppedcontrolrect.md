---
title: Messaggio CB_GETDROPPEDCONTROLRECT (winuser. h)
description: Un'applicazione invia un \_ messaggio CB GETDROPPEDCONTROLRECT per recuperare le coordinate dello schermo di una casella combinata nello stato di eliminazione.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- Controlli di Windows Message CB_GETDROPPEDCONTROLRECT
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477333"
---
# <a name="cb_getdroppedcontrolrect-message"></a><span data-ttu-id="d5c84-104">\_Messaggio GETDROPPEDCONTROLRECT CB</span><span class="sxs-lookup"><span data-stu-id="d5c84-104">CB\_GETDROPPEDCONTROLRECT message</span></span>

<span data-ttu-id="d5c84-105">Un'applicazione invia un messaggio **CB \_ GETDROPPEDCONTROLRECT** per recuperare le coordinate dello schermo di una casella combinata nello stato di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="d5c84-105">An application sends a **CB\_GETDROPPEDCONTROLRECT** message to retrieve the screen coordinates of a combo box in its dropped-down state.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5c84-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5c84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5c84-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c84-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="d5c84-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d5c84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5c84-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c84-110">Puntatore alla struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve le coordinate della casella combinata nello stato di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="d5c84-110">A pointer to the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the coordinates of the combo box in its dropped-down state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c84-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5c84-111">Return value</span></span>

<span data-ttu-id="d5c84-112">Se il messaggio ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="d5c84-112">If the message succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="d5c84-113">Se il messaggio ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="d5c84-113">If the message fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c84-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5c84-114">Requirements</span></span>



| <span data-ttu-id="d5c84-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c84-115">Requirement</span></span> | <span data-ttu-id="d5c84-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d5c84-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c84-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5c84-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c84-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5c84-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d5c84-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5c84-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c84-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5c84-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d5c84-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5c84-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5c84-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5c84-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c84-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5c84-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5c84-124">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5c84-124">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

