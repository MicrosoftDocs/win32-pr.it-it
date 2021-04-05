---
title: Messaggio TCM_SETEXTENDEDSTYLE (COMmctrl. h)
description: Imposta gli stili estesi che il controllo struttura a schede utilizzerà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl SetExtendedStyle.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- Controlli di Windows Message TCM_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048386"
---
# <a name="tcm_setextendedstyle-message"></a><span data-ttu-id="cd923-105">\_Messaggio TCM SETEXTENDEDSTYLE</span><span class="sxs-lookup"><span data-stu-id="cd923-105">TCM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="cd923-106">Imposta gli stili estesi che il controllo struttura a schede utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="cd923-106">Sets the extended styles that the tab control will use.</span></span> <span data-ttu-id="cd923-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="cd923-107">You can send this message explicitly or by using the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd923-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd923-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd923-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd923-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd923-110">Valore **DWORD** che indica quali stili in *lParam* devono essere interessati.</span><span class="sxs-lookup"><span data-stu-id="cd923-110">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="cd923-111">Solo gli stili estesi in *wParam* verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="cd923-111">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="cd923-112">Tutti gli altri stili verranno mantenuti così come sono.</span><span class="sxs-lookup"><span data-stu-id="cd923-112">All other styles will be maintained as they are.</span></span> <span data-ttu-id="cd923-113">Se questo parametro è zero, saranno interessati tutti gli stili in *lParam* .</span><span class="sxs-lookup"><span data-stu-id="cd923-113">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="cd923-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd923-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd923-115">Valore che specifica gli stili del controllo scheda esteso.</span><span class="sxs-lookup"><span data-stu-id="cd923-115">Value specifying the extended tab control styles.</span></span> <span data-ttu-id="cd923-116">Questo valore è una combinazione di [stili estesi](tab-control-extended-styles.md)del controllo scheda.</span><span class="sxs-lookup"><span data-stu-id="cd923-116">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd923-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd923-117">Return value</span></span>

<span data-ttu-id="cd923-118">Restituisce un valore **DWORD** che contiene gli stili estesi del controllo tab precedente.</span><span class="sxs-lookup"><span data-stu-id="cd923-118">Returns a **DWORD** value that contains the previous tab control extended styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd923-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd923-119">Remarks</span></span>

<span data-ttu-id="cd923-120">Il parametro *wParam* consente di modificare uno o più stili estesi senza dover prima recuperare gli stili esistenti.</span><span class="sxs-lookup"><span data-stu-id="cd923-120">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="cd923-121">Se, ad esempio, si [**passa TCS \_ ex \_ FLATSEPARATORS**](tab-control-extended-styles.md) per *wParam* e 0 per *lParam*, lo stile **\_ \_ FLATSEPARATORS di TC ex** verrà cancellato, ma tutti gli altri stili rimarranno invariati.</span><span class="sxs-lookup"><span data-stu-id="cd923-121">For example, if you pass [**TCS\_EX\_FLATSEPARATORS**](tab-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **TCS\_EX\_FLATSEPARATORS** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="cd923-122">Per motivi di compatibilità con le versioni precedenti, la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) non è stata aggiornata per l'uso di *dwExMask*.</span><span class="sxs-lookup"><span data-stu-id="cd923-122">For backward compatibility reasons, the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro has not been updated to use *dwExMask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd923-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd923-123">Requirements</span></span>



| <span data-ttu-id="cd923-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd923-124">Requirement</span></span> | <span data-ttu-id="cd923-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cd923-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd923-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd923-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cd923-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd923-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd923-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd923-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cd923-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd923-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd923-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd923-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd923-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd923-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd923-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd923-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd923-133">**TCM \_ GETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="cd923-133">**TCM\_GETEXTENDEDSTYLE**</span></span>](tcm-getextendedstyle.md)
</dt> </dl>

 

 





