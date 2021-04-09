---
title: Messaggio LB_INSERTSTRING (winuser. h)
description: Inserisce i dati di una stringa o di un elemento in una casella di riepilogo. A differenza del \_ messaggio lb ADDSTRING, il \_ messaggio lb INSERTSTRING non determina l'ordinamento di un elenco con lo \_ stile di ordinamento lbs.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- Controlli di Windows Message LB_INSERTSTRING
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121014"
---
# <a name="lb_insertstring-message"></a><span data-ttu-id="fe5b8-105">\_Messaggio INSERTSTRING lb</span><span class="sxs-lookup"><span data-stu-id="fe5b8-105">LB\_INSERTSTRING message</span></span>

<span data-ttu-id="fe5b8-106">Inserisce i dati di una stringa o di un elemento in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-106">Inserts a string or item data into a list box.</span></span> <span data-ttu-id="fe5b8-107">A differenza del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) , il messaggio **lb \_ INSERTSTRING** non determina l'ordinamento di un elenco con lo stile di [**\_ ordinamento lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5b8-107">Unlike the [**LB\_ADDSTRING**](lb-addstring.md) message, the **LB\_INSERTSTRING** message does not cause a list with the [**LBS\_SORT**](list-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe5b8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe5b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe5b8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe5b8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe5b8-110">Indice in base zero della posizione in corrispondenza della quale inserire la stringa.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="fe5b8-111">Se questo parametro è-1, la stringa viene aggiunta alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="fe5b8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe5b8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe5b8-113">Puntatore alla stringa con terminazione null da inserire.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="fe5b8-114">Se la casella di riepilogo ha uno stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , questo parametro viene archiviato come dati di elemento anziché come stringa.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="fe5b8-115">È possibile inviare i messaggi [**lb \_ GETITEMDATA**](lb-getitemdata.md) e [**lb \_ SETITEMDATA**](lb-setitemdata.md) per recuperare o modificare i dati dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-115">You can send the [**LB\_GETITEMDATA**](lb-getitemdata.md) and [**LB\_SETITEMDATA**](lb-setitemdata.md) messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe5b8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe5b8-116">Return value</span></span>

<span data-ttu-id="fe5b8-117">Il valore restituito è l'indice della posizione in cui è stata inserita la stringa.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-117">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="fe5b8-118">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="fe5b8-119">Se non è disponibile spazio sufficiente per archiviare la nuova stringa, il valore restituito è LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-119">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe5b8-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe5b8-120">Remarks</span></span>

<span data-ttu-id="fe5b8-121">Il messaggio [**lb \_ INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione di caselle di riepilogo con un numero elevato di elementi (più di 100).</span><span class="sxs-lookup"><span data-stu-id="fe5b8-121">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="fe5b8-122">Si riserva la quantità di memoria specificata in modo che i messaggi **lb \_ INSERTSTRING** il tempo più breve possibile.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-122">It reserves the specified amount of memory so that subsequent **LB\_INSERTSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="fe5b8-123">È possibile utilizzare le stime per i parametri *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="fe5b8-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="fe5b8-124">Se si esegue la sovrastima, viene allocata la memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene utilizzata per gli elementi che superano la quantità richiesta.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="fe5b8-125">Se nella casella di riepilogo è presente lo stile [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e si inserisce una stringa più ampia della casella di riepilogo, inviare un messaggio [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-125">If the list box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="fe5b8-126">Per un'applicazione ANSI, il sistema converte il testo in una casella di riepilogo in formato Unicode usando CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-126">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="fe5b8-127">Ciò può causare problemi.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-127">This can cause problems.</span></span> <span data-ttu-id="fe5b8-128">Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode nelle finestre giapponesi verranno disattivati.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-128">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="fe5b8-129">Per risolvere questo problema, compilare l'applicazione come Unicode o utilizzare una casella di riepilogo creata dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="fe5b8-129">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe5b8-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe5b8-130">Requirements</span></span>



| <span data-ttu-id="fe5b8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe5b8-131">Requirement</span></span> | <span data-ttu-id="fe5b8-132">Valore</span><span class="sxs-lookup"><span data-stu-id="fe5b8-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe5b8-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe5b8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fe5b8-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe5b8-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fe5b8-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe5b8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fe5b8-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe5b8-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe5b8-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe5b8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe5b8-138"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe5b8-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe5b8-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe5b8-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe5b8-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fe5b8-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fe5b8-141">**\_ADDSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="fe5b8-141">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="fe5b8-142">**\_SELECTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="fe5b8-142">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="fe5b8-143">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="fe5b8-143">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

