---
title: Messaggio CB_RESETCONTENT (winuser. h)
description: Rimuove tutti gli elementi dalla casella di riepilogo e il controllo di modifica di una casella combinata.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- Controlli di Windows Message CB_RESETCONTENT
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873793"
---
# <a name="cb_resetcontent-message"></a><span data-ttu-id="fc604-104">\_Messaggio ResetContent CB</span><span class="sxs-lookup"><span data-stu-id="fc604-104">CB\_RESETCONTENT message</span></span>

<span data-ttu-id="fc604-105">Rimuove tutti gli elementi dalla casella di riepilogo e il controllo di modifica di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="fc604-105">Removes all items from the list box and edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc604-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc604-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc604-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc604-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc604-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fc604-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fc604-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc604-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc604-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fc604-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc604-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc604-111">Return value</span></span>

<span data-ttu-id="fc604-112">Questo messaggio restituisce sempre CB \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fc604-112">This message always returns CB\_OKAY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc604-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc604-113">Remarks</span></span>

<span data-ttu-id="fc604-114">Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il proprietario della casella combinata riceve un messaggio [**WM \_ DeleteItem**](wm-deleteitem.md) per ogni elemento nella casella combinata.</span><span class="sxs-lookup"><span data-stu-id="fc604-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the owner of the combo box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc604-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc604-115">Requirements</span></span>



| <span data-ttu-id="fc604-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc604-116">Requirement</span></span> | <span data-ttu-id="fc604-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fc604-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc604-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc604-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fc604-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc604-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc604-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc604-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fc604-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc604-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc604-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc604-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc604-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc604-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc604-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc604-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="fc604-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fc604-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fc604-126">**CB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="fc604-126">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="fc604-127">**\_DeleteItem WM**</span><span class="sxs-lookup"><span data-stu-id="fc604-127">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





