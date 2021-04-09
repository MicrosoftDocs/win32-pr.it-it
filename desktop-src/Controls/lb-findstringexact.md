---
title: Messaggio LB_FINDSTRINGEXACT (winuser. h)
description: Trova la prima stringa della casella di riepilogo che corrisponde esattamente alla stringa specificata, ad eccezione del fatto che la ricerca non fa distinzione tra maiuscole e minuscole.
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- Controlli di Windows Message LB_FINDSTRINGEXACT
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048712"
---
# <a name="lb_findstringexact-message"></a><span data-ttu-id="c9039-104">\_Messaggio FINDEXACTSTRING lb</span><span class="sxs-lookup"><span data-stu-id="c9039-104">LB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="c9039-105">Trova la prima stringa della casella di riepilogo che corrisponde esattamente alla stringa specificata, ad eccezione del fatto che la ricerca non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c9039-105">Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9039-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9039-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9039-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9039-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9039-108">Indice in base zero dell'elemento che precede il primo elemento da cercare.</span><span class="sxs-lookup"><span data-stu-id="c9039-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="c9039-109">Quando la ricerca raggiunge la fine della casella di riepilogo, continua a eseguire la ricerca dalla parte superiore della casella di riepilogo all'elemento specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="c9039-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="c9039-110">Se *wParam* è-1, viene eseguita la ricerca dell'intera casella di riepilogo dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="c9039-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="c9039-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="c9039-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="c9039-112">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="c9039-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="c9039-113">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="c9039-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="c9039-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9039-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9039-115">Puntatore alla stringa con terminazione null in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="c9039-115">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="c9039-116">Per la ricerca non viene fatta distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c9039-116">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9039-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9039-117">Return value</span></span>

<span data-ttu-id="c9039-118">Il valore restituito è l'indice in base zero dell'elemento corrispondente o LB \_ Err se la ricerca ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c9039-118">The return value is the zero-based index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9039-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9039-119">Remarks</span></span>

<span data-ttu-id="c9039-120">Questa funzione ha esito positivo solo se la stringa specificata e un elemento casella di riepilogo hanno la stessa lunghezza (ad eccezione del valore null alla fine della stringa specificata) e hanno esattamente gli stessi caratteri.</span><span class="sxs-lookup"><span data-stu-id="c9039-120">This function is only successful if the specified string and a list box item have the same length (except for the null at the end of the specified string) and have exactly the same characters.</span></span>

<span data-ttu-id="c9039-121">Se la casella di riepilogo ha lo stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , l'azione eseguita da **lb \_ FindExactString** dipende dal fatto che venga usato lo stile di [**\_ ordinamento lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c9039-121">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRINGEXACT** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="c9039-122">Se viene usato l' **\_ ordinamento lbs** , il sistema invia messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) al proprietario della casella di riepilogo per determinare l'elemento corrispondente alla stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="c9039-122">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="c9039-123">In caso contrario, **lb \_ FindExactString** tenta di trovare un elemento con un valore Long (specificato come parametro *lParam* del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) ) che corrisponde al parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c9039-123">Otherwise, **LB\_FINDSTRINGEXACT** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9039-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9039-124">Requirements</span></span>



| <span data-ttu-id="c9039-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9039-125">Requirement</span></span> | <span data-ttu-id="c9039-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c9039-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9039-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9039-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c9039-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9039-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c9039-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9039-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c9039-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9039-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c9039-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9039-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9039-132"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9039-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9039-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9039-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9039-134">**\_FindString lb**</span><span class="sxs-lookup"><span data-stu-id="c9039-134">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> </dl>

 

 





