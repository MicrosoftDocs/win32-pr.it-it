---
title: Messaggio LVM_SETHOVERTIME (COMmctrl. h)
description: Imposta la quantità di tempo per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetHoverTime di ListView.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- Controlli di Windows Message LVM_SETHOVERTIME
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118991"
---
# <a name="lvm_sethovertime-message"></a><span data-ttu-id="0447e-105">\_Messaggio SETHOVERTIME LVM</span><span class="sxs-lookup"><span data-stu-id="0447e-105">LVM\_SETHOVERTIME message</span></span>

<span data-ttu-id="0447e-106">Imposta la quantità di tempo per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato.</span><span class="sxs-lookup"><span data-stu-id="0447e-106">Sets the amount of time which the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="0447e-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHoverTime di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) .</span><span class="sxs-lookup"><span data-stu-id="0447e-107">You can send this message explicitly or use the [**ListView\_SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0447e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0447e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0447e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0447e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0447e-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0447e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0447e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0447e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0447e-112">La nuova quantità di tempo, in millisecondi, in base alla quale il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato.</span><span class="sxs-lookup"><span data-stu-id="0447e-112">The new amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="0447e-113">Se questo valore è (**DWORD**)-1, l'ora del passaggio del mouse viene impostata sull'ora del passaggio del mouse predefinita.</span><span class="sxs-lookup"><span data-stu-id="0447e-113">If this value is (**DWORD**)-1, then the hover time is set to the default hover time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0447e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0447e-114">Return value</span></span>

<span data-ttu-id="0447e-115">Restituisce l'ora precedente del passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="0447e-115">Returns the previous hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="0447e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0447e-116">Remarks</span></span>

<span data-ttu-id="0447e-117">L'ora del passaggio del mouse influiscono solo sui controlli visualizzazione elenco con lo stile di visualizzazione elenco esteso [**LVS ex \_ \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0447e-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0447e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0447e-118">Requirements</span></span>



| <span data-ttu-id="0447e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0447e-119">Requirement</span></span> | <span data-ttu-id="0447e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0447e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0447e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0447e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0447e-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0447e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0447e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0447e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0447e-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0447e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0447e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0447e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0447e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0447e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





