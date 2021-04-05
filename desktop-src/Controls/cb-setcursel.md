---
title: Messaggio CB_SETCURSEL (winuser. h)
description: Un'applicazione invia un \_ messaggio di errore CB per selezionare una stringa nell'elenco di una casella combinata.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- Controlli di Windows Message CB_SETCURSEL
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048347"
---
# <a name="cb_setcursel-message"></a><span data-ttu-id="69600-104">\_Messaggio SEcursel CB</span><span class="sxs-lookup"><span data-stu-id="69600-104">CB\_SETCURSEL message</span></span>

<span data-ttu-id="69600-105">Un'applicazione invia un messaggio di errore **CB \_** per selezionare una stringa nell'elenco di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="69600-105">An application sends a **CB\_SETCURSEL** message to select a string in the list of a combo box.</span></span> <span data-ttu-id="69600-106">Se necessario, l'elenco scorre la stringa nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="69600-106">If necessary, the list scrolls the string into view.</span></span> <span data-ttu-id="69600-107">Il testo nel controllo di modifica della casella combinata viene modificato in modo da riflettere la nuova selezione e qualsiasi selezione precedente nell'elenco viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="69600-107">The text in the edit control of the combo box changes to reflect the new selection, and any previous selection in the list is removed.</span></span>

## <a name="parameters"></a><span data-ttu-id="69600-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="69600-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69600-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69600-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69600-110">Specifica l'indice in base zero della stringa da selezionare.</span><span class="sxs-lookup"><span data-stu-id="69600-110">Specifies the zero-based index of the string to select.</span></span> <span data-ttu-id="69600-111">Se questo parametro è-1, qualsiasi selezione corrente nell'elenco verrà rimossa e il controllo di modifica verrà cancellato.</span><span class="sxs-lookup"><span data-stu-id="69600-111">If this parameter is -1, any current selection in the list is removed and the edit control is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="69600-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69600-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69600-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="69600-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69600-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69600-114">Return value</span></span>

<span data-ttu-id="69600-115">Se il messaggio ha esito positivo, il valore restituito è l'indice dell'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="69600-115">If the message is successful, the return value is the index of the item selected.</span></span> <span data-ttu-id="69600-116">Se *wParam* è maggiore del numero di elementi nell'elenco o se *wParam* è-1, il valore restituito è CB \_ Err e la selezione viene deselezionata.</span><span class="sxs-lookup"><span data-stu-id="69600-116">If *wParam* is greater than the number of items in the list or if *wParam* is -1, the return value is CB\_ERR and the selection is cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="69600-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69600-117">Requirements</span></span>



| <span data-ttu-id="69600-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="69600-118">Requirement</span></span> | <span data-ttu-id="69600-119">Valore</span><span class="sxs-lookup"><span data-stu-id="69600-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69600-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69600-120">Minimum supported client</span></span><br/> | <span data-ttu-id="69600-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69600-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="69600-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69600-122">Minimum supported server</span></span><br/> | <span data-ttu-id="69600-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69600-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="69600-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69600-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="69600-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69600-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69600-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69600-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="69600-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="69600-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="69600-128">**CB \_ FindString**</span><span class="sxs-lookup"><span data-stu-id="69600-128">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="69600-129">**CB \_ GETcursel**</span><span class="sxs-lookup"><span data-stu-id="69600-129">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="69600-130">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="69600-130">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> </dl>

 

 





