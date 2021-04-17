---
title: Messaggio LB_FINDSTRING (winuser. h)
description: Trova la prima stringa in una casella di riepilogo che inizia con la stringa specificata.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- Controlli di Windows Message LB_FINDSTRING
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b528dbafbc386af05a091f24c8c28327739f5d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478965"
---
# <a name="lb_findstring-message"></a><span data-ttu-id="03bd5-104">\_Messaggio FindString lb</span><span class="sxs-lookup"><span data-stu-id="03bd5-104">LB\_FINDSTRING message</span></span>

<span data-ttu-id="03bd5-105">Trova la prima stringa in una casella di riepilogo che inizia con la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="03bd5-105">Finds the first string in a list box that begins with the specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="03bd5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="03bd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03bd5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03bd5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03bd5-108">Indice in base zero dell'elemento che precede il primo elemento da cercare.</span><span class="sxs-lookup"><span data-stu-id="03bd5-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="03bd5-109">Quando la ricerca raggiunge la fine della casella di riepilogo, continua a eseguire la ricerca dalla parte superiore della casella di riepilogo all'elemento specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="03bd5-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="03bd5-110">Se *wParam* è-1, viene eseguita la ricerca dell'intera casella di riepilogo dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="03bd5-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="03bd5-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="03bd5-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="03bd5-112">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="03bd5-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="03bd5-113">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="03bd5-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="03bd5-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03bd5-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03bd5-115">Puntatore alla stringa con terminazione null che contiene la stringa in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="03bd5-115">A pointer to the null-terminated string that contains the string for which to search.</span></span> <span data-ttu-id="03bd5-116">La ricerca è indipendente dalla distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="03bd5-116">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03bd5-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03bd5-117">Return value</span></span>

<span data-ttu-id="03bd5-118">Il valore restituito è l'indice dell'elemento corrispondente o LB \_ Err se la ricerca ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="03bd5-118">The return value is the index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="03bd5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="03bd5-119">Remarks</span></span>

<span data-ttu-id="03bd5-120">Se la casella di riepilogo ha lo stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , l'azione eseguita da **lb \_ FindString** dipende dal fatto che venga usato lo stile di [**\_ ordinamento lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="03bd5-120">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="03bd5-121">Se viene usato l' **\_ ordinamento lbs** , il sistema invia messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) al proprietario della casella di riepilogo per determinare l'elemento corrispondente alla stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="03bd5-121">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="03bd5-122">In caso contrario, **lb \_ FindString** tenta di trovare un elemento con un valore Long (specificato come parametro *lParam* del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) ) che corrisponde al parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="03bd5-122">Otherwise, **LB\_FINDSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="03bd5-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03bd5-123">Requirements</span></span>



| <span data-ttu-id="03bd5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="03bd5-124">Requirement</span></span> | <span data-ttu-id="03bd5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="03bd5-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03bd5-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03bd5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="03bd5-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03bd5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="03bd5-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03bd5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="03bd5-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03bd5-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="03bd5-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03bd5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="03bd5-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03bd5-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03bd5-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03bd5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03bd5-133">**\_FINDEXACTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="03bd5-133">**LB\_FINDSTRINGEXACT**</span></span>](lb-findstringexact.md)
</dt> </dl>

 

 





