---
title: Messaggio LVM_GETHOVERTIME (COMmctrl. h)
description: Recupera la quantità di tempo per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetHoverTime di ListView.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- Controlli di Windows Message LVM_GETHOVERTIME
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477573"
---
# <a name="lvm_gethovertime-message"></a><span data-ttu-id="08789-105">\_Messaggio GETHOVERTIME LVM</span><span class="sxs-lookup"><span data-stu-id="08789-105">LVM\_GETHOVERTIME message</span></span>

<span data-ttu-id="08789-106">Recupera la quantità di tempo per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato.</span><span class="sxs-lookup"><span data-stu-id="08789-106">Retrieves the amount of time that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="08789-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetHoverTime di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) .</span><span class="sxs-lookup"><span data-stu-id="08789-107">You can send this message explicitly or use the [**ListView\_GetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="08789-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="08789-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08789-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08789-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="08789-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="08789-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="08789-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08789-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="08789-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="08789-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08789-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08789-113">Return value</span></span>

<span data-ttu-id="08789-114">Restituisce la quantità di tempo, in millisecondi, per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato.</span><span class="sxs-lookup"><span data-stu-id="08789-114">Returns the amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="08789-115">Se il valore restituito è (**DWORD**)-1, l'ora del passaggio del mouse corrisponde al valore predefinito del passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="08789-115">If the return value is (**DWORD**)-1, then the hover time is the default hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="08789-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="08789-116">Remarks</span></span>

<span data-ttu-id="08789-117">L'ora del passaggio del mouse influiscono solo sui controlli visualizzazione elenco con lo stile di visualizzazione elenco esteso [**LVS ex \_ \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="08789-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="08789-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08789-118">Requirements</span></span>



| <span data-ttu-id="08789-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="08789-119">Requirement</span></span> | <span data-ttu-id="08789-120">Valore</span><span class="sxs-lookup"><span data-stu-id="08789-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08789-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08789-121">Minimum supported client</span></span><br/> | <span data-ttu-id="08789-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08789-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08789-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08789-123">Minimum supported server</span></span><br/> | <span data-ttu-id="08789-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08789-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08789-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08789-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="08789-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08789-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





