---
title: Messaggio LB_SELECTSTRING (winuser. h)
description: Cerca un elemento in una casella di riepilogo che inizia con i caratteri di una stringa specificata. Se viene trovato un elemento corrispondente, l'elemento viene selezionato.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- Controlli di Windows Message LB_SELECTSTRING
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478550"
---
# <a name="lb_selectstring-message"></a><span data-ttu-id="9933f-105">\_Messaggio SELECTSTRING lb</span><span class="sxs-lookup"><span data-stu-id="9933f-105">LB\_SELECTSTRING message</span></span>

<span data-ttu-id="9933f-106">Cerca un elemento in una casella di riepilogo che inizia con i caratteri di una stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="9933f-106">Searches a list box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="9933f-107">Se viene trovato un elemento corrispondente, l'elemento viene selezionato.</span><span class="sxs-lookup"><span data-stu-id="9933f-107">If a matching item is found, the item is selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="9933f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9933f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9933f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9933f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9933f-110">Indice in base zero dell'elemento che precede il primo elemento da cercare.</span><span class="sxs-lookup"><span data-stu-id="9933f-110">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="9933f-111">Quando la ricerca raggiunge la fine della casella di riepilogo, continua dalla parte superiore della casella di riepilogo all'elemento specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="9933f-111">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="9933f-112">Se *wParam* è-1, viene eseguita la ricerca dell'intera casella di riepilogo dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="9933f-112">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="9933f-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="9933f-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="9933f-114">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="9933f-114">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="9933f-115">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="9933f-115">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="9933f-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9933f-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9933f-117">Puntatore alla stringa con terminazione null che contiene il prefisso per il quale eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="9933f-117">A pointer to the null-terminated string that contains the prefix for which to search.</span></span> <span data-ttu-id="9933f-118">La ricerca è indipendente dalla distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9933f-118">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9933f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9933f-119">Return value</span></span>

<span data-ttu-id="9933f-120">Se la ricerca ha esito positivo, il valore restituito è l'indice dell'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="9933f-120">If the search is successful, the return value is the index of the selected item.</span></span> <span data-ttu-id="9933f-121">Se la ricerca ha esito negativo, il valore restituito è LB \_ Err e la selezione corrente non viene modificata.</span><span class="sxs-lookup"><span data-stu-id="9933f-121">If the search is unsuccessful, the return value is LB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9933f-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="9933f-122">Remarks</span></span>

<span data-ttu-id="9933f-123">Se necessario, viene visualizzata la casella di riepilogo per visualizzare l'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="9933f-123">The list box is scrolled, if necessary, to bring the selected item into view.</span></span>

<span data-ttu-id="9933f-124">Non usare questo messaggio con una casella di riepilogo con gli stili [**\_ MULTIPLESEL lbs**](list-box-styles.md) o [**\_ EXTENDEDSEL lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9933f-124">Do not use this message with a list box that has the [**LBS\_MULTIPLESEL**](list-box-styles.md) or the [**LBS\_EXTENDEDSEL**](list-box-styles.md) styles.</span></span>

<span data-ttu-id="9933f-125">Un elemento viene selezionato solo se i caratteri iniziali dal punto iniziale corrispondono ai caratteri nella stringa specificata dal parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="9933f-125">An item is selected only if its initial characters from the starting point match the characters in the string specified by the *lParam* parameter.</span></span>

<span data-ttu-id="9933f-126">Se la casella di riepilogo ha lo stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , l'azione eseguita da **lb \_ SELECTSTRING** dipende dal fatto che venga usato lo stile di [**\_ ordinamento lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9933f-126">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_SELECTSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="9933f-127">Se viene usato l' **\_ ordinamento lbs** , il sistema invia messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) al proprietario della casella di riepilogo per determinare l'elemento corrispondente alla stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="9933f-127">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="9933f-128">In caso contrario, **lb \_ SELECTSTRING** tenta di trovare un elemento con un valore Long (specificato come parametro *lParam* del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) ) che corrisponde al parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="9933f-128">Otherwise, **LB\_SELECTSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9933f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9933f-129">Requirements</span></span>



| <span data-ttu-id="9933f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9933f-130">Requirement</span></span> | <span data-ttu-id="9933f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9933f-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9933f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9933f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9933f-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9933f-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9933f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9933f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9933f-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9933f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9933f-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9933f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9933f-137"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9933f-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9933f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9933f-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="9933f-139">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9933f-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9933f-140">**\_ADDSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="9933f-140">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="9933f-141">**\_FindString lb**</span><span class="sxs-lookup"><span data-stu-id="9933f-141">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> <dt>

[<span data-ttu-id="9933f-142">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="9933f-142">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





