---
title: Messaggio LB_DELETESTRING (winuser. h)
description: Elimina una stringa in una casella di riepilogo.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- Controlli di Windows Message LB_DELETESTRING
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874265"
---
# <a name="lb_deletestring-message"></a><span data-ttu-id="2a42a-104">\_Messaggio DELETESTRING lb</span><span class="sxs-lookup"><span data-stu-id="2a42a-104">LB\_DELETESTRING message</span></span>

<span data-ttu-id="2a42a-105">Elimina una stringa in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="2a42a-105">Deletes a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a42a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a42a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a42a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a42a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a42a-108">Indice in base zero della stringa da eliminare.</span><span class="sxs-lookup"><span data-stu-id="2a42a-108">The zero-based index of the string to be deleted.</span></span>

<span data-ttu-id="2a42a-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="2a42a-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="2a42a-110">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="2a42a-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="2a42a-111">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="2a42a-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="2a42a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a42a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a42a-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="2a42a-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a42a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a42a-114">Return value</span></span>

<span data-ttu-id="2a42a-115">Il valore restituito è un conteggio delle stringhe rimaste nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="2a42a-115">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="2a42a-116">Il valore restituito è LB \_ Err se il parametro *wParam* specifica un indice maggiore del numero di elementi nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="2a42a-116">The return value is LB\_ERR if the *wParam* parameter specifies an index greater than the number of items in the list.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a42a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a42a-117">Remarks</span></span>

<span data-ttu-id="2a42a-118">Se un'applicazione crea la casella di riepilogo con uno stile disegnato dal proprietario ma senza lo stile [**\_ HASSTRINGS di lbs**](list-box-styles.md) , il sistema invia un messaggio [**WM \_ DeleteItem**](wm-deleteitem.md) al proprietario della casella di riepilogo in modo che l'applicazione possa liberare i dati aggiuntivi associati all'elemento.</span><span class="sxs-lookup"><span data-stu-id="2a42a-118">If an application creates the list box with an owner-drawn style but without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the list box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a42a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a42a-119">Requirements</span></span>



| <span data-ttu-id="2a42a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a42a-120">Requirement</span></span> | <span data-ttu-id="2a42a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2a42a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a42a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a42a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2a42a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a42a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2a42a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a42a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2a42a-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a42a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a42a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a42a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a42a-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a42a-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a42a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a42a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a42a-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2a42a-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2a42a-130">**\_ADDSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="2a42a-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="2a42a-131">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="2a42a-131">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="2a42a-132">**\_DeleteItem WM**</span><span class="sxs-lookup"><span data-stu-id="2a42a-132">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





