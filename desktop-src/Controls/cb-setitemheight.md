---
title: Messaggio CB_SETITEMHEIGHT (winuser. h)
description: Un'applicazione invia un \_ messaggio CB SETITEMHEIGHT per impostare l'altezza degli elementi dell'elenco o il campo di selezione in una casella combinata.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- Controlli di Windows Message CB_SETITEMHEIGHT
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302371"
---
# <a name="cb_setitemheight-message"></a><span data-ttu-id="c08f7-104">\_Messaggio SETITEMHEIGHT CB</span><span class="sxs-lookup"><span data-stu-id="c08f7-104">CB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="c08f7-105">Un'applicazione invia un messaggio **CB \_ SETITEMHEIGHT** per impostare l'altezza degli elementi dell'elenco o il campo di selezione in una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="c08f7-105">An application sends a **CB\_SETITEMHEIGHT** message to set the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="c08f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c08f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c08f7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c08f7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c08f7-108">Specifica il componente della casella combinata per la quale impostare l'altezza.</span><span class="sxs-lookup"><span data-stu-id="c08f7-108">Specifies the component of the combo box for which to set the height.</span></span>

<span data-ttu-id="c08f7-109">Questo parametro deve essere 1 per impostare l'altezza del campo di selezione.</span><span class="sxs-lookup"><span data-stu-id="c08f7-109">This parameter must be  1 to set the height of the selection field.</span></span> <span data-ttu-id="c08f7-110">Deve essere zero per impostare l'altezza degli elementi dell'elenco, a meno che la casella combinata non abbia lo stile [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c08f7-110">It must be zero to set the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="c08f7-111">In tal caso, il parametro *wParam* è l'indice in base zero di un elemento di elenco specifico.</span><span class="sxs-lookup"><span data-stu-id="c08f7-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="c08f7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c08f7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c08f7-113">Specifica l'altezza, in pixel, del componente della casella combinata identificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="c08f7-113">Specifies the height, in pixels, of the combo box component identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c08f7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c08f7-114">Return value</span></span>

<span data-ttu-id="c08f7-115">Se l'indice o l'altezza non è valido, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="c08f7-115">If the index or height is invalid, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c08f7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c08f7-116">Remarks</span></span>

<span data-ttu-id="c08f7-117">L'altezza del campo di selezione in una casella combinata viene impostata indipendentemente dall'altezza degli elementi dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="c08f7-117">The selection field height in a combo box is set independently of the height of the list items.</span></span> <span data-ttu-id="c08f7-118">Un'applicazione deve garantire che l'altezza del campo di selezione non sia minore dell'altezza di un particolare elemento di elenco.</span><span class="sxs-lookup"><span data-stu-id="c08f7-118">An application must ensure that the height of the selection field is not smaller than the height of a particular list item.</span></span>

## <a name="requirements"></a><span data-ttu-id="c08f7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c08f7-119">Requirements</span></span>



| <span data-ttu-id="c08f7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c08f7-120">Requirement</span></span> | <span data-ttu-id="c08f7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c08f7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c08f7-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c08f7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c08f7-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c08f7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c08f7-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c08f7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c08f7-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c08f7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c08f7-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c08f7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c08f7-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c08f7-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c08f7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c08f7-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c08f7-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c08f7-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c08f7-130">**CB \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="c08f7-130">**CB\_GETITEMHEIGHT**</span></span>](cb-getitemheight.md)
</dt> <dt>

[<span data-ttu-id="c08f7-131">**\_MeasureItem WM**</span><span class="sxs-lookup"><span data-stu-id="c08f7-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





