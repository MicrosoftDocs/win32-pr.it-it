---
title: Messaggio LVM_INSERTGROUPSORTED (COMmctrl. h)
description: Inserisce un gruppo in un elenco ordinato di gruppi.
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- Controlli di Windows Message LVM_INSERTGROUPSORTED
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874310"
---
# <a name="lvm_insertgroupsorted-message"></a><span data-ttu-id="ba138-104">\_Messaggio INSERTGROUPSORTED LVM</span><span class="sxs-lookup"><span data-stu-id="ba138-104">LVM\_INSERTGROUPSORTED message</span></span>

<span data-ttu-id="ba138-105">Inserisce un gruppo in un elenco ordinato di gruppi.</span><span class="sxs-lookup"><span data-stu-id="ba138-105">Inserts a group into an ordered list of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba138-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba138-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba138-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba138-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ba138-108">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> contenente il gruppo da inserire.</span><span class="sxs-lookup"><span data-stu-id="ba138-108">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> structure that contains the group to insert.</span></span></dd> <dt>

<span data-ttu-id="ba138-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba138-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ba138-110">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="ba138-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba138-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba138-111">Return value</span></span>

<span data-ttu-id="ba138-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ba138-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba138-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba138-113">Remarks</span></span>

<span data-ttu-id="ba138-114">L'ordinamento dell'elenco è basato sull'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="ba138-114">The ordering of the list is based on the ID of the group.</span></span> <span data-ttu-id="ba138-115">L'ordine viene definito dalla funzione di ordinamento definita dall'applicazione, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), che viene passata nella struttura [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="ba138-115">The order is defined by the application-defined ordering function, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), that is passed in the [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) structure by the *wParam* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="ba138-116">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="ba138-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ba138-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ba138-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba138-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba138-118">Requirements</span></span>



| <span data-ttu-id="ba138-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba138-119">Requirement</span></span> | <span data-ttu-id="ba138-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ba138-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba138-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba138-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba138-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba138-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba138-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba138-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba138-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba138-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba138-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba138-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba138-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba138-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba138-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba138-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba138-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ba138-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ba138-129">**LVGroupCompare**</span><span class="sxs-lookup"><span data-stu-id="ba138-129">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[<span data-ttu-id="ba138-130">**LVINSERTGROUPSORTED**</span><span class="sxs-lookup"><span data-stu-id="ba138-130">**LVINSERTGROUPSORTED**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

