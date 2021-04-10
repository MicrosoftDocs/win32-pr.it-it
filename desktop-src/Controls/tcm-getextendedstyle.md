---
title: Messaggio TCM_GETEXTENDEDSTYLE (COMmctrl. h)
description: Recupera gli stili estesi attualmente in uso per il controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl GetExtendedStyle.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- Controlli di Windows Message TCM_GETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964791"
---
# <a name="tcm_getextendedstyle-message"></a><span data-ttu-id="91aee-105">\_Messaggio TCM GETEXTENDEDSTYLE</span><span class="sxs-lookup"><span data-stu-id="91aee-105">TCM\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="91aee-106">Recupera gli stili estesi attualmente in uso per il controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="91aee-106">Retrieves the extended styles that are currently in use for the tab control.</span></span> <span data-ttu-id="91aee-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="91aee-107">You can send this message explicitly or by using the [**TabCtrl\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="91aee-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="91aee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91aee-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91aee-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="91aee-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="91aee-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="91aee-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91aee-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="91aee-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="91aee-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91aee-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91aee-113">Return value</span></span>

<span data-ttu-id="91aee-114">Restituisce un valore **DWORD** che rappresenta gli stili estesi attualmente in uso per il controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="91aee-114">Returns a **DWORD** value that represents the extended styles currently in use for the tab control.</span></span> <span data-ttu-id="91aee-115">Questo valore è una combinazione di [stili estesi](tab-control-extended-styles.md)del controllo scheda.</span><span class="sxs-lookup"><span data-stu-id="91aee-115">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91aee-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91aee-116">Requirements</span></span>



| <span data-ttu-id="91aee-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="91aee-117">Requirement</span></span> | <span data-ttu-id="91aee-118">Valore</span><span class="sxs-lookup"><span data-stu-id="91aee-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91aee-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91aee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="91aee-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91aee-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91aee-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91aee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="91aee-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="91aee-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91aee-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91aee-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="91aee-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91aee-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91aee-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91aee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91aee-126">**TCM \_ SETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="91aee-126">**TCM\_SETEXTENDEDSTYLE**</span></span>](tcm-setextendedstyle.md)
</dt> </dl>

 

 





