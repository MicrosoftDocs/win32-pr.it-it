---
title: Messaggio CB_SELECTSTRING (winuser. h)
description: Esegue la ricerca nell'elenco di una casella combinata per un elemento che inizia con i caratteri in una stringa specificata. Se viene trovato un elemento corrispondente, questo viene selezionato e copiato nel controllo di modifica.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- Controlli di Windows Message CB_SELECTSTRING
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048349"
---
# <a name="cb_selectstring-message"></a><span data-ttu-id="d3844-105">\_Messaggio SELECTSTRING CB</span><span class="sxs-lookup"><span data-stu-id="d3844-105">CB\_SELECTSTRING message</span></span>

<span data-ttu-id="d3844-106">Esegue la ricerca nell'elenco di una casella combinata per un elemento che inizia con i caratteri in una stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="d3844-106">Searches the list of a combo box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="d3844-107">Se viene trovato un elemento corrispondente, questo viene selezionato e copiato nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="d3844-107">If a matching item is found, it is selected and copied to the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3844-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3844-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3844-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3844-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3844-110">Indice in base zero dell'elemento che precede il primo elemento da cercare.</span><span class="sxs-lookup"><span data-stu-id="d3844-110">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="d3844-111">Quando la ricerca raggiunge la fine dell'elenco, viene proseguita dall'inizio dell'elenco fino all'elemento specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="d3844-111">When the search reaches the bottom of the list, it continues from the top of the list back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="d3844-112">Se *wParam* è-1, viene eseguita una ricerca nell'intero elenco dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="d3844-112">If *wParam* is -1, the entire list is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="d3844-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3844-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3844-114">Puntatore alla stringa con terminazione null che contiene i caratteri da cercare.</span><span class="sxs-lookup"><span data-stu-id="d3844-114">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="d3844-115">Per la ricerca non viene fatta distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d3844-115">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3844-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3844-116">Return value</span></span>

<span data-ttu-id="d3844-117">Se la stringa viene trovata, il valore restituito è l'indice dell'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="d3844-117">If the string is found, the return value is the index of the selected item.</span></span> <span data-ttu-id="d3844-118">Se la ricerca ha esito negativo, il valore restituito è CB \_ Err e la selezione corrente non viene modificata.</span><span class="sxs-lookup"><span data-stu-id="d3844-118">If the search is unsuccessful, the return value is CB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3844-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3844-119">Remarks</span></span>

<span data-ttu-id="d3844-120">Viene selezionata una stringa solo se i caratteri del punto iniziale corrispondono ai caratteri nella stringa di prefisso.</span><span class="sxs-lookup"><span data-stu-id="d3844-120">A string is selected only if the characters from the starting point match the characters in the prefix string.</span></span>

<span data-ttu-id="d3844-121">Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il messaggio **\_ SELECTSTRING di CB** dipende dal fatto che si usi lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d3844-121">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_SELECTSTRING** message does depends on whether you use the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="d3844-122">Se viene usato lo stile di **\_ ordinamento CBS** , il sistema invia messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) al proprietario della casella combinata per determinare l'elemento corrispondente alla stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="d3844-122">If the **CBS\_SORT** style is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="d3844-123">Se non si usa lo stile **di \_ ordinamento CBS** , **CB \_ SELECTSTRING** tenta di trovare una corrispondenza tra il valore **DWORD** e il valore del parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="d3844-123">If you do not use the **CBS\_SORT** style, **CB\_SELECTSTRING** attempts to match the **DWORD** value against the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3844-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3844-124">Requirements</span></span>



| <span data-ttu-id="d3844-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3844-125">Requirement</span></span> | <span data-ttu-id="d3844-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d3844-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3844-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3844-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d3844-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3844-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d3844-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3844-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d3844-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3844-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3844-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3844-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3844-132"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3844-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3844-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3844-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="d3844-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d3844-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d3844-135">**CB \_ FindString**</span><span class="sxs-lookup"><span data-stu-id="d3844-135">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="d3844-136">**CB \_ FindExactString**</span><span class="sxs-lookup"><span data-stu-id="d3844-136">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="d3844-137">**\_CAcursel CB**</span><span class="sxs-lookup"><span data-stu-id="d3844-137">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="d3844-138">**\_COMPAREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="d3844-138">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





