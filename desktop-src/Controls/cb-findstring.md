---
title: Messaggio CB_FINDSTRING (winuser. h)
description: Cerca nella casella di riepilogo di una casella combinata un elemento che inizia con i caratteri in una stringa specificata.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- Controlli di Windows Message CB_FINDSTRING
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119738"
---
# <a name="cb_findstring-message"></a><span data-ttu-id="83c2e-104">\_Messaggio FindString CB</span><span class="sxs-lookup"><span data-stu-id="83c2e-104">CB\_FINDSTRING message</span></span>

<span data-ttu-id="83c2e-105">Cerca nella casella di riepilogo di una casella combinata un elemento che inizia con i caratteri in una stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="83c2e-105">Searches the list box of a combo box for an item beginning with the characters in a specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="83c2e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83c2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83c2e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83c2e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83c2e-108">Indice in base zero dell'elemento che precede il primo elemento da cercare.</span><span class="sxs-lookup"><span data-stu-id="83c2e-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="83c2e-109">Quando la ricerca raggiunge la fine della casella di riepilogo, continua dalla parte superiore della casella di riepilogo all'elemento specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="83c2e-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="83c2e-110">Se *wParam* è-1, viene eseguita la ricerca dell'intera casella di riepilogo dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="83c2e-110">If *wParam* is  -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="83c2e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83c2e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83c2e-112">Puntatore alla stringa con terminazione null che contiene i caratteri da cercare.</span><span class="sxs-lookup"><span data-stu-id="83c2e-112">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="83c2e-113">Per la ricerca non viene fatta distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="83c2e-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83c2e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83c2e-114">Return value</span></span>

<span data-ttu-id="83c2e-115">Il valore restituito è l'indice in base zero dell'elemento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="83c2e-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="83c2e-116">Se la ricerca ha esito negativo, è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="83c2e-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="83c2e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="83c2e-117">Remarks</span></span>

<span data-ttu-id="83c2e-118">Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il messaggio **\_ FindString di CB** dipende dal fatto che l'applicazione usi lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="83c2e-118">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_FINDSTRING** message does depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="83c2e-119">Se si usa lo stile di **\_ ordinamento CBS** , i messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) vengono inviati al proprietario della casella combinata per determinare l'elemento corrispondente alla stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="83c2e-119">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="83c2e-120">Se non si usa lo stile **di \_ ordinamento CBS** , il messaggio **CB \_ FindString** Cerca un elemento elenco che corrisponda al valore del parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="83c2e-120">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRING** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="83c2e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83c2e-121">Requirements</span></span>



| <span data-ttu-id="83c2e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="83c2e-122">Requirement</span></span> | <span data-ttu-id="83c2e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="83c2e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c2e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83c2e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="83c2e-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83c2e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="83c2e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83c2e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="83c2e-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83c2e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83c2e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83c2e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="83c2e-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83c2e-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83c2e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83c2e-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="83c2e-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="83c2e-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="83c2e-132">**CB \_ FindExactString**</span><span class="sxs-lookup"><span data-stu-id="83c2e-132">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="83c2e-133">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="83c2e-133">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="83c2e-134">**\_CAcursel CB**</span><span class="sxs-lookup"><span data-stu-id="83c2e-134">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="83c2e-135">**\_COMPAREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="83c2e-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





