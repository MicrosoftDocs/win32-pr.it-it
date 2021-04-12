---
title: Messaggio CB_FINDSTRINGEXACT (winuser. h)
description: Trova la prima stringa della casella di riepilogo in una casella combinata che corrisponde alla stringa specificata nel parametro lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- Controlli di Windows Message CB_FINDSTRINGEXACT
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f70c56a5f13fffa8dfedebd13f9830c62ef941cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519342"
---
# <a name="cb_findstringexact-message"></a><span data-ttu-id="2fabc-104">\_Messaggio FINDEXACTSTRING CB</span><span class="sxs-lookup"><span data-stu-id="2fabc-104">CB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="2fabc-105">Trova la prima stringa della casella di riepilogo in una casella combinata che corrisponde alla stringa specificata nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="2fabc-105">Finds the first list box string in a combo box that matches the string specified in the *lParam* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="2fabc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fabc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fabc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2fabc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fabc-108">Indice in base zero dell'elemento che precede il primo elemento da cercare.</span><span class="sxs-lookup"><span data-stu-id="2fabc-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="2fabc-109">Quando la ricerca raggiunge la fine della casella di riepilogo, continua dalla parte superiore della casella di riepilogo all'elemento specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="2fabc-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="2fabc-110">Se *wParam* è 1, viene eseguita la ricerca dell'intera casella di riepilogo dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="2fabc-110">If *wParam* is  1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="2fabc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2fabc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fabc-112">Puntatore alla stringa con terminazione null in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="2fabc-112">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="2fabc-113">Per la ricerca non viene fatta distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2fabc-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fabc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fabc-114">Return value</span></span>

<span data-ttu-id="2fabc-115">Il valore restituito è l'indice in base zero dell'elemento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2fabc-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="2fabc-116">Se la ricerca ha esito negativo, è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="2fabc-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fabc-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fabc-117">Remarks</span></span>

<span data-ttu-id="2fabc-118">Questa funzione ha esito positivo solo se la stringa specificata e un elemento casella combinata hanno la stessa lunghezza (ad eccezione del carattere di terminazione null) e gli stessi caratteri.</span><span class="sxs-lookup"><span data-stu-id="2fabc-118">This function is successful only if the specified string and a combo box item have the same length (except for the terminating null character) and the same characters.</span></span>

<span data-ttu-id="2fabc-119">Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo [**stile \_ HASSTRINGS CBS**](combo-box-styles.md) , la funzionalità del **messaggio \_ CB FindExactString** dipende dal fatto che l'applicazione usi lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2fabc-119">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the functionality of **CB\_FINDSTRINGEXACT** message depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="2fabc-120">Se si usa lo stile di **\_ ordinamento CBS** , i messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) vengono inviati al proprietario della casella combinata per determinare l'elemento corrispondente alla stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="2fabc-120">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="2fabc-121">Se non si usa lo stile **di \_ ordinamento CBS** , il messaggio **CB \_ FindExactString** Cerca un elemento elenco che corrisponda al valore del parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="2fabc-121">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRINGEXACT** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fabc-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fabc-122">Requirements</span></span>



| <span data-ttu-id="2fabc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fabc-123">Requirement</span></span> | <span data-ttu-id="2fabc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2fabc-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fabc-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fabc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2fabc-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2fabc-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2fabc-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fabc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2fabc-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2fabc-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2fabc-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2fabc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fabc-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2fabc-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fabc-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fabc-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2fabc-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2fabc-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2fabc-133">**CB \_ FindString**</span><span class="sxs-lookup"><span data-stu-id="2fabc-133">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="2fabc-134">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="2fabc-134">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="2fabc-135">**\_COMPAREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="2fabc-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





