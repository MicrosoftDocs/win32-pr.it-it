---
title: Messaggio CB_INITSTORAGE (winuser. h)
description: Un'applicazione invia il \_ messaggio INITSTORAGE CB prima di aggiungere un numero elevato di elementi alla casella di riepilogo di una casella combinata. Questo messaggio alloca memoria per archiviare gli elementi della casella di riepilogo.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- Controlli di Windows Message CB_INITSTORAGE
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119734"
---
# <a name="cb_initstorage-message"></a><span data-ttu-id="311e2-105">\_Messaggio INITSTORAGE CB</span><span class="sxs-lookup"><span data-stu-id="311e2-105">CB\_INITSTORAGE message</span></span>

<span data-ttu-id="311e2-106">Un'applicazione invia il **messaggio \_ INITSTORAGE CB** prima di aggiungere un numero elevato di elementi alla casella di riepilogo di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="311e2-106">An application sends the **CB\_INITSTORAGE** message before adding a large number of items to the list box portion of a combo box.</span></span> <span data-ttu-id="311e2-107">Questo messaggio alloca memoria per archiviare gli elementi della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="311e2-107">This message allocates memory for storing list box items.</span></span>

## <a name="parameters"></a><span data-ttu-id="311e2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="311e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="311e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="311e2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="311e2-110">Numero di elementi da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="311e2-110">The number of items to add.</span></span>

</dd> <dt>

<span data-ttu-id="311e2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="311e2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="311e2-112">Quantità di memoria da allocare per le stringhe di elemento, in byte.</span><span class="sxs-lookup"><span data-stu-id="311e2-112">The amount of memory to allocate for item strings, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="311e2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="311e2-113">Return value</span></span>

<span data-ttu-id="311e2-114">Se il messaggio ha esito positivo, il valore restituito è il numero totale di elementi per cui la memoria è stata pre-allocata, ovvero il numero totale di elementi aggiunti da tutti i messaggi **CB \_ INITSTORAGE** correttamente.</span><span class="sxs-lookup"><span data-stu-id="311e2-114">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **CB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="311e2-115">Se il messaggio ha esito negativo, il valore restituito è CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="311e2-115">If the message fails, the return value is CB\_ERRSPACE.</span></span>

<span data-ttu-id="311e2-116">Il messaggio alloca memoria e restituisce i valori di esito positivo e negativo descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="311e2-116">The message allocates memory and returns the success and error values described above.</span></span>

## <a name="remarks"></a><span data-ttu-id="311e2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="311e2-117">Remarks</span></span>

<span data-ttu-id="311e2-118">Il messaggio **CB \_ INITSTORAGE** consente di velocizzare l'inizializzazione di caselle combinate con un numero elevato di elementi (oltre 100).</span><span class="sxs-lookup"><span data-stu-id="311e2-118">The **CB\_INITSTORAGE** message helps speed up the initialization of combo boxes that have a large number of items (over 100).</span></span> <span data-ttu-id="311e2-119">Si riserva la quantità di memoria specificata in modo che i messaggi [**CB \_ ADDSTRING**](cb-addstring.md), [**CB \_ INSERTSTRING**](cb-insertstring.md)e [**CB \_**](cb-dir.md) successivi abbiano il minor tempo possibile.</span><span class="sxs-lookup"><span data-stu-id="311e2-119">It reserves the specified amount of memory so that subsequent [**CB\_ADDSTRING**](cb-addstring.md), [**CB\_INSERTSTRING**](cb-insertstring.md), and [**CB\_DIR**](cb-dir.md) messages take the shortest possible time.</span></span> <span data-ttu-id="311e2-120">È possibile utilizzare le stime per i parametri *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="311e2-120">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="311e2-121">Se si esegue la sovrastima, viene allocata la memoria aggiuntiva, se si sottovaluta, per gli elementi che superano la quantità richiesta viene utilizzata l'allocazione normale.</span><span class="sxs-lookup"><span data-stu-id="311e2-121">If you overestimate, the extra memory is allocated, if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="311e2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="311e2-122">Requirements</span></span>



| <span data-ttu-id="311e2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="311e2-123">Requirement</span></span> | <span data-ttu-id="311e2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="311e2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="311e2-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="311e2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="311e2-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="311e2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="311e2-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="311e2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="311e2-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="311e2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="311e2-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="311e2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="311e2-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="311e2-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="311e2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="311e2-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="311e2-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="311e2-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="311e2-133">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="311e2-133">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="311e2-134">**DIR della CB \_**</span><span class="sxs-lookup"><span data-stu-id="311e2-134">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="311e2-135">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="311e2-135">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





