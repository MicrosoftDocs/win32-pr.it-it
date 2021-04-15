---
title: Messaggio WM_DELETEITEM (winuser. h)
description: Inviato al proprietario di una casella di riepilogo o di una casella combinata quando la casella di riepilogo o la casella combinata viene distrutta o quando gli elementi vengono rimossi dal \_ messaggio lb DELETESTRING, lb \_ ResetContent, CB \_ DELETESTRING o CB \_ ResetContent.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- Controlli di Windows Message WM_DELETEITEM
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476474"
---
# <a name="wm_deleteitem-message"></a><span data-ttu-id="01e70-104">\_Messaggio DeleteItem WM</span><span class="sxs-lookup"><span data-stu-id="01e70-104">WM\_DELETEITEM message</span></span>

<span data-ttu-id="01e70-105">Inviato al proprietario di una casella di riepilogo o di una casella combinata quando la casella di riepilogo o la casella combinata viene distrutta o quando gli elementi vengono rimossi dal messaggio [**lb \_ DELETESTRING**](lb-deletestring.md), [**lb \_ ResetContent**](lb-resetcontent.md), [**CB \_ DELETESTRING**](cb-deletestring.md)o [**CB \_ ResetContent**](cb-resetcontent.md) .</span><span class="sxs-lookup"><span data-stu-id="01e70-105">Sent to the owner of a list box or combo box when the list box or combo box is destroyed or when items are removed by the [**LB\_DELETESTRING**](lb-deletestring.md), [**LB\_RESETCONTENT**](lb-resetcontent.md), [**CB\_DELETESTRING**](cb-deletestring.md), or [**CB\_RESETCONTENT**](cb-resetcontent.md) message.</span></span> <span data-ttu-id="01e70-106">Il sistema invia un messaggio **WM \_ DeleteItem** per ogni elemento eliminato.</span><span class="sxs-lookup"><span data-stu-id="01e70-106">The system sends a **WM\_DELETEITEM** message for each deleted item.</span></span> <span data-ttu-id="01e70-107">Il sistema invia il messaggio **WM \_ DeleteItem** per qualsiasi casella di riepilogo o casella combinata eliminata con dati di elementi diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="01e70-107">The system sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="01e70-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="01e70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01e70-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01e70-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01e70-110">Specifica l'identificatore del controllo che ha inviato il messaggio **WM \_ DeleteItem** .</span><span class="sxs-lookup"><span data-stu-id="01e70-110">Specifies the identifier of the control that sent the **WM\_DELETEITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="01e70-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01e70-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01e70-112">Puntatore a una struttura [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) che contiene informazioni sull'elemento eliminato da una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="01e70-112">Pointer to a [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) structure that contains information about the item deleted from a list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01e70-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01e70-113">Return value</span></span>

<span data-ttu-id="01e70-114">Un'applicazione deve restituire **true** se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="01e70-114">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="01e70-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="01e70-115">Remarks</span></span>

<span data-ttu-id="01e70-116">Microsoft Windows NT e versioni successive: Windows invia un messaggio **WM \_ DeleteItem** solo per gli elementi eliminati da una casella di riepilogo creata dal proprietario (con lo [**stile \_ OwnerDrawVariable**](list-box-styles.md) [**lbs \_ OwnerDrawFixed**](list-box-styles.md) o lbs) o una casella combinata creata dal proprietario (con lo stile [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) o [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="01e70-116">Microsoft Windows NT and later: Windows sends a **WM\_DELETEITEM** message only for items deleted from an owner-drawn list box (with the [**LBS\_OWNERDRAWFIXED**](list-box-styles.md) or [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style) or owner-drawn combo box (with the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style).</span></span>

<span data-ttu-id="01e70-117">Windows 95: Windows invia il messaggio **WM \_ DeleteItem** per qualsiasi casella di riepilogo o casella combinata eliminata con dati di elementi diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="01e70-117">Windows 95: Windows sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>

## <a name="requirements"></a><span data-ttu-id="01e70-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01e70-118">Requirements</span></span>



| <span data-ttu-id="01e70-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="01e70-119">Requirement</span></span> | <span data-ttu-id="01e70-120">Valore</span><span class="sxs-lookup"><span data-stu-id="01e70-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01e70-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01e70-121">Minimum supported client</span></span><br/> | <span data-ttu-id="01e70-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01e70-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="01e70-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01e70-123">Minimum supported server</span></span><br/> | <span data-ttu-id="01e70-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01e70-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="01e70-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01e70-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="01e70-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01e70-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01e70-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01e70-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="01e70-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="01e70-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="01e70-129">**CB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="01e70-129">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="01e70-130">**CB \_ ResetContent**</span><span class="sxs-lookup"><span data-stu-id="01e70-130">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="01e70-131">**DELETEITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="01e70-131">**DELETEITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[<span data-ttu-id="01e70-132">**\_DELETESTRING lb**</span><span class="sxs-lookup"><span data-stu-id="01e70-132">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="01e70-133">**\_ResetContent lb**</span><span class="sxs-lookup"><span data-stu-id="01e70-133">**LB\_RESETCONTENT**</span></span>](lb-resetcontent.md)
</dt> </dl>

 

 





