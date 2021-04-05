---
title: Messaggio CB_GETITEMHEIGHT (winuser. h)
description: Determina l'altezza degli elementi dell'elenco o il campo di selezione in una casella combinata.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- Controlli di Windows Message CB_GETITEMHEIGHT
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873801"
---
# <a name="cb_getitemheight-message"></a><span data-ttu-id="2a69b-104">\_Messaggio GETITEMHEIGHT CB</span><span class="sxs-lookup"><span data-stu-id="2a69b-104">CB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="2a69b-105">Determina l'altezza degli elementi dell'elenco o il campo di selezione in una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="2a69b-105">Determines the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a69b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a69b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a69b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a69b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a69b-108">Componente della casella combinata di cui è necessario recuperare l'altezza.</span><span class="sxs-lookup"><span data-stu-id="2a69b-108">The combo box component whose height is to be retrieved.</span></span> <span data-ttu-id="2a69b-109">Questo parametro deve essere-1 per recuperare l'altezza del campo di selezione.</span><span class="sxs-lookup"><span data-stu-id="2a69b-109">This parameter must be -1 to retrieve the height of the selection field.</span></span> <span data-ttu-id="2a69b-110">Deve essere zero per recuperare l'altezza degli elementi dell'elenco, a meno che la casella combinata non abbia lo stile [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2a69b-110">It must be zero to retrieve the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="2a69b-111">In tal caso, il parametro *wParam* è l'indice in base zero di un elemento di elenco specifico.</span><span class="sxs-lookup"><span data-stu-id="2a69b-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="2a69b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a69b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a69b-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="2a69b-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a69b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a69b-114">Return value</span></span>

<span data-ttu-id="2a69b-115">Il valore restituito è l'altezza, in pixel, degli elementi dell'elenco in una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="2a69b-115">The return value is the height, in pixels, of the list items in a combo box.</span></span> <span data-ttu-id="2a69b-116">Se la casella combinata ha lo stile [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) , è l'altezza dell'elemento specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="2a69b-116">If the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, it is the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="2a69b-117">Se *wParam* è-1, il valore restituito è l'altezza della parte del controllo di modifica (o del testo statico) della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="2a69b-117">If *wParam* is -1, the return value is the height of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="2a69b-118">Se si verifica un errore, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="2a69b-118">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a69b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a69b-119">Requirements</span></span>



| <span data-ttu-id="2a69b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a69b-120">Requirement</span></span> | <span data-ttu-id="2a69b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2a69b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a69b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a69b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2a69b-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a69b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2a69b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a69b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2a69b-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a69b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a69b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a69b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a69b-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a69b-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a69b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a69b-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a69b-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2a69b-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2a69b-130">**CB \_ SETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="2a69b-130">**CB\_SETITEMHEIGHT**</span></span>](cb-setitemheight.md)
</dt> <dt>

[<span data-ttu-id="2a69b-131">**\_MeasureItem WM**</span><span class="sxs-lookup"><span data-stu-id="2a69b-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





