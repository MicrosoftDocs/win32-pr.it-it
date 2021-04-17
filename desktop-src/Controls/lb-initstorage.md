---
title: Messaggio LB_INITSTORAGE (winuser. h)
description: Alloca memoria per archiviare gli elementi della casella di riepilogo. Questo messaggio viene usato prima che un'applicazione aggiunga un numero elevato di elementi a una casella di riepilogo.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- Controlli di Windows Message LB_INITSTORAGE
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476816"
---
# <a name="lb_initstorage-message"></a><span data-ttu-id="10be7-105">\_Messaggio INITSTORAGE lb</span><span class="sxs-lookup"><span data-stu-id="10be7-105">LB\_INITSTORAGE message</span></span>

<span data-ttu-id="10be7-106">Alloca memoria per archiviare gli elementi della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="10be7-106">Allocates memory for storing list box items.</span></span> <span data-ttu-id="10be7-107">Questo messaggio viene usato prima che un'applicazione aggiunga un numero elevato di elementi a una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="10be7-107">This message is used before an application adds a large number of items to a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="10be7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="10be7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10be7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10be7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10be7-110">Numero di elementi da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="10be7-110">The number of items to add.</span></span>

<span data-ttu-id="10be7-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="10be7-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="10be7-112">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="10be7-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="10be7-113">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="10be7-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="10be7-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10be7-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10be7-115">Quantità di memoria, in byte, da allocare per le stringhe di elemento.</span><span class="sxs-lookup"><span data-stu-id="10be7-115">The amount of memory, in bytes, to allocate for item strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10be7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10be7-116">Return value</span></span>

<span data-ttu-id="10be7-117">Se il messaggio ha esito positivo, il valore restituito è il numero totale di elementi per cui la memoria è stata pre-allocata, ovvero il numero totale di elementi aggiunti da tutti i messaggi **lb \_ INITSTORAGE** riusciti.</span><span class="sxs-lookup"><span data-stu-id="10be7-117">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **LB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="10be7-118">Se il messaggio ha esito negativo, il valore restituito è LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="10be7-118">If the message fails, the return value is LB\_ERRSPACE.</span></span>

<span data-ttu-id="10be7-119">Microsoft Windows NT 4,0: questo messaggio non alloca la quantità di memoria specificata. Tuttavia, restituisce sempre il valore specificato nel parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="10be7-119">Microsoft Windows NT 4.0 : This message does not allocate the specified amount of memory; however, it always returns the value specified in the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="10be7-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="10be7-120">Remarks</span></span>

<span data-ttu-id="10be7-121">Il messaggio **lb \_ INITSTORAGE** consente di velocizzare l'inizializzazione di caselle di riepilogo con un numero elevato di elementi (più di 100).</span><span class="sxs-lookup"><span data-stu-id="10be7-121">The **LB\_INITSTORAGE** message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="10be7-122">Si riserva la quantità di memoria specificata in modo che i messaggi [**lb \_ ADDSTRING**](lb-addstring.md), [**lb \_ INSERTSTRING**](lb-insertstring.md), [**lb \_ dir**](lb-dir.md)e [**lb \_ AddFile**](lb-addfile.md) prendano il minor tempo possibile.</span><span class="sxs-lookup"><span data-stu-id="10be7-122">It reserves the specified amount of memory so that subsequent [**LB\_ADDSTRING**](lb-addstring.md), [**LB\_INSERTSTRING**](lb-insertstring.md), [**LB\_DIR**](lb-dir.md), and [**LB\_ADDFILE**](lb-addfile.md) messages take the shortest possible time.</span></span> <span data-ttu-id="10be7-123">È possibile utilizzare le stime per i parametri *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="10be7-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="10be7-124">Se si esegue la sovrastima, viene allocata la memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene utilizzata per gli elementi che superano la quantità richiesta.</span><span class="sxs-lookup"><span data-stu-id="10be7-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="10be7-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10be7-125">Requirements</span></span>



| <span data-ttu-id="10be7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="10be7-126">Requirement</span></span> | <span data-ttu-id="10be7-127">Valore</span><span class="sxs-lookup"><span data-stu-id="10be7-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10be7-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10be7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="10be7-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10be7-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="10be7-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10be7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="10be7-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10be7-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="10be7-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10be7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="10be7-133"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10be7-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10be7-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10be7-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="10be7-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="10be7-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="10be7-136">**\_AddFile lb**</span><span class="sxs-lookup"><span data-stu-id="10be7-136">**LB\_ADDFILE**</span></span>](lb-addfile.md)
</dt> <dt>

[<span data-ttu-id="10be7-137">**\_ADDSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="10be7-137">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="10be7-138">**\_dir lb**</span><span class="sxs-lookup"><span data-stu-id="10be7-138">**LB\_DIR**</span></span>](lb-dir.md)
</dt> <dt>

[<span data-ttu-id="10be7-139">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="10be7-139">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





