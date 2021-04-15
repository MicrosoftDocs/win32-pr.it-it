---
title: Messaggio CB_INSERTSTRING (winuser. h)
description: Inserisce i dati di una stringa o di un elemento nell'elenco di una casella combinata. A differenza del \_ messaggio CB ADDSTRING, il \_ messaggio CB INSERTSTRING non determina l'ordinamento di un elenco con lo \_ stile di ordinamento CBS.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- Controlli di Windows Message CB_INSERTSTRING
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476649"
---
# <a name="cb_insertstring-message"></a><span data-ttu-id="616fc-105">\_Messaggio INSERTSTRING CB</span><span class="sxs-lookup"><span data-stu-id="616fc-105">CB\_INSERTSTRING message</span></span>

<span data-ttu-id="616fc-106">Inserisce i dati di una stringa o di un elemento nell'elenco di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="616fc-106">Inserts a string or item data into the list of a combo box.</span></span> <span data-ttu-id="616fc-107">A differenza del messaggio [**CB \_ ADDSTRING**](cb-addstring.md) , il messaggio **CB \_ INSERTSTRING** non determina l'ordinamento di un elenco con lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="616fc-107">Unlike the [**CB\_ADDSTRING**](cb-addstring.md) message, the **CB\_INSERTSTRING** message does not cause a list with the [**CBS\_SORT**](combo-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="616fc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="616fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="616fc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="616fc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="616fc-110">Indice in base zero della posizione in corrispondenza della quale inserire la stringa.</span><span class="sxs-lookup"><span data-stu-id="616fc-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="616fc-111">Se questo parametro è-1, la stringa viene aggiunta alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="616fc-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="616fc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="616fc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="616fc-113">Puntatore alla stringa con terminazione null da inserire.</span><span class="sxs-lookup"><span data-stu-id="616fc-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="616fc-114">Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo [**stile \_ HASSTRINGS CBS**](combo-box-styles.md) , il valore del parametro *lParam* viene archiviato anziché la stringa a cui altrimenti indicherà.</span><span class="sxs-lookup"><span data-stu-id="616fc-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored rather than the string to which it would otherwise point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="616fc-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="616fc-115">Return value</span></span>

<span data-ttu-id="616fc-116">Il valore restituito è l'indice della posizione in cui è stata inserita la stringa.</span><span class="sxs-lookup"><span data-stu-id="616fc-116">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="616fc-117">Se si verifica un errore, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="616fc-117">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="616fc-118">Se non è disponibile spazio sufficiente per archiviare la nuova stringa, è CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="616fc-118">If there is insufficient space available to store the new string, it is CB\_ERRSPACE.</span></span>

<span data-ttu-id="616fc-119">Se lo stile della casella combinata è [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e si inserisce una stringa più ampia della casella combinata, è necessario inviare un messaggio [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="616fc-119">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the combo box, you should send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

## <a name="requirements"></a><span data-ttu-id="616fc-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="616fc-120">Requirements</span></span>



| <span data-ttu-id="616fc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="616fc-121">Requirement</span></span> | <span data-ttu-id="616fc-122">Valore</span><span class="sxs-lookup"><span data-stu-id="616fc-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="616fc-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="616fc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="616fc-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="616fc-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="616fc-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="616fc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="616fc-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="616fc-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="616fc-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="616fc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="616fc-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="616fc-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="616fc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="616fc-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="616fc-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="616fc-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="616fc-131">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="616fc-131">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="616fc-132">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="616fc-132">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="616fc-133">**DIR della CB \_**</span><span class="sxs-lookup"><span data-stu-id="616fc-133">**CB\_DIR**</span></span>](cb-dir.md)
</dt> </dl>

 

