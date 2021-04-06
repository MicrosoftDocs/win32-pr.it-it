---
title: Messaggio LVM_GETHOTCURSOR (COMmctrl. h)
description: Recupera il valore HCURSOR utilizzato quando il puntatore è posizionato su un elemento mentre è abilitata la funzionalità di rilevamento a caldo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetHotCursor di ListView.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- Controlli di Windows Message LVM_GETHOTCURSOR
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743007"
---
# <a name="lvm_gethotcursor-message"></a><span data-ttu-id="5208f-105">\_Messaggio GETHOTCURSOR LVM</span><span class="sxs-lookup"><span data-stu-id="5208f-105">LVM\_GETHOTCURSOR message</span></span>

<span data-ttu-id="5208f-106">Recupera il valore HCURSOR utilizzato quando il puntatore è posizionato su un elemento mentre è abilitata la funzionalità di rilevamento a caldo.</span><span class="sxs-lookup"><span data-stu-id="5208f-106">Retrieves the HCURSOR value used when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="5208f-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetHotCursor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .</span><span class="sxs-lookup"><span data-stu-id="5208f-107">You can send this message explicitly or use the [**ListView\_GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5208f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5208f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5208f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5208f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5208f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5208f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5208f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5208f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5208f-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5208f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5208f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5208f-113">Return value</span></span>

<span data-ttu-id="5208f-114">Restituisce un valore HCURSOR che rappresenta l'handle del cursore utilizzato dal controllo elenco-visualizzazione quando è abilitata la funzionalità di rilevamento a caldo.</span><span class="sxs-lookup"><span data-stu-id="5208f-114">Returns an HCURSOR value that is the handle to the cursor that the list-view control uses when hot tracking is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="5208f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5208f-115">Remarks</span></span>

<span data-ttu-id="5208f-116">Un controllo di visualizzazione elenco Usa il rilevamento a caldo e la selezione del passaggio del mouse quando lo stile [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) è impostato.</span><span class="sxs-lookup"><span data-stu-id="5208f-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5208f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5208f-117">Requirements</span></span>



| <span data-ttu-id="5208f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5208f-118">Requirement</span></span> | <span data-ttu-id="5208f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5208f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5208f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5208f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5208f-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5208f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5208f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5208f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5208f-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5208f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5208f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5208f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5208f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5208f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





