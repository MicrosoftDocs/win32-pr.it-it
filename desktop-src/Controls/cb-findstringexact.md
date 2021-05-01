---
title: CB_FINDSTRINGEXACT messaggio (Winuser.h)
description: Trova la prima stringa della casella di riepilogo in una casella combinata che corrisponde alla stringa specificata nel parametro lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- CB_FINDSTRINGEXACT messaggio Controlli Windows
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
ms.openlocfilehash: 7f99d85c7dddb95bdfb168443d6f977c22273a87
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327176"
---
# <a name="cb_findstringexact-message"></a><span data-ttu-id="70274-104">Messaggio CB \_ FINDSTRINGEXACT</span><span class="sxs-lookup"><span data-stu-id="70274-104">CB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="70274-105">Trova la prima stringa della casella di riepilogo in una casella combinata che corrisponde alla stringa specificata nel *parametro lParam.*</span><span class="sxs-lookup"><span data-stu-id="70274-105">Finds the first list box string in a combo box that matches the string specified in the *lParam* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="70274-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="70274-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70274-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70274-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70274-108">Indice in base zero dell'elemento che precede il primo elemento in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="70274-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="70274-109">Quando la ricerca raggiunge la parte inferiore della casella di riepilogo, continua dalla parte superiore della casella di riepilogo all'elemento specificato dal *parametro wParam.*</span><span class="sxs-lookup"><span data-stu-id="70274-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="70274-110">Se *wParam è* -1, l'intera casella di riepilogo viene cercata dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="70274-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="70274-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70274-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70274-112">Puntatore alla stringa con terminazione Null in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="70274-112">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="70274-113">La ricerca non fa distinzione tra maiuscole e minuscole, quindi questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="70274-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70274-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70274-114">Return value</span></span>

<span data-ttu-id="70274-115">Il valore restituito è l'indice in base zero dell'elemento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="70274-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="70274-116">Se la ricerca ha esito negativo, si tratta di CB \_ ERR.</span><span class="sxs-lookup"><span data-stu-id="70274-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="70274-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="70274-117">Remarks</span></span>

<span data-ttu-id="70274-118">Questa funzione ha esito positivo solo se la stringa specificata e un elemento della casella combinata hanno la stessa lunghezza (ad eccezione del carattere Null di terminazione) e degli stessi caratteri.</span><span class="sxs-lookup"><span data-stu-id="70274-118">This function is successful only if the specified string and a combo box item have the same length (except for the terminating null character) and the same characters.</span></span>

<span data-ttu-id="70274-119">Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**\_ CBS HASSTRINGS,**](combo-box-styles.md) la funzionalità del messaggio **CB \_ FINDSTRINGEXACT** dipende dal fatto che l'applicazione usi lo stile [**CBS \_ SORT.**](combo-box-styles.md)</span><span class="sxs-lookup"><span data-stu-id="70274-119">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the functionality of **CB\_FINDSTRINGEXACT** message depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="70274-120">Se si usa lo **stile CBS \_ SORT,** i messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) vengono inviati al proprietario della casella combinata per determinare quale elemento corrisponde alla stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="70274-120">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="70274-121">Se non si usa lo stile **CBS \_ SORT,** il messaggio **CB \_ FINDSTRINGEXACT** cerca un elemento dell'elenco che corrisponde al valore del *parametro lParam.*</span><span class="sxs-lookup"><span data-stu-id="70274-121">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRINGEXACT** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="70274-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70274-122">Requirements</span></span>



| <span data-ttu-id="70274-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="70274-123">Requirement</span></span> | <span data-ttu-id="70274-124">Valore</span><span class="sxs-lookup"><span data-stu-id="70274-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70274-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70274-125">Minimum supported client</span></span><br/> | <span data-ttu-id="70274-126">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="70274-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="70274-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70274-127">Minimum supported server</span></span><br/> | <span data-ttu-id="70274-128">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="70274-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="70274-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70274-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="70274-130"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="70274-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70274-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70274-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="70274-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="70274-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="70274-133">**CB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="70274-133">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="70274-134">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="70274-134">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="70274-135">**WM \_ COMPAREITEM**</span><span class="sxs-lookup"><span data-stu-id="70274-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





