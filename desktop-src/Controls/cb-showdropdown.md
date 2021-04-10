---
title: Messaggio CB_SHOWDROPDOWN (winuser. h)
description: Un'applicazione invia un \_ messaggio CB SHOWDROPDOWN per mostrare o nascondere la casella di riepilogo di una casella combinata con lo \_ stile di menu a discesa CBS o CBS \_ DropDownList.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- Controlli di Windows Message CB_SHOWDROPDOWN
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121054"
---
# <a name="cb_showdropdown-message"></a><span data-ttu-id="00011-104">\_Messaggio SHOWDROPDOWN CB</span><span class="sxs-lookup"><span data-stu-id="00011-104">CB\_SHOWDROPDOWN message</span></span>

<span data-ttu-id="00011-105">Un'applicazione invia un messaggio **CB \_ SHOWDROPDOWN** per mostrare o nascondere la casella di riepilogo di una casella combinata con lo stile di [**menu a \_ discesa CBS**](combo-box-styles.md) o [**CBS \_ DropDownList**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="00011-105">An application sends a **CB\_SHOWDROPDOWN** message to show or hide the list box of a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="00011-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00011-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00011-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00011-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00011-108">Valore **booleano** che specifica se la casella di riepilogo a discesa deve essere mostrata o nascosta.</span><span class="sxs-lookup"><span data-stu-id="00011-108">A **BOOL** that specifies whether the drop-down list box is to be shown or hidden.</span></span> <span data-ttu-id="00011-109">Il valore **true** Mostra la casella di riepilogo; il valore **false** lo nasconde.</span><span class="sxs-lookup"><span data-stu-id="00011-109">A value of **TRUE** shows the list box; a value of **FALSE** hides it.</span></span>

</dd> <dt>

<span data-ttu-id="00011-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00011-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00011-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="00011-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00011-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00011-112">Return value</span></span>

<span data-ttu-id="00011-113">Il valore restituito è sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="00011-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="00011-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="00011-114">Remarks</span></span>

<span data-ttu-id="00011-115">Questo messaggio non ha alcun effetto su una casella combinata creata con lo stile [**\_ semplice CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="00011-115">This message has no effect on a combo box created with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="00011-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00011-116">Requirements</span></span>



| <span data-ttu-id="00011-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="00011-117">Requirement</span></span> | <span data-ttu-id="00011-118">Valore</span><span class="sxs-lookup"><span data-stu-id="00011-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00011-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00011-119">Minimum supported client</span></span><br/> | <span data-ttu-id="00011-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00011-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="00011-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00011-121">Minimum supported server</span></span><br/> | <span data-ttu-id="00011-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="00011-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="00011-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00011-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="00011-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00011-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00011-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00011-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00011-126">**CB \_ GETDROPPEDSTATE**</span><span class="sxs-lookup"><span data-stu-id="00011-126">**CB\_GETDROPPEDSTATE**</span></span>](cb-getdroppedstate.md)
</dt> </dl>

 

 





