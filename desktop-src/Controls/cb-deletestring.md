---
title: Messaggio CB_DELETESTRING (winuser. h)
description: Elimina una stringa nella casella di riepilogo di una casella combinata.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- Controlli di Windows Message CB_DELETESTRING
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121319"
---
# <a name="cb_deletestring-message"></a><span data-ttu-id="7eca5-104">\_Messaggio DELETESTRING CB</span><span class="sxs-lookup"><span data-stu-id="7eca5-104">CB\_DELETESTRING message</span></span>

<span data-ttu-id="7eca5-105">Elimina una stringa nella casella di riepilogo di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7eca5-105">Deletes a string in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="7eca5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7eca5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eca5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7eca5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7eca5-108">Indice in base zero della stringa da eliminare.</span><span class="sxs-lookup"><span data-stu-id="7eca5-108">The zero-based index of the string to delete.</span></span>

</dd> <dt>

<span data-ttu-id="7eca5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7eca5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7eca5-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="7eca5-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eca5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7eca5-111">Return value</span></span>

<span data-ttu-id="7eca5-112">Il valore restituito è un conteggio delle stringhe rimaste nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7eca5-112">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="7eca5-113">Se il parametro *wParam* specifica un indice maggiore del numero di elementi nell'elenco, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="7eca5-113">If the *wParam* parameter specifies an index greater than the number of items in the list, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eca5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7eca5-114">Remarks</span></span>

<span data-ttu-id="7eca5-115">Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo [**stile \_ HASSTRINGS CBS**](combo-box-styles.md) , il sistema invia un [**messaggio \_ WM DeleteItem**](wm-deleteitem.md) al proprietario della casella combinata in modo che l'applicazione possa liberare i dati aggiuntivi associati all'elemento.</span><span class="sxs-lookup"><span data-stu-id="7eca5-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the combo box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eca5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7eca5-116">Requirements</span></span>



| <span data-ttu-id="7eca5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eca5-117">Requirement</span></span> | <span data-ttu-id="7eca5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7eca5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eca5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7eca5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7eca5-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7eca5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7eca5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7eca5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7eca5-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7eca5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7eca5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7eca5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7eca5-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7eca5-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eca5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7eca5-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="7eca5-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7eca5-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7eca5-127">**CB \_ ResetContent**</span><span class="sxs-lookup"><span data-stu-id="7eca5-127">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="7eca5-128">**\_DeleteItem WM**</span><span class="sxs-lookup"><span data-stu-id="7eca5-128">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





