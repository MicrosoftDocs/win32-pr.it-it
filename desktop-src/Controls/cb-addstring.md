---
title: Messaggio CB_ADDSTRING (winuser. h)
description: Aggiunge una stringa alla casella di riepilogo di una casella combinata. Se la casella combinata non ha lo stile di \_ ordinamento CBS, la stringa viene aggiunta alla fine dell'elenco. In caso contrario, la stringa viene inserita nell'elenco e l'elenco viene ordinato.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- Controlli di Windows Message CB_ADDSTRING
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964761"
---
# <a name="cb_addstring-message"></a><span data-ttu-id="4df1a-106">\_Messaggio ADDSTRING CB</span><span class="sxs-lookup"><span data-stu-id="4df1a-106">CB\_ADDSTRING message</span></span>

<span data-ttu-id="4df1a-107">Aggiunge una stringa alla casella di riepilogo di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4df1a-107">Adds a string to the list box of a combo box.</span></span> <span data-ttu-id="4df1a-108">Se la casella combinata non ha lo stile [**di \_ ordinamento CBS**](combo-box-styles.md) , la stringa viene aggiunta alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="4df1a-108">If the combo box does not have the [**CBS\_SORT**](combo-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="4df1a-109">In caso contrario, la stringa viene inserita nell'elenco e l'elenco viene ordinato.</span><span class="sxs-lookup"><span data-stu-id="4df1a-109">Otherwise, the string is inserted into the list, and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="4df1a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4df1a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df1a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4df1a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4df1a-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="4df1a-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4df1a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4df1a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4df1a-114">Puntatore **LPCTSTR** alla stringa con terminazione null da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="4df1a-114">An **LPCTSTR** pointer to the null-terminated string to be added.</span></span> <span data-ttu-id="4df1a-115">Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo [**stile \_ HASSTRINGS CBS**](combo-box-styles.md) , il valore del parametro *lParam* viene archiviato come dati dell'elemento anziché come stringa a cui altrimenti indicherà.</span><span class="sxs-lookup"><span data-stu-id="4df1a-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored as item data rather than the string it would otherwise point to.</span></span> <span data-ttu-id="4df1a-116">È possibile recuperare o modificare i dati dell'elemento inviando il messaggio [**CB \_ GETITEMDATA**](cb-getitemdata.md) o [**CB \_ SETITEMDATA**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="4df1a-116">The item data can be retrieved or modified by sending the [**CB\_GETITEMDATA**](cb-getitemdata.md) or [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df1a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4df1a-117">Return value</span></span>

<span data-ttu-id="4df1a-118">Il valore restituito è l'indice in base zero della stringa nella casella di riepilogo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4df1a-118">The return value is the zero-based index to the string in the list box of the combo box.</span></span> <span data-ttu-id="4df1a-119">Se si verifica un errore, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="4df1a-119">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="4df1a-120">Se è disponibile spazio insufficiente per archiviare la nuova stringa, è CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="4df1a-120">If insufficient space is available to store the new string, it is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="4df1a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="4df1a-121">Remarks</span></span>

<span data-ttu-id="4df1a-122">Se si crea una casella combinata creata dal proprietario con lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) ma senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il messaggio [**WM \_ COMPAREITEM**](wm-compareitem.md) viene inviato una o più volte al proprietario della casella combinata, in modo che il nuovo elemento possa essere inserito correttamente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="4df1a-122">If you create an owner-drawn combo box with the [**CBS\_SORT**](combo-box-styles.md) style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the [**WM\_COMPAREITEM**](wm-compareitem.md) message is sent one or more times to the owner of the combo box so the new item can be properly placed in the list.</span></span>

<span data-ttu-id="4df1a-123">Per inserire una stringa in una posizione specifica all'interno dell'elenco, usare il messaggio [**CB \_ INSERTSTRING**](cb-insertstring.md) .</span><span class="sxs-lookup"><span data-stu-id="4df1a-123">To insert a string at a specific location within the list, use the [**CB\_INSERTSTRING**](cb-insertstring.md) message.</span></span>

<span data-ttu-id="4df1a-124">Se lo stile della casella combinata è [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e si aggiunge una stringa più ampia della casella combinata, inviare un messaggio [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="4df1a-124">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the combo box, send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="4df1a-125">**Comclt32.dll versione 5,0 o successiva:** Se si imposta [**CBS \_ minuscole**](combo-box-styles.md) o [**CBS \_ maiuscola**](combo-box-styles.md) , la versione Unicode di **CB \_ ADDSTRING** modifica la stringa.</span><span class="sxs-lookup"><span data-stu-id="4df1a-125">**Comclt32.dll version 5.0 or later:** If [**CBS\_LOWERCASE**](combo-box-styles.md) or [**CBS\_UPPERCASE**](combo-box-styles.md) is set, the Unicode version of **CB\_ADDSTRING** alters the string.</span></span> <span data-ttu-id="4df1a-126">Se si utilizza la memoria globale di sola lettura, l'applicazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4df1a-126">If using read-only global memory, this causes the application to fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df1a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4df1a-127">Requirements</span></span>



| <span data-ttu-id="4df1a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4df1a-128">Requirement</span></span> | <span data-ttu-id="4df1a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4df1a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df1a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4df1a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4df1a-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4df1a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4df1a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4df1a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4df1a-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4df1a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4df1a-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4df1a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4df1a-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4df1a-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df1a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4df1a-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="4df1a-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4df1a-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4df1a-138">**DIR della CB \_**</span><span class="sxs-lookup"><span data-stu-id="4df1a-138">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="4df1a-139">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="4df1a-139">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="4df1a-140">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="4df1a-140">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="4df1a-141">**\_COMPAREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="4df1a-141">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

