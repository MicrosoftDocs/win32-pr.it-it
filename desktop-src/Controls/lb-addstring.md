---
title: Messaggio LB_ADDSTRING (winuser. h)
description: Aggiunge una stringa a una casella di riepilogo. Se la casella di riepilogo non ha lo \_ stile di ordinamento lbs, la stringa viene aggiunta alla fine dell'elenco. In caso contrario, la stringa viene inserita nell'elenco e l'elenco viene ordinato.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- Controlli di Windows Message LB_ADDSTRING
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048297"
---
# <a name="lb_addstring-message"></a><span data-ttu-id="3c787-106">\_Messaggio ADDSTRING lb</span><span class="sxs-lookup"><span data-stu-id="3c787-106">LB\_ADDSTRING message</span></span>

<span data-ttu-id="3c787-107">Aggiunge una stringa a una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="3c787-107">Adds a string to a list box.</span></span> <span data-ttu-id="3c787-108">Se la casella di riepilogo non ha lo stile di [**\_ ordinamento lbs**](list-box-styles.md) , la stringa viene aggiunta alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3c787-108">If the list box does not have the [**LBS\_SORT**](list-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="3c787-109">In caso contrario, la stringa viene inserita nell'elenco e l'elenco viene ordinato.</span><span class="sxs-lookup"><span data-stu-id="3c787-109">Otherwise, the string is inserted into the list and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c787-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c787-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c787-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c787-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c787-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="3c787-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3c787-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c787-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c787-114">Puntatore alla stringa con terminazione null da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="3c787-114">A pointer to the null-terminated string that is to be added.</span></span>

<span data-ttu-id="3c787-115">Se la casella di riepilogo ha uno stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , questo parametro viene archiviato come dati di elemento anziché come stringa.</span><span class="sxs-lookup"><span data-stu-id="3c787-115">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="3c787-116">È possibile inviare i messaggi **lb \_ GETITEMDATA** e **lb \_ SETITEMDATA** per recuperare o modificare i dati dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3c787-116">You can send the **LB\_GETITEMDATA** and **LB\_SETITEMDATA** messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c787-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c787-117">Return value</span></span>

<span data-ttu-id="3c787-118">Il valore restituito è l'indice in base zero della stringa nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="3c787-118">The return value is the zero-based index of the string in the list box.</span></span> <span data-ttu-id="3c787-119">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="3c787-119">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="3c787-120">Se non è disponibile spazio sufficiente per archiviare la nuova stringa, il valore restituito è LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="3c787-120">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c787-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c787-121">Remarks</span></span>

<span data-ttu-id="3c787-122">Se la casella di riepilogo ha uno stile disegnato dal proprietario e lo stile di [**\_ ordinamento lbs**](list-box-styles.md) , ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , il sistema invia il messaggio [**WM \_ COMPAREITEM**](wm-compareitem.md) una o più volte al proprietario della casella di riepilogo per inserire il nuovo elemento correttamente nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="3c787-122">If the list box has an owner-drawn style and the [**LBS\_SORT**](list-box-styles.md) style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends the [**WM\_COMPAREITEM**](wm-compareitem.md) message one or more times to the owner of the list box to place the new item properly in the list box.</span></span>

<span data-ttu-id="3c787-123">Il messaggio [**lb \_ INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione di caselle di riepilogo con un numero elevato di elementi (più di 100).</span><span class="sxs-lookup"><span data-stu-id="3c787-123">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="3c787-124">Si riserva la quantità di memoria specificata in modo che i messaggi **lb \_ ADDSTRING** il tempo più breve possibile.</span><span class="sxs-lookup"><span data-stu-id="3c787-124">It reserves the specified amount of memory so that subsequent **LB\_ADDSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="3c787-125">È possibile utilizzare le stime per i parametri *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="3c787-125">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="3c787-126">Se si esegue la sovrastima, viene allocata la memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene utilizzata per gli elementi che superano la quantità richiesta.</span><span class="sxs-lookup"><span data-stu-id="3c787-126">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="3c787-127">Se la casella di riepilogo ha lo stile [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e si aggiunge una stringa più ampia della casella di riepilogo, inviare un messaggio [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="3c787-127">If the list box has the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="3c787-128">Per un'applicazione ANSI, il sistema converte il testo in una casella di riepilogo in formato Unicode usando CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="3c787-128">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="3c787-129">Ciò può causare problemi.</span><span class="sxs-lookup"><span data-stu-id="3c787-129">This can cause problems.</span></span> <span data-ttu-id="3c787-130">Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode nelle finestre giapponesi verranno disattivati.</span><span class="sxs-lookup"><span data-stu-id="3c787-130">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="3c787-131">Per risolvere questo problema, compilare l'applicazione come Unicode o utilizzare una casella di riepilogo creata dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="3c787-131">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c787-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c787-132">Requirements</span></span>



| <span data-ttu-id="3c787-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c787-133">Requirement</span></span> | <span data-ttu-id="3c787-134">Valore</span><span class="sxs-lookup"><span data-stu-id="3c787-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c787-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c787-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3c787-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c787-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c787-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c787-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3c787-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c787-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3c787-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c787-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c787-140"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c787-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c787-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c787-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c787-142">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3c787-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3c787-143">**\_DELETESTRING lb**</span><span class="sxs-lookup"><span data-stu-id="3c787-143">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="3c787-144">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="3c787-144">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="3c787-145">**\_SELECTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="3c787-145">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="3c787-146">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="3c787-146">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="3c787-147">**\_COMPAREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="3c787-147">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

