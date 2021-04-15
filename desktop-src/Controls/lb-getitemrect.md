---
title: Messaggio LB_GETITEMRECT (winuser. h)
description: Ottiene le dimensioni del rettangolo che delimita un elemento della casella di riepilogo come attualmente visualizzato nella casella di riepilogo.
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- Controlli di Windows Message LB_GETITEMRECT
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b66c7c1a3e9f93e90beea40869cecb2081cb20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476313"
---
# <a name="lb_getitemrect-message"></a><span data-ttu-id="1c5f0-104">\_Messaggio GETITEMRECT lb</span><span class="sxs-lookup"><span data-stu-id="1c5f0-104">LB\_GETITEMRECT message</span></span>

<span data-ttu-id="1c5f0-105">Ottiene le dimensioni del rettangolo che delimita un elemento della casella di riepilogo come attualmente visualizzato nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="1c5f0-105">Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c5f0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c5f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c5f0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c5f0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c5f0-108">Indice in base zero di un elemento.</span><span class="sxs-lookup"><span data-stu-id="1c5f0-108">The zero-based index of the item.</span></span>

<span data-ttu-id="1c5f0-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="1c5f0-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="1c5f0-110">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="1c5f0-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="1c5f0-111">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="1c5f0-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="1c5f0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c5f0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c5f0-113">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà le coordinate client per l'elemento nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="1c5f0-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the client coordinates for the item in the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c5f0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c5f0-114">Return value</span></span>

<span data-ttu-id="1c5f0-115">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="1c5f0-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c5f0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c5f0-116">Requirements</span></span>



| <span data-ttu-id="1c5f0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c5f0-117">Requirement</span></span> | <span data-ttu-id="1c5f0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1c5f0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5f0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c5f0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1c5f0-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c5f0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1c5f0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c5f0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1c5f0-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1c5f0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1c5f0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c5f0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c5f0-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c5f0-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c5f0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c5f0-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c5f0-126">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1c5f0-126">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

