---
title: Messaggio CB_GETCURSEL (winuser. h)
description: Un'applicazione invia un \_ messaggio XMLcursel di CB per recuperare l'indice dell'elemento attualmente selezionato, se presente, nella casella di riepilogo di una casella combinata.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- Controlli di Windows Message CB_GETCURSEL
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874726"
---
# <a name="cb_getcursel-message"></a><span data-ttu-id="e826c-104">\_Messaggio GETcursel CB</span><span class="sxs-lookup"><span data-stu-id="e826c-104">CB\_GETCURSEL message</span></span>

<span data-ttu-id="e826c-105">Un'applicazione invia un **messaggio \_ xmlcursel di CB** per recuperare l'indice dell'elemento attualmente selezionato, se presente, nella casella di riepilogo di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="e826c-105">An application sends a **CB\_GETCURSEL** message to retrieve the index of the currently selected item, if any, in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e826c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e826c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e826c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e826c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e826c-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e826c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e826c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e826c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e826c-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e826c-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e826c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e826c-111">Return value</span></span>

<span data-ttu-id="e826c-112">Il valore restituito è l'indice in base zero dell'elemento attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="e826c-112">The return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="e826c-113">Se non è selezionato alcun elemento, è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="e826c-113">If no item is selected, it is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="e826c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e826c-114">Requirements</span></span>



| <span data-ttu-id="e826c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e826c-115">Requirement</span></span> | <span data-ttu-id="e826c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e826c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e826c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e826c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e826c-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e826c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e826c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e826c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e826c-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e826c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e826c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e826c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e826c-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e826c-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e826c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e826c-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="e826c-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e826c-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e826c-125">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="e826c-125">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="e826c-126">**\_CAcursel CB**</span><span class="sxs-lookup"><span data-stu-id="e826c-126">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> </dl>

 

 





