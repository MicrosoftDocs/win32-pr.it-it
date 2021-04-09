---
title: Messaggio LB_SETITEMDATA (winuser. h)
description: Imposta un valore associato all'elemento specificato in una casella di riepilogo.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- Controlli di Windows Message LB_SETITEMDATA
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d9f9cc952ea3bf2d83358ce3b15ce6c3a2546b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121006"
---
# <a name="lb_setitemdata-message"></a><span data-ttu-id="6c562-104">\_Messaggio SETITEMDATA lb</span><span class="sxs-lookup"><span data-stu-id="6c562-104">LB\_SETITEMDATA message</span></span>

<span data-ttu-id="6c562-105">Imposta un valore associato all'elemento specificato in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="6c562-105">Sets a value associated with the specified item in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c562-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c562-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c562-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c562-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c562-108">Specifica l'indice in base zero dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6c562-108">Specifies the zero-based index of the item.</span></span> <span data-ttu-id="6c562-109">Se questo valore è-1, il valore *lParam* si applica a tutti gli elementi nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="6c562-109">If this value is -1, the *lParam* value applies to all items in the list box.</span></span>

<span data-ttu-id="6c562-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="6c562-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="6c562-111">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="6c562-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="6c562-112">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="6c562-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="6c562-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c562-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c562-114">Specifica il valore da associare all'elemento.</span><span class="sxs-lookup"><span data-stu-id="6c562-114">Specifies the value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c562-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c562-115">Return value</span></span>

<span data-ttu-id="6c562-116">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6c562-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c562-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c562-117">Remarks</span></span>

<span data-ttu-id="6c562-118">Se l'elemento si trova in una casella di riepilogo creata dal proprietario creata senza lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , questo messaggio sostituisce il valore contenuto nel parametro *lParam* del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) che ha aggiunto l'elemento alla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="6c562-118">If the item is in an owner-drawn list box created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this message replaces the value contained in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c562-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c562-119">Requirements</span></span>



| <span data-ttu-id="6c562-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c562-120">Requirement</span></span> | <span data-ttu-id="6c562-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6c562-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c562-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c562-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6c562-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c562-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6c562-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c562-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6c562-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c562-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c562-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c562-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c562-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c562-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c562-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c562-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c562-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6c562-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6c562-130">**\_ADDSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="6c562-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="6c562-131">**\_GETITEMDATA lb**</span><span class="sxs-lookup"><span data-stu-id="6c562-131">**LB\_GETITEMDATA**</span></span>](lb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="6c562-132">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="6c562-132">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





